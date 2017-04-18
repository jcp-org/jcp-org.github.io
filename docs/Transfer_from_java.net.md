# Content transfer from java.net

Here are some technical guidelines for transfer of the availbale content from the java.net site to JCP GitHub Organization.

__ATTENTION:__ All these instructions for exporting content from java.net are applicable while java.net is online - until 28th of April 2017. 
After that date please contact java.net admins to get the content of your projects.

1. __Files in the donwload area__

   * To download the files from downloads area of java.net you can just use `wget` command:
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
     

2. __JIRA Issues__
   
   * For import of JIRA issues into GitHub issue tracker you can use [jira-github-issues](https://github.com/doctrine/jira-github-issues) converter.
     JIRA export feature of this converter is implemented via JIRA REST API and will only work while java.net JIRA is online. (until 28th of April 2017)
    