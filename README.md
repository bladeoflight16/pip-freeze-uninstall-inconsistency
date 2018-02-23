For reproducing an issue with pip


Make sure `python.exe` and `pip.exe` are on `PATH`, checkout the repository to C:\temp, and run the following commands:

```
C:\temp>pip freeze

C:\temp>python .\setup.py bdist_wheel

C:\temp>SET PYTHONPATH=%CD%

C:\temp>pip freeze
mypack==1.0

C:\temp>pip uninstall
Can't uninstall 'mypack'. No files were found to uninstall.
```

This assumes a clean install of Python. If you have packages installed globally, you will see them in both `freeze` commands.
