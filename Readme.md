# Notebook for Ocean for Apache Spark

This doc explain how to run notebook connected to a Ocean Spark cluster with VSCode

## Installation

- Prerequisites: 
  - You should be familiar with running a notebook on OfAS, you can follow this [doc](https://docs.spot.io/ocean-spark/tools-integrations/connect-jupyter-notebooks) 
  - You should have the Jupyter notebook Python package installed locally

### Clone this repo

`git clone https://github.com/epignot/vscode-ofas-notebook-template.git`

### Open the project with VSCode
- Open manually the folder `vscode-ofas-notebook-template`
- Or from your terminal : `code vscode-ofas-notebook-template`


## Connect to Remote server

- Go to "Run and Debug" panel
- Select `Connect to remote Jupyter`
- Click on triangle icon  
- Enter your OfAS cluster id when prompted and hit enter
- Enter your Spot personal access token when prompted and hit enter


You should see the notebook app starting in the terminal

**copy the url in the output like :  `http://localhost:8888/?token=xxx`**


## Launch a notebook  

- Open a notebook file (.ipynb)
- In the status bar, click on "Jupyter Server: remote" (down-right corner)
- When the Palette input prompts: 
  - Select : `Existing`
  - Paste the url copied before
  - And hit Enter
  - wait few seconds for the palette to close
- In the upper-right corner of the notebook, click on the kernel, and pick a config-template

Now, if you run code in your notebook, it will start an app for you in OfAS.  
_Please note that it can take few minutes for the app to be ready to execute your code_

Note: Auto-start of notebooks is disabled to avoid starting multiple app before you're sure of the config template you want to use. Feel free to change this in the setting file. (`jupyter.disableJupyterAutoStart`)

### End connection to remote server
When you're done, Go to terminal panel and Hit `Ctrl-C` then enter `y` to shutdown connections and kernels.  



