---
layout: default
title: ROT-13
---
<p>Re-order the lines to put the ASCII value of each character into a list.</p>
<div id="sortableTrash" class="sortable-code"></div> 
<div id="sortable" class="sortable-code"></div> 
<div style="clear:both;">
    <p> 
        <input id="feedbackLink" value="Get Feedback" type="button" /> 
        <input id="newInstanceLink" value="Reset Problem" type="button" /> 
        <fieldset class="feedbackFieldset"><legend>Feedback:</legend><div id="feedback"/></fieldset>
    </p> 
</div> 
<script type="text/javascript"> 
(function(){
  var initial = "message = input(&quot;Enter the message to encrypt: &quot;)\n" +
    "ascii_values = []\n" +
    "for ch in message:\n" +
    "    ascii_values.append(ord(ch))\n" +
    "print(ascii_values)";
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
