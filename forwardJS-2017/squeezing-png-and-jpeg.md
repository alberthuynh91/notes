# Squeezing PNG and JPEG

- Goal: Reduce the file size without any noticeable loss of visual quality
- Three steps: Identify trade-offs -> reduce details -> and encode exhaustively

## Squeezing PNG (Portable Network Graphics)
- Reducing color in PNGs allows us to save more space
- Lossless Encoding
- PNG works in the RGB color space
- Has good compression (use DEFLATE)
- Lempel-Ziv Algorithm (de-duplication)
- There is a tool called PNG Thermal (shows areas easy/difficult to compress in an image)
- Reducing the amount of unique colors used can drastically lower the size of a image without losing visual quality
- pngquant is a png compression tool

## Squeezing JPEG
- Blurring/Reducing details in JPEGs allows us to save more space
- JPEG works in the YCbCr colorspace vs RGB
- MozJPEG - A popular JPEG Encoder
- Alternative JPEG Encoder: Guetzli
- A down side to Guetzli is that it's extremely slow
- Blurring background of an image is an option to save on image size (similar to the bokeh effect)
