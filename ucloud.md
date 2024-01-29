## Quick setup for GitHub with VS Code

Steps:
- 1) Run an instance of VS code on UCloud
  - Use limited compute for the first classes
  - Mount your own (private!) folder to the instance in which you create the following files.
- 2) Create a file called `setup_git.sh` containing the following code:


```bash
# run using 
# bash path_to_folder/setup_git.sh

git config --global user.email "yourmail@mail.com"
git config --global user.name "Your Name (UCloud)"
```

Make sure to fill in the correct username and email. This will set up GitHub, but you also need to:

- 3) Create a file called `git_token.txt` which contain your [personal access token](https://docs.github.com/en/github/authenticating-to-github/keeping-your-account-and-data-secure/creating-a-personal-access-token).

Save the files and you can now close the session. Next time you start a session you can mount your folder and run:

```
bash path_to_folder/setup_git.sh
```

to set up git. If you want to use the VS code GitHub integration you will still need to log in using the GitHub access token, which can simply be copied from the file `git_token.txt`.

## Collaborate with VS Code
In the [VS code documentation](https://docs.cloud.sdu.dk/Apps/coder.html?highlight=coder%20share#start-live-share) on UCloud there is a guide to setting up live share on UCloud.


## Integration between UCloud and GitHub
Let's look at how to use the repository with course materials. First, log in to https://github.com and go to the repository's link: https://github.com/rbroc/DataSci-AU-23. 

##### Forking the repository
Click on `Fork` (top-right of the page). This creates a copy of the repository which is partly independent of the original repository. You will be submitting changes to *this* repository. 
The original repository will be iteratively updated with new materials or exercises. You can sync the two by setting them both as *remotes* in your local instance of the repository. 

##### Cloning the repository and setting up remotes
With the VS Code app on UCloud open, and a Terminal open, you can clone your repository by `cd`-ing into your private drive (the one called `MemberFiles[yourname][idnr]`), and running: 
```
git clone https://github.com/your_username/DataSci-AU-23
```

You can visualize your remotes by typing: `git remote -v`.
You should add my repository as a remote, by running:
```
git remote add [robertas_remote_name] https://github.com/rbroc/DataSci-AU-23.git
```

##### Our workflow
As my repository gets updated, you can pull it into yours by running:
```
git pull [robertas_remote_name]
```

You can push to your remote by typing:
```
git push origin [branch_name]
```

Once you have done this, our workflow will be the following:
- You run the github setup script (and log in with your token if needed)
- You go to your local repo
- You pull my repo
- You make changes and push to your fork

## Virtual environments
A good way to manage dependencies for specific projects and avoid conflicts is to create virtual environments (which contain bundles of libraries that you can "activate" and "deactivate" at will, without those interfering with your global environment). I tend to keep my virtual environments in the same place, e.g., a subfolder called `venvs` in my private drive on UCloud.

##### Creating, activating, and deactivating a virtual environment

Run these two lines (or add them to your setup script):
```
sudo apt-get update
sudo apt-get install python3-venv
```

Let's create a virtual enviroment.
1. Navigate to your private drive if you are not there already, or to wherever location you want to keep your enviroments in (`path_to_folder`)
2. Create a virtual environment folder, e.g., by running `mkdir venvs`
3. Create a new virtual environment (`nlp-e23`), by running:
`python -m venv path_to_folder/venvs/nlp-e23`
4. You can activate it by running: `source path_to_folder/nlp-e23/bin/activate`
5. To deactivate it, you can simply run: `deactivate`
Anything you `pip install` while the enviroment is active stays inside the environment. 
To make sure you have the latest pip, run:
```
pip install --upgrade pip
```
The nice thing about this is that you don't need to reinstall stuff whenever you open UCloud, just load your virtual environment.

##### Using it in a notebook
Everything you install which the virtual environment is active is fully contained inside the virtual environments.
If you virtual environment is active, scripts will use it, but an extra step is needed to use it as part of notebooks.
First, we need to install ipykernel:
```
pip install ipykernel
```

Then, we need to create a new kernel using our virtual environment:
```
python3 -m ipykernel install --user --name=nlp-e23
```

Now try to open a notebook (you can create an empty one by running `touch notebook_name.ipynb`). On the top right, you can choose a kernel. A kernel based on the virtual environment will be available.

##### Installing libraries from a requirements file
An easy way to keep track of your dependencies is to add them to a requirements file. They are generally called something like `requirements.txt`, and they are simply a list of libraries your project needs.
The content of the text file looks something like this:
```
datasets==2.12.0
pandas==1.5.3
```
You will have one library per line, and -- although it is not obligatory -- you can pin the package to the version you know is needed for your project.
You can install all the dependencies needed from your requirements file, by running:

`pip install -r requirements.txt`