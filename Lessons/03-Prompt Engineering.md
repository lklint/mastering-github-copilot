# Prompt Engineering

Prompt engineering is the art of crafting clear, specific instructions that guide GitHub Copilot toward generating exactly the code you need—no more, no less. In this lesson, we’ll explore how thoughtful prompt design can turn an AI assistant into a reliable coding partner, whether you’re implementing game logic for our classic Snake project or refactoring a complex function. You’ll learn to balance context with conciseness, leverage examples to shape output style, and iteratively refine your prompts until the generated code fits seamlessly into your codebase. By the end of this session, you’ll have hands-on experience transforming vague requests into precise, self-contained prompts that unlock Copilot’s full potential.

## Utilizing Prompt Engineering for Effective AI Code Suggestions

Let's delve into prompt engineering a bit more. After all, that is the primary language that Copilot speaks. To effectively use prompt engineering with GitHub Copilot for coding tasks, follow these guidelines:

- **Be Specific**: Clearly describe the task, including details about functionality, inputs, and expected outputs. For the snake game we could have added "and make sure the game ends after eating 10 food" to make sure the game has some sort of completion. 
- **Use Comments**: Write detailed comments in your code to guide Copilot on what you want to achieve. The more context you can provide, the better answers Copilot will provide. 
- **Provide Examples**: Include examples of inputs and desired outputs to clarify your requirements. For example, we could say that the snake game should display food in various colours, such as yellow, green and blue. 
- **Break It Down**: Divide complex tasks into smaller, manageable parts and tackle them one at a time with Copilot's assistance. Do this for each of the features in the game that are mentioned below in the next section. A smaller issue is easier to solve than a big one that has multiple parts to the solution. 
- **Iterate**: Refine your prompts based on Copilot's responses to get closer to your desired solution. In the example above we could ask Copilot to improve on the method that checks if a word has been found (it doesn't work).  
- **Review Suggestions**: Carefully review Copilot's code suggestions for accuracy and efficiency before incorporating them into your project. It can be confidently wrong! 

## Exercises

### Ask general software questions

You can ask Copilot Chat general software questions. For example:

- `tell me about nodejs web server frameworks`
- `how can I create an Express app`
- `how to update an npm package`

### Ask questions about your project

You can ask Copilot Chat questions about your project.

- `What architecture is this snake game?`
- `how is the snake controlled?`
- `#file:gameReducer.js #file:gameInit.js how are these files related`

Below are some suggested exercises to practice your prompt engineering. You may have already done some of the features in the previous lesson. Copilot is a non-deterministic tool, meaning you get a different answer for the same question asked multiple times, hence we don't always know what happens 🤓

1. **Draft a clear, self-contained prompt**

   - **Objective:** Generate the snake’s movement logic.

   - **Starter prompt:**

     > “In JavaScript, write a function `updateSnake(snake, direction)` that takes an array of `[x,y]` coordinates (`snake`) and a string (`'up'|'down'|'left'|'right'`), moves the snake’s head one cell in that direction, shifts the rest of the body, and returns the new array.”

   - **Criteria:** Copilot returns a complete function with correct head-insertion and tail-removal logic, with no extra commentary.

2. **Iteratively refine a vague prompt**

   - **Objective:** Add collision detection to `updateSnake()`.

   - **Vague prompt 1:**

     > “Add collision checking to my snake game.”

   - **Refinement steps:**

     1. Ask for a function signature, e.g. `hasCollision(snake, gridSize) → Boolean`.
     2. Specify grid-bounds behaviour (wrapping vs. game-over).
     3. Show a sample input & expected output.

   - **Criteria:** Final prompt yields a standalone `hasCollision` function that returns `true` when the snake’s head hits itself or goes out of bounds.

3. **Use few-shot examples to guide output style**

   - **Objective:** Generate a `placeFood()` function that never overlaps the snake.

   - **Few-shot prompt:**

     ```js
     // Example 1:
     // snake = [[2,2],[2,3],[2,4]], gridSize = 10
     // returns e.g. [5,7]
     
     // Example 2:
     // snake = [[0,0]], gridSize = 5
     // returns [1,3]
     
     // Now, write the function:
     function placeFood(snake, gridSize) { … }
     ```

   - **Criteria:** Copilot follows the pattern, returning code that picks a random free cell.

4. **Generate keyboard-input handling**

   - **Objective:** Create a function to map key presses to snake direction changes (and ignore illegal reversals).

   - **Starter prompt:**

     > “Write a function `handleKeyPress(event, currentDirection)` that takes a keyboard event and the current direction string (`'up'|'down'|'left'|'right'`), returns the new direction, and prevents reversing (e.g. from `'left'` to `'right'`).”

   - **Criteria:** Copilot outputs a single `handleKeyPress` that reads `event.key`, maps arrow-keys or WASD to directions, and returns `currentDirection` if the requested turn is directly opposite.

5. **Extract configuration constants**

   - **Objective:** Refactor magic numbers into a separate config object.

   - **Starter prompt:**

     > “Refactor this Snake game code by extracting all hard-coded values (grid size, initial snake length, frame rate, cell size) into a `const config = { … }` at the top, and replace usages accordingly.”

   - **Criteria:** Copilot returns the full file with a `config` object and no remaining literals for those parameters.