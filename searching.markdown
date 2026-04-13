---
# Feel free to add content and custom Front Matter to this file.
# To modify the layout, see https://jekyllrb.com/docs/themes/#overriding-theme-defaults

layout: default
title: Parsons Problems - Searching Algorithms
permalink: /searching/
---

## Linear Search
Re-arrange the blocks below to construct a method that carries out linear search. Drag each line to its correct level of indentation.

<div id="linearsearch-sortableTrash" class="sortable-code"></div> 
<div id="linearsearch-sortable" class="sortable-code"></div> 
<div style="clear:both;"></div> 
<p> 
    <input id="linearsearch-feedbackLink" value="Get Feedback" type="button" /> 
    <input id="linearsearch-newInstanceLink" value="Reset Problem" type="button" /> 
</p> 
<script type="text/javascript"> 
(function(){
  var initial = "public static int linearSearch(int[] arr, int target) {    \n" +
    "    for (int i = 0; i &lt; arr.length; i++) {    \n" +
    "        if (arr[i] == target) {    \n" +
    "            return i;    \n" +
    "        }    \n" +
    "    }\n" +
    "    return -1;    \n" +
    "}";
  var parsonsPuzzle = new ParsonsWidget({
    "sortableId": "linearsearch-sortable",
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
  $("#linearsearch-newInstanceLink").click(function(event){ 
      event.preventDefault(); 
      parsonsPuzzle.shuffleLines(); 
  }); 
  $("#linearsearch-feedbackLink").click(function(event){ 
      event.preventDefault(); 
      parsonsPuzzle.getFeedback(); 
  }); 
})(); 
</script>


## Binary Search
Construct a method that performs binary search. Drag each line to its correct level of indentation.

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
    "        } else if (arr[middle] &lt; target) {\n" +
    "            low = middle + 1;\n" +
    "        } else {\n" +
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
