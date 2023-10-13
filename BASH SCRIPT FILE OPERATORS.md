# BASH SCRIPT FILE OPERATORS

-e  Check whether the file exists at a given path.
        { if [ -e /myfile ]; then
            echo "File exists"
          fi
        }

-f  Check whether the given file path points to a regular file or not.
        { if [ -f /myfile ]; then
            echo "File is aregular file."
          fi
        }

-d  Check whether the given path refers to an existing directory or not.
        { if [ -d /myfolder ]; then
            echo "Directory exists."
          fi
        }

-h  Finds whether the given path is a symbolic link.
        { if [ -h /myfile ]; then
            echo "File is a symbolic link"
          fi
        }

-L  It checks for the symbolic link as the -h does, but it will also check whether it resolves to an actual file or directory.
        { if [ -L /myfile ]; then
            echo "File exists and is a symbolic link"
          fi
        }

-N  Checks if file has been modified since the last read.
        { if [ -N /myfile ]; then
            echo "File has been modified"
          fi
        }

-nt  Checks if one file is newer than the other.
        { if [ file1 -nt file2 ]; then
            echo "File1 is newer than file2"
          fi
        }

-p  Checks for a named pipe (FIFO).
        {fifo_path=/path/to/your/named_pipe

         if [ -p $fifo_path ]; then
            echo "The file at $fifo_path is a named pipe."
        else
            echo "The file at $fifo_path is not a named pipe or doesn't exist."
        fi }

-s  Used to find whether the file size is greater than zero or not.
        { if [ -s /myfile ]; then
            echo "File1 is not empty."
          fi
        }

-t  Check whether the file descriptor(typically representng a terminal or keyboard input) is associated with the terminal or not.
        { if [ -t 0 ]; then
            echo "This script is running interactively."
          fi
        }

-r  Used to find whether the file is readable or not.
        { if [ -r /myfile ]; then
            echo "File is readable."
          fi
        }

-w  Checks for whether the file is write permissions or not.
        { if [ -w /myfile ]; then
            echo "File is writeable."
          fi
        }

-x  It checks for the executable permissions for a specified file.
        { if [ -x /myfile ]; then
            echo "File is executable"
          fi
        }

-g  Checks for "set-group-ID" (SGID) permission set on a specific file.
       { file_path="/path/to/your/file.txt"

        if [ -g "$file_path" ]; then
            echo "The file at $file_path has the SGID permission set."
        fi
       }

-ot Checks if one file is older thsn the other.
        { if [ file1 -ot file2 ]; then
            echo "File1 is older than file2"
          fi
        }