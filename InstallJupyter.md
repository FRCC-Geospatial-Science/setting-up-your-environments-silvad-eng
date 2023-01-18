# Installing Jupyter Notebooks via Anaconda
In this section, we will look at the necessary tasks for installing Jupyter Notebooks, the actual place we will be doing a fair amount of the work. Locally, you can access the ArcPy library, which - ironically - we won't be using. The ArcPy library assumes you have at least one Esri product installed on your machine. While one *could* download the ArcPy library, unless it is authorized with a current license file, one cannot actually call/utilize the library.

ArcGIS Pro does come with Jupyter notebooks installed, and most likely, you've used a Pro Notebook by this point in your education. However, this semester will focus solely on open source GIS softwares, meaning we can't just use the ArcGIS Pro notebooks (well, technically, you can pull any locally stored library into an ArcGIS Pro notebook, but you still need that whole authorization thing!).

Before we can use Jupyter Notebooks, we need to first install Anaconda as a path to using the notebooks.

## Contents
1. <a href="#anaconda-and-jupyter-notebooks">Install Anaconda and the Required Packages</a>
2. <a href="#create-a-batch-file-and-set-the-anaconda-prompt-to-always-run-as-an-administrator-windows-10">Create a Batch File to Launch Jupyter Lab Automatically (Optional but recommended)</a>
3. <a href="#change-the-default-jupyter-notebook-default-browser">Change the Default Notebook Browser (Optional)</a>

## Anaconda and Jupyter Notebooks
### Install Anaconda
<table><tbody><tr><td colspan="2">
 <ol><li>Click on the start menu button for you computer</li>
  <li>Search for "Control Panel"</li></ol></td></tr>
<tr><td style="width:60%;">
<ol start="3"><li>Click on Programs and Features (you may need to change the View by: "Categories" to View by: "Large or Small Icons" in the upper right first)</li></ol></td><td><img style="width:50%;" src="https://lh3.googleusercontent.com/pw/AL9nZEWU_unTK-Tp4xSC8mJgkxMq482winqpcrwWtHNfMYL8RgACWDFKVxfA1Mw9ylEJeozXbBghcxiWKYq_LI6hd8F9dP_PeMUXDWUMrXU3g_T3ShrPm0f5keThTxxEOWWbGRbXfJMB_dLFsyQl41mLOVXB=w1125-h738-no?authuser=0" /></td></tr>

<tr><td>
<ol start="4"><li>In the A's, see if you have Anaconda3 installed, go ahead and uninstall so you can update to the newest version.</li></ol></td><td>
<img style="width:50%;" src="https://lh3.googleusercontent.com/pw/AL9nZEV4PF8SHfThiyfWnxXCLHKoAgtCI1g-ByWkqP6129d94_5GjHPoZ4sC1znbuKXUl2JjvQ6UA08XTXLIcP4oZPpe5enLEQNYR34xdxsAEuQvAzoPj3mAmEP0JIaTROAGFmgxJtsCQUzeHz5vC5CBplQf=w1125-h738-no?authuser=0" /></td></tr>

<tr><td  colspan="2"><ol start="5"><li>Close the Programs and Features window</li>
<li>Visit: https://www.anaconda.com/products/distribution</li>
<li>Download the most recent Anaconda distribution for Windows</li>
<li><strong>When installing Anaconda</strong> BE SURE to select "Install Only for Me". This helps later with the environments</li>
<li>Once the installation is complete, launch an Anaconda Prompt AS AN ADMINISTRATOR (click on the start menu and start typing "Anaconda", once you find the Anaconda Prompt, right click and select "Run as Administrator")</li>
<li>In the prompt, type <code>conda --version</code>. A version number should be returned (also, you should be able to open an Anaconda command prompt)</li></ol></td></tr>
<tr><td><ol start="11"><li>Next, still in the Anaconda prompt, change to the directory where your Advanced Analysis folder resides. The easist way to do this is to first find the path of the folder using Windows Explorer, then copy the path from the Address bar (click in the white area to find the whole path)</li><ul><li>I HIGHLY recommend using a folder on the C: drive with no space, for example, C://Users//Yoda//Documents//GIS-3011.  Originally, I was saving everything to my OneDrive folder, which has spaces and is on the D:// of my computer, and GitHub kept throwing "Post 500 - Invalid Credentials" and "Dubious folder" errors, even though I took the time to add the OneDrive folder to the "safe locations" of the Git config file and updating the "credential.store" settings https://renenyffenegger.ch/notes/development/version-control-systems/git/options/safe/directory. In the end, the easiest and most direct fix was simply moving the folder to the C:// drive and removing the spaces.</li></ul></td><td>
<img style="width:50%;" src="https://lh3.googleusercontent.com/pw/AL9nZEWCwE-OokTEeObiwtzdwatUb9E9vmj12BY-1Pc9oqhiRhHhbEoSSnSdfChY21kh069-1bgASwVe5WEvESSD-pAdkX_4THPKiIp5jC5pMatGKU07OMaz5tofCtk-mYnCFX2VfMc9j3HWaDFQpPGrg5E2=w1095-h371-no?authuser=0" /></td></tr>

