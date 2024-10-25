# Building a Chat AI

## Introduction

### I’ve always loved using ChatGPT, but paying for it wasn’t something I wanted to do. So, when I discovered that I could build my own GPT AI on my local machine, I was thrilled! With the right GPU, it can be just as fast—if not faster—than ChatGPT. I use AI regularly to help me study for certifications and identify flaws in code. Sometimes, I even rely on it to answer basic questions, much like a search engine. However, depending on your usage, free limits can run out quickly, forcing you to switch to a less powerful model. I often found myself alternating between Claude AI and ChatGPT, only to still run out of free server time.  

### That’s when I came across Open-WebUI, an open-source AI project you can install on your local machine. It has a layout and functionality similar to ChatGPT and runs a model called Ollama.  

### Ollama is a platform that allows you to run language models locally, rather than relying on cloud-based services like ChatGPT. This provides several advantages, with lower latency being a major one. If you’ve ever experienced running out of free server time on ChatGPT, you know how frustrating lag can be. Running a local AI also offers enhanced privacy. Unlike cloud-based solutions where your data is uploaded and potentially used for AI training, local AI ensures that your documents stay on your machine. Even if you opt out of data sharing, you still have to trust the company's policies. With a local model, that worry is gone—your data is part of the algorithm only on your machine.  

### Another great feature of Ollama is its customizability. It allows you to fine-tune models and configure how you want the AI to communicate, giving you greater control over the entire experience.  

---

 <b>Table of Contents<b>
   - [Initial Windows Setup](https://github.com/GSecAwareness/ChatAI/blob/main/setup.md)
   - [Ubuntu and Ollama](https://github.com/GSecAwareness/ChatAI/blob/main/linux.md)
   - [Docker and OpenWebUI](https://github.com/GSecAwareness/ChatAI/blob/main/part3.md)  
---

## Initial Setup  

***Step 1***  

Go to Windows Features (Turn on and off)  

***Step 2***  

Checkmark Virtual Machine Platform and Windows Subsystem for Linux  

![get-content](https://github.com/GSecAwareness/ChatAI/blob/main/1%20features.PNG)

***Step 3***  

Go to PowerShell (as an administrator) and type wsl -install  

***Step 4***  

Next, type:  

**wsl –update**    

This should install the WSL 2 Linux kernel 

![get-content](https://github.com/GSecAwareness/ChatAI/blob/main/1%20wsl%20update.PNG)

***Step 5***  

Next, set the default version to WSL 2, using the following commands:  

**wsl –set-default-version 2**  

![get-content](https://github.com/GSecAwareness/ChatAI/blob/main/2%20wsl%20default.PNG)  





