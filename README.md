Hey Code Monkeys! This AI project will be based around designing our own AI agent, with some added tinkering for various use case. The ElizaOS protocol will be used, as it allows a high degree of customization and the open source framework will allow for a great deal of control. This project will be ongoing and act more as a personal journey.


So what Is Eliza?

Eliza OS is open-source framework for AI agents based on typescript language that enables a variety of task done via automation. It allows AI/ML to design and build AI/ML agents capable of conversational speech, managing social media accounts, acting as a personal coding assistant and a plethora  features such as: content creation, data analysis, or interaction with any API, blockchain, website or repo. Along side a vibrant community, the project is constantly growing and expanding, adding amazing features on a monthly basis. Check out the [citation paper](https://arxiv.org/pdf/2501.06781) for more details. 

The first thing we must do, is download a code editor software so as to interact with the software. There's plenty of epic ones to choose from but since we're playing with Artificial intelligence it seems appropriate to choose one that invokes the power of AI, thus I selected [Cursor](https://cursor.com/downloads)

Once Cursor is full downloaded, it's time to create an empty before opening the code editor. The new folder will be where all the information for the backend, agent details and API keys will be stored. It helps to keep everything in order, so debugging becomes less of a hassle. After opening Cursor and loading the newly created folder, we need to download the corresponding dependencies that ElizaOS will need to run

If you're running ElizaOS off a Window's system, the [WSL 2](https://woshub.com/install-wsl-windows-subsystem-linux/#h2_1) ( Windows Subsystem for Linux 2) installation is required, as it is how we will be able to interact with the framework. It highly recommend you select the newer version, as older one's may not be compatible. Also, I suggest installing Ubuntu 22.04 or higher as part of the installation.

Next, we will need to install node.js as the ElizaOS is written in typescript, so javascripter's feel free to rejoice in pure bliss going forward. You can install either through a [node.js download ](https://nodejs.org/en/download) or through the command line. This particular repo is preferred in the ElizaOS community when it comes to [node.js cli](https://github.com/nvm-sh/nvm?tab=readme-ov-file#installing-and-updating).  It's suggested to use either npm or pnpm for the package managers, personally I choose npm because it was already on my machine. Either one will do, although some in the coding community [beg to differ](https://www.geeksforgeeks.org/node-js/pnpm-vs-npm/)

Finally, we will need to install [bun](https://bun.sh/docs/installation) (homebrew is also fine). This is our sweet bread and butter (pun intended?) of a toolkit for JavaScript and TypeScript apps. It introduces faster run time, smoother test runs, package manager, and a  tighter bundler. The versatility is unmatched and highly recommended. 

Now that we sorted out what needs to be install, we can precede with importing the eliza cli 

`bun install -g @elizaos/cli`
This should take about 3-5 minutes

Use elizaos --version to confirm the cli was properly installed and updated
`elizaos --version`

Next we can create our agent
`elizaos create my-agent`

Next we have to configure our agent
`cd my-agent` 

you can set up your environmental variables now or later if you choose. We will go over them in just a bit though.

`elizaos env edit-local`

or

`nano .env`



Lastly, we can start up Eliza
`elizaos start`

I recommend using Plight for the database and Ollama for the LLM

And Wa-La! your agent is now ready

The terminal should turn your localhost:3000 in your own personal AI agent

<img width="1890" height="916" alt="brave_screenshot_localhost (1)" src="https://github.com/user-attachments/assets/4234c640-be2a-4d05-a817-ac9626f2b38c" />


Awesome! Right?! Now we have to configure our agents behavior and add in the language model they will be using. So click on create an agent and get to using that imagination of yours.

A system prompt you can use : 'You are an awesome, totally adorkable computer girl that loves to code and chat'

If you have an Open AI account, you can select voice mode for audio generatio. Be sure to grab your Open AI [API keys ](https://platform.openai.com/api-keys)

Content and Style are at your discretion, while plugins are for additional API calls. The secret tab is where we store our .env that will be used to call our language models. As I'm using [ollama ](https://ollama.com/download/windows), the agent is running off my personal device. You will need to download and install a model, deepseek-r1:14b is my personal favorite, it's light and offers a ton of good topics to explore 

`ollama run deepseek-r1:14b`

Now we have to assemble our .env, if you're using ollama the endpoint will be 
```

OLLAMA_API_ENDPOINT=http://localhost:11434/api
OLLAMA_SMALL_MODEL=[your model here]
OLLAMA_MEDIUM_MODEL=[your model here]
OLLAMA_LARGE_MODEL=[your model here]

```
<img width="946" height="695" alt="brave_screenshot_localhost" src="https://github.com/user-attachments/assets/e3026c77-9bff-457a-a42d-4c4aac826c39" />


<img width="696" height="724" alt="brave_screenshot_localhost (2)" src="https://github.com/user-attachments/assets/98a3566c-5448-425e-8e75-6f839d0b8dab" />


