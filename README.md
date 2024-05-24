# DynamicStringDecrypterV2
This is a update version of DynamicStringDecrypter
ORIGINAL SOURCE: https://github.com/ribthegreat99OrN0P/DynamicStringDecrypter
## UPDATES:

### Changes and Improvements in the New Code

1. **Improved User Interface**:
   - **New Code**: Introduces an initial menu that allows the user to select the decryption method automatically or manually.
   - **Old Code**: Doesn't have an initial selection, only attempts to find the decryption method automatically and prompts for the method name if it fails.

2. **Manual Decryption Method**:
   - **New Code**: Introduces a `ManualDecryptionMethod()` method that allows the user to manually enter the decryption method name.
   - **Old Code**: Only allows searching for decryption methods automatically or by name after a failure.

3. **Enhanced Exception Handling**:
   - **New Code**: Adds more specific exception handling and informative error messages.
   - **Old Code**: More generic exception handling that may not provide clear messages in case of errors.

4. **Code Organization**:
   - **New Code**: Divides logic into smaller, specialized methods (`GetDecryptionMethod()`, `GetDecryptionMethodByName()`, `DecryptVariables()`, etc.).
   - **Old Code**: All code is inside the `Main` method, which could make it less readable and harder to maintain.

5. **Decryption and Assembly Modification Structure**:
   - **New Code**: Uses a structured approach to decrypt and modify assembly code.
     - Uses `CilMethodBody.Instructions` to iterate over instructions.
     - Uses methods like `Invoke` to execute the decryption method.
   - **Old Code**: While performing similar operations, the code is less structured and might be harder to understand and maintain.

6. **Writing Modified Assembly**:
   - **New Code**: Uses `ManagedPEImageBuilder` and `DotNetDirectoryFactory` to write the modified assembly.
   - **Old Code**: Does not use `ManagedPEImageBuilder`, only writes the modified assembly directly.

7. **Handling Output File Names**:
   - **New Code**: Detects if the original assembly is a `.dll` or `.exe` and generates the output file name accordingly.
   - **Old Code**: Does not detect or adjust the output file name based on the assembly type.

8. **Console Messages**:
   - **New Code**: Improves console messages to provide more information to the user about what is happening.
   - **Old Code**: Console messages are simpler and may not provide enough information in case of failures.

### Conclusion

The new code significantly improves the user experience by providing clear options for selecting decryption methods and detailed error messages. Additionally, it better organizes the program logic into specialized methods and handles exceptions more effectively. This makes the code more robust, readable, and maintainable compared to the old code.
