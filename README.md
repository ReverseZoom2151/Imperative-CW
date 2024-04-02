# Binary Converter (visualise.c)

The Binary Converter is a versatile command-line tool designed for a wide audience including developers, students, and enthusiasts who need a fast and reliable method for converting decimal numbers to their binary representations and vice versa. This tool is invaluable for those looking to deepen their understanding of low-level computing operations, binary arithmetic, and how data is represented digitally. It supports a comprehensive range of data types—both signed and unsigned integers, characters, and long integers. Beyond mere conversion, it verifies the accuracy of binary strings and adeptly handles conversions for both positive and negative numbers, making it an essential utility for various computational applications.

## Key Features

- **Decimal to Binary Conversion:** Convert decimal numbers of different data types (int, unsigned int, char, unsigned char, long) to their binary string representation. This feature takes into account the size limits of each data type to ensure accurate conversion, even for negative numbers using two's complement notation.
- **Binary to Decimal Conversion:** This utility can also convert binary strings back into their decimal form for specific types (char, int, long), correctly handling two's complement binary strings for negative values.
- **Binary Validation:** Before converting from binary to decimal, the tool validates the binary string to ensure it represents a valid binary number, increasing the reliability of conversions.
- **Negative Number Handling:** For signed data types, the converter supports negative numbers, automatically performing two's complement conversion to ensure the binary representation is correct.
- **Unit Testing Framework:** Includes a suite of unit tests to validate the functionality of each conversion method, ensuring the reliability and accuracy of the tool.

# Sketch Viewer (sketch.c)

The Sketch Viewer is a specialized software tool developed in C for rendering graphical sketches from binary-encoded files. It's designed to serve as a lightweight, cross-platform utility that interprets a compact, byte-oriented command language for drawing. This approach allows for the efficient storage and playback of drawing commands, making it an ideal tool for educational purposes, simple animations, and even rudimentary graphical design tasks. At its core, the Sketch Viewer operates by reading a binary file where each byte can represent either an instruction (opcode) or data (operand). These bytes are parsed sequentially to execute drawing commands such as drawing lines, setting the drawing color, moving to a new position, and other graphical operations. The Viewer utilizes a simple state machine to keep track of the current position, color, and other settings, enabling it to render complex sketches from minimal data.

## Key Features

- **Binary File Interpretation:** Reads and interprets binary files that contain drawing instructions. This feature allows for compact storage of drawings and easy sharing or embedding within other files.
- **Line Drawing:** Supports drawing straight lines from one point to another. Users can specify the start and end points, and the Sketch Viewer will render the line accordingly. This is the basic building block for more complex drawings.
- **Color Support:** Allows for the setting of the drawing color via encoded instructions in the binary file. This feature enables sketches to be more expressive and visually appealing by incorporating multiple colors.
- **Block Drawing:** Capable of drawing filled rectangles (blocks) by specifying corner points. This adds versatility to the types of graphics that can be created, from simple shapes to pixel-art-style images.
- **Dynamic Target Positioning:** Implements commands for dynamically changing the "target" position — where the next drawing operation will occur — without actually drawing. This allows for more complex and efficient drawing sequences.
- **Display Controls:** Includes instructions for manipulating the display directly from the binary file, such as showing the current state of the drawing, pausing for a specified duration, and signaling the end of a frame in animations.

# Circular Doubly Linked List (list.c)

This project implements a circular doubly linked list in C, providing a versatile and dynamic data structure for storing sequences of elements. Circular doubly linked lists are an advanced type of linked list where each node points to both the next and the previous nodes in the sequence, and the list is circular in nature, meaning the last node points back to the first node, creating a complete loop. This implementation includes a variety of functions for creating, navigating, modifying, and destroying the list, making it a powerful tool for handling ordered data efficiently.

## Key Features

### 1. Dynamic List Creation and Management

- _newList(item e):_ Initializes a new circular doubly linked list with a single node containing the value e. This function dynamically allocates memory for both the list and its sentinel node, setting up the structure for further use.
- _freeList(list *xs):_ Safely deallocates all nodes in the list, including the sentinel node, and frees the list structure itself. This function ensures that all memory allocated for the list is properly released, preventing memory leaks.

### 2. Navigation Functions

These functions allow traversal of the list in both forward and backward directions, enabling flexible data access patterns.

- _first(list *xs):_ Sets the current position to the first actual element of the list, skipping the sentinel node.
- _last(list *xs):_ Moves the current position to the last element, showcasing the circular nature of the list by navigating directly from the sentinel node to the last element.
- _none(list *xs):_ Checks if the current position is the sentinel node, indicating either an empty list or a full loop traversal.
- _after(list *xs)_ and _before(list *xs):_ These functions move the current position one node forward or backward, respectively, allowing step-wise navigation through the list.

