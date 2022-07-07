## Branch Git
- Git branch base.
1. View all branch (trừ branch trên remote).
    ```
        git branch
    ```
2. View all branch (cả local và remote).
    ```
        git branch -a
    ```
    ===
    ```
        git branch -al
    ```
3. Create a new branch (không chuyển sang 1 branch đấy mà vẫn giữ ở current branch).
    ```
        git branch <name branch>
    ```
4. Create a new branch and switch branch.
    ```
        git checkout -b <name branch>
    ```
5. Switch to a branch.
    ```
        git checkout <name branch>
    ```
6. Rename branch to new branch.
    ```
        git branch -m <old name> <new name>
    ```
    ===
    ```
        git branch -m <new name>
    ```
7. Delete a branch local.
    ```
        git branch -d <name branch>
    ```
8. Delete a branch remote
    ```
        git push origin :<name branch>
    ```
    ===
    ```
        git push origin -d <name branch>
    ```
9. Delete all branch local <ngoại trừ master>
    ```
        git branch | grep -v "master" | xargs git branch -D
    ```
    ===
   ```
      git branch -D `git branch --merged | grep -v \* | xargs`
   ```
    ===
   ```
      git branch --merged | grep -v \* | xargs git branch -D 
   ```
    ===
   ```
      git for-each-ref --format '%(refname:short)' refs/heads | grep -v "master\|main" | xargs git branch -D
   ```
10. Delete all branch local <mà trong đó có cả những branch: master-product, master-test-, master-ui,...nhưng chỉ muốn giữ lại mỗi master thôi).
    ```
        git branch | grep -v "master$" | xargs git branch -D
    ```