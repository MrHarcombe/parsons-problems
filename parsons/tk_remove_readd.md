---
layout: default
title: Tkinter remove/re-add widgets
---
# Re-order the lines for an example of how to remove/re-add widgets in Tkinter.
<div id="sortableTrash" class="sortable-code"></div> 
<div id="sortable" class="sortable-code"></div> 
<div style="clear:both;"></div> 
<p> 
    <input id="feedbackLink" value="Get Feedback" type="button" /> 
    <input id="newInstanceLink" value="Reset Problem" type="button" /> 
</p> 
<script type="text/javascript"> 
(function(){
  var initial = "import tkinter as tk\n" +
    "from tkinter import ttk\n" +
    "def click_forget():\n" +
    "    loser.grid_forget()\n" +
    "def click_remove():\n" +
    "    loser.grid_remove()\n" +
    "def click_reset():\n" +
    "    loser.grid()\n" +
    "root = tk.Tk()\n" +
    "root.title(&#039;Forget/Remove Example&#039;)\n" +
    "root.resizable(False, False)\n" +
    "loser = ttk.Label(root, text=&quot;One to lose&quot;, anchor=tk.CENTER)\n" +
    "loser.grid(columnspan=2, sticky=tk.NSEW)\n" +
    "ttk.Button(root, text=&quot;Forget&quot;, command=click_forget).grid(row=1, column=0, sticky=tk.NSEW)\n" +
    "ttk.Button(root, text=&quot;Remove&quot;, command=click_remove).grid(row=1, column=1, sticky=tk.NSEW)\n" +
    "ttk.Button(root, text=&quot;Reset&quot;, command=click_reset).grid(row=2, column=0, columnspan=2, sticky=tk.EW)\n" +
    "root.mainloop()";
  var parsonsPuzzle = new ParsonsWidget({
    "sortableId": "sortable",
    "max_wrong_lines": 10,
    "grader": ParsonsWidget._graders.LineBasedGrader,
    "exec_limit": 2500,
    "can_indent": true,
    "x_indent": 50,
    "lang": "en",
    "show_feedback": true
  });
  parsonsPuzzle.init(initial);
  parsonsPuzzle.shuffleLines();
  $("#newInstanceLink").click(function(event){ 
      event.preventDefault(); 
      parsonsPuzzle.shuffleLines(); 
  }); 
  $("#feedbackLink").click(function(event){ 
      event.preventDefault(); 
      parsonsPuzzle.getFeedback(); 
  }); 
})(); 
</script>
