# ee442-assignment-3-solved
**TO GET THIS SOLUTION VISIT:** [EE442 Assignment 3 Solved](https://www.ankitcodinghub.com/product/ee442-solved/)


---

📩 **If you need this solution or have special requests:** **Email:** ankitcoding@gmail.com  
📱 **WhatsApp:** +1 419 877 7882  
📄 **Get a quote instantly using this form:** [Ask Homework Questions](https://www.ankitcodinghub.com/services/ask-homework-questions/)

*We deliver fast, professional, and affordable academic help.*

---

<h2>Description</h2>



<div class="kk-star-ratings kksr-auto kksr-align-center kksr-valign-top" data-payload="{&quot;align&quot;:&quot;center&quot;,&quot;id&quot;:&quot;112883&quot;,&quot;slug&quot;:&quot;default&quot;,&quot;valign&quot;:&quot;top&quot;,&quot;ignore&quot;:&quot;&quot;,&quot;reference&quot;:&quot;auto&quot;,&quot;class&quot;:&quot;&quot;,&quot;count&quot;:&quot;1&quot;,&quot;legendonly&quot;:&quot;&quot;,&quot;readonly&quot;:&quot;&quot;,&quot;score&quot;:&quot;5&quot;,&quot;starsonly&quot;:&quot;&quot;,&quot;best&quot;:&quot;5&quot;,&quot;gap&quot;:&quot;4&quot;,&quot;greet&quot;:&quot;Rate this product&quot;,&quot;legend&quot;:&quot;5\/5 - (1 vote)&quot;,&quot;size&quot;:&quot;24&quot;,&quot;title&quot;:&quot;EE442 Assignment 3 Solved&quot;,&quot;width&quot;:&quot;138&quot;,&quot;_legend&quot;:&quot;{score}\/{best} - ({count} {votes})&quot;,&quot;font_factor&quot;:&quot;1.25&quot;}">

<div class="kksr-stars">

<div class="kksr-stars-inactive">
            <div class="kksr-star" data-star="1" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" data-star="2" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" data-star="3" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" data-star="4" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" data-star="5" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
    </div>

<div class="kksr-stars-active" style="width: 138px;">
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
    </div>
</div>


<div class="kksr-legend" style="font-size: 19.2px;">
            5/5 - (1 vote)    </div>
    </div>
&nbsp;

• Send your homework compressed in an archive file with name “eXXXXXXX_ee442_pa3.tar.gz”, where X’s are your 7-digit student ID number. You will not get full credit if you fail to submit your work as required.

• Your work will be graded on its correctness, efficiency, clarity and readability as a whole.

• Comments will be graded. You should insert comments in your source code at appropriate places without including any unnecessary detail.

o Later submissions : HW will NOT be evaluated.

• The homework must be written in C (not in C++ or any other language).

• You should not call any external programs in your code.

• Check what you upload. Do not send corrupted, wrong files or unnecessary files.

• The homework is to be prepared individually. Group work is not allowed. Your code will be checked for cheating.

• The design should be your original work. However, if you partially make use of a code from the Web, give proper reference to the related website in your comments. Uncited use is unacceptable.

Description:

In this homework, you are expected to implement a simple user mode file system (FS) that employs a file allocation table (FAT). The FS obtained could be used on a physical drive or on a disk image to be named as “disk”.

The FS consist of three parts:

1. File Allocation Table

2. File List

3. Disk Data

Block size is 512 bytes, meaning that the files are written in 512 byte blocks. FS has no directories.

1. File Allocation Table (FAT):

• FAT consists of 4096 entries. Each entry is 4 bytes long and bytes are laid out in little-endian order (meaning the most significant byte is at the highest address).

• The first entry must always be 0xFFFFFFFF.

• If an entry is 0x0, then the block is assumed to be empty.

• If an entry is 0xFFFFFFFF, then the block is assumed to be the last block of a file.

• If an entry has a value between 0x0 and 0x1000, the value points to the entry in the table where the next block of the file is located.

Example: Consider three files; “File A” occupies 4 blocks, “File B” occupies 2, and “File C” occupies 1.

Then, the following FAT is possible (Table 1):

Entry Value Entry Value Entry Value Entry Value

0000 0 x FF FF FF FF 0001 0 x 02 00 00 00 0002 0 x 05 00 00 00 0003 0 x 04 00 00 00

0004 0 x FF FF FF FF 0005 0 x 06 00 00 00 0006 0 x FF FF FF FF 0007 0 x 00 00 00 00

0008 0 x 00 00 00 00 0009 0 x FF FF FF FF 0010 0 x 00 00 00 00 0011 0 x 00 00 00 00

4092 0 x 00 00 00 00 4093 0 x 00 00 00 00 4094 0 x 00 00 00 00 4095 0 x 00 00 00 00

Table 1: Example File Allocation Table

In Table 1, “File A” occupies the blocks 1, 2, 5 and 6, while “File B” occupies the blocks 3 and 4, and “File C” occupies only block 9. Notice that the entries are laid out in little-endian style, so 0x05000000 simply means the number 5.

2. File List:

• The file list contains 128 items, each of which is 256 bytes long.

• A file item in the list has the following layout:

 File name: Maximum of 247 characters + the ‘/0’ string delimiter (248 bytes)

 First block: Location of the first block of the file in the FAT (4 bytes)

 File size: Size of the file in bytes (4 bytes)

Example: Following the previous example, let “File A” be 2000 bytes long (4 blocks), “File B” be 900 bytes long (2 blocks), and “File C” be 100 bytes long (1 block). Then, the following file list (Table 2) is valid:

Item File name First block File size (Bytes)

000 “File A” 1 2000

001 “File B” 3 900

002 “File C” 9 100

003 NULL 0 0

127 NULL 0 0

Table 2: Example File List

3. Data:

File contents are written in 512-byte chunks.

Core Features:

FS is expected to support the following features:

1. Formatting: Overwrites the disk header with an empty FAT and an empty file list. The user should be able to format a disk from the terminal by typing ./myfs disk –format The first entry must be 0xFFFFFFFF, the others must be 0x00000000.

2. Writing: Copies a file to the disk. The command ./myfs disk -write source_file destination_file should obtain the source_file and write it to the disk with name destination_file.

3. Reading: Copies a file from the disk. The command ./myfs disk -read source_file destination_file should get the source_file in the disk and copy it to the computer as destination_file.

4. Deleting: Deletes a file in the disk. Entries occupied by the deleted file should be emptied (0x00000000). Command: ./myfs disk -delete file

5. Listing: Prints all visible files (i.e. files whose names do not start with a ‘.’) and their respective sizes in the disk. Alphabetical order is not required. Command: ./myfs disk –list

6. Sorting: Sorts files by their sizes. Command (ascending): ./myfs disk –sorta Command (descending): ./myfs disk –sortd

7. Printing File List: Prints File List to the “filelist.txt” file. The layout of the output will be same as File List in Table 2. All the entries of the file (including empty ones) should be printed. Command: ./myfs disk –printfilelist

8. Printing FAT: Prints FAT to the “fat.txt” file. The layout of the output will be same as FAT in Table 1 (Use tab character to separate columns.). All the entries of the FAT (including empty ones) should be printed. Command: ./myfs disk –printfat

9. Disk Defragmentation: Merges fragmented files into one contiguous space or block. This will allow your system to access files save new ones more efficiently. Command: ./myfs disk –defragment.

*In order to test the correctness of the “Disk Defragmentation” you need to implement “Printing FAT” feature. Without implementing it, you will not get a grade from “Disk Defragmentation”.

Example: Consider the FAT for the first example. After defragmentation, the following FAT will be obtained.

Entry Value Entry Value Entry Value Entry Value

0000 0 x FF FF FF FF 0001 0 x 02 00 00 00 0002 0 x 03 00 00 00 0003 0 x 04 00 00 00

0004 0 x FF FF FF FF 0005 0 x 06 00 00 00 0006 0 x FF FF FF FF 0007 0 x FF FF FF FF

0008 0 x 00 00 00 00 0009 0 x 00 00 00 00 0010 0 x 00 00 00 00 0011 0 x 00 00 00 00

4092 0 x 00 00 00 00 4093 0 x 00 00 00 00 4094 0 x 00 00 00 00 4095 0 x 00 00 00 00

Table 3: Example Defragmented File Allocation Table

Extra Features: In addition to core features, the following should also be implemented for a full functional FS (You are NOT required to do so) within the scope of the present homework.

1. Renaming: Changes the name of the target file in the disk. Sample command: ./myfs disk -rename file_name new_name

2. Duplicating: Creates a copy of a file in the disk with a new name. Sample command: ./myfs disk

-duplicate file_name new_name

3. Hiding &amp; Unhiding: Hides or unhides the file in the disk. It should throw an error if the user tries hiding an already hidden file or unhiding an already visible file. Sample commands: ./myfs disk -hide file and ./myfs disk -unhide file

Other Specifications:

Your code should be written in C and compiled with GCC (GNU Compiler Collection). You can compile your code in the command line by typing gcc myfs.c -o myfs -lm

Hints:

• For disk in the terminal commands, you can use either a real drive or a disk image, since there is not any difference between the two in Unix systems.

 If a disk image is used, the image should pre-exist, and should be formatted before used. To create a disk image, simply enter dd if=/dev/zero of=disk.image bs=2146304 count=1 in the terminal. This will create a “disk.image” file in the current directory. Then, you can format the image, for example, with the command ./myfs disk.image -format

 void Format();

 void Write(char *srcPath, char *destFileName);

 void Read(char *srcFileName, char *destPath);

 void Delete(char *filename);

 void List();

 void SortA();

 void SortD();

 void PrintFileList();

 void PrintFAT();

 void Defragment();

• While implementing the writing feature, you can search the file allocation table for empty blocks. For each block, use a buffer to transfer data from the local file to the disk. Do not forget to keep the first block information since you will need to store it in the file list.

 The buffer can be declared as char buffer[512];

 Before writing the file data to the disk, you can use the fseek function to adjust the offset of the file position.

• While implementing the reading feature, you can search the file list for the target file name and pick the first entry whose name matches. Then, you can copy the file block by block using a similar buffer.
