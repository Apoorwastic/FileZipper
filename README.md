# FileZipper

File zipper via Huffman coding is a data compression technique used to reduce the size of a file by encoding its contents using Huffman coding in java.

Huffman coding is a lossless data compression algorithm. In this algorithm, a variable-length code is assigned to input different characters. The code length is related to how frequently characters are used. Most frequent characters have the smallest codes and longer codes for the least frequent characters.


The process involves two main parts:


1. Constructing a Huffman tree depending on the frequency of characters through minimum priority queue(The natural ordering of Priority Queue has the least or smallest element at the head of the queue and thus the ordering is ascending) and basic tree implementation.


3. The Huffman tree is constructed by adding two least frequencies of the leaf nodes(characters) and forming the parent node. The process is continued until one single node is achieved which will be the root node.


2. Generating Huffman codes by traversing through the root to each leaf node for every character. The left branch corresponds to appending a '0' to the code, and the right branch corresponds to appending a '1'.


3. The file will be compressed by replacing every single character with its corresponding Huffman code.
Hence, reducing the size of the original data. This results in a more compact representation of the original data, allowing for efficient storage and transmission.


Example for constructing a Huffman tree:


Huffman tree generated from the exact frequencies of the text "this is an example of a Huffman tree". The Huffman tree constructed from the character and its frequencies will be as follows:Huffman Tree

The frequencies and Huffman codes of each character are:

Char	Freq	Code
space	7	111
a	4	010
e	4	000
f	3	1101
h	2	1010
i	2	1000
m	2	0111
n	2	0010
s	2	1011
t	2	0110
l	1	11001
o	1	00110
p	1	10011
r	1	11000
u	1	00111
x	1	10010
 

Hence, for a character represented by 8 bits can be represented in 3,4 or 5 bits reducing the overall size of the file and implementing lossless data copression.The below code is written in java which by using Priority Queue and Hashmaps for Huffman Coding Algorithm and modules like Swing and Awt for creating a simple Graphics User Interface by using JLabels and JButtons for displaying the input file and and output file sizes
