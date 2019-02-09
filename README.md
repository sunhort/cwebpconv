# cwebpconv
Batch cwebp converter

Converts files in its folder and subfolders using cwebp and parallel for better speed. 

If you uncomment strings with rm command it will remove source files after conversion

Please note, that script converts all files into webp format first and only after will delete source jpegs or whatever you decided to convert, so keep in mind that you need space on the hard drive to perform full conversion or convert small portions.

I noticed that using this settings and cwebp I can get better results without heavy degradation in quality than if using other software, so decided someone might like it. "cwebp -q 90 -m 6 -segments 4 -sharp_yuv -v -metadata all"

Before running install software with command sudo apt install webp parallel -y (for ubuntu and such), other linux you know your package manager.
