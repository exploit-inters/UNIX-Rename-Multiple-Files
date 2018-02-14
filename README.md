# UNIX Rename Multiple Files
Small shell script to rename mass/bulk/multiple filenames and its extensions

## Step 1 : Navigate to the folder where the files are present
    
    cd my-folder
    
## Step 2 : Prepare the script
   
    touch rename.sh
    chmod +x rename.sh
    nano rename.sh

## Step 3 : The Script

The script below renames all files to .xml

    for file in *; do
        if [ -f ${file} ]; then
            mv ${file} ${file}.xml
        fi
    done

To do this recursively on all subdirectories, you should use find:

    for file in $(find -type f); do
        mv ${file} ${file}.xml
    done


