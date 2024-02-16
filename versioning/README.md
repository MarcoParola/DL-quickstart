# Versioning
Versioning is essential for tracking changes and facilitating collaboration in software development, providing a stable framework for managing project evolution and enabling easy reverting of modifications when needed.

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
