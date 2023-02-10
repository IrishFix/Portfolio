# My Programming Portfolio

## This Portfolio contains any and all relevant projects and otherwise showing my experience in programming over the years I have hobbied and careered in it!

## • The programming languages I know
#### Following, is a list of all of the programming languages I know and understand; my understanding of some is higher than of some others however I have worked with all of them within the last year.
<img src="https://upload.wikimedia.org/wikipedia/commons/thumb/c/cf/Lua-Logo.svg/2048px-Lua-Logo.svg.png" alt="LUA" width="100"/> &nbsp; &nbsp; &nbsp; <img src="https://user-images.githubusercontent.com/60940670/184181684-364140f7-2c85-42fb-851b-9b228456e191.png" alt="PYTHON" width="100"/> &nbsp; &nbsp; &nbsp; <img src="https://upload.wikimedia.org/wikipedia/commons/thumb/1/18/ISO_C%2B%2B_Logo.svg/1200px-ISO_C%2B%2B_Logo.svg.png" alt="C++" width="100"/> &nbsp; &nbsp; &nbsp; <img src="https://upload.wikimedia.org/wikipedia/commons/thumb/4/4c/Typescript_logo_2020.svg/512px-Typescript_logo_2020.svg.png" alt="TypeScript" width="100"/> &nbsp; &nbsp; &nbsp; <img src="https://upload.wikimedia.org/wikipedia/commons/thumb/9/99/Unofficial_JavaScript_logo_2.svg/480px-Unofficial_JavaScript_logo_2.svg.png" alt="JavaScript" width="100"/>

### &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Lua&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Python&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;C++&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;TypeScript&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;JavaScript

## • Projects
#### ``(Will contain relevant snippits of code in some of the languages listed above in order to show functionality to those who understand it!)``
### 1) Directory Sorter.
#### I developed this small Python project as a way to automatically and logically sort and clear my Desktop if it got too cluttered.
#### It worked very well and was reasonably customisable, however, not that complex. Code shown below!
``DirectorySorter.py``
```python
 1 | import os
 2 | import shutil
 3 |
 4 | Sort_Link = open('Sort_Link.txt')
 5 | Read_Link = Sort_Link.read()
 6 |
 7 | exec(Read_Link)
 8 |
 9 | for Path in os.listdir(To_Sort):
10 |    for Ext, Sort in Sort_Files.items():
11 |        if Ext in Path.lower():
12 |            try:
13 |                shutil.move(To_Sort+"/"+Path, Sort)
14 |                print("File that was located at ["+To_Sort+"/"+Path+"] is now located at ["+Sort+"] because it had '"+Ext+"' in it")
15 |            except:
16 |                print("File that was located at ["+To_Sort+"/"+Path+"] could not be relocated to ["+Sort+"] because it errored")
17 |                Delete_File = input("Would you like to delete the file located at ["+Path+"] ?: ")
18 |                if Delete_File.lower() == "y" or Delete_File.lower() == "yes":
19 |                    print("Deleting the file located at ["+To_Sort+"/"+Path+"]")
20 |                    os.remove(To_Sort+"/"+Path)
21 |                else:
22 |                    print("Skipping the file located at ["+To_Sort+"/"+Path+"]")
23 |        else:
24 |            if os.path.isdir(To_Sort+"/"+Path):
25 |                try:
26 |                    shutil.move(To_Sort+"/"+Path, 'C:/Users/benkn/Desktop/MAIN/Loose Folders')
27 |                except:
28 |                    print("Could not move folder located at ["+To_Sort+"/"+Path+"] to Loose Folders")
```

#### You may notice on line 4 of the above code, that it uses a file referenced as ``Sort_Link.txt``; this is where the customisability comes in.

#### ``Sort_Link.txt`` is a txt file that stores a Python table and python variable set as plain text, allowing you to give it the extensions and locations without opening the code! Example of ``Sort_Link.txt`` below:

``Sort_Link.txt``
```
  1 | Sort_Files = {
  2 |            ".png":'D:/MAIN/PNG, JPG',
  3 |            ".obj":'D:/MAIN/OBJ, MTL, TEX, BLENDER',
  4 |            ".mtl":'D:/MAIN/OBJ, MTL, TEX, BLENDER',
  5 |            ".mp3":'D:/MAIN/MP3, MP4',
  6 |            ".mp4":'D:/MAIN/MP3, MP4',
  7 |            ".rbxm":'D:/MAIN/RBXM',
  8 |            ".rbxl":'D:/MAIN/STUDIO FILES',
  9 |            ".txt":'D:/MAIN/Text',
 10 |            ".jpg":'D:/MAIN/PNG, JPG',
 11 |            ".py":'D:/MAIN/Loose Coding Projects',
 12 |            ".lnk":'D:/MAIN/Shortcuts',
 13 |            ".pdn":'D:/MAIN/P.net IMAGES',
 14 |            ".exe":'D:/MAIN/Exe'
 15 |            }
 16 |
 17 | To_Sort = 'C:/Users/benkn/Desktop'
```

#### It was designed to take a ``Sort_Link.txt`` file, and use that data to sort the listed ``To_Sort`` directory. It would run through all files, and when it cannot move one to the desired location it will prompt you, asking what to do with it!

