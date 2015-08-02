
Fedora:
	./autogen.sh
  bash
	LIBLEPT_HEADERSDIR=$HOME/local/leptonica/include  ./configure 
    --enable-debug \
    --prefix=$HOME/local/tesseract \
    --with-extra-libraries=$HOME/local/leptonica/lib 
  make; sudo make install
  make training; sudo make training-install
  
  Language Data

    1.Download langugage data file (e.g. 'wget http://tesseract-ocr.googlecode.com/files/tesseract-ocr-3.01.eng.tar.gz' for 3.01 version)
    2. Decompress it ('tar xf tesseract-ocr-3.01.eng.tar.gz')
    3. Move it to installation of tessdata (e.g. 'mv tesseract-ocr/tessdata $TESSDATA_PREFIX' if defined TESSDATA_PREFIX) 
