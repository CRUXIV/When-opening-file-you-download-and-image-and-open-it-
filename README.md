# When-opening-file-you-download-and-image-and-open-it-
Open a Terminal.

Create a new script file. For example, name it download_and_open.sh:

touch download_and_open.sh

Edit the file using a text editor like nano:

nano download_and_open.sh

Add the following content to the file:
-----------------------------------
#!/bin/bash

IMAGE_URL="https://www.example.com/image.jpg"

DESTINATION="downloaded_image.jpg"

wget $IMAGE_URL -O $DESTINATION

if [ -f "$DESTINATION" ]; then
    # Open the image with the default image viewer
    xdg-open $DESTINATION
else
    echo "Failed to download the image."
fi

Replace https://www.example.com/image.jpg with the URL of the image you want to download.
---------------------------------------------------------------------------------------
Save and exit the editor. If you’re using nano, press CTRL + X, then Y, and Enter.

Make the script executable:

chmod +x download_and_open.sh

Run the script to test it:

./download_and_open.sh
