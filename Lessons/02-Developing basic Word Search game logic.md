# Developing basic snake game logic

Before you start creating our snake game, make sure VS Code is set up correctly. 

## Setting Up Visual Studio Code

You may have noticed that extensions in VS Code that were preconfigured either required a reload of VSCode/codespace or required you to login to your GitHub account. 

  - Before proceeding further check the extensions do not need an update or reload by opening the extensions panel (on the left, or by Ctrl+Shift+X).
  - You will see a list of installed extensions
    - locally if you are running your codespace via VSCode, and
    - within the codespace itself.
  - Pay particular attention to the copilot extensions. There should be a Copilot Chat button at the top next to the search bar too.
    - If you don't have the Copilot Chat button, make sure you have installed the Copilot and Copilot chat extensions.
    - Make sure you have logged into GitHub through VS Code.


## Writing Basic Game Logic using GitHub Copilot in Visual Studio Code:

- **Getting the first answer from Copilot**
  
  - Within Visual Studio Code (GitHub Codespace), navigate to the snake project.
  
  - Let's start doing some Copilot goodness! Using the Copilot chat window, describe the snake Game. Use precise natural language outlining the snake game logic, such as "Can you help me write the code for the classic snake game, where players have to grow a snake by controlling it with the arrow keys to eat squares? The gaming area should be 400px by 400px. The language used is JavaScript, HTML, and CSS". 
    Feel free to change how you want to instruct co-pilot. 
    
  - Copilot is likely to give you a whole directory structure and offer to create the workspace for you. You may also get instructions telling you how to approach setting up the project for the game. From experience the workspace solution generation is hit and miss, and may result in lots of errors. The simple approach to creating a project is often better. You can clarify to Copilot that you want basic instructions on how to start rather than a full solution from the beginning. 
  
- **Review and Refinement:**

  It is very likely Copilot didn't get it quite right, and there are bugs or missing parts. The actual game might not be implemented, at least not in any meaningful way. This is usually due to us humans not giving great instructions. After all, we aren't great at talking computer in the first place. 

  For example, step 1 of the instructions Copilot gives us might say "create new website project". If you don't know how to do that, that isn't helpful. We can ask clarifying questions of Copilot to help us get started.
  
  You should see a version of the snake game, depending on what Copilot suggested to you. 
  
  - Review Copilot's suggestions and accept or modify them based on your game requirements. Use either the chat to refine your instructions, or use the inline comments to trigger Copilot for suggestions. 
  - Refine the generated code to align with specified game logic requirements.
  - If you haven't already, run the game and see what it looks like. 
  

## Finish building the Core Mechanics of the Snake Game:

Use the remaining time for this module to get a basic version of the Snake Game working on your machine. It should at least have the following features

- A single snake being controlled by the arrow keys on the keyboard. 
- A big enough grid to make the game simple enough to start.
- Food being placed and replaced when eaten
- The snake getting longer for each food it eats.
- Inform the player when the game ends.