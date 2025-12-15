---
layout: default
title: Tkinter Using Styles
---
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
    "root = tk.Tk()\n" +
    "root.title(&#039;Widget Style Example&#039;)\n" +
    "style = ttk.Style(root)\n" +
    "style.configure(&#039;TFrame&#039;, background=&#039;green&#039;)\n" +
    "style.configure(&#039;yellow.TLabel&#039;, background=&#039;yellow&#039;, font=&#039;Consolas 24&#039;)\n" +
    "f = ttk.Frame(root)\n" +
    "f.grid(sticky=tk.NSEW)\n" +
    "ttk.Label(f, text=&quot;Hello&quot;, anchor=tk.CENTER, style=&#039;yellow.TLabel&#039;).grid()\n" +
    "f.rowconfigure(0, weight=1)\n" +
    "f.columnconfigure(0, weight=1)\n" +
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
