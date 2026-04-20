---
# Feel free to add content and custom Front Matter to this file.
# To modify the layout, see https://jekyllrb.com/docs/themes/#overriding-theme-defaults

layout: default
title: Parsons Problems - Sorting Algorithms
permalink: /sorting/
---

## Selection Sort
Re-arrange the blocks below to construct a method that carries out selection sort. Drag each line to its correct level of indentation.

<div id="selection-sortableTrash" class="sortable-code"></div> 
<div id="selection-sortable" class="sortable-code"></div> 
<div style="clear:both;"></div> 
<p> 
    <input id="selection-feedbackLink" value="Get Feedback" type="button" /> 
    <input id="selection-newInstanceLink" value="Reset Problem" type="button" /> 
</p> 
<script type="text/javascript"> 
(function(){
  var initial = "public static void selectionSort(int[] elements) {\n" +
    "    for (int j = 0; j &lt; elements.length - 1; j++) {\n" +
    "        int minIndex = j;\n" +
    "        for (int k = j + 1; k &lt; elements.length; k++) {\n" +
    "            if (elements[k] &lt; elements[minIndex]) {\n" +
    "                minIndex = k;\n" +
    "            }\n" +
    "        }\n" +
    "        int temp = elements[j];\n" +
    "        elements[j] = elements[minIndex];\n" +
    "        elements[minIndex] = temp;\n" +
    "    }\n" +
    "}";
  var parsonsPuzzle = new ParsonsWidget({
    "sortableId": "selection-sortable",
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
  $("#selection-newInstanceLink").click(function(event){ 
      event.preventDefault(); 
      parsonsPuzzle.shuffleLines(); 
  }); 
  $("#selection-feedbackLink").click(function(event){ 
      event.preventDefault(); 
      parsonsPuzzle.getFeedback(); 
  }); 
})(); 
</script>

## Insertion Sort
Construct a method that performs insertion sort. Drag each line to its correct level of indentation.

<div id="insertion-sortableTrash" class="sortable-code"></div> 
<div id="insertion-sortable" class="sortable-code"></div> 
<div style="clear:both;"></div> 
<p> 
    <input id="insertion-feedbackLink" value="Get Feedback" type="button" /> 
    <input id="insertion-newInstanceLink" value="Reset Problem" type="button" /> 
</p> 
<script type="text/javascript"> 
(function(){
  var initial = "public static void insertionSort(int[] elements) {\n" +
    "    for (int j = 1; j &lt; elements.length; j++) {\n" +
    "        int temp = elements[j];\n" +
    "        int possibleIndex = j;\n" +
    "        while (possibleIndex &gt; 0 &amp;&amp; temp &lt; elements[possibleIndex - 1]) {\n" +
    "            elements[possibleIndex] = elements[possibleIndex - 1];\n" +
    "            possibleIndex--;\n" +
    "        }\n" +
    "        elements[possibleIndex] = temp;\n" +
    "    }\n" +
    "}";
  var parsonsPuzzle = new ParsonsWidget({
    "sortableId": "insertion-sortable",
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
  $("#insertion-newInstanceLink").click(function(event){ 
      event.preventDefault(); 
      parsonsPuzzle.shuffleLines(); 
  }); 
  $("#insertion-feedbackLink").click(function(event){ 
      event.preventDefault(); 
      parsonsPuzzle.getFeedback(); 
  }); 
})(); 
</script>