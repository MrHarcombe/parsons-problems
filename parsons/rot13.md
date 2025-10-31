---
layout: default
title: Template
---
<div id="rot13-sortableTrash" class="sortable-code"></div> 
<div id="rot13-sortable" class="sortable-code"></div> 
<div style="clear:both;"></div> 
<p> 
    <input id="rot13-feedbackLink" value="Get Feedback" type="button" /> 
    <input id="rot13-newInstanceLink" value="Reset Problem" type="button" /> 
</p> 
<script type="text/javascript"> 
(function(){
  var initial = "message = input(&quot;Enter the message to encrypt: &quot;)
\n" +
    "ascii_values = []
\n" +
    "for ch in message:
\n" +
    "    ascii_values.append(ord(ch))
\n" +
    "print(ascii_values)
\n" +
    "";
  var parsonsPuzzle = new ParsonsWidget({
    "sortableId": "rot13-sortable",
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
  $("#rot13-newInstanceLink").click(function(event){ 
      event.preventDefault(); 
      parsonsPuzzle.shuffleLines(); 
  }); 
  $("#rot13-feedbackLink").click(function(event){ 
      event.preventDefault(); 
      parsonsPuzzle.getFeedback(); 
  }); 
})(); 
</script>
