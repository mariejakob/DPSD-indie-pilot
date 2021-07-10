# DPSD-indie-pilot

This project contains the implementation of a recognition memory experiment using Javascript and the JSPsych library.
The experiment will be the pilot study for my Master's Thesis on the independence assumption of Yonelinas (1994) 
Dual Process Signal Detection Theory Model. 

Author: Marie Jakob marie.a.jakob@gmail.com

Project Contributors: Constantin Meyer-Grant, Karl Christoph Klauer

Department of Psychology, Social Psychology and Methodology Unit

University of Freiburg, April 2021

Status: first version of the strength and LOP condition done --> .jzip folders contain the final JATOS versions

__Those versions are considered archived and do not work with the current versions of the experiment-files!_

### TODOs

* implementation familiarity rating
* instructions familiarity rating
* fix some things in the data saving function


### Procedural Details (short)

* __Learning Phase__ (type of manipulation (LOP vs. strength) is manipulated between participants)
* _LOP condition_: Participants are sequentially presented with words and are instructed to type either a semantically related word ("deep" condition) or the number of vowels of the given word ("shallow" condition) into a text box
* _Strength condition_: Participants are sequentially presented with words for a fixed duration and are instructed to remember them. 
* Some words are presented once ("weak items"), some three times ("strong items")
* __Test Phase__: All words from the learning phase + an equal amount of new words are presented. Participants have to make a Remember-Know-New judgement, 
followed by a familiarity rating on a pseduo-continuous scale



### Files

```index-LOP.html```: main file for the LOP group -> open locally to test the experiment in the LOP condition

```index-strength.html```: main file for the strength group -> open locally to test the experiment in the strength condition

```.gitignore```: the usual stuff

```LICENCE```: copyright information

```instructions.docx```: Instructions (not up to date, several changes were directly made in the implementation)


**Folders**

```experiment-files```:
* ```demographics.js```: Contains demographic questions
* ```dummy_stimuli.js```: Contains dummy stimuli in a format that can be read from the other .js files. Generated by stimuli_to_json.py
* ```functions.js```: Contains all functions used in the experiment and related files.
* ```global-variables.js```: Declares and sets all global variables that are used
* ```instructions.js```: Contains the instructions as JSPsych variables
* ```post-exp-questions.js```: Contains the post-experimental questions


```stimuli```: 
* ```description word list.docx```: Description of the stimuli
* ```dummy_stimuli.csv```: random strings serving as dummy stimuli until we've decided on the actual stimuli. Generated by the python script
* ```stimuli_to_json.py```: Reads the wordpool and writes the words to a .js file so that the stimuli can be used from the other .js files
also contains functions to generate dummy stimuli, save them, and put those into a .js file
* ```wordpool.xlsx```: Actual stimuli

```test```: Contains test data files and a short R script to test whether the randomization works and all important information is saved in the data.

```jspsych-6.3.0```: Latest version of the jspsych library. See https://github.com/jspsych/jsPsych + some modified files (-custom).
