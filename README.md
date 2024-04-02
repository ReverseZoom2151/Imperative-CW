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
