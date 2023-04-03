# How to use?

> The tutorial is divided into two parts: the model part and the texture part

## Model

#### Configuration Tool

1. You need to install Python (I have provided it in the file, if you have already installed you can use your own.)
2. Open cmd, **use the cd command to mount the path to the following path**: 

   `C:\Users\<Your-user-name>\AppData\Local\Programs\Python\Python311` (Python311 maybe not the name if you use other version)
   
3. Type `pip install csplitb` to install `csplitb`.
4. Find the `csplitb` file in the `Scripts` **folder** of the `Python311` folder
5. Cut the `csplitb` file into the `Python311` folder
6. Close the cmd

#### Get the corresponding model file from the game file

> Find the path: WMMT6R\data\course\stage\<Map_name_long>\<map_name>\model\bin

1. Open the `WMMT6R\data\course\stage` folder (This folder stores the files of each day/night map)
2. Take **Kobe** as an example, find the `A_KOBE_DAY_NML` folder (Whether it is DAY or NGT depends on your personal needs)
3. Enter the folder
4. In the `KOBE\model\bin` folder under the `A_KOBE_DAY_NML` folder, you can see many bin files
5. Copy it all to a new folder on the desktop (note plain English)
6. Use **bandzip** to open these bin files separately, and decompress the files without suffix inside to another folder (also put on the desktop, plain English folder)
7. Add the suffix of `.bin` to these files without suffix
8. Obtained

#### Set output folder

1. First of all, you must understand clearly that the above bin file has names such as 101, 102, 103, etc. at the end of its file name, and you must understand clearly how much they are from 101
2. Create a "model" folder on the desktop
3. Create new folders in the order of 101, 102
4. Setup is complete

#### Convert file

1. Open cmd, use the cd command to mount the path to `C:\Users\<your-user-name>\AppData\Local\Programs\Python\Python311`
2. Refer to the following code:

   `./python csplitb -f <path to output folder> -s .nud -n 1 4E445744 <path to bin file>`
   
   Take a file in Kobe as an example:
   `./python csplitb -f C:\Users\Takas\Desktop\model\101\ -s .nud -n 1 4E445744 C:\Users\Takas\Desktop\original\A_KOBE_DAY_NML_KOBE_SECT101.bin`
   Press Enter, the converted nud file will appear in the output folder

3. Repeat the second step to convert all bin files into nud and store them in the corresponding output folder
4. Export is complete

#### Import into 3dsmax

1. Put the nud file and the texture in the same folder (the names of the nud model files will conflict, it is recommended to import 101 and 102 in the order of such folders)
2. Open 3dsmax
3. Drag the PokkenTournament_NDWD.ms file into max
4. No need to adjust popup settings
5. Click Import to start importing from the first item
6. After importing all nud models, you can see the whole map




