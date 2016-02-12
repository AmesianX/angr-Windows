# angr-Windows

WARNING! THIS ISN'T FULLY WORKING YET! While the wheel files appear to install correctly, pyvex is misbehaving and causing angr in general to not be terribly helpful. Basically all the modules EXCEPT for pyvex should be working as expected and certainly installable. However, since PyVEX itself isn't working right, you won't be able to use angr just yet on Windows.

Windows builds for use with angr framework

## Installing Angr

Make sure you have Visual C++ Redistributable for Visual Studio 2012 installed
  http://www.microsoft.com/en-us/download/details.aspx?id=30679#

```bash
git clone https://github.com/Owlz/angr-Windows.git
cd angr-Windows
pip install virtualenv
virtualenv --python=C:\Python2.7-64bit\python.exe angr
angr\Scripts\activate
pip install <capstone>
pip install <z3>
pip install <pyvex>
pip install angr
```

Then move the "c++filt" executable into your angr/Scripts directory. And yes, the order matters somewhat. Primarily I think capstone needs to be installed first, then the other wheel files in any order. Make sure you install the wheel files prior to attempting to install angr proper.
