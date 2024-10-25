
# Introduction to Part 2  

## Now, let's install Linux using WSL and Ollama. Windows Subsystem for Linux (WSL) is a feature in Windows that allows you to run a full Linux environment directly within Windows, without the need for a virtual machine or dual-boot setup. This is especially useful for those who want to use Linux-based tools, such as Python or Bash, while keeping the Windows interface. 

## By removing the dependency on virtual machines, WSL reduces overhead, leading to better performance and lower memory usage. We’ll be using WSL 2, the latest version, which includes a full Linux kernel, greatly improving compatibility with Docker containers—an essential part of our setup moving forward. I chose to use Ubuntu because of its compatability and support with the Windows WSL service, but there are multiple options in the Microsoft store to choose from.  


 <b>Table of Contents<b>
   - [Initial Windows Setup](https://github.com/GSecAwareness/ChatAI/blob/main/setup.md)
   - [Ubuntu and Ollama](https://github.com/GSecAwareness/ChatAI/blob/main/linux.md)
   - [Docker and OpenWebUI](https://github.com/GSecAwareness/ChatAI/blob/main/part3.md)  
---


***Step 1***  

Either go to the Microsoft Store and search for the app Ubuntu. You can install it from the store. Or you can install it from Power Shell, which is much easier.   

From PS, type:  

**wsl –install -d ubuntu**  
This will take some time. 

![get-content](https://github.com/GSecAwareness/ChatAI/blob/main/3%20ubuntu%20install.PNG)  

***Step 2***   

Upon completion, it will ask for a username and password. Set them both up.  

***Step 3***  

With Ubuntu installed, we need to open it. You can choose it from the recently added Program List, or you can open a folder (file explorer) and type WSL (hit enter). Both work to open Ubuntu command line. 

Now that everything is set up correctly, we want to install Ollama, which will run our AI models.  

***Step 4***  

We will use the curl command and type it directly into command shell to install it from the website.   

**curl -fsSL https://ollama.com/install.sh | sh**  

![get-content](https://github.com/GSecAwareness/ChatAI/blob/main/4%20install%20ollama.PNG)  

***Step 5***  

Once completed, type:  

**ollama serve** to start the program. 

My installation failed twice due to an inconsistent network connection, but on the third attempt, it completed successfully with no errors. It's unlikely that you'll encounter the same issue, but I wanted to share this to reassure you that the installation can resume from where it left off if interrupted. Now, here are the available commands for the program.  

![get-content](https://github.com/GSecAwareness/ChatAI/blob/main/5%20ollama%20serve.PNG)  

***Step 6***  

With Ollama running, we need to install the latest model, specifically llam3.1. To do this, use the following command:  

**Ollama pull llama3.1:latest** 

![get-content](https://github.com/GSecAwareness/ChatAI/blob/main/6%20ollama%20pull.PNG)

***Step 7***  

Once completed, type ollama list to see the currently installed models. This will verify that the model downloaded and installed correctly.

![get-content](https://github.com/GSecAwareness/ChatAI/blob/main/7%20ollama%20list.PNG)  

***Step 8***  

If you want to run the command-based model, type the command:  

**ollama run llama3.1:latest**

This works like a charm and you effectively have an operational language-based AI model installed on your local machine!!  
However, lets' install a web-based graphical user interface called OpenWebUI to manage our model and give us our much desired GUI. 
