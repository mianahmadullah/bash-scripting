Mastering the cat Command in Linux

The cat command, short for concatenate, is a versatile utility in Unix-like operating systems that is primarily used to display the content of files, concatenate multiple files, or create new files. Understanding the various use cases of cat is essential for efficient command-line navigation and file manipulation. In this guide, we'll explore the different ways to harness the power of the cat command.
Displaying File Contents

The most common use of cat is to display the content of a file on the terminal. To achieve this, simply provide the filename as an argument:

bash

cat filename.txt

This command will output the entire content of filename.txt to the terminal.
Concatenating Multiple Files

cat excels at concatenating multiple files into a single file. To concatenate two or more files, list them as arguments:

bash

cat file1.txt file2.txt > combined_file.txt

This command combines the content of file1.txt and file2.txt into a new file named combined_file.txt. The > symbol is used for redirection, which creates or overwrites the destination file.
Appending to a File

Appending the content of one file to another is another useful application of cat. To append the content of file2.txt to file1.txt, use the >> symbol:

bash

cat file2.txt >> file1.txt

This command adds the content of file2.txt to the end of file1.txt without overwriting the original file.
Displaying Line Numbers

To display the content of a file with line numbers, use the -n option:

bash

cat -n filename.txt

This command numbers each line in the output, providing a quick reference for locating specific lines within the file.
Creating a New File

In addition to working with existing files, cat can be used to create a new file by combining standard input with the output redirection. For example:

bash

cat > new_file.txt

This command allows you to input text directly into the terminal. Press Ctrl + D to signify the end of input, and the content will be saved to new_file.txt.
Displaying Non-Printable Characters

To reveal non-printable characters, such as tabs and end-of-line characters, use the -v option:

bash

cat -v filename.txt

This command displays the content of filename.txt with special characters represented visibly.
Conclusion

The cat command is a powerful and versatile tool for handling files in a Unix-like environment. By mastering its various applications, you can efficiently display, concatenate, and manipulate file content, making it an invaluable asset in your command-line toolkit. Explore these cat command usages to enhance your file manipulation skills and streamline your workflow on the command line.
You can use the cat command with xargs to concatenate the contents of these files:

bash

cat file_list.txt | xargs cat > combined_files.txt

In this example:

    cat file_list.txt outputs the content of file_list.txt.
    xargs cat takes each line (filename) from the input and passes it as an argument to the cat command.
    > combined_files.txt redirects the concatenated output to a new file named combined_files.txt.

Using cat with tr:
Scenario:

Suppose you have a file with unwanted characters, and you want to remove or replace those characters using tr.
Example:

Assuming you have a file named unwanted_chars.txt with some unwanted characters, and you want to remove all occurrences of the character 'a':

bash

cat unwanted_chars.txt | tr -d 'a' > cleaned_text.txt

In this example:

    cat unwanted_chars.txt outputs the content of unwanted_chars.txt.
    tr -d 'a' removes all occurrences of the character 'a' from the input.
    > cleaned_text.txt redirects the cleaned output to a new file named cleaned_text.txt.
