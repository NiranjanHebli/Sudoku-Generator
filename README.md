
# Sudoku Generator 

In this project I have implemented a sudoku generator using javascript.For the frontend I have used some basic CSS integrated with JS to make it very interactive.The project is deployed in the form of a game so you can try solving the generated puzzle on the site whose link is given below:

Deployed using Gcloud: https://sunny-caldron-373813.ue.r.appspot.com/                                                                                                      
Deployed on Github Pages:https://github.com/NiranjanHebli/Sudoku-Generator/deployments/activity_log?environment=github-pages

## Screenshots


![Sudoku Generator - Google Chrome 16-02-2022 19_48_00](https://user-images.githubusercontent.com/84934990/154283968-9c9ae07b-07dd-41d4-8b73-ce8231a2b104.png)


![Sudoku Generator - Google Chrome 16-02-2022 19_47_49](https://user-images.githubusercontent.com/84934990/154284069-f112f8cb-805c-47fd-a447-44f774ba0d7b.png)


## Features

- Light/dark mode toggle
- Various difficulty levels
- Interactive interface


## Demo

A short demo:

![ezgif com-gif-maker](https://user-images.githubusercontent.com/84934990/154282602-c2237c2b-99ec-4820-8e89-9515d6afec99.gif)

## How to Deploy On Google Cloud?

First step, you have to enable App Engine Admin API in your Project,After enabling the API go to Cloud Shell and write the Command:
 ```gcloud app create```

Second step,open the Text Editor and create a new directory www and add the project folders and files in it.In the root directory create a file deploy.yaml add the following code in it:
```
runtime: python27                             
api_version: 1                                  
threadsafe: true                      

handlers:                      
\- url: /                      
  static_files: www/index.html                              
  upload: www/index.html                               
   
\- url: /(.*)                       
  static_files: www/\1
  upload: www/(.*)
  
 ```
Third step,run the following commands:

```gcloud app deploy deploy.yaml                              
   gcloud app browse```                              
(remember to run this commands in the root directory)

There you go :D
