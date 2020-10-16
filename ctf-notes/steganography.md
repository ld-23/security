# Steganography



### Digital Invisible Ink Toolkit

### Stegoveritas

`stegoveritas stego2.jpg`

### **binwalk**  

* binwalk file : Displays the embedded data in the given file
* binwalk -e file : Displays and extracts the data from the given file
* binwalk --dd='jpeg:jpg' file.jpg  \(Actually extracts data. Set output folder with -C\)
* binwalk --dd='.\*' file \( force extract specific file type\)
* binwalk -B ==&gt; look into specifying png specifically

### exiftool

### exiv2

### file

### steghide

### stegosuite

### stegsolve 

* stegsolve.jar &gt;run with&gt; java -jar stegsolve.jar

### strings

* strings -a \[FILE\] \| grep SEARCH\_TERM • 
* strings stego2.jpg \| awk 'length\($0\)&gt;8' \| sort -u

### xxd

xxd \[FILE\] &gt; output\_file

### zsteg 

* Gem install zsteg  
* Usage: zsteg \[options\] filename.png \[param\_string\] 
* Useful commands: zsteg -a file : Runs all the methods on the given file  
* zsteg -E file : Extracts data from the given payload \(example : zsteg -E b4,bgr,msb,xy name.png\)

