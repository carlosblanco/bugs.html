bugs.html
=========

Simple issue tracking that incorporates a kanaban board contained in one single html file. 

![bugs.html](/doc/bugs-html.jpg)

Overview
=========

bugs.html is a simple one file html application that can be used to track issues about your development project. 
It has no dependencies since all the required tools are bundled inside this one file. It can be dropped in the doc folder
of your repository and then tracked by your source control tool along with your project's code.


Usage
=====

You can drag taskss around and drop them into one of the development states. If you want to edit, 
add or remove tasks, click on the "Data" button on the top right corner. You can then:

* Click on the New Task button to clear the input boxes and generate a new ID automatically.
* Save a task with the same ID as an existing one to update it.
* Double click on a task from the list of tasks to delete them. 
* Group taks into milestones by typing the same value in the Milestone text box.
* Vissually differentiate on the Kanban board between Defects and Improvements.
* Vissually notice the completion progress of your milestone with the progress bar on the top right corner. 

bugs.html has two modes for storing data.

* *Manual Mode* is excelent for tracking your bugs inside your source control system. 
Just drop bugs.html file inside your repository and use it. Then once you're done click the Get Data button, copy it 
by clicking CTRL+C and replace the data in the HTML file. You bugs will be tracked inside you repo. Excelent for simple
projects that don't need a bug trcking software which bigger than the project itself.

* *Automatic Mode* saves your changes automatic as you're making changes to the data. This mode is a more user friendly
and behaves more like onw of those big bug tracking systems. *This mode is still beta. See the TODO section for more info*

TODO
====

* Use PouchDB, once it comes out of alpha, to save data when using automatic save mode. 
Right now the storage is done using localStorage, or browser cookies if localStorage is not supported.
