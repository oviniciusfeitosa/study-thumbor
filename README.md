# study-thumbor

### Steps
```
  $ sudo apt-get install libcurl4-openssl-dev
  $ sudo apt-get install build-essential autoconf libtool pkg-config python-opengl python-imaging python-pyrex python-pyside.qtopengl idle-python2.7 qt4-dev-tools qt4-designer libqtgui4 libqtcore4 libqt4-xml libqt4-test libqt4-script libqt4-network libqt4-dbus python-qt4 python-qt4-gl libgle3 python-dev libssl-dev
  $ pip install thumbor
  $ thumbor 
```

### How it works?

When you start Thumbor it will start on default port ```8888```.

* In your browser let's play changing sizes:
```
  http://localhost:8888/unsafe/1000x1000/http://4.bp.blogspot.com/-6fBAtJqHt60/VVuyzppfiII/AAAAAAAABA4/lkFYjLUvjjw/s1600/o_que_e_xpto.png
```

* Flipping the image
```
  http://localhost:8888/unsafe/-0x-0/http://4.bp.blogspot.com/-6fBAtJqHt60/VVuyzppfiII/AAAAAAAABA4/lkFYjLUvjjw/s1600/o_que_e_xpto.png
```

* Applying Filters ( more [here](http://thumbor.readthedocs.io/en/latest/filters.html))
```
  http://localhost:8888/unsafe/filters:brightness(10):contrast(30)/http://4.bp.blogspot.com/-6fBAtJqHt60/VVuyzppfiII/AAAAAAAABA4/lkFYjLUvjjw/s1600/o_que_e_xpto.png
```

* Image Endpoint Example:
```
  http://*thumbor-server*/hmac/trim/AxB:CxD/fit-in/-Ex-F/HALIGN/VALIGN/smart/filters:FILTERNAME(ARGUMENT):FILTERNAME(ARGUMENT)/*image-uri*
```
