+++
title = 'How to Use Ai in Programming'
date = 2025-04-15T17:01:39-03:00
description = 'How to use ai for your benefit while also breaking some misconception about the tool'
draft = false
tags = ['talk',]
+++

AI today is a hot topic, everywhere on the news, everyone is using, making lots of money, may it be producing GPUs, scraping data, training... But the tools are available for us to use for free, we have OSS models and free use in chatgpt daily that we can use to improve ourselves, but how?  


## Dimissing some misconceptions and learning about the tool


### AI is 100% correct all the time, I swear!  

The AI is really good, too good to be true in truth. Its answers are too cool and well made to be fake, right? right?! Well, no. First thing we need to dismiss is that idea that the AI is correct all the time because of its well formed answers.  
That is why my first tip is, at least have an idea about what you will ask, not the whole thing, of course, because the point in using AI is to learn new topics, for it to be a documentation on doping, but sometimes it derails with information that isn't true or mixed, to not go along with it having a rough idea of the topic before using is really important.

### AI will make all my work in the future and take my job!

Yes, unfortunately I want to say that you will be unemployed and serving the machines in the future, so at least say 'thank you' after asking anything to the LLMs you use ^-^.  
Yes, it was a joke, but I am joking with something a lot of people say seriously that I don't agree. A lot will be get with AI, some jobs will indeed have less need for a lot of workers because AI will be a great assistant, but intelectual jobs will always exist, AI can only produce material using as base its training data, which means only replicating.  
Using AI and knowing how it can be a good assistant will be a better effort than despairing about it taking over your job and not having your income anymore.  
Also notice that I focused in intellectual labor, physical labor also isn't affected by AI since it is restricted to computer and internet right now. Maybe robots in the future...


## How to use the AI chat correctly (prompt engineering or however you call it)


### Help in projects  

First you have a task you want help to accomplish, let's say you want to know how to make an API in FastAPI but you only know what an API is, never worked with FastAPI before, what do you do now?  
You declared what you wanted to do: make an API in fast api, great, the first step was done, now you need to provide context for the AI to analyze and answer accordingly.  
Remember when I said about having a rough idea? That is where it enters, before making a project in programming you know you need to prepare the environment.  
The prompt will be constructed in that way: context + task + result wanted  
It will be something like that:  
`I am a junior programmer that knows little about fastapi, I am responsible for creating an API with it, but before programming I want you to prepare the environment and guide me along the commands explaining me each step`  
What this prompt shows? your context (junior developer, responsible for creating an API), task (prepare for create an API, organize the setup), result (environment prepared and explanation for each step).  
What it does? It says what you want and it will be also saved as context for the chatgpt, because it now knows you will use `FastAPI` and will build an API, also for it to provide explanations for each step since you explicitely told to be inexperienced.  

### Help to Study

The outcome in this section wont be different from before, you can provide a prompt that asks for a direction or an explanation for the AI, but I want to specify a few things. Before you do have in mind 2 things.  
1. You will ask for something and its explanation, understand each step so you can reproduce or change the AI results (of course if you wish to learn it, if it is only production, just ignore and copy the outcome to paste somewhere else).
2. You will need to provide context about what you are doing and what you want to do, if it is related to programming, specify the name of classes/functions, what is the purpose of each and what they do, it helps to get more quality in the answer.

## Conclusion

I know this post is simple, but I hope it was of help to you. I made this post with chatgpt in mind, but in case you want to run a local model, I want to recommend you to look into the project [ollama](https://ollama.com/), but be aware that you have to have a dedicated GPU to get good results and run big models.
