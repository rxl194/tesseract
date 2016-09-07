
Fedora:
	./autogen.sh
  bash
	LIBLEPT_HEADERSDIR=$HOME/local/leptonica/include  ./configure 
    --enable-debug \
    --prefix=$HOME/local/tesseract \
    --with-extra-libraries=$HOME/local/leptonica/lib 
  make; sudo make install; sudo ldconfig;

  make training; sudo make training-install
  :) If failed: vi training/Makefile
                    CPPFLAGS =  -I/opt/cv/include/leptonica   \
                                -I/usr/include/pango-1.0 \
                                -I/usr/include/glib-2.0 \
                                -I/usr/lib/x86_64-linux-gnu/glib-2.0/include \
                                -I/usr/include/cairo \
                                -I/usr/include/freetype2


  
  Language Data

    1.Download langugage data file (e.g. 'wget http://tesseract-ocr.googlecode.com/files/tesseract-ocr-3.01.eng.tar.gz' for 3.01 version)
    2. Decompress it ('tar xf tesseract-ocr-3.01.eng.tar.gz')
    3. Move it to installation of tessdata (e.g. 'mv tesseract-ocr/tessdata $TESSDATA_PREFIX' if defined TESSDATA_PREFIX) 

Windows: CMake+MingW:
  git\tesseract\tesseract_output is the output path
  cp dlDVD_36_NEW\tesseract-ocr-3.01\tessdata-master.zip chi_tra.* chi_sim.* eng.* /opt/ocv3/share/tessdata
  set ENV: TESSDATA_PREFIX C:/opt/ocv3/share
