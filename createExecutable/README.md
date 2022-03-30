# defines how to create a py executable package

derived from https://gist.github.com/asimjalis/4237534

- Create a file `__main__.py` containing:`print ("Hello world from Python")`
- Zip up the Python files (in this case just this one file) into app.zip by typing: `zip app.zip *`
- The next step adds a shebang to the zip file and saves it as `app` — at this point the file `app` is a zip file containing all your Python sources.
    
    `echo '#!/usr/bin/env python3' | cat - app.zip > app`
    
    `chmod 755 app`

- That’s it. The file `app` is now have a zipped Python application that is ready to deploy as a single file.
- You can run `app` either using a Python interpreter as: `python3 app`
- Or you can run it directly from the command line: `./app`