# BitcoinOnPython



### Mac Setup:

- Set Python to specific version

  https://stackoverflow.com/questions/18425379/how-to-set-pythons-default-version-to-3-x-on-os-x
  
  - Changing the default python version system wide would break some applications that depend on python2.
  - You can alias the commands in most shells, Mac OS X uses bash by default, if you also do put this into your ~/.bash_profile:

  ```sh
  alias python='python3'
  ```
  
  - python command now refers to python3. 
  - If you want the original python (that refers to python2), you can escape the alias i.e. doing \python will launch python2 leaving the alias untouched)

  - If you launch interpreters more often (I do), better is to:

```sh
alias 2='python2'
alias 3='python3'
```

 - Tip: Instead of doing:
  ```sh
   #!/usr/bin/env python
   ```
   
 - use:

```sh
#!/usr/bin/env python3
```
   - system will use python3 for running python executables.

   - Verify Python version(s) and running version on MAC

- https://stackoverflow.com/questions/33175827/what-version-of-python-is-on-my-mac

  ```
  You could have multiple Python versions on your macOS.

  You may check that by type or which command, like:

  which -a python python2 python2.7 python3 python3.6
  Or by typing python in Terminal and hitting Tab few times for auto completion.

  By default python/pip commands points to the first binary found in PATH environment variable depending what's actually installed. So   before installing Python packages with Homebrew, the default Python is installed in /usr/bin which is shipped with your macOS (e.g. Python 2.7.10 on High Sierra). Any versions found in /usr/local (such as /usr/local/bin) are provided by external packages.

  It is generally advised, that when working with multiple versions, for Python 2 you may use python2/pip2 command, respectively for Python 3 you can use python3/pip3, but it depends on your configuration which commands are available.

  It is also worth to mention, that since release of Homebrew 1.5.0+ (on 19 January 2018), the python formula has been upgraded to Python 3.x and a python@2 formula will be added for installing Python 2.7. Before, python formula was pointing to Python 2.

  For instance, if you've installed different version via Homebrew, try the following command:

  brew list python python3
  or:

  brew list | grep ^python
  it'll show you all Python files installed with the package.

  Alternatively you may use apropos or locate python command to locate more Python related files.

  To check any environment variables related to Python, run:

  env | grep ^PYTHON
```
