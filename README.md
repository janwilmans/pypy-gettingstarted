# pypy-gettingstarted
Getting started with pypy (Python 3.6)  and matplotlib in Windows 10

- create a directory `c:\pypy` and 
- download [wget](https://eternallybored.org/misc/wget/) from https://eternallybored.org/misc/wget/1.20.3/64/wget.exe and save it as `c:\pypy\wget.exe`
- open a command line, using Win-R, cmd.exe <enter>, and type `pushd c:\pypy` <enter>
- then `wget http://bootstrap.pypa.io/get-pip.py` as per instructions at https://pip.pypa.io/en/stable/installing/
- also `wget https://bitbucket.org/pypy/pypy/downloads/pypy3.6-v7.1.1-win32.zip` 
- put the content of pypy3.6-v7.1.1-win32.zip directly into `c:\pypy` so you have `c:\pypy\pypy3.exe`
- then execute `pypy3.exe get-pip.py`
- test if pip is working correctly by using `pypy3 -m pip install -U pip`
  (you should see something like `Requirement already up-to-date: pip in .\site-packages (19.2.3)`
  
