# Python Kernel crashes when running Matplotlib

Most likely from using an arm chip and Miniforge 



There are 3 fixes to this issue, one takes way less time to install



## Fix 1: Open in the right Context

The idea is to open vs code in the right context.



1. Open the `miniforge3 prompt` terminal
2. Activate your environment (recall `conda activate apml26-27`)
3. Navigate to the folder where your code is stored 
   `cd C:/path/to/folder`
4. Open vs-code from the terminal 
   `code .`



That worked so far.





## Fix 2: Adding conda to the PATH variables

With this fix, you *should* be able to just open vs code without additional hacks, and it _should_ just work.



1. Find out what conda version you are using 
   - Anaconda
   - Miniconda
   - Miniforge
2. Find out where the program is saved
   - Search on google for keywords like "Miniconda bin path" or "add Miniconda to PATH"
   - You should find a path like `C:/Users/user/anaconda3/condabin` 
     - The important part is to have a folder with `bin` in the name
3. Add that path to the PATH environment variables
   - Assuming that you are on windows
   - You can follow this tutorial:
     https://helpdeskgeek.com/add-windows-path-environment-variable/
4. **Restart** vs code after you have added (and saved) the PATH variable



After this, vs code _should_ work and you then only need to open vs code. There _should_ not be any crashes after that.



## Fix 3: Using Anaconda



If you have an arm chip (you can google the name of the chip of your laptop), you should not use prompt forge but Anaconda, as Anaconda has proper arm chip support.



1. **Uninstall** your current conda version
   - if you do not do that, there may be issues arrising where the proper conda version is not selected when you run commands and co.
2. Install Anaconda (https://www.anaconda.com/download)
3. Restart your laptop. 
4. Make all of the same installations as in the first tutorial slides. You should be good to go then.



