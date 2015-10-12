# JavaScript JPEG Parser

This is a port of Martin Fiedler's [NanoJPEG library](http://keyj.emphy.de/nanojpeg/) from C to [Skew](http://skew-lang.org). It supports both grayscale and RGB JPEGs but doesn't support progressive or CMYK JPEGs. I've also added automatic EXIF orientation correction. For development, first install the compiler using `npm install`, then invoke the compiler using `npm run build`.

Usage:

    var encoded; // Input: a JPEG file as a Uint8Array
    var decoded = decodeJPEG(encoded); // Or "require('nanojpeg').decodeJPEG(encoded);" for node
    if (decoded !== null) {
      console.log('width', decoded.width);
      console.log('height', decoded.height);
      console.log('rgb', decoded.rgb);
    }

* Install: `npm install nanojpeg`
* Download: [nanojpeg.js](http://evanw.github.io/skew-nanojpeg/nanojpeg.js) (less than 10kb)
* Live demo: [http://evanw.github.io/skew-nanojpeg/](http://evanw.github.io/skew-nanojpeg/)
