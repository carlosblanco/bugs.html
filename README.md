# bugs.html

Simple issue tracking that incorporates a kanaban board. The hole thing contained in one single html file. 

![bugs.html](/doc/bugs-html.png)

### Overview

bugs.html is a simple one file html application that can be used to track issues for your development project. 
It has no dependencies since all the required tools are bundled inside this one file. It can easily be dropped into 
the doc folder of your repository and then in this way be tracked by your source control tool along with your project's 
code.


### Usage

Download the latest version from [here](https://raw.github.com/carlosblanco/bugs.html/master/bugs.html). Open it in your
favorite text editor and prove a title for your project by setting the value for the title variable. You can also 
provide a logo image by settting the value of the logo variable to the base64 encoding of your image. 

    <script>
     var logo ;//= "Your org's logo image base64 encoded"
     var title;//= "Your project name";
     var tasks;// = []
     
    </script>

You can then drag tasks around and drop them into one of the available development states. If you want to edit, 
add or remove tasks, click on the "Data" button on the top right corner. Then you can:

* Click on the New Task button to clear the input boxes and generate a new ID automatically so you can create a new task.
* Click on a task from the list of tasks and then save it with the same ID to update it.
* Double click on a task from the list of tasks to delete them. 
* Group taks into projects and milestones by typing the same value in the Project or Milestone text box.
* Vissually differentiate on the Kanban board between Defects and Improvements.
* Vissually notice the completion of your project/milestone with the progress bar on the top right corner. 


### Storing Data

bugs.html has two modes for storing data. The way to select what storage method to use is to set or not the value for 
the tasks variable located at the top of the file. If the tasks variable is not defined then Automatic Mode will 
be enabled (this mode is still beta but works for simple projects with short durations). Manual Mode will be enabled 
if the tasks variable has a value set.

* *Manual Mode* is excelent for tracking your bugs inside your source control system. 
Just drop bugs.html file inside your repository and use it. Then once you're done click the "Get Data" button, copy the 
content of the dialog by clicking CTRL+C and then replace the data for the tasks variable in the HTML file with the data
you just copied. You bugs will be tracked inside you repo. Excelent for simple projects that don't need a bug trcking software 
which is bigger than the project itself.

* *Automatic Mode* saves your changes automatic as you're making changes to the data. This mode is a more user friendly
and behaves more like one of those big bug tracking systems. *This mode is still beta. See the TODO section for more info*

### TODO

* Use PouchDB, once it comes out of alpha, to save data when using automatic save mode. 
Right now the storage is done using localStorage, or browser cookies if localStorage is not supported.
