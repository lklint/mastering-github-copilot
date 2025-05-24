### Finding and Fixing Bugs with GitHub Copilot

#### 1. Identify Bug Symptoms:
   - Begin by identifying any symptoms or unexpected behavior in the snake game, such as incorrect word placements, grid rendering issues, or game crashes. If you have made the perfect game, get your colleague next to you to introduce a couple of bugs. Make them subtle 😏
   - Pay attention to user-reported issues, error messages, or anomalies observed during gameplay.

#### 2. Reproduce the Bug:
   - Attempt to reproduce the bug consistently by following specific steps or interactions within the game.
   - Record the steps taken to trigger the bug and note any patterns or conditions that may contribute to its occurrence.

#### 3. Analyse Code Surrounding the Bug:
   - Navigate to the relevant sections of the codebase where the bug may be originating.
   - Review the code surrounding the suspected bug area, paying attention to logic flow, variable assignments, and function calls.

#### 4. Use Copilot for Debugging Suggestions:
   - Write natural language comments describing the bug symptoms and the expected behaviour. Use Copilot chat to tell it what the issue is.
   - Trigger Copilot suggestions by writing code snippets or descriptions related to the bug.
   - Copilot may provide suggestions for debugging techniques, error handling strategies, or code modifications to address the bug.
   - Use the tools provided by the Copilot extension, such as quick fixes.

#### 5. Review and Customize Copilot Suggestions:
   - Review the debugging suggestions provided by Copilot and evaluate their relevance to the bug at hand.
   - Customize and refine the suggestions as needed to align with your understanding of the bug and your debugging approach.
   - Consider incorporating Copilot's suggestions into your debugging process to streamline the bug-fixing effort.

#### 6. Test the Fix:
   - Implement the suggested fixes or modifications in the codebase to address the bug.
   - Test the fixed functionality within the snake game to verify that the bug has been resolved.
   - Validate the fix across different scenarios and edge cases to ensure its effectiveness and stability.

#### 7. Test Regression:
   - Test for regressions by verifying that the bug fix does not introduce new issues or unintended side effects.
   - Conduct thorough testing across different parts of the game to ensure that the fix remains stable and does not impact existing functionality.

#### 8. Commit Changes:
   - Commit the bug fix to version control with a meaningful commit message that describes the issue addressed and the actions taken to resolve it.
   - Include any relevant references or documentation related to the bug fix to provide context for future developers.

#### 9. Using GitHub `/fix`

1. Highlight any part of your code that you believe is buggy.
   - Press `Ctrl + i` on a Windows machine, or `Option + i` on a Mac to open Copilot chat inline.
   - Type `/fix` which will ask Copilot to fix the highlighted chunk.
2. Review the suggestion and refresh the output or edit it. 

By following these practical instructions and leveraging GitHub Copilot's assistance, you can effectively find and fix bugs in the snake game, ensuring a smoother and more enjoyable gameplay experience for users.