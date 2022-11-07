[![Open in GitHub Codespaces](https://github.com/codespaces/badge.svg)](https://github.com/codespaces/new?hide_repo_select=true&ref=main&repo=526669888)

# Python Codespace Template

* **Who is this for?** _Educators of all levels_. 
* **How much experience do students need?** _Zero_. This template is built with basic elements complete with comments so it can be used in beginner to advanced lessons.
* **Prerequisites:** _None_. This template will provide a working and deployable web app you can immediately extend for your needs.

_Create or extend a ready-to-use repository for teaching Python in minutes_

With this template repository you can quickly create a normalized environment to teach or learn Python. Make your students focus on learning rather than setting up their environment. This template uses Codespaces, a development environment that's hosted in the cloud with [Visual Studio Code](https://visualstudio.microsoft.com/?WT.mc_id=academic-77460-alfredodeza), a powerful text editor.

🤔 Curious? Watch the following video where we explain all the details:

[![Teaching Python with Codespaces](https://img.youtube.com/vi/7rMvb03hHpI/0.jpg)](https://youtu.be/7rMvb03hHpI "Teaching Python with Codespaces")

<details>
   <summary><b>🎥 Watch the video tutorial to learn more about Codespaces</b></summary>
   
   [![Codespaces Tutorial](https://img.youtube.com/vi/ozuDPmcC1io/0.jpg)](https://aka.ms/CodespacesVideoTutorial "Codespaces Tutorial")
</details>

🚀 Codespaces features:

- Repeatable cloud environment offering a push-button experience.
- Can be configured and customized.
- Integrates with your repositories on GitHub and [VSCode](https://visualstudio.microsoft.com/?WT.mc_id=academic-77460-alfredodeza)

As a teacher that means that you can create an environment, in the cloud, for your class that all students can use with zero or next to zero configuration regardless of what operating system they are using.

## 🧑‍🏫 What is GitHub Codespace and how can I use it in my teaching?

A Codespace is a development environment that's hosted in the cloud that you can configure. The Codespaces Education benefit gives Global Campus teachers a free monthly allowance of GitHub Codespaces hours to use in [GitHub Classroom](classroom.github.com). Learn more [here](https://docs.github.com/en/education/manage-coursework-with-github-classroom/integrate-github-classroom-with-an-ide/using-github-codespaces-with-github-classroom) about Using GitHub Codespaces with GitHub Classroom.

If you are not already a Global Campus teacher, apply [here](https://education.github.com/discount_requests/pack_application) or for more information, see [Apply to GitHub Global Campus as a teacher](https://docs.github.com/en/education/explore-the-benefits-of-teaching-and-learning-with-github-education/github-global-campus-for-teachers/apply-to-github-global-campus-as-a-teacher).

## Customization

Customize your project for GitHub Codespaces by committing configuration files to your repository (often known as Configuration-as-Code), which creates a repeatable codespace configuration for all users of your project.

You can configure things like:

- Extensions, you can specify what extensions should be preinstalled.
- Dotfiles and settings.
- Operating system libraries and dependencies

> 💡 Learn more about [customization and configuration in the official documentation](https://docs.github.com/en/codespaces/customizing-your-codespace/personalizing-github-codespaces-for-your-account)


## Codespaces template

This repo is a GitHub template. It contains the following:

- [example-notebook.ipynb](./example-notebook.ipynb): A Jupyter notebook using the [Pandas](https://pandas.pydata.org/) library to teach basic operations with a small CSV (Comma Separated Value file) [dataset](./wine-regions.csv)
- [.devcontainer/Dockerfile](./.devcontainer/Dockerfile): Configuration file used by Codespaces to determine operating system and other details.
- [.devcontainer/devcontainer.json](./.devcontainer/devcontainer.json), A configuration file used by Codespaces to configure [Visual Studio Code](https://visualstudio.microsoft.com/?WT.mc_id=academic-77460-alfredodeza) settings, such as the enabling of additional extensions.
- `README.md`. This file describes this repository and what's in it.

## 🧐 Try it out

Try out this template repository using Codespaces following these steps:

1. Create a repository from this template. Use this [create repo link](https://github.com/microsoft/codespaces-teaching-template-py/generate). You can make the repository private or public, up to you.
1. Navigate to the main page of the newly created repository.
1. Under the repository name, use the Code drop-down menu, and in the Codespaces tab, select "Create codespace on main".
   ![Create codespace](https://docs.github.com/assets/cb-138303/images/help/codespaces/new-codespace-button.png)
1. Wait as Github initializes the codespace:
   ![Creating codespace](./images/Codespace_build.png)


### Inspect your codespaces environment

What you have at this point is a pre-configured environment where all the runtimes and libraries you need are already installed - a zero config experience.

You also have a Jupyter Notebook that you can start using without any configuration.

> This environment will run the same regardless of whether your students are on Windows, macOS or Linux.

Open up your Jupyter Notebook file [example-notebook.ipynb](./example-notebook.ipynb) and note how you can add code and run it.

## Customize the Codespace

Let's make changes to your environment. We'll cover two different challenges that you are likely to want to do:

1. Change the Python version installed
1. Add an extension


### Step 1: Change the Python environment

Let's say you want to change what version of Python is installed. This is something you can control.

Open [.devcontainer/devcontainer.json](./.devcontainer/devcontainer.json) and replace the following section:

```json
"VARIANT": "3.8-bullseye"
```

with the following instruction:

```json
"VARIANT": "3.9-bullseye"
```

This change instructs Codespaces to use Python 3.9 instead of 3.8.

If you make any configuration change in `devcontainer.json`, a box will appear after saving.

![Recreating Codespace](./images/Codespace_rebuild.png)

Click on rebuild. Wait for your Codespace to rebuild the VS Code environment.

### Step 2: Add an extension

Your environment comes with pre-installed extensions. You can change which extensions your Codespaces environment starts with. Here's how:

1. Open file [.devcontainer/devcontainer.json](./.devcontainer/devcontainer.json) and locate the following JSON element **extensions**:

   ```json
   "extensions": [
    "ms-python.python",
    "ms-python.vscode-pylance"
   ]
   ```

1. Add _"ms-python.black-formatter"_ to the list of extensions. It should end up looking like the following:

   ```json
   "extensions": [
    "ms-python.python",
    "ms-python.vscode-pylance",
    "ms-python.black-formatter"
   ]
   ```

   That string is the unique identifier of [Black Formatter](https://marketplace.visualstudio.com/items?itemName=ms-python.black-formatter&WT.mc_id=academic-77460-alfredodeza), a popular extension for formatting Python code according to best practices. Adding the _"ms-python.black-formatter"_ identifier to the list lets Codespaces know that this extension should be pre-installed upon startup.

   Remainder: When you change any configuration on the json, a box will appear after saving.

   ![Reacreating codespace](./images/Codespace_rebuild.png)

   Click on rebuild. Wait for your codespace to rebuild the VS Code environment.

To find the unique identifier of an extension:

- Navigate to the extension's web page, for example [https://marketplace.visualstudio.com/items?itemName=ms-python.black-formatter](https://marketplace.visualstudio.com/items?itemName=ms-python.black-formatter&WT.mc_id=academic-77460-alfredodeza)
- Locate the *Unique Identifier* field under **More info** section on your right side.

## Learn more

- [GitHub Codespaces docs overview](https://docs.github.com/en/codespaces/overview)
- [GitHub Codespaces docs quickstart](https://docs.github.com/en/codespaces/getting-started/quickstart)
- [Using GitHub Codespaces with GitHub Classroom](https://docs.github.com/en/education/manage-coursework-with-github-classroom/integrate-github-classroom-with-an-ide/using-github-codespaces-with-github-classroom)



### 🔎 Found an issue or have an idea for improvement? 
Help us make this template repository better by [letting us know and opening an issue!](/../../issues/new). 
