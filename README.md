# VSCODE-C-Compiler-and-Executer
This Project can help you to Build C source and Execute Program at ONCE!

## info
This Program helps you 

### tasks.json
```json
{
   "version": "2.0.0",
   "runner": "terminal",
   "type": "shell",
   "echoCommand": true,
   "presentation" : { "reveal": "always" },
   "tasks": [
         {
           "label": "save and compile for C++",
           "command": "gcccmp",
           "args": [
                "cpp",
                "${file}",
                "${fileDirname}",
                "${fileBasenameNoExtension}"
           ],
           "group": "build",

           "problemMatcher": {
               "fileLocation": [
                   "relative",
                   "${workspaceRoot}"
               ],
               "pattern": {
                   "regexp": "^(.*):(\\d+):(\\d+):\\s+(warning error):\\s+(.*)$",
                   "file": 1,
                   "line": 2,
                   "column": 3,
                   "severity": 4,
                   "message": 5
               }
           }
       },
       {
           "label": "save and compile for C",
           "command": "gcccmp",
           "args": [
               "c",
               "${file}",
               "${fileDirname}",
               "${fileBasenameNoExtension}"
           ],
           "group": "build",
           "problemMatcher": {
               "fileLocation": [
                   "relative",
                   "${workspaceRoot}"
               ],
               "pattern": {
                   "regexp": "^(.*):(\\d+):(\\d+):\\s+(warning error):\\s+(.*)$",
                   "file": 1,
                   "line": 2,
                   "column": 3,
                   "severity": 4,
                   "message": 5
               }
           }
       }
   ]
}
```
