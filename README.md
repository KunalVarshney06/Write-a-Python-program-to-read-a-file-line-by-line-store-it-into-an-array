# Write-a-Python-program-to-read-a-file-line-by-line-store-it-into-an-array
def read_file_into_array(file_path):
    lines_array = []
    try:
        with open(file_path, 'r') as file:
            for line in file:
                lines_array.append(line.strip())
    except FileNotFoundError:
        print("File not found.")
    except IOError:
        print("An error occurred while reading the file.")
    return lines_array

# Example usage
file_path = 'path/to/your/text/file.txt'  # Replace with the actual file path
lines_array = read_file_into_array(file_path)
print("Lines in the file:")
for line in lines_array:
    print(line)
