<header>

# Project 2: Using GitHub Copilot To Create a QR Code Generator

In this workshop, we will focus on using the power of GitHub Copilot to enhance your coding efficiency.

As a developer, your goal is to create a **QR Code Generator**. The generator should accept a URL as a data input and return a QR code image. You will also need a README to explain to users how to use your generator. It is a good idea to include a few unit tests to ensure your code works as expected.

GitHub Copilot acts as your AI pair programmer, offering suggestions based on context and code patterns. In this workshop, you'll use GitHub Copilot to generate, test, and document code through suggestions and prompts. As you work through the exercises, you'll learn how to use GitHub Copilot to improve your projects and increase your productivity. While working, document or keep in mind the suggestions that GitHub Copilot provides to help you understand the code better.

## 🎯 Learning Objectives

</header>

- **Who this is for**: Developers, DevOps Engineers, Software development managers, Testers.
- **What you'll learn**: Using GitHub Copilot to create code and add comments to your work.
- **What you'll build**: Python files that will have code generated by Copilot AI for code and comment suggestions.
- **Prerequisites**: To use GitHub Copilot you must have an active GitHub Copilot subscription. 
- **Timing**: This workshop can be completed in 20 to 30 minutes.

By the end of this workshop, you'll acquire the skills to be able to:

- Craft prompts to generate suggestions from GitHub Copilot
- Apply GitHub Copilot to improve your projects.

## 🌻Optional reading:
If you have extra time, you can read more about GitHub Copilot and how to use it in your projects:
- [Introduction to prompt engineering with GitHub Copilot](https://learn.microsoft.com/training/modules/introduction-prompt-engineering-with-github-copilot//?WT.mc_id=academic-113596-abartolo)
- [GitHub Copilot in VS Code](https://code.visualstudio.com/docs/copilot/overview)
- [How to use GitHub Copilot: Prompts, tips, and use cases](hhttps://github.blog/2023-06-20-how-to-write-better-prompts-for-github-copilot/)
- [10 Unexpected Ways to Use Github Copilot](https://github.blog/2024-01-22-10-unexpected-ways-to-use-github-copilot/)

## ✅ Requirements
The following are required to complete this workshop:
1. A GitHub Copilot subscription
2. Python 3.6 or later 

> [!NOTE]
>  This workshop is `Python focused, but you can use Java 8 or later for the same exercises`. Remember that the examples and prompts will be Python-based. Ask GitHub Copilot for help if you need to convert the code to Java.


## 🥅 Goal

1. Create a QR Code Generator that takes a URL as input and returns a QR code image.
2. Properly add comments and documentation to your code for future engineers.
3. Write tests for the QR Code Generator.
4. Document the QR Code Generator in a README file.


## 💪🏽 Exercise


### 🛠 Step 1: Create a QR Code Generator 

Create a `main.py` file, and add a comment anywhere in the file that prompts GitHub Copilot to generate a `QR Code Generator Function` for you. For example you could add a comment like: 

```
# Create a QR Code Generator Function that takes a URL as input and returns a QR code image
```

The generated model should look like this:

```python
def generate_qr_code(url): 

text: str
```

> [!NOTE]
> In VS Code, you can use the `Ctrl + i` keyboard shortcut to open the GitHub Copilot chat interface. You can also use the `Ctrl + Shift + P` keyboard shortcut to open the command palette and then type `GitHub Copilot: Open Chat` to open the chat interface.
>
>❕You can also use the chat interface to ask GitHub Copilot to generate a QR Code Generator Function for you.

Add another function that will save the QR code image to a file. You can use a comment to prompt GitHub Copilot to generate the function. This time create your own prompt to generate the function.

This function should look something like this:

```python
def save_qr_code(image, filename):
    ...
```


### 🏃Step 2: Run Python Script

Prompt GitHub Copilot to add a main block that will run the QR Code Generator and Save Function. Either in the chat or code window, prompt GitHub Copilot to generate the main block and then run the script.

> [!NOTE]
> If you ever forget how to run a particular command when you’re working in your VS Code, GitHub Copilot Chat is here to help! With the `@terminal` agent in VS Code, you can ask GitHub Copilot how to run a particular command. Once it generates a response, you can then click the “Insert into Terminal” button to run the suggested command. Just type `@terminal` in the chat interface to get started!
>
> ❕You can use this feature to run the Python script that GitHub Copilot generates for you.

---

*For bonus points,* prompt Github Copilot to handle arguments from the command line. The desired goal is to have a script that can take a URL as an argument and generate a QR code image.

**Input:**
```python
python main.py 'https://example.com'
```
**Output:**
```
A saved QR code image file in the same directory as your script.
```
---



At this point, you should have a Python script that generates a QR code and saves it to a file. Run the script to verify that it works as expected. You should see a QR code image saved to a file in the same directory as your script.

If you encounter any issues, you can ask GitHub Copilot for help in the chat interface.

### ✏️ Step 3: Explain code

The `generate_qr_code()` function might be difficult to fully understand. Select the whole function, and then right click on the selection, then select the Copilot menu item, and then the _"Explain This"_ option. The GitHub Copilot chat interface will open to the left and provide you a useful explanation which you can use to interactively ask more questions.

🚀 Congratulations, you not only used Copilot to generate code but also used copilot to explain it back to you! GitHub Copilot can not only generate code, but write documentation, test your applications and more.

### 🧠 Step 4: Using Slash Commands

Now that you've used GitHub Copilot to generate and explain code, you can also explore some other alternative approaches to perform developer tasks. These extra challenges will help you dive deeper into other GitHub Copilot features in addition to the ones you already know. For these extra challenges, you will use the Chat interface. Click on the GitHub Copilot Chat icon on the left sidebar if you don't have it open yet.

#### **Step 4.1 Generate documentation**

The `/doc` part of the prompt is called a _"slash command"_ and it is a specific feature of GitHub Copilot that allows you to interact with the AI in a more structured way. In this case, the `/doc` command will guide you through on writing a new documentation for your code and give you everything you need so that you can document your work.

With `main.py` open, use the chat interface by typing the `/doc` slash command. 


#### **Step 4.2 Generate tests**
 
The `/tests` slash command will guide you through on writing a new test for your route and give you everything you need so that you can verify your work.

With `main.py` open, use the chat interface by typing the `/tests` slash command & create a prompt that mentions the following:

- Write a test for the QR Code Generator Function.
- Use the Pytest framework.
- Describe how to run the tests.

For best practice, tests should be in a separate file. GitHub Copilot can guide you through the process of creating a test file, adding the Pytest dependency to your project, and running the tests.


### 📝 Step 5: Add a user README.md
For the last step, create a `README.md` file that explains how to use your QR Code Generator. You can use the `/doc` slash command to generate a README template. The read me should include the following:
* How to run the script.
* What the script does.
* What the expected input and output are.
 
 ### Congratulations! 🎉
You have successfully used GitHub Copilot to create a QR Code Generator. You have also learned how to use GitHub Copilot to generate code, write documentation, and create tests. You can now use GitHub Copilot to improve your projects and increase your productivity.

---
### 🎁 Bonus Challenge!
If you have extra time, you can try the following bonus challenge:

- Add a cli interface to your script that allows users to input a URL and generate a QR code image.
- Ask Github Copilot how to create a CLI interface for your script.
- Create an optional parameter that allows users to specify the output file name. 