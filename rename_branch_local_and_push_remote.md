Đổi tên 1 branch local và push lại lên remote.
[Link search](https://stackoverflow.com/questions/30590083/how-do-i-rename-both-a-git-local-and-remote-branch-name/30590238#30590238)

- Step 1: Đổi tên branch local thành branch mới.
    ```
        git branch -m <new name>
    ```
  ===
    ```
        git branch -m <old name> <new name>
  ```
- Step 2: Xóa branch cũ trên remote.
    ```
    git push origin :<old name>
  ```
  ===
    ```
    git push origin -d <old name>
  ```
- Step 3: Ngăn git sử dụng tên cũ. Nếu không code vẫn sẽ push lên branh cũ thay vì branch mới.
    ```
    git branch --unset-upstream <new name>
  ```
- Step 4. Đẩy branch mới lên remote
    ```
    git push origin <new name>
  ```