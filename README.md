# COSC 1437: Programming Fundamentals II - Home Repository

Welcome to your personal "Home" repository for COSC 1437! This repository is the central hub for your development work this semester. All your assignments will be completed within the cloud-based development environment (a GitHub Codespace) that you launch from here.

This repository comes pre-configured with the Google Test framework, which will be used for automated grading on all assignments.

## 🚀 Your Development Environment: GitHub Codespaces

To ensure a consistent and professional development environment for everyone, we will use **GitHub Codespaces**. A Codespace is a complete, cloud-based version of VS Code that runs in your browser. You do not need to install a C++ compiler, CMake, or any other tools on your own computer.

To get started, simply click the green **"<> Code"** button on this repository's main page, select the "Codespaces" tab, and create your codespace.

---

## ⚙️ The Standard Assignment Workflow

Every assignment in this class, from debugging warm-ups to homework, follows the same professional workflow. Please refer to these steps for every assignment you work on.

### Step 1: Getting the Assignment

1.  **Accept the Assignment:** You will receive a GitHub Classroom link for each new assignment (e.g., `homework01`, `debug-warmup01`). Clicking this link will create a new, private repository for you (e.g., `homework01-yourusername`).

2.  **Clone into Your Codespace:** In your Home repository's Codespace terminal, make sure you are in the root directory (`/workspaces/YourName`). Clone the new assignment repository here.

    ```bash
    git clone https://github.com/your-org/homework01-yourusername.git
    ```

3.  **Add to Workspace:** To easily access the files, add the new assignment folder to your VS Code workspace by clicking **File > Add Folder to Workspace...** and selecting the new folder.

### Step 2: The Coding & Testing Loop

This is the core cycle you will follow as you write your code.

1.  **Create Issues:** For most assignments, you will need to create the required "features" from templates. Go to the **"Issues"** tab of the assignment repository and create a new issue from each of the provided templates.

2.  **Create a Feature Branch:** Before writing any code, select an issue to work on and create a branch for it. **Direct pushes to the `main` branch are disabled.** Your branch name should follow our naming convention:
    * `add/{feature-name}`: For adding a new feature.
    * `fix/{bug-name}`: For fixing a bug.
    * `update/{feature-name}`: For improving an existing feature.
    * `try/{idea-name}`: For experimenting.

    ```bash
    # Example for adding the feature in Issue #1
    git checkout -b add/1-count-vowels
    ```
3. **Make an initial change:** Add a comment on the file you are going to be working with, then add, commit, and push the change to establish the branch.

    ```bash
    git add <file>
    git commit
    git push origin add/1-count-vowels
    ```

4.  **Create a Pull Request:** Go to the assignment repository on GitHub. Follow the steps below to create a Pull Request:

    > **[📄 Read: The Life Cycle of a Pull Request](pull-request.md)**

5.  **Write Your Code:** Implement the required functionality in the `src/` and `include/` directories.

6.  **Build and Test:** To check your work against the provided unit tests, you must configure, build, and run the tests. From the **root of the assignment folder** (e.g., `homework01-yourusername`), run:

    ```bash
    # 1. Configure the build system (only needs to be run once)
    cmake -S . -B build

    # 2. Build the code
    cmake --build build

    # 3. Run the tests
    cd build
    ctest
    cd ..
    ```
    > **Pro Tip:** The "CMake Tools" extension in VS Code can automate this process with buttons in the status bar.

### Step 3: The Submission Process (Commits & Pull Requests)

1.  **Make Atomic Commits:** Once the tests for a specific feature pass, commit your work. It is a professional standard to make small, "atomic" commits for each distinct piece of functionality. **Do not use `git add .`**. Instead, add only the specific files you changed.

    ```bash
    # Stage only the specific file(s) you modified
    git add src/analyzer.cpp

    # Write a clear commit message that closes the corresponding issue
    git commit -m "add: Implement count_vowels function (closes #1)"
    ```

2.  **Push Your Branch:** Push your feature branch to GitHub.

    ```bash
    git push
    ```

3.  **Merge and Submit:** For individual assignments, you will merge your own Pull Request. This is the final step of submission. Once your branch is merged into `main`, that feature is considered complete.

4.  **Clean Up and Repeat:** Before starting the next feature, switch back to your `main` branch and pull the latest changes to ensure your local environment is up-to-date.

    ```bash
    git checkout main
    git pull
    ```
    Now you are ready to create a new branch for the next issue!
