---
layout: default
title: Tkinter creates a new window
---
# Re-order the lines for an example of how to create new pop-up windows in Tkinter.
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
    "def launch_window():\n" +
    "    new_window = tk.Toplevel(root)\n" +
    "    new_window.title(&quot;A standalone window&quot;)\n" +
    "    ttk.Label(new_window, text=&quot;Oh look, a new window above the parent!&quot;, anchor=tk.CENTER).grid(sticky=tk.EW)\n" +
    "    ttk.Button(new_window, text=&quot;Close&quot;, command=lambda: new_window.destroy()).grid(sticky=tk.NSEW)\n" +
    "    new_window.rowconfigure(0, weight=3)\n" +
    "    new_window.rowconfigure(1, weight=1)\n" +
    "    new_window.columnconfigure(0, weight=1)\n" +
    "root = tk.Tk()\n" +
    "root.title(&#039;New Window Example&#039;)\n" +
    "frame = ttk.Frame(root)\n" +
    "ttk.Label(frame, text=&quot;Click the button to launch a new window&quot;, anchor=tk.CENTER).grid(sticky=tk.EW)\n" +
    "ttk.Button(frame, text=&quot;Launch&quot;, command=launch_window).grid(sticky=tk.EW)\n" +
    "frame.grid(sticky=tk.NSEW)\n" +
    "root.rowconfigure(0, weight=1)\n" +
    "root.columnconfigure(0, weight=1)\n" +
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
