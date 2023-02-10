[![Open in GitHub Codespaces](https://github.com/codespaces/badge.svg)](https://github.com/codespaces/new?hide_repo_select=true&ref=main&repo=526669888)

# Python Codespace Template

_Create or extend a ready-to-use repository for teaching Python in minutes_

* **Who is this for?** _Educators of all levels_. 
* **How much experience do students need?** _Zero_. This template is built with basic elements complete with comments so it can be used in beginner to advanced lessons.
* **Prerequisites:** _None_. This template will provide a working Jupyter Notebook with Pandas using a dataset so that you can immediately start analyzing data as well as an example Notebook that you can use to teach Python with [GitHub Copilot](https://copilot.github.com), a powerful AI tool that helps you write code faster.


With this template repository you can quickly create a normalized environment to teach or learn Python. Make your students focus on learning rather than setting up their environment. This template uses Codespaces, a development environment that's hosted in the cloud with [Visual Studio Code](https://visualstudio.microsoft.com/?WT.mc_id=academic-77460-alfredodeza), a powerful text editor.

You'll also get the chance to try out Copilot to create a lesson plan using the [example-lesson.ipynb](./example-lesson.ipynb) file.

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

## 🤖 Use Copilot to create a lesson for students
GitHub Copilot is now available in GitHub Codespaces. You can use Copilot to create a lesson for your students. This repository includes the extension for Copilot so that you can use it right away. Make sure your account has access to Copilot. If you don't have access, you can [request access here](https://github.com/login?return_to=%2Fgithub-copilot%2Fsignup).

GitHub Copilot is free for students and faculty. [Learn more](https://education.github.com/pack/offers?WT.mc_id=academic-77460-alfredodeza). Follow [these steps]( ) to enable Copilot for free.

GitHub Copilot is free for students and faculty. [Learn more](https://education.github.com/pack/offers?WT.mc_id=academic-77460-alfredodeza). Follow [these steps](https://techcommunity.microsoft.com/t5/educator-developer-blog/step-by-step-setting-up-github-student-and-github-copilot-as-an/ba-p/3736279?WT.mc_id=academic-0000-alfredodeza) to verify your student or faculty membership and enable Copilot for free.

### Step 1: Write a description for your lesson
Open the [example-notebook.ipynb](./example-notebook.ipynb) file and write a description for your lesson in the first cell. Make sure Copilot is enabled by clicking on the Copilot icon in the status bar and ensuring you're logged into GitHub.

Edit the first cell and start typing `For this lesson`. Copilot will suggest a description for your lesson. Select the suggestion and press `Tab` to accept it.

The cell should now look similar to this:

```markdown
# Create a lesson using GitHub Copilot
For this lesson, you'll use GitHub Copilot to create a lesson for students to learn how to write functions in Python. You'll use Copilot to write code, and you'll use Copilot to write text.
```

It is OK if Copilot doesn't suggest an exact replica of the text above. You can edit the text to make it more suitable for your lesson.

### Step 2 Add steps to your lesson
Add a new cell below the description cell and start typing `### Step 1: Enable` to create a new step in your lesson. Copilot will suggest a step for your lesson. Select the suggestion and press `Tab` to accept it.

The cell should now look similar to this:

```markdown
## Step 1: Enable GitHub Copilot
Enable Copilot by following the instructions in the [GitHub Copilot documentation](https://docs.github.com/en/codespaces/developing-with-codespaces/using-codespaces-with-github-copilot). If you are a student, you can get a free [GitHub Student Developer Pack](https://education.github.com/pack) to get access to Copilot.
```

Keep adding more steps and continue typing to get more accurate suggestions for the content you are interested in. For example, this is a step that Copilot suggested for the next step in the lesson:

```markdown
## Step 3: Create challenges for this lesson
You'll teach students how to write functions in Python.
```

You can use the example above to see what Copilot can suggest and auto-complete. Feel free to add as many steps as you think are necessary for your lesson.

### Step 3: Add code challenges for students
Add a new code cell below the last step and start with a Python comment that describes the challenge. For example, you can write `# create a challenge for a student to write a function that returns the sum of two numbers`. Copilot will suggest a solution for the challenge. Select the suggestion and press `Tab` to accept it. For every new line, you can press `Return` (or `Enter`) to get a new suggestion.

This is a sample of what Copilot suggested for the challenge above:

```python
# create a challenge for a student to write a function that returns the sum of two numbers
"""
In this challenge, you'll write a function that returns the sum of two numbers.
You'll use the `sum` function to add the two numbers.
Start by writing a function that takes two numbers as parameters.
Then, use the `sum` function to add the two numbers.
Finally, return the sum of the two numbers.
"""
```

Again, your challenge may not be exactly the same as the one above. You can edit the challenge to make it more suitable for your lesson.

Create as many code cells with example prompts for your lesson.

### Step 4: Create a quiz for students
Add a new cell below for writing Markdown (not code!) and start by writing `### Quiz`. Then add an _HTML_ comment to create a prompt so that GitHub Copilot understands what type of quiz you want to create. For example, you could use something similar to this:

```html
<!-- generate a quiz of 5 questions about using Python functions with a mix of variable arguments and keyword arguments -->
```

Copilot might not suggest a quiz for you right away. If that's the case, add new lines to the comment and press `Return` (or `Enter`) and start enumerating the questions you want to ask. For example, you could write:

```markdown
1. What is the output of the following code?
```

Of if you are looking for a specific question about a topic it could be:

```markdown
2. When you create a function that
```

Copilot suggested a question using variable arguments which is what the challenge is about:

```markdown
2. When you create a function that accepts a variable number of arguments, what is the name of the parameter that you use to access the arguments?
```

Finally, review the cells and make changes as necessary. You can also add more steps, challenges, and questions to your lesson. 

Congratulations! You've created a lesson for students to learn how to write functions in Python using GitHub Copilot. You can use Copilot to assist you in documentation, writing examples, or challenges like in this repository. Even this whole section was written using Copilot!

## Learn more

- [GitHub Codespaces docs overview](https://docs.github.com/en/codespaces/overview)
- [GitHub Codespaces docs quickstart](https://docs.github.com/en/codespaces/getting-started/quickstart)
- [Using GitHub Codespaces with GitHub Classroom](https://docs.github.com/en/education/manage-coursework-with-github-classroom/integrate-github-classroom-with-an-ide/using-github-codespaces-with-github-classroom)



### 🔎 Found an issue or have an idea for improvement? 
Help us make this template repository better by [letting us know and opening an issue!](/../../issues/new). 
