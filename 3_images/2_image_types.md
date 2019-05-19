# Image Types
- Three main types: jpg, png, gif

## JPG
- Jay-peg most common image format for images used in web docs
- Suitable for photos, drawings, diagrams, etc.
- Good balance of image quality and compression
- Compression encodes the file in a way that reduces its size
- JPGs use a **lossy** form of compression: they lose information in exchange for a file size reduction
  - In some cases, you compress an image down to 10% of its original size or less
  - Sacrifices quality in return for compression
- If you edit a jpg, resulting file has less detail than the original 
- If you update the file again, the result loses more detail.  If you repeat process enough, you end up with an image you no longer recognize
- You can set the amount of compression and associated lossiness when you save a jpg file

## PNG
- In general, JPGs don't work well as CSS backgrounds
- Photos are too intricate visually for use as a background
- Most non-photographic graphics show visible results of compression even at the highest quality
- Thus, PNG format is the choice for backgrounds and non-photographic images
- PNG uses compression to reduce size of file, but PNG compression is non-lossy.  
  - Leads to higher quality and larger file sizes
- PNGs also provide both single-color and alpha-transparency: allows you to see the background behind an image while still viewing the image's main subject
  - This feature is useful with logos, icons, and line drawings
  - Single color transparency allows part of an image to be entirely clear by reserving a single color - any pixel that matches that color in the png reveals the content (typically a background color) behind the image
  - Alpha transparency adds an alpha channel to images which allows up to 65k different levels of transparency tinted by color
- PNGs ideal for images that need all their detail, transparency, or that must support more than 16.7 million colors

## GIF
- GIFS are suitable for small images used as user interface icons in an app
- Limits color range (256 colros) but allows for miniscule files, making them perfect for images where size, detail, and broad color palette arent significant