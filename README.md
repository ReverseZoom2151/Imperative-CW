# Binary Converter (visualise.c)

The Binary Converter is a versatile command-line tool designed for a wide audience including developers, students, and enthusiasts who need a fast and reliable method for converting decimal numbers to their binary representations and vice versa. This tool is invaluable for those looking to deepen their understanding of low-level computing operations, binary arithmetic, and how data is represented digitally. It supports a comprehensive range of data types—both signed and unsigned integers, characters, and long integers. Beyond mere conversion, it verifies the accuracy of binary strings and adeptly handles conversions for both positive and negative numbers, making it an essential utility for various computational applications.

## Key Features

- **Decimal to Binary Conversion:** Convert decimal numbers of different data types (int, unsigned int, char, unsigned char, long) to their binary string representation. This feature takes into account the size limits of each data type to ensure accurate conversion, even for negative numbers using two's complement notation.
- **Binary to Decimal Conversion:** This utility can also convert binary strings back into their decimal form for specific types (char, int, long), correctly handling two's complement binary strings for negative values.
- **Binary Validation:** Before converting from binary to decimal, the tool validates the binary string to ensure it represents a valid binary number, increasing the reliability of conversions.
- **Negative Number Handling:** For signed data types, the converter supports negative numbers, automatically performing two's complement conversion to ensure the binary representation is correct.
- **Unit Testing Framework:** Includes a suite of unit tests to validate the functionality of each conversion method, ensuring the reliability and accuracy of the tool.
