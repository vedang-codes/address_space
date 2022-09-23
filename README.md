# address_space
C program to be executed in Unix environment

* It takes three command line arguments with the following information:
  a) The type of the page table. Only two values 1 and 2 can be accepted. 1 means single-level 
     linear page table and 2 means two-level tree-structured page table.
  b) The total number of bits in the binary format of the memory address. This can be an integer 
     in the range [8..65].
  c) The page size in terms of the number of KB (1024 Bytes). This can be 1, 2, 4, 8, 16, 32, 
     64, 128, 256, 512

* If the given three arguments are not consistent with each other, your program will terminate with 
  an error message. The error message should include an explanation why the arguments cannot be 
  accepted. For example, (1, 10, 2) cannot be accepted because with 10-bit address, the memory size 
  is 1 KB, so it is impossible to have a page of size 2 KB. 

* If the given three arguments are consistent, your program should give the following output (in decimal): 
  a) the size of the memory in terms of the number of bytes, the number of KB, the number of MB, or the number of GB, whichever is the most appropriate.
  b) the total number of pages
  c) the total number of page table entries
  d) the size of the page table in terms of the number of bytes
  e) the total number of bits in an address for the VPN
  f) the total number of bits in an address for the offset within a page
  g) the total number of page table entries in a page of a page table (type 2 only)
  h) the total number of pages in a page table (type 2 only)
  i) the total number of bits in an address for the page directory index (type 2 only)
  j) the total number of bits in an address for the page table index (type 2 only)
  
* After the output of the above data, your program should repeatedly prompt the user to input a decimal virtual address and output the related information (including     any error messages). 

* If the input address is not consistent with the command line arguments, your program should print an error message and prompt the user for the next input of the       virtual address. The error message should include an explanation why the input cannot be accepted. For example, with 10-bit address, an input of virtual address       12345 cannot be accepted because the memory size is only 1 KB.

* If the input address is consistent with the command line arguments, your program should provide the following output:
  a) the VPN of the input address in decimal format
  b) the page offset of the input address in decimal format
  c) the page directory index of the input address in decimal format (type 2 only)
  d) the page table index of the input address in decimal format (type 2 only)
  e) the input address in binary format
  f) the VPN of the input address in binary format
  g) the page offset of the input address in binary format
  h) the page directory index of the input address in binary format (type 2 only)
  i) the page table index of the input address in binary format (type 2 only)

* Note that the numbers in binary format should include zeros at the beginning if necessary. After the above output, the program should prompt the user for the next     input of the virtual address.

  
