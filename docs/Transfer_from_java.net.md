# Content transfer from java.net

Here are some technical guidelines regarding transfer of the availbale content from the java.net site to JCP GitHub Organization.

__ATTENTION:__ All these instructions for exporting content from java.net are applicable while java.net is online - until 28th of April. 
After that date please contact java.net admins to get the content of your projects.

1. __Files in the donwload area__

   * To download the files from downloads area of java.net you can just use `wget` command:
   ```wget -r --no-parents https://java.net/downloads/$project_name``` where `$project_name` is the name of your project.

   * To import the content to the GitGub repository just clone newly created repository `git clone <rpository path>` and add all your content using usual git commands:
     ``` git add <files>
         git commit <files> -m <message>
         git push```

   