<tr><td  colspan="2"><ol start="12"><li>In the Anaconda Prompt, type <code>cd /d </code> and paste the copied path. This means: Change Directory (cd) to the specific directory stated (/d)</li>
 <ul><li>The prompt should change to read your Advanced Analysis folder</li></ul>
Here is some more information on managing Python environments stored on your computer: https://conda.io/projects/conda/en/latest/user-guide/tasks/manage-environments.html</li>
<li>Change the directory again using the command <code>cd gis-3011-setting-up-your-environments-<em>your github user name</em></code></li>
 <ul><li>Hint: Use the command <code>dir</code> to see the names of all the folders inside your GIS 3011 folder</li></ul>
 <li>Run the command: <code>conda install mamba -n base -c conda-forge</code></li>
<li>Check that mamba was installed correctly and in in the correct environment with the command <code>mamba --version</code></li>
 <li>Create the needed environment by using the command <code>mamba env create -f gis-3011.yml</code></li>
<ul><li>Solving and creating the environment may take up to 20 minutes, depending on your computer's hardware and space available</li></ul></ol>
Once the environment is created, you will need to activate said environment. This is necessary every time you start Jupyter Lab/Notebooks, but first, you are going to make sure the environments match.</li>
<ol><li>Find your environment's path with the command <code>conda info --envs</code></li>
<li>Determine if your environment was installed in one of the accessible conda environments with the command <code>conda config --show envs_dirs</code></li>
 <ul><li>If the allowed path and the installed path match, you're good to go.</li>
  <img src="https://lh3.googleusercontent.com/pw/AL9nZEVYvdpAIZisif5zNbEaTX73QWP-YLzeW84vqQ4I-KIDl8S87FnGh5UxI8DSGd0TMkLMlXvPVRYch03Bniej396FgYDs_SzrCyMfnyoDxlQh8DrWUX3B7lmhYwZ1I7FhAOTuKJAK4YpE8yCADFhJFWB3=w1234-h322-no?authuser=0" />
 <li>If it doesn't match, you'll need to add the path that *is* showing (everything before gis-3011) using this command <code>conda config --append envs_dirs /anaconda3/envs</code> (but do change it to the path you're showing). Then run the command <code>conda config --prepend envs_dirs /Users/<user>/anaconda3/envs</code> (be sure to change <user> to your user name!)</li></ul></ol>

 <ol start="17"><li>Activate the environment with the command <code>activate gis-3011</code></li>
<ul><li>You will need to activate the environment every time you plan to launch a Jupyter Notebook or Jupyter Lab.</li>
 <li>You may elect to add the following line to your text file which contains your GitHub Access Code (using your paths, obviously)</br><code>cd /d C:\Users\Jennifer/Documents\GIS-3011 && activate gis-3011</code></li>
 <li>You'll know the environment is active when (gis-3011) is showing at the start of the line.</li>
<img src="https://lh3.googleusercontent.com/pw/AL9nZEXPvz8iFtl7e7xYo1--gEYPdJtYWNJCmbk5yp9yD_-B5By89MBI7aGs304WNd2XBgwQzI6scsPTaolfwCqQAvXe5Xx2Cgosv-T6T_Ma677c9Na2_NxGSHg_DMJDB9JievLk3hSNb3sj2suMyraGTwTd=w502-h85-no?authuser=0" /></li>
 
<li>When you use a Jupyter notebook in ArcGIS Pro and it's spinning and says "Initializing kernel", it is using the conda activate command</li></ul></ol>
 <strong>MAKE SURE YOU'VE ACTIVATED THE GIS-3011 ENVIRONMENT BEFORE CONTINUING!</strong></ul>
 <ol start="18">
<li>Install the Jupyter Notebook extensions with the following command <code>pip install jupyter_contrib_nbextensions</code></li>
<ul><li>In this case, we were able to use the conda-forge package to install mamba, but if we were to do the same for the Notebook Extensions (nbextensions), we would get an error which reads <code>Config option `template_path` not recognized by ...</code> when we run the notebook.  The pip package is updated, while the conda-forge package is no longer maintained, per this article: https://github.com/ipython-contrib/jupyter_contrib_nbextensions/issues/1529 How did I figure that out? I Googled the error and read about it. The I did a <code>conda remove jupyter_contrib_nbextensions</code> to remove the conda-forge package and then ran the <code>pip install ...</code> command. The error went away</li>
<li>When possible, use the conda-forge packages with Python environments which use Jupyter as the update command is complete and inclusive.  In order to update packages installed with pip, you'll need to complete more steps: https://www.activestate.com/resources/quick-reads/how-to-update-all-python-packages/</li> </ul>
<li>Update all the packages with the command <code>conda update --all</code>
<li>Lastly, launch a instance of Jupyter Lab with the command <code>jupyter lab</code></li>
<ul><li>Alternatively, you could launch just a Jupyter Notebook via <code>jupyter notebook .</code> (yes, that's a period at the end and you do need it)</li>
<li>You may elect to add the following line to your GitHub Access Code text file: <br />
 <code>cd /d C:\Users\Jennifer/Documents\GIS-3011 && activate gis-3011 && jupyter notebook . </code> <br />
 and <br /><code>cd /d C:\Users/Jennifer\Documents\GIS-3011 && activate gis-3011 && jupyter lab</code>
 
so you can just copy and paste the whole command. Make sure it's all on one line (otherwise, it won't run all the commands if there are line breaks). The && means "run this command, then run this command, then run ..."</li>
 <li>Alternatively, you can launch Anaconda Navigator instead of the Anaconda Prompt and select a Jupyter Notebook (do be sure you have the gis-3011 environment selected in the drop down). Do be sure to launch Anaconda Navigator as an Administrator.</li>
<li>This will launch a Jupyter Notebook in Microsoft Edge, even if your default browser is Chrome or Firefox.</li></ul></ol>
<ol start="21"><li>Close out of Microsoft Edge and the Anaconda prompt.</li></ol>
</td></tr>
</tbody></table>

### Create a Batch File and Set the Anaconda Prompt to Always Run as an Administrator - Windows 10 (Optional, but recommended)

<table><tbody><tr><td colspan="2">
 <ol><li>Start a new text file with either Notepad</li>
 <li>In that Notepad file paste the following, <strong>making sure to change the GIS 3011 path to the appropriate path on your computer</strong></li>
 <ul style="list-style:none;><li">
<code>@echo on
call C:\ProgramData\Anaconda3\Scripts\activate.bat
call cd C:\Users\Jennifer\Documents\GIS-3011
call activate gis-3011
call jupyter lab
cmd \k</code></li></ul>
 <li>Save the file to your GIS 3011 folder, naming it JupyterLaunch.bat (change the dropdown in Notepad to *all files)</li>
 </ol></td></tr>
 
<tr><td><ol start="4"><li>RIGHT-CLICK the JupyterLaunch.bat file and select "Create Shortcut", renaming it something line JupyterLaunch.bat - Administrator</li><ul><li>Only shortcuts can be set to always run as an administrator</li></ul></td><td>
<img style="width:50%;" src="https://lh3.googleusercontent.com/pw/AL9nZEVKgmeUzFjezxSe2TWwWrIlNQIJurN3v2PQcThhPsAzie_iYjgvhcXcO034lLq0-ZTVmE0BQR5DSWOhwkEKy6MXcDyO7JBqOGbxsGBBGaXlSSdf_1jsiIs-NPpo9s3g39Tx-oAwHr55gMHoLNrOfFg5=w457-h200-no?authuser=0" /></td></tr>

<tr><td><ol start="3"><li>Right-click on the JupyterLaunch.bat - Administrator shortcut and select <strong>Properties</strong></li></ol></td><td>
<img style="width:50%;" src="https://lh3.googleusercontent.com/pw/AL9nZEWTsUXQxIVGQgUZVIL0FMvF-7ew1WKtS4s5B7Y-TwsSNhJNlvYYCLjK00tkzDdY9wppGlge3iQblNlNfDDk_ZWq75Ud9c0QzanGWql5f_s8OLsZLJ-plEV4G6eilhPocLuOPWlNqjyKqpsL_r75F3Nx=w507-h556-no?authuser=0" /></td></tr>

<tr><td><ol start="4"><li>Click on the <strong>Advanced</strong> button</li></ol></td><td>

<img style="width:50%;" src="https://lh3.googleusercontent.com/pw/AL9nZEUy7-wyZD7SggfBxt4xk5Zrss2BuOxHUc1RnfbONZPVMG5kPIZiSId3ZCIctF6HunvTYGjC9w8c7aQE66FfMPT8DKM4KWYR00jO3ebKz1Zemj6Zz3rIQuCLYGqzkz7saEEfnlh4WVs_9yuU0KuBE0cn=w390-h527-no?authuser=0" /></td></tr>

<tr><td><ol start="5"><li>Check the box for <strong>Run as Administrator</strong></li></ol></td><td>
<img style="width:50%;" src="https://lh3.googleusercontent.com/pw/AL9nZEVnuHDqADgnvSNxGtuJuKeqCt3ynRZ2LHvc3G5ZR8S8zQFTGtEq7ubw_buev-0S9daMNk_HbMX9jYOMZE09tUH_Ik3V-OYb0Ms6ElOGsY-wSYFypV5fQQjYzg4i2Bj9KkfG8eQsBkt__F0zWtmhKSBF=w380-h294-no?authuser=0" /></td></tr>

 <tr><td colspan="2"><ol start="6"><li>Hit OK twice to save the setting.</li>
 <li>From now on, you can just launch the JupyterLaunch.bat - Administrator shortcut and it will run. You could even add said shortcut to the start menu!
 <ol><li>Open C:\ProgramData\Microsoft\Windows\Start Menu\Programs in File Explorer (alternatively, right click on any of your Start Menu items and select More > Open File Location)</li>
  <li>Paste the shortcut in the Programs folder</li><li>Optionally, pin the shortcut to your Start Menu or Taskbar</li></ol></ol></td></tr></tbody></table>

### Change the Default Jupyter Notebook Default Browser (Optional)
 If you would like the notebook to launch in Chrome or Firefox, complete the following steps:
<table><tbody><tr><td colspan="2">
<ol><li>Launch an Anaconda Prompt as an Administrator (if you don't have one running)</li>
<li>Activate the gis-3011 environment</li>
<li>Run the command <code>jupyter notebook --generate-config</code> to generate (or expose) the Jupyter Notebook config file</li></ol></td></tr>
<tr><td><ol start="4"><li>Using Windows Explorer and the path shown, find the jupyter_notebook_config.py file (if you can't see the .jupyter folder, you'll need to show Hidden Items under the View menu of Windows/File Explorer) and RIGHT CLICK on the file, selecting <strong>Edit </strong> or <strong>Edit with Notepad++</strong></li></ol></td>
 
<td><img src="https://lh3.googleusercontent.com/pw/AL9nZEUQODmUiAVgfyqXK1XnHd0Vr1hEV1By-uj61HEwe94S9ZI1QCR2pX1JLTAx3ur3lSxawJTWyZn-yA4rm1VLxLeroWPD1o-lK78cJTb9yEXvoXGybaExiymKwupgocpgRotzq3ieZVsLgToFr5dgh7rc=w1007-h354-no?authuser=0" /></td></tr>
<tr><td colspan="2"><ol start="4"><li>Find the line which reads: <code># c.NotebookApp.browser = ''</code></li>
<li>Paste one of the following on the next line (find the line, press enter for a new line):</li>
<ul style="styel:none;><li">
<code>import webbrowser
 webbrowser.register('chrome', None, webbrowser.GenericBrowser('C:\\Program Files (x86)\\Google\\Chrome\\Application\\chrome.exe'))
 c.NotebookApp.browser = 'chrome'
</code>
 </li></ul>

or
<ul style="styel:none;><li">
<code>import webbrowser
 webbrowser.register('firefox', None, webbrowser.GenericBrowser('C:\\Program Files\\Mozilla Firefox\\firefox.exe'))
 c.NotebookApp.browser = 'firefox'
</code></li></ul></ol></td></tr>

<tr><td colspan="2"><ol start="5"><li>Save and close the jupyter_notebook_config.py file</li>
<li>Launch the Anaconda Prompt, change the directory, activate the gis-3011 environment, and launch a Jupyter Notebook.</li>
<ul><li>If the desired browser doesn't launch, make sure the program file paths are correct. The above are default paths.</li></ul></ol></td></tr></tbody></table>
