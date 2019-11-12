# Azure Batch Templates for CMG Simulation

## 1. Templates Folder

Templates are located in the `templates` folder. They need to follow a **strict** folder structure for Batch Explorer to be able to parese it.

Under the `[templates/..]` folder:

* **index.json** _Index file that reference all applications_
* [myappId]/
    * **index.json** _Index file that reference all different actions you can do in this application_
    * [actionId]/
        * **pool.template.json** _Template to build a pool for this action_
        * **job.template.json** _Template to build a job for this action_

## 2. How to Write a Template

  1. Add an application in `templates/index.json`

  * Add an application info to the `index.json` with id, name, description
  * Create a folder with the id of the application [templates/myappId]
  * Add an icon (*.svg) file in the root of the application folder [myappId/..]
  * Create a `index.json` file inside the foler [myappId/..]

  2. Add the actions and templates for an application

  * Add the action to the `index.json` with id, name, description
  * Create a foler with the id of the action [templates/myappId/actionId]
  * Create a `job.template.json` and a `pool.template.json` file inside the action foler [templates/myappId/actionId/..]

Note on the pool template: all pool templates must have the `numberNodes` and `vmSize` parameters.

* `numberNodes`: with a default value
* `vmSize`: with a default value