# This Portfolio contains any and all relevant projects and otherwise showing my experience in programming over the years I have hobbied and careered in it!

## • The programming languages I know
#### Following, is a list of all of the programming languages I know and understand; my understanding of some is higher than of some others however I have worked with all of them within the last year.
<img src="https://upload.wikimedia.org/wikipedia/commons/thumb/c/cf/Lua-Logo.svg/2048px-Lua-Logo.svg.png" alt="LUA" width="100"/> &nbsp; &nbsp; &nbsp; <img src="https://user-images.githubusercontent.com/60940670/184181684-364140f7-2c85-42fb-851b-9b228456e191.png" alt="PYTHON" width="100"/> &nbsp; &nbsp; &nbsp; <img src="https://upload.wikimedia.org/wikipedia/commons/thumb/1/18/ISO_C%2B%2B_Logo.svg/1200px-ISO_C%2B%2B_Logo.svg.png" alt="C++" width="100"/> &nbsp; &nbsp; &nbsp; <img src="https://upload.wikimedia.org/wikipedia/commons/thumb/4/4c/Typescript_logo_2020.svg/512px-Typescript_logo_2020.svg.png" alt="TypeScript" width="100"/> &nbsp; &nbsp; &nbsp; <img src="https://upload.wikimedia.org/wikipedia/commons/thumb/9/99/Unofficial_JavaScript_logo_2.svg/480px-Unofficial_JavaScript_logo_2.svg.png" alt="JavaScript" width="100"/>

### &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Lua&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Python&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;C++&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;TypeScript&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;JavaScript

## • Projects
#### ``(Will contain relevant snippits of code in some of the languages listed above in order to show functionality to those who understand it!)``
### 1) Directory Sorter.
#### I developed this small Python project as a way to automatically and logically sort and clear my Desktop if it got too cluttered.
#### It worked very well and was reasonably customisable, however, not that complex. Code shown below!

```lua
import os
import shutil

Sort_Link = open('Sort_Link.txt')
Read_Link = Sort_Link.read()

exec(Read_Link)

for Path in os.listdir(To_Sort):
    for Ext, Sort in Sort_Files.items():
        if Ext in Path.lower():
            try:
                shutil.move(To_Sort+"/"+Path, Sort)
                print("File that was located at ["+To_Sort+"/"+Path+"] is now located at ["+Sort+"] because it had '"+Ext+"' in it")
            except:
                print("File that was located at ["+To_Sort+"/"+Path+"] could not be relocated to ["+Sort+"] because it errored")
                Delete_File = input("Would you like to delete the file located at ["+Path+"] ?: ")
                if Delete_File.lower() == "y" or Delete_File.lower() == "yes":
                    print("Deleting the file located at ["+To_Sort+"/"+Path+"]")
                    os.remove(To_Sort+"/"+Path)
                else:
                    print("Skipping the file located at ["+To_Sort+"/"+Path+"]")
        else:
            if os.path.isdir(To_Sort+"/"+Path):
                try:
                    shutil.move(To_Sort+"/"+Path, 'C:/Users/benkn/Desktop/MAIN/Loose Folders')
                except:
                    print("Could not move folder located at ["+To_Sort+"/"+Path+"] to Loose Folders")
```

