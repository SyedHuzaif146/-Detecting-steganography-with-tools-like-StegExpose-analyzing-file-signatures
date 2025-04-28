# NAME=SYED HUZAIF
# REG NO=212224240166
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
![image](https://github.com/user-attachments/assets/a129d16e-b2c2-4eb7-a670-2d3a9e9adfb7)

### Embed the Secret Message into the Image
![image](https://github.com/user-attachments/assets/00ebfedf-774a-4413-ab1a-1995387b1837)


### Delete Original Secret File
![image](https://github.com/user-attachments/assets/d67c04a7-38f0-462f-8f85-f47699abc07e)


###  Extract the Hidden Secret from Image
![image](https://github.com/user-attachments/assets/d6e66929-7023-46a3-bb02-c9722e37541b)

### Verify the Extracted Message
![image](https://github.com/user-attachments/assets/907b0a76-6bc5-4571-8891-f00600be7117)


### Retrieve Information About the Embedded Data
![image](https://github.com/user-attachments/assets/68d5b376-f0a8-4467-9841-1790a283b0ba)


### Analyze File Signature
![image](https://github.com/user-attachments/assets/00834b59-fc40-4bff-ad46-dd3fdee2a993)

![image](https://github.com/user-attachments/assets/60d009ee-8a50-4763-b7c7-39361a01b858)

## RESULT:
Hidden data was successfully detected and file signatures were analyzed for irregularities.
