# Azure Batch Templates for CMG Simulation

## 01 Templates Folder

Templates are located in the `templates` folder. They need to follow a **strict** folder structure for Batch Explorer to be able to parese it.

* templates/
    * index.json _Index file that reference all applications_
    * [myappId]/
        * index.json _Index file that reference all different actions you can do in this application_
        * [actionId]/
            * pool.template.json _Template to build a pool for this action_
            * job.template.json _Template to build the job for this action_

## 02 How to Write a Template

1. Add application in `templates/index.json`

* Add it