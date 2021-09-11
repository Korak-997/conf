Download the db file

```
  sudo dpkg -i DEB_FILE*
```
and press ENTER. Let it run through the process. Once it's finished, pass or fail, type the following into terminal:

```
  sudo apt-get install -f
```

This will install all of the dependencies of the .deb file that dpkg doesn't do. Any time you install a .deb file, always use
```
  sudo dpkg -i *file_name*
```
What this does is it adds the program to the apt archives, and lists it as a failed install. It shows that it has unmet dependencies, and to install the dependencies and finish installing the program, you need to run
```
  sudo apt-get install -f
```
Boom, you have what ever .deb file you downloaded successfully :)
