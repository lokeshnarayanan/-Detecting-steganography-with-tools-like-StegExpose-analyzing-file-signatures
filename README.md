# Detecting-steganography-with-tools-like-StegExpose-analyzing-file-signatures
## AIM:
To detect hidden data using steganography detection tools like StegExpose and analyze file signatures for authenticity and manipulation.

## DESIGN STEPS:
### Step 1:
Install StegExpose or use the JAR version to detect steganography in image files.

### Step 2:
Run StegExpose on a directory of suspected image files using the command:

### Step 3:
Analyze file signatures using tools like file, binwalk, or xxd to check for inconsistencies or embedded content.

## PROGRAM:
- **Install and Verify Steghide Tool**
  ```bash
  sudo apt update
  sudo apt install steghide
  steghide --version 
  ```
- **Embed the Secret Message into the Image** 
  ```bash
  steghide embed -cf image.jpg -ef hidden.txt
  ```

- **Extract the Hidden Secret from Image and Verify the Extracted Message**
  ```bash
  steghide extract -sf image.jpg
   cat hidden.txt
  ```

- **Retrieve Information About the Embedded Data**
  ```bash
   steghide info image.jpg
  ```

- **Analyze File Signature**
  ```bash
    file image.jpg
    binwalk image.jpg
  ```
 
## OUTPUT:
### Install and Verify Steghide Tool
![8-1](https://github.com/user-attachments/assets/9e5f495e-1898-4ed1-b030-62736f361243)

### Embed the Secret Message into the Image
![464+1](https://github.com/user-attachments/assets/02abc0dd-4983-47ed-9b3c-99ebe8aa5483)

### Delete Original Secret File
![8-3](https://github.com/user-attachments/assets/8d95f990-3b3c-4b79-a821-63228c448006)

###  Extract the Hidden Secret from Image
![8-4](https://github.com/user-attachments/assets/8d871fa9-60a6-410b-aa17-241600c49d3e)



### Retrieve Information About the Embedded Data
![8-6](https://github.com/user-attachments/assets/45225e67-d6db-4fae-897e-ce26187d3609)

### Analyze File Signature
![8-7](https://github.com/user-attachments/assets/85236ce3-9a25-4d94-aba7-0366285ce2e1)

## RESULT:
Hidden data was successfully detected and file signatures were analyzed for irregularities.
