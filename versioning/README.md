## **Versioning**
Versioning is a crucial aspect of any software development project, including deep learning. It helps in keeping track of changes, managing codebase evolution, and facilitating collaboration among team members. In this section, we'll discuss the importance of versioning and how to implement it effectively in your deep learning project, especially focusing on Git, a widely used version control system.

# **Versioning**

**Tracking Changes**: Deep learning projects involve multiple iterations and modifications to code, data, and model architectures. Versioning enables you to track these changes over time, providing a clear history of the project's evolution.

**Collaboration**: When working in a team, versioning allows team members to synchronize their work, merge changes seamlessly, and resolve conflicts efficiently. It promotes collaboration by providing a centralized repository for sharing and reviewing code.

**Reproducibility**: Versioning ensures reproducibility by preserving the state of the project at different stages. You can always revert to previous versions to reproduce results, debug issues, or experiment with alternative approaches.

# **Best Practices for Versioning**
**Descriptive Commit Messages**: Use clear and concise commit messages to describe the changes made in each commit. This helps in understanding the purpose of each change and facilitates collaboration.

**Frequent Commits**: Commit changes frequently in logical units, rather than making a large number of changes without committing. This ensures granular versioning and simplifies the process of reverting or reviewing changes.

**Documentation**: Document significant changes, decisions, and dependencies in a README.md file within your repository. This provides context for collaborators and helps newcomers understand the project structure and requirements.

# **Branching Strategy**
One of the strategies is to keep a "main" branch and many "develop" branch.
each developer works on his develop branch to new features for the global project. When something new on the develop branch is finished it is merged into the main branch.
The main branch has to remain clean, all the code in the main branch has to be commented and has to be tested, the main branch has to be a working version of the project.


## Quick start
- Clone project:
```sh
git clone <repository-url>
```

- Branch handling:
  - Create a New Branch:
  ```sh
  git checkout -b <branch-name>
  ```

  - Change branch if already created:
  ```sh
  git checkout -b <branch-name>
  ```

  - See all branches:
  ```sh
  git branch -a
  ```

- Commit:
  - Add changes to commit
  ```sh
  git add <file-path>
  ```

  - Commit changes:
  ```sh
  git commit -m "Implemented feature X"
  ```

- Push your branch: 
```sh
git push origin <branch-name>
```

- Delete a branch:
  - locally:
  ```sh
  git branch -d <branch-name>
  ```
  - on GitHub:
  ```sh
  git push origin --delete <branch-name>
  ```
## Official giude:
[https://git-scm.com/docs](https://git-scm.com/docs)