### 3. Data Access and Modification

- _get(list *xs):_ Retrieves the value of the node at the current position. This function provides read access to the data within the list without modifying the list structure.
- _set(list *xs, item x):_ Replaces the value of the node at the current position with a new value x. This function allows for direct modification of the list's contents at any given point.

### 4. Insertion and Deletion Operations

These functions modify the list structure by adding or removing nodes, demonstrating the flexibility and dynamic nature of linked lists.

- _insertAfter(list *xs, item x)_ and _insertBefore(list *xs, item x):_ Insert a new node containing the value x immediately after or before the current position, respectively. These functions adjust the surrounding nodes' pointers to maintain the list's integrity.
- _deleteToAfter(list *xs)_ and _deleteToBefore(list *xs):_ Remove the node immediately after or before the current position. These operations ensure the list remains circular by properly re-linking the adjacent nodes.

### 5. Robust Testing Framework

The provided test suite covers various use cases and edge cases, validating the functionality of all operations. By defining _test_list_, users can run a comprehensive set of assertions that check the correctness of the list's behavior under different conditions, ensuring reliability and stability of the implementation.

# Sketch2PGM Converter (converter.c)

This project is a comprehensive C-based application designed to convert sketch instructions from a .sk file format into a .pgm (Portable GrayMap) image. It introduces an innovative way to interpret drawing commands encoded in binary within .sk files and render them as grayscale images. This conversion process not only showcases the versatility of binary file handling in C but also bridges the gap between simple encoded drawing instructions and visual representations.

## Description

At its core, the program operates by reading a series of encoded commands from a .sk file, which contain instructions for drawing lines, blocks (rectangles), and setting colors (grayscale intensity). These commands are decoded and executed to modify an in-memory representation of the image. Once all commands have been processed, the resultant image is saved as a .pgm file, a widely supported format for grayscale images that can be easily viewed or processed further with image editing tools. The encoding scheme for the drawing commands uses a combination of opcodes and operands, allowing for compact and efficient storage of drawing instructions. This approach demonstrates a practical application of binary file operations, bitwise manipulation, and the implementation of custom drawing algorithms.

## Key Features

- **Command Decoding:** Efficiently decodes drawing commands stored in binary format within .sk files.
- **Drawing Primitives:** Supports basic drawing operations, including lines and filled rectangles, with plans to extend functionality to more complex shapes.
- **Grayscale Support:** Implements grayscale coloring, allowing for varied intensity in the drawings, which can be utilized to add depth or shading to the images.
- **Dynamic Memory Management:** Utilizes dynamic memory allocation for image data storage, ensuring efficient use of resources for images of variable sizes.
- **Error Handling:** Incorporates basic error handling for file operations, ensuring robustness and reliability of the conversion process.
- **Portable GrayMap (PGM) Output:** Generates output in the .pgm format, facilitating easy viewing and further processing of the converted images.
- **Modular Design:** Structured in a way that separates the drawing logic from file handling and the main application flow, making the codebase easier to understand and extend.

## Setup and Initialization

The program begins by initializing a new state for the conversion process, including setting up an empty image buffer. This is accomplished through the newState function, which prepares the environment for processing drawing commands.

## Command Processing

Drawing commands are read from the .sk file in a binary format. Each command consists of an opcode and an operand, dictating the action to be taken (e.g., drawing a line, setting the color) and the parameters for the action, respectively. The readSketch function oversees reading these commands and delegating their execution to appropriate handlers.

## Drawing Operations

Based on the decoded commands, the program performs drawing operations on the in-memory image buffer. It supports drawing lines and blocks (rectangles) as specified by the sketch instructions, adjusting for color intensity as dictated by the grayscale color commands. The drawing logic, encapsulated in convertLine and convertBlock, demonstrates basic computer graphics algorithms for rasterizing shapes.

## Finalizing the Image

Once all commands have been processed, the resultant image is written to a .pgm file using the writeFile function. This function also handles formatting the output according to the .pgm specifications, ensuring compatibility with image viewers and editors.

## Memory Management and Cleanup

Dynamic memory allocated for the image buffer and the application state is properly freed at the end of the conversion process, preventing memory leaks and ensuring efficient resource use.

## Extension and Customization

The modular design of the program allows for easy extension and customization. New drawing commands can be added by introducing additional opcodes and implementing corresponding drawing functions. Similarly, the output format can be adapted to support other image types with minimal adjustments to the image writing logic.
