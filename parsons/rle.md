---
layout: default
title: RLE hint
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
  var initial = "uncompressed = input(&quot;Enter the binary stream to compress (space separated): &quot;).split()\n" +
    "bit_length = len(uncompressed[0])\n" +
    "index = 0\n" +
    "value = uncompressed[index]\n" +
    "count = 0\n" +
    "while index &lt; len(uncompressed) and uncompressed[index] == value:\n" +
    "    count += 1\n" +
    "    index += 1\n" +
    "print(&quot;value:&quot;, value, &quot;occurs:&quot;, count, &quot;times so next value starts at index:&quot;, index)";
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
