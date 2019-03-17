* Make the project folder
````
$ mkdir book-catalog
$ cd book-catalog
````
* Create virtual environment
````
$ python -m venv env
````
* Put the 'env' folder in .gitignore
````
$ echo 'env' > .gitignore
````
* If you use VS Code as IDE for Python, you can put .vscode in .gitignore also
````
$ echo '.vscode' >> .gitignore
````
* Activate the environment
````
$ source ./env/bin/activate
````
* Install flask
````
(env)$ pip install flask
````
* Freeze the requirements
````
(env)$ pip freeze > requirements.txt
(env)$ git add requirements.txt
````
* Using VS Code as IDE
    * [VS Code Python Flask Tutorial](https://code.visualstudio.com/docs/python/tutorial-flask)
    * Open the project folder in VS Code
    * In VS Code, open the Command Palette (View > Command Palette). Then select the Python: Select Interpreter command:
    *  From the list, select the virtual environment in your project folder that starts with ./env
    * Run Terminal: Create New Integrated Terminal from the Command Palette, which creates a terminal and automatically activates the virtual environment by running its activation script.
    * The selected environment appears on the left side of the VS Code status bar, and notice the "(venv)" indicator that tells you that you're using a virtual environment:
    * Install Flask in the virtual environment by running one of the following commands in the VS Code Terminal:
    ````
    (env)$ pip install flask
    ````
    * In the terminal, run an app by entering 
    ````
    (env)$ python -m flask run
    ````
    * Anyone (or any build server) that receives a copy of the project needs only to run the pip install -r requirements.txt command to reinstall the packages in the original the environment. (The recipient still needs to create their own virtual environment, however.)
    