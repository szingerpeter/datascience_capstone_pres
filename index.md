---
title       : Next word prediction Application
subtitle    : Project presentation for the word predictor app developed for the Data Science Coursera Specialization Capstone project
author      : Péter Szinger
job         : 
framework   : revealjs      # {io2012, html5slides, shower, dzslides, ...}
highlighter : highlight.js  # {highlight.js, prettify, highlight}
hitheme     : tomorrow      # 
widgets     : []            # {mathjax, quiz, bootstrap}
mode        : selfcontained # {standalone, draft}
knit        : slidify::knit2slides
---

<!-- Limit image width and height -->

<style type='text/css'>
img {
    max-height: 560px;
    max-width: 964px;
}
</style>

<!-- Center image on slide -->

<script src="http://ajax.aspnetcdn.com/ajax/jQuery/jquery-1.7.min.js"></script>

<script type='text/javascript'>
$(function() {
    $("p:has(img)").addClass('centered');
});
</script>

## Next word prediction presentation

Project presentation for the word predictor app developed for the Data Science Coursera Specialization Capstone project

--- .class #id 

## Motivation

Building an algorithm for predicting the most probable word based on the typed in phrase.

<br>
<hr>

Credit goes to [SwiftKey](http://example.com/ "URL") for providing the data,      which I could build my predictive model on.


--- .class #id 

## The model

<div style='text-align: center;'>
    <img height='560' src='https://raw.githubusercontent.com/szingerpeter/hello-world/master/model.jpg'/>
</div>

--- .class #id 

## In detail

The input phrase is cleaned and calculated how many words (n) it includes.
<br>
<br>
Thereafter, the n+1-gram table is checked if there is any match between the input and the n+1-gram table without tail. If there is a match, the most frequently appearing tail is chosen as output and stored in a table along with n+1-gram table information. 
<br>
<br>
Then, the first word from the input is excluded and the process continues with the reduced input until a single word becomes the input.
<br>
Thereafter, the output is chosen, which is referred to the highest n-gram table. If no prediction is found, the output is 'Sorry, nothing found'.

--- .class #id 

## Application

You can find the application [here, on shinyapps](https://szingerpeter.shinyapps.io/Word_predictor_Coursera_Project_NLP/ "URL").

You need to enter the wished phrase and the algorithm will try to predict

And on the other side, the predicted word appears along with the other possible predicted words in a table.



