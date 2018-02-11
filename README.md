# About
This repo has one-off programs I developed for different projects. Refer to the README in each folder for details.

# PyCharm Setup

I use this repo to demonstrate how I setup PyCharm for different projects with different Python versions and packages using virtual environments. I use Atom to write this README and work on simple programs and only use PyCharm for projects that may need more debugging features.

1. Create a repo on Github (make sure to add Python .gitigore file so that the virtual environment folder won't be committed and uploaded, I have also added `.idea` to that file to ignore PyCharm setting folders) and clone that to the local computer, such as `$ git clone https://github.com/harrywang/one-off.git`
2. Create a new folder in `one-off`, such as `inside-airbnb` and switch to that folder.
3. Create a README.md to describe the project and a requirements.txt file for the required packages (for example, we have `pandas==0.21.0` for the movie-genre project)
4. Create the python virtual environment (https://virtualenv.pypa.io/en/stable/installation/) and install required packages (Use Homebrew to install Python 2 and 3 if needed):

  Python 2
  - create virtual environment: `$virtualenv venv`
  - activate virtual env: `$source venv/bin/activate`
  - install required packages (this needs to be repeated every time you have added new packages): `pip install -r requirements.txt`

  Python 3
  - create virtual environment: `$virtualenv -p python3 venv`
  - activate virtual env: `$source venv/bin/activate`
  - install required packages (this needs to be repeated every time you have added new packages): `pip3 install -r requirements.txt`

  For example, for the new inside-airbnb project, I have the following after this step:
  ```
  dami:inside-airbnb harrywang$ ls
  README.md		requirements.txt	venv
  ```
5. Open PyCharm, create a new project:

  ![screen shot 2018-02-11 at 12 10 21 pm](https://user-images.githubusercontent.com/595772/36076363-2c6e1f24-0f29-11e8-9c15-7e9afc10b593.png)

  Add a new local interpreter, e.g., for `inside-airbnb`, we point this to `venv/bin/python3.6`:
  ![screen shot 2018-02-11 at 12 16 36 pm](https://user-images.githubusercontent.com/595772/36076372-4cd0008e-0f29-11e8-84be-67202505d5cd.png)

  confirm Yes in the next screen because this folder is not empty:
  ![screen shot 2018-02-11 at 12 49 27 pm](https://user-images.githubusercontent.com/595772/36076437-09ab16b2-0f2a-11e8-9736-1a867e00ce05.png)

  Now, you can create new files in the IDE and run the programs:
  ![screen shot 2018-02-11 at 12 50 42 pm](https://user-images.githubusercontent.com/595772/36076457-51ac9b52-0f2a-11e8-920b-bb23019f4ae7.png)

6. Configure PyCharm to show iPython console: (see original post for this at https://stackoverflow.com/questions/42562734/how-to-run-a-file-in-ipython-console-as-default-instead-of-terminal)

  a. Go to File -> Default Settings and make sure to select Use IPython if available.
  ![gi77e](https://user-images.githubusercontent.com/595772/36077020-28080f94-0f33-11e8-8717-0f5eaf259342.png)

  b. Go to Run -> Edit Configurations and select Show command line afterwards:
  ![eim3r](https://user-images.githubusercontent.com/595772/36077025-46c516e8-0f33-11e8-916a-79c573df0cae.png)

  Now you can run selected parts of your code in PyCharm with ALT+SHIFT+E more or less exactly like in Spyder.
