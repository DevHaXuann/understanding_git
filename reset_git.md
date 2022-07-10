## Git reset.
1. Git reset HEAD~N (số commit muốn reset N).
    ```
        git reset HEAD~N
   ```
2. Git rest HEAD -- <file> (trở về trạng thái chưa commit với file đó).
   ```
      git reset HEAD -- <file>
   ```
3. Git reset --soft (trở về trạng thái staging area).
   ```
      git reset --soft <id commit>
   ```
4. Git reset --mixed (trở về trạng thái working directory).
   ```
      git reset --mixed <id commit>
   ```
5. Git reset --hard (xóa luôn những thay đổi (roll back)).
   ```
      git reset --hard <id commit>   
   ```