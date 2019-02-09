# cwebpconv
Batch c webp converter for linux uses cwebp tool from google

Converts files in its folder and subfolders using cwebp and parallel for better speed. 

Please note, that script converts all files into webp format first and only after will delete source jpegs or whatever you decided to convert (uncomment string with rm command to delete source files), so keep in mind that you need space on the hard drive to perform full conversion or convert with small portions.

I noticed that using this settings and cwebp I can get better results without heavy degradation in quality than if using other software, so decided someone might like it. "cwebp -q 90 -m 6 -segments 4 -sharp_yuv -v -metadata all"

Before running install software with command sudo apt install webp parallel -y (for ubuntu and such), other linux you know your package manager.

To run conversion just put script cwebpconv.sh to to folder with you pictures and run it in terminal with ./cwebpconv.sh command

Uncomment (remove #) in following strings to delete files after conversion:

#echo 'Removing source files in 30 seconds, be carefull..'

#sleep 30

#find . -name "*.jp*g" | parallel --bar --eta rm {} \;

In order to conver files like png or other formats just replace "jpg" with your extenstion in line 

find . -name "*.jpg" | parallel --bar --eta cwebp -q 90 -m 6 -segments 4 -sharp_yuv -v -metadata all {} -o {.}.webp
