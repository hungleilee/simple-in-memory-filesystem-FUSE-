In its original form, the filesystem was limited by static allocation, which restricted the number of directories and files it could handle. This was due to the use of fixed-size arrays for storing directory and file data, imposing a ceiling on the maximum quantity of directories and files manageable within the system.

To overcome these limitations, the filesystem underwent significant modifications, shifting from a static to a dynamic allocation model. The key changes include:

Dynamic Directory Management: The static array for directories was replaced with a dynamically allocated array. This change allows the filesystem to expand the directory list as needed, removing the upper limit on the number of directories.

Dynamic File Management: Similarly, the file metadata storage was transitioned to a dynamic structure, enabling the filesystem to accommodate an increasing number of files without a predefined limit.

Linked List for File Content: To support larger file sizes, file contents are now managed using a linked list for each file. This approach allows for the storage of file sizes beyond the constraints of static arrays.

These enhancements significantly improve the scalability and flexibility of the filesystem, making it more capable of handling varying numbers and sizes of files and directories in a memory-efficient manner.

The project is a reference to "Writing a Less Simple, Yet Not Stupid Filesystem Using FUSE in C".
```
make
```
```
./lsysfs -f [mount point]
```
