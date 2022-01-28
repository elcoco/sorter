# sorter

A python3 script to auto sort a directory of files, like a download folder.
Sorting can be done based on creation time and or file type.

You can run the script everytime the kernel detects a create/move event in you download directory

    # watch and auto cleanup download dir
    while inotifywait -e create -e move ~/tmp/browser; do sorter --yes --sort-method 'type' --overwrite ~/tmp/browser; done &
