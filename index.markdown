---
# Feel free to add content and custom Front Matter to this file.
# To modify the layout, see https://jekyllrb.com/docs/themes/#overriding-theme-defaults

layout: default
title: Multiple Parson's Problems on One Page
---
# Parsons Practice

## Parsons 1 (Line Based Grader)
Re-arrange the blocks below so they print out "Hello World!"

<div id="p1-sortableTrash" class="sortable-code"></div>
<div id="p1-sortable" class="sortable-code"></div>
<div style="clear:both;"></div>
<p>
    <input id="p1-feedbackLink" value="Get Feedback" type="button" />
    <input id="p1-newInstanceLink" value="Reset Problem" type="button" />
</p>
<script type="text/javascript">
(function() {
  var initial = "print(\"Hello\")\n" +
    "print(\" \")\n" +
    "print(\"World\")\n" +
    "print(\"!\")";
  var parsonsPuzzle = new ParsonsWidget({
    "sortableId": "p1-sortable",
    "max_wrong_lines": 10,
    "grader": ParsonsWidget._graders.LineBasedGrader,
    "exec_limit": 2500,
    "can_indent": false,
    "x_indent": 50,
    "lang": "en",
    "trashId": "p1-sortableTrash"
  });
  parsonsPuzzle.init(initial);
  parsonsPuzzle.shuffleLines();
  $("#p1-newInstanceLink").click(function(event){
      event.preventDefault();
      parsonsPuzzle.shuffleLines();
  });
  $("#p1-feedbackLink").click(function(event){
      event.preventDefault();
      parsonsPuzzle.getFeedback();
  });
})();
</script>


## Binary Search
Construct a method that performs binary search.

<div id="binarysearch-sortableTrash" class="sortable-code"></div> 
<div id="binarysearch-sortable" class="sortable-code"></div> 
<div style="clear:both;"></div> 
<p> 
    <input id="binarysearch-feedbackLink" value="Get Feedback" type="button" /> 
    <input id="binarysearch-newInstanceLink" value="Reset Problem" type="button" /> 
</p> 
<script type="text/javascript"> 
(function(){
  var initial = "public static int binarySearch(int arr[], int target) {\n" +
    "    int low = 0;\n" +
    "    int high = arr.length - 1;\n" +
    "    while (low &lt;= high) {\n" +
    "        int middle = low + (high - low) / 2;\n" +
    "        if (arr[middle] == target) {\n" +
    "            return middle;\n" +
    "        }\n" +
    "        if (arr[middle] &lt; target) {\n" +
    "            low = middle + 1;\n" +
    "        }\n" +
    "        if (arr[middle] &gt; target) {\n" +
    "            high = middle - 1;\n" +
    "        }\n" +
    "    }\n" +
    "    return -1;\n" +
    "}";
  var parsonsPuzzle = new ParsonsWidget({
    "sortableId": "binarysearch-sortable",
    "max_wrong_lines": 10,
    "grader": ParsonsWidget._graders.LineBasedGrader,
    "exec_limit": 2500,
    "can_indent": true,
    "x_indent": 50,
    "lang": "en",
    "show_feedback": true,
    "python3": true
  });
  parsonsPuzzle.init(initial);
  parsonsPuzzle.shuffleLines();
  $("#binarysearch-newInstanceLink").click(function(event){ 
      event.preventDefault(); 
      parsonsPuzzle.shuffleLines(); 
  }); 
  $("#binarysearch-feedbackLink").click(function(event){ 
      event.preventDefault(); 
      parsonsPuzzle.getFeedback(); 
  }); 
})(); 
</script>
