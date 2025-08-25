# The Life Cycle of a Pull Request

In a professional development environment, a Pull Request (PR) is more than just a request to merge code. It is the central place for discussion, feedback, and collaboration on a specific feature or fix. In our class, you will follow a structured process for every PR you create.
## The First Principle: Small, Focused Changes
Your natural instinct might be to create one giant branch and build an entire assignment in it. Stop! It is crucial to break your work down into the smallest logical pieces (in our case, one function per issue). Each piece should become its own branch and its own Pull Request. Smaller changes are much easier to review, test, and merge.
## The Workflow
Once you have created an issue for the first small piece of your assignment, follow this process:
### 1. Create Your Branch
Create a new branch from `main` that follows our class naming conventions. The name should clearly communicate the intent of your changes.
- `add/{feature-name}`: For adding a brand new feature (e.g., `add/count-vowels`).
- `update/{feature-name}`: For iterating on or improving an existing feature.
- `fix/{bug-name}`: For fixing something that is broken (e.g., `fix/off-by-one-error`).
- `try/{idea-name}`: For experimenting with an idea you want feedback on (more common in the group project).
### 2. Create the Pull Request Immediately
As soon as you make your first commit, create the Pull Request on GitHub. Don't wait until you are finished.
- Go to your repository and click on the "Pull requests" menu (**Do not use the `Compare & pull request` option)
- Click on "New Pull Request" button
- Click on the "compare" drop down and select your branch, then "Create pull request"
- Use a Clear Title: The title should be descriptive (e.g., `Add count_vowels function`).
- Write a Detailed Description: The body of the PR should automatically link to the issue you are solving. Add a brief summary of the changes you are making.
- Mark as a Draft (Optional but Recommended): On GitHub, you can create a "Draft" Pull Request. This indicates that the PR is a work in progress and not yet ready for a final review, but it welcomes early feedback and shows what you are working on.
### 3. Develop and Push Commits
Now, continue working on your branch.
- Push Frequently: Push your commits often. This backs up your work and keeps the PR on GitHub up-to-date with your progress.
- Make Atomic Commits: As you work, continue to make small, logical commits for each distinct part of your solution.
### 4. Prepare for the "Final Review" (Self-Review)
When you believe your code is complete and solves the issue, perform a final check before merging.
- Do all tests pass? Make sure you've run `ctest` one last time and everything is green.
- Is your code clean? Have you removed any unnecessary comments or debugging print statements?
- Does your branch merge cleanly? GitHub will tell you if your PR can be merged without conflicts.
### 5. Merge Your Pull Request
Once you are confident in your solution:
- If your PR was a draft, click the "Ready for review" button.
- Click the "Merge pull request" button to merge your changes into the `main` branch.
- Delete your feature branch after the merge is complete.
You have now successfully completed the lifecycle for one feature. Return to your `main` branch, pull the latest changes, and start the process over for the next issue!