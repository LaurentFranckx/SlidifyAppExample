---
title       : Interactive linear model comparison
subtitle    : Illustration with the mtcars dataset
author      : Laurent Franckx 
job         : 
framework   : io2012        # {io2012, html5slides, shower, dzslides, ...}
highlighter : highlight.js  # {highlight.js, prettify, highlight}
hitheme     : tomorrow      # 
widgets     : [bootstrap, quiz, shiny, interactive]         # {mathjax, quiz, bootstrap}
mode        : selfcontained # {standalone, draft}
knit        : slidify::knit2slides

---


## Introduction

- app addresses  determinants of  miles per callon (MPG) of passenger cars 
- mtcars dataset contains 32 observations on 11 variables
- app allows user to compare two different linear model specifications with different regressors
- user can fine tune displayed information

--- .class #id 


## Output info of the app

- default summary for the dataset

- histogram for chosen variable

- default summary tables for each model

- model diagnostics  to identify influential observations.

- plots to identify outliers and influential observations 

- ANOVA table comparing the two models if embedded 

--- .class #id 


## Illustration

- The complete app can be found at:

https://lfranckx.shinyapps.io/course_shiny_project/

- Illustration of the choice possibilities for the histogram:

- Next slide: Illustration of regressor choice and model summary:



<div class="row-fluid">
  <div class="span4">
    <form class="well">
      <div class="row-fluid">
        <h4>Show histogram for one selected variable:</h4>
        <label class="control-label" for="histo_var">Chosen variable:</label>
        <select id="histo_var"><option value="mpg">mpg</option>
<option value="cyl" selected>cyl</option>
<option value="disp">disp</option>
<option value="hp">hp</option>
<option value="drat">drat</option>
<option value="wt">wt</option>
<option value="qsec">qsec</option>
<option value="vs">vs</option>
<option value="am">am</option>
<option value="gear">gear</option>
<option value="carb">carb</option></select>
        <script type="application/json" data-for="histo_var" data-nonempty="">{}</script>
        <label for="bin">Maximal number of bins:</label>
        <input id="bin" type="number" value="10"/>
      </div>
    </form>
  </div>
  <div class="span8">
    <h4>The histogram of the chosen variable is:</h4>
    <div id="plothisto" class="shiny-plot-output" style="width: 100% ; height: 400px"></div>
  </div>
</div>

 
--- .class #id 
##Test

- this is some test text

--- .class #id 


<div class="row-fluid">
  <div class="span4">
    <form class="well">
      <h3>Parameters for the  model:</h3>
      <div id="Var_choice_1" class="control-group shiny-input-checkboxgroup">
        <label class="control-label" for="Var_choice_1">
          <h4>Regressors to include in first model:</h4>
        </label>
        <label class="checkbox ">
          <input type="checkbox" name="Var_choice_1" id="Var_choice_11" value="cyl" checked="checked"/>
          <span>cyl</span>
        </label>
        <label class="checkbox ">
          <input type="checkbox" name="Var_choice_1" id="Var_choice_12" value="disp"/>
          <span>disp</span>
        </label>
        <label class="checkbox ">
          <input type="checkbox" name="Var_choice_1" id="Var_choice_13" value="hp"/>
          <span>hp</span>
        </label>
        <label class="checkbox ">
          <input type="checkbox" name="Var_choice_1" id="Var_choice_14" value="drat"/>
          <span>drat</span>
        </label>
        <label class="checkbox ">
          <input type="checkbox" name="Var_choice_1" id="Var_choice_15" value="wt"/>
          <span>wt</span>
        </label>
        <label class="checkbox ">
          <input type="checkbox" name="Var_choice_1" id="Var_choice_16" value="qsec"/>
          <span>qsec</span>
        </label>
        <label class="checkbox ">
          <input type="checkbox" name="Var_choice_1" id="Var_choice_17" value="vs"/>
          <span>vs</span>
        </label>
        <label class="checkbox ">
          <input type="checkbox" name="Var_choice_1" id="Var_choice_18" value="am"/>
          <span>am</span>
        </label>
        <label class="checkbox ">
          <input type="checkbox" name="Var_choice_1" id="Var_choice_19" value="gear"/>
          <span>gear</span>
        </label>
        <label class="checkbox ">
          <input type="checkbox" name="Var_choice_1" id="Var_choice_110" value="carb"/>
          <span>carb</span>
        </label>
      </div>
    </form>
  </div>
  <div class="span8">
    <h4>The first model results are:</h4>
    <pre id="modres1" class="shiny-text-output"></pre>
  </div>
</div>

