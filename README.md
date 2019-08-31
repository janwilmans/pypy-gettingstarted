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
  

Now to install `matplotlib` you need a couple of prerequisites:

- Install Visual Studio 2019 with the `Desktop development with C++` workload
- `wget https://github.com/ubawurinna/freetype-windows-binaries/releases/download/v2.10.1/freetype.zip`

If Visual studio is not installed or you are not running from a x86 (32-bit) command line, you will see:
`RuntimeError: Broken toolchain: cannot link a simple C program`

- Put the content of `freetype.zip` in c:\pypy\include, so you have `C:\pypy\include\ft2build.h` and a directory `C:\pypy\include\freetype`.
- copy win32\freetype.lib from `freetype.zip` into C:\pypy\libs\freetype.lib

Start the correct developer command prompt by looking for `x86 Native Tools Command Prompt for VS 2019` in the start menu.

- setup the environment using `"%VS140COMNTOOLS%\vsvars32.bat"`
- then enter `pypy3 -m pip install matplotlib`

result:

```
 LINK : fatal error LNK1181: cannot open input file 'z.lib'
```

* TODO * find out how to continue.
see https://github.com/matplotlib/matplotlib/issues/15160

