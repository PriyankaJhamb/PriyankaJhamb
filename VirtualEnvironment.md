- pip install virtualenv 
- virtualenv environmentName
- source env/bin/activate
- deactivate
- pip freeze > requirements.txt
- pip install -r ./requirements.txt 
- virtualenv --system-site-packages env2  (if you want same packages in your new virtual environment 2)
- pip install packageName==version

### install all libraries in virtual environment using requirements.txt file
- cd to the directory where requirements.txt is located.
- activate your virtualenv.
- run: pip install -r requirements.txt in your shell.

#### ERROR Solution : https://linuxhint.com/error-command-gcc-failed-exit-status-1/#:~:text=Cause%20of%20%E2%80%9CError%20Command%20%E2%80%9Cgcc,with%20exit%20status%201%E2%80%9D%20error.
