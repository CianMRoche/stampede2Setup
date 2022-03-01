# After getting a python virtualenv working
(See https://packaging.python.org/en/latest/guides/installing-using-pip-and-virtual-environments/ for instructions. If link broken, google "python venv")

- Note: If expected behaviour isnt seen, always consider closing the vscode window and reopening *(and typing the login code, annoying yes)* to see if it fixes it. this sort of thing is only necessary during this setup phase, and not when actually working day-to-day

- In a remote window, go to the vscode extensions tab (on the left) and install the jupyter extension, aswell as the python extension

- Add the kernel (named "py3" in the below example) to jupyters list of kernels via

`python3 -m ipykernel install --user --name py3 --display-name "Python 3.7 (py3)"`

  where the last argument is the name of the new kernel as a string

- When using vscode, opena .ipynb file and select the kernel from the top-right. A python 3.7 environment should be available, and should load your custom path too. 