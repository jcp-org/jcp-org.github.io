# Migrating from java.net into JCP GitHub

## Background
With java.net EOL project leads may decide to migrate projects to another location like this JCP GitHub organization.
If you need to learn about GitHub, start reading these [https://guides.github.com/](Quick Introduction pages).

__The planned Java.net closing date is the 12th of May 2017__


## java.net project data
* Tarball of project assets can be requested here: https://community.oracle.com/community/java/javanet-forge-sunset 
* You may also request a redirect to a new homepage of your choice.  
* The old Java.net home page redirects to https://community.oracle.com/community/java now.
* If you need to log in to Java.net you can do so at https://java.net/people/login.
* If you have any questions please ask in the discussion area of the request page here - https://community.oracle.com/community/java/javanet-forge-sunset, or send a note to communitymanager@java.net. 


## Repositories
* Java.net projects may have zero or more repositories. GitHub only hosts repositories.
* It provides exactly one repository for each java.net project analog.
* Each repository includes an optional issue tracker, social tools (updates, readme, documentation, etc.) and the location for your code.
* Because of this, some changes will be required for each migrating project to GitHub. One repository must be designated as the "project replacement" repository. This repository should host all the material for your project.


## Downloads

   * While java.net is online you can download all your content via `wget` command:
   ```
	wget -r --no-parents https://java.net/downloads/$project_name
   ``` 
   where `$project_name` is the name of your project.

   * To import the content to the GitGub repository just clone newly created repository `git clone <rpository path>` and add all your content using usual git commands:
     ``` 
        git add <files>
        git commit <files> -m <message>
        git push
     ```
  
   * HTML files. GitHub doesn't properly set the content type when HTML file is viewed from web interface. 
     So it's recommended to convert all HTML files into marked down (.md) files for proper presentation.
     You can use this converter [to-markdown](https://github.com/domchristie/to-markdown)
     

## Issues
   
   * For import of JIRA issues into GitHub issue tracker you can use [jira-github-issues](https://github.com/doctrine/jira-github-issues) converter.
     JIRA export feature of this converter is implemented via JIRA REST API and will only work while java.net JIRA is online. (until 12th of May 2017)

   * Another possible option is to use JIM comverter https://github.com/brianoliver/jim



## Wikis
GitHub does have a wiki system. Project owners may want to use this system

## E-mail

At the present time there is no direct replacement for java.net mailing lists.


## Maven artifacts
 
Java.net used to provide an authentication interface for project users to publish to maven.central.
There is no replacement fro this feature
    