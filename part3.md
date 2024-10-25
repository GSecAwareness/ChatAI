# Docker and Open WebUI

## Next, let’s install OpenWebUI, a web-based interface that makes managing AI models like Llama 3.1 much easier. With OpenWebUI, you can load and interact with the model directly from your browser, eliminating the need for command-line inputs. This interface provides a user-friendly platform for configuring and experimenting with Llama 3.1. 

![get-content](https://github.com/GSecAwareness/ChatAI/blob/main/docker-2752207-2285024-91679242.png)

---

 <b>Table of Contents<b>
   - [Initial Windows Setup](https://github.com/GSecAwareness/ChatAI/blob/main/setup.md)
   - [Ubuntu and Ollama](https://github.com/GSecAwareness/ChatAI/blob/main/linux.md)
   - [Docker and OpenWebUI](https://github.com/GSecAwareness/ChatAI/blob/main/part3.md)  
---


## Docker  

***Step 1***  

To get started, we’ll need to install Docker, which can be done using the following command:  

**sudo snap install docker**  

Snap is a package management system designed to streamline software installation by offering self-contained packages. These packages come with all the necessary dependencies included, making them convenient as they bundle everything needed for the software to run smoothly in one cohesive package. This makes installation a snap!  

***Step 2***  

Once the setup completes, we want to run llama3.1 inside docker and launch it on port 3000. To do this, use the following command:  

**sudo docker run -d -p 3000:8080 --gpus=all -v ollama:/root/.ollama -v open-webui:/app/backend/data --name open-webui --restart always ghcr.io/open-webui/open-webui:ollama**

Just for fun, I tried omitting the **--gpus-all** portion of the command, which forces it to run the model without a GPU. I do not recommend this, unless you want to see the performance enhancement by using a GPU to run the model. 

***Step 3***  

Once the command has completed, type the following to verify and see the list of running containers:  

**docker ps**  

![get-content](https://github.com/GSecAwareness/ChatAI/blob/main/10%20docker%20running.PNG)  

***Step 4***  

Go to your web browser, such as Firefox, and type:  

**http://localhost:3000**  

It should prompt you to sign in or create a username (email) and password for authentication. Because it is stored locally and really doesn’t matter, I used a@a.com and an easy to remember password. 

I faced a few challenges during this project, including needing to repeat the installation and troubleshoot several steps. Some of the difficulties arose from using commands meant for WSL1 while working with WSL2, which led to some unexpected complications. Consequently, the Llama 3.1 model wasn't included in my final setup. However, this is not a significant issue. I’ll guide you through the process of installing Llama 3.1 directly from the interface.

![get-content](https://github.com/GSecAwareness/ChatAI/blob/main/ollama.png)

***Step 6***  

a. Navigate to your profile icon at the top right. Choose Admin Panel.  

b. Choose Settings --> Models  

c. Pull a model from https://ollama.com/library (click the link to see the list of models)  

d. Copy llama3.1 or just enter it into the field. Click the Download button on the far right.  

e. Once your model has downloaded, installed, and verified the hash, naviage back to the main dashboard screen.

![get-content](https://github.com/GSecAwareness/ChatAI/blob/main/11%20llama.PNG)

That covers most of the process. I spent some time exploring the settings and visiting the official website. From there, you can easily download additional models and prompts to support your studies, work, or casual chats.













