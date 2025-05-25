## Chat Participants (Agents) in Copilot Chat

GitHub Copilot Chat lets you target specialized “agents” — called *chat participants* — by prefixing your prompt with `@`. These agents act like domain experts, bringing focused context and capabilities into your conversation. To explore all available participants, simply type `@` in the chat box and pick from the list ([GitHub Docs](https://docs.github.com/en/copilot/using-github-copilot/copilot-chat/getting-started-with-prompts-for-copilot-chat)).

Below are some of the most commonly used chat participants:

- **@azure**
  Has deep knowledge of Azure services and deployment patterns. Use this agent when you need assistance integrating or managing Azure resources.
- **@github**
  Unlocks GitHub-specific skills such as issue creation, pull-request summaries, or repository insights. Ideal for automating GitHub workflows directly from chat.
- **@terminal**
  Understands your VS Code integrated terminal environment. Invoke this agent to generate or debug shell commands, scripting tasks, or CI/CD scripts.
- **@vscode**
  Brings in knowledge of Visual Studio Code commands, extensions, and editor features. Perfect for IDE-centric guidance like keybinding changes or debugging workflows.
- **@workspace**
  Provides visibility across all files in your current workspace. Use it when you want Copilot to consider the structure, inter-file dependencies, or architecture patterns of your project.

## Exercises

Here are five hands-on exercises to help you get comfortable invoking and combining Copilot chat agents. In each, you’ll prefix your prompt with the appropriate `@agent` and then inspect how the expert responds.

1. **Explore Your Workspace with `@workspace`**

   - **Objective:** Get a high-level summary of your Snake project files and dependencies.

   - **Prompt to Use:**

     ```
     @workspace Give me a summary of the folder structure, key modules, and dependencies in this Snake game repo.
     ```

   - **Success Criteria:** You receive a breakdown of directories/files (e.g. `src/index.js`, `src/game.js`, `package.json`), plus notes on which modules handle movement, rendering, and config.

2. **Craft Dev Scripts with `@terminal`**

   - **Objective:** Generate a cross-platform npm script to both start a dev server and watch for code changes.

   - **Prompt to Use:**

     ```
     @terminal I need an npm script in package.json called "dev" that runs a local web server on port 3000 and rebuilds on file changes.
     ```

   - **Success Criteria:** The agent returns a `package.json` snippet with a `"scripts": { "dev": "..." }` entry using something like `live-server` or `webpack serve` and includes any necessary flags for watching.

3. **Automate PR Summaries with `@github`**

   - **Objective:** Draft a pull-request description for adding a “high-score leaderboard” feature.

   - **Prompt to Use:**

     ```
     @github I’ve just implemented a high-score leaderboard in src/leaderboard.js. Write a clear PR title and description that explains the change, testing steps, and needed screenshots.
     ```

   - **Success Criteria:** You get a concise title (e.g. “feat: add high-score leaderboard”) plus a structured description covering what was added, how to test, and where to see the UI.

4. **Configure IDE Settings with `@vscode`**

   - **Objective:** Enable the Prettier extension and set it to format on save for JavaScript files.

   - **Prompt to Use:**

     ```
     @vscode Show me the settings.json entries to enable Prettier formatting on save for all .js and .jsx files.
     ```

   - **Success Criteria:** You receive a `settings.json` snippet with `"editor.formatOnSave": true` and the appropriate `[javascript]` or `[javascriptreact]` scope tied to Prettier as the default formatter.

5. **Plan Deployment with `@azure`** (optional if you have an Azure subscription)

   - **Objective:** Scaffold an Azure Static Web App workflow for hosting your Snake game.

   - **Prompt to Use:**

     ```
     @azure Generate an Azure Static Web Apps GitHub Actions workflow yaml to build and deploy the Snake game from main branch.
     ```

   - **Success Criteria:** The agent returns a `.github/workflows/azure-static-web-apps.yml` file that checks out code, installs dependencies, builds the project, and deploys to an Azure Static Web App.

------

**Discussions:** 

- How accurately the agent understood the request
- Any tweaks needed to get a perfect result
- Which agent were most or least helpful—and why

## “#” Context-and-tool commands

Here’s a summary of the most useful “#” context-and-tool commands you can invoke in Copilot Chat:

- **`#changes`**
   Injects the diff of all files you’ve modified (but not yet committed) into your prompt.
   *Example:*

  ```
  Summarize the #changes in my workspace
  ```

- **`#codebase`**
   Tells Copilot to automatically search your entire project for the most relevant files and include them as context.
   *Example:*

  ```
  Optimize the path-finding algorithm using #codebase
  ```

- **`#fetch`**
   Adds the “Fetch Web Page” tool so Copilot can pull in content from any public URL.
   *Example:*

  ```
  #fetch https://example.com/snake-game-spec  
  Generate the game initialization code based on this spec.
  ```

- **`#githubRepo`**
   Performs a code search on a remote GitHub repository you specify.
   *Example:*

  ```
  What test helpers exist in #githubRepo microsoft/vscode-docs?
  ```

- **`#terminalLastCommand`**
   Attaches the output of the last run in your integrated terminal to the prompt.
   *Example:*

  ```
  #terminalLastCommand  
  Why is my build failing?
  ```

- **`#testFailure`**
   Pulls in the details of your most recent test-run failure.
   *Example:*

  ```
  #testFailure  
  Suggest a fix for this Jest error.
  ```

------

**How to use them:**

1. Type `#` in the Copilot Chat input box and select the desired command from the picker.

2. For those that take arguments (like `#fetch` or `#githubRepo`), follow the `#command` with the URL or repo path.

3. Combine multiple context tools in a single prompt for ultra-precise requests—for example:

   ```text
   Using #changes and #codebase, refactor the collision logic in updateSnake()
   ```

Leveraging these “hash” commands lets Copilot ground its answers in exactly the bits of code, diffs, web docs, or test output you need—no manual copy-and-paste required.

More info: https://code.visualstudio.com/docs/copilot/chat/copilot-chat-context 

## Slash Commands 

Slash commands let you invoke common Copilot Chat actions instantly, without crafting a full natural-language prompt. Just type `/` in the chat input and pick a command. Available commands vary by environment (VS Code, Visual Studio, GitHub web), but many are consistent across platforms.

### Common Slash Commands (VS Code)

- **`/clear`**
   Start a fresh chat session, discarding prior context.
- **`/explain`**
   Explain how the code in your active editor works.
- **`/fix`**
   Propose fixes for problems in the selected code.
- **`/fixTestFailure`**
   Find and fix a failing test in your most recent run.
- **`/tests`**
   Generate unit tests for the selected code.
- **`/help`**
   Show a quick reference for Copilot Chat usage.
- **`/new`**
   Create a new project scaffold from scratch.

*(To see all available commands, type `/` in your chat box and browse the menu.)* ([GitHub Docs](https://docs.github.com/en/copilot/using-github-copilot/copilot-chat/github-copilot-chat-cheat-sheet))

------

## Hands-On Exercises

1. **Inspect Movement Logic with `/explain`**
   - Open your `updateSnake` function in the editor.
   - Type `/explain` and send.
   - **Goal:** Read the AI’s explanation and identify any gaps or misunderstandings in the description.
2. **Auto-Fix a Boundary Bug with `/fix`**
   - Introduce a deliberate error in a function in your game, such as for the boundary logic (e.g. off-by-one check).
   - Select the broken code, then type `/fix`.
   - **Goal:** Evaluate whether Copilot corrects the boundary logic without additional guidance.
3. **Generate Tests for Food Placement with `/tests`**
   - Highlight your `placeFood` implementation.
   - Type `/tests using Jest` and send.
   - **Goal:** Confirm Copilot produces at least three meaningful test cases covering normal, edge, and collision-avoidance scenarios.
4. **Document Your Game with `/help` and `/test`**
   - Use `/help` to discover commands you haven’t tried yet.
   - Then select a code snippet (e.g. your rendering loop) and try `/tests` or `/fix` based on what you learn.
   - **Goal:** Practice exploring the command set and applying different ones to the same snippet.
5. **Start a New Mini-Project with `/new`**
   - Type `/new JavaScript snake tutorial` in a blank chat.
   - **Goal:** Observe how Copilot bootstraps a simple Snake project scaffold—files, dependencies, and basic logic.

------

By practicing these exercises, you’ll build fluency with slash commands—quickly toggling between code exploration, debugging, testing, and scaffolding without ever leaving the chat interface.