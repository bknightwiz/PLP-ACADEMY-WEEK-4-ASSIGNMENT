# PLP-ACADEMY-WEEK-4-ASSIGNMENT
WEEK 4 ASSIGNMENT
def modify_file_content(filename):
    try:
        # Try to open and read the file
        with open(filename, 'r') as file:
            content = file.read()
        
        # Modify the content (example: convert to lowercase)
        modified_content = content.lower()

        # Define new output filename
        output_filename = f"modified_{filename}"

        # Write the modified content to a new file
        with open(output_filename, 'w') as file:
            file.write(modified_content)

        print(f"✅ Successfully created '{output_filename}' with modified content.")

    except FileNotFoundError:
        print(f"❌ Error: The file '{filename}' does not exist.")
    except IOError:
        print(f"❌ Error: The file '{filename}' could not be read.")
    except Exception as e:
        print(f"❌ An unexpected error occurred: {e}")

# Ask the user for the filename
user_filename = input("Enter the name of the file to read and modify: ")

# Call the function
modify_file_content(user_filename)

If the file exists:
Enter the name of the file to read and modify: input.txt
✅ Successfully created 'modified_input.txt' with modified content.

If the file doesn't exist:
Enter the name of the file to read and modify: missing.txt
❌ Error: The file 'missing.txt' does not exist.
