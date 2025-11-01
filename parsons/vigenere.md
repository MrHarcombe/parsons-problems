---
layout: default
title: Vigenère Cipher
---
<h1>The solved version of this puzzle will help you work through the corresponding characters from the key and cipher string in combination.</h1>
<div id="sortableTrash" class="sortable-code"></div> 
<div id="sortable" class="sortable-code"></div> 
<div style="clear:both;"></div> 
<p> 
    <input id="feedbackLink" value="Get Feedback" type="button" /> 
    <input id="newInstanceLink" value="Reset Problem" type="button" /> 
</p> 
<script type="text/javascript"> 
(function(){
  var initial = "plain_text = input(&quot;Enter the message to encrypt: &quot;).upper().replace(&quot; &quot;, &quot;&quot;)\n" +
    "key = input(&quot;Enter the encryption key: &quot;).upper()\n" +
    "for i, ch in enumerate(plain_text):\n" +
    "    ch_index = ord(ch) - 65\n" +
    "    key_index = ord(key[i % len(key)]) - 65\n" +
    "    print(f&quot;message letter index {ch_index}, key letter index {key_index}&quot;)\n";
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
