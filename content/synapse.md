---
title: Setting Up Synapse for Fabric
---

If you're a Microsoft Fabric user, as well as a Jupyter Notebook user, you may have noticed the "Open in VS Code" button at the top but haven't figured out just how to use Fabric Notebooks in VS Code.  While there is an official page that shows how to do exactly this, it is incomplete and leaves on still unable to work with their Fabric Notebooks in VS Code.  Here's how I got it working (it took a while to figure out):

As the documentation states, the software requirements for this to work are:
- OpenJDK8
- Conda
- Jupyter extension for VS Code

Followed by making these changes:
1. Add JAVA_HOME to the environment variables and point it to the directory where Java 1.8 is installed
2. Add both %JAVA_HOME%/bin and the condabin subfolder of the Conda installation to the system path directory

Seems simple but still leaves a lot open to interpretation, so heres a more detailed guide:



## Installs
<u>OpenJDK8</u>

Here you can just follow the link that the documentation provides, and from there scroll down to your operation system and architecture, and click the JRE .msi download link and go through with the install.  Below should be the options you choose during the install setup.




<u>Conda</u>

A lot of Python users use Conda already so you may or may not already have it installed, if that's the case you can skip this and we can verify it's in the Path later.  If you do not, navigate to the Conda link per the documentation, and here I ended up going with the full Anaconda download versus the Miniconda download.  During the install setup you will be prompted with some options to select from, I personally deselected the "Register Anaconda3 as my default Python 3.11" because I don't want Conda to be my default, and it is easy enough to choose your kernel when working with Jupyter Notebooks in VS Code.

<u>Jupyter extension for VS Code</u>
This one is pretty straightforward and it is likely that you already have it installed if you already work with notebooks in VS Code.

## Environment Variables for Windows
1. Add JAVA_HOME to the environment variables and point it to the directory where you installed the Java 1.8 JRE, like below.  If you downloaded from Adoptium per the link your path should look similar.
![image](https://github.com/cdreetz/vercel-portfolio/assets/117322020/657d4760-4f3a-4cc7-96d0-5522a1592eb3)

   
2. Add both <b>%JAVA_HOME%/bin</b> and the <b>condabin</b> subfolder to the path directory.  Per the screenshot.  
![image](https://github.com/cdreetz/vercel-portfolio/assets/117322020/17b540b7-872d-4e2b-bd54-7d145964cd51)

## Install the extension
1. Search for Synapse VS Code in VS Code extension marketplace and install prelease version.
2. Restart VS Code

## Set up

Once you have all this and restart VS Code you should see a new extension symbol for the Synapse extension.  If you click that you will be prompted to set your local directory.  This can be an existing directory you have or one option is creating a fresh project folder that will be the directory for all of your Fabric Notebooks stored locally.  After this you should be able to login to your Microsoft account and select the workspace you want to use.  All that's left is to download the notebook you want to work on from the Notebooks dropdown.  Keep in mind you are more than likely going to need to install all your dependencies whether from Conda or Pip after activating the environment.  
![image](https://github.com/cdreetz/vercel-portfolio/assets/117322020/1f9d9c89-f980-4116-afe4-21c4ba77a024)
