---
layout: default
title: Playfair Duplicates
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
  var initial = "key = input(&quot;Enter the encryption key: &quot;).upper().replace(&quot; &quot;, &quot;&quot;)\n" +
    "key_text = [ch for i, ch in enumerate(key) if ch not in key[:i]]\n" +
    "matrix_text = list(key_text) + [ch for ch in &quot;ABCDEFGHIJKLMNOPRSTUVWXYZ&quot; if ch not in key_text]\n" +
    "for n in range(0, len(matrix_text), 5):\n" +
    "    print(matrix_text[n:n+5])";
  var parsonsPuzzle = new ParsonsWidget({
    "sortableId": "sortable",
    "max_wrong_lines": 0,
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
