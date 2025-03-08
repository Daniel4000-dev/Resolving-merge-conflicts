## Resolving Merge Conflicts
### Create and Clone a New Repository
- Create a new repository
- Clone repository on local machine
```bash
git clone https://github.com/Daniel4000-dev/Resolving-merge-conflicts.git
```

### Create `edit-text` Branch and Modify a file

```bash
echo "Line from edit-text branch" >> conflict.txt
git add conflict.txt
git commit -m "Add line from edit-text branch"
```

### Switch to `main` and modify same file
```bash
git checkout main
echo "Line from main branch" >> conflict.txt
git add conflict.txt
git commit -m "Add line from main branch"
```

### Merge `edit-text` into main
```bash
git merge edit-text
```

### Resolved the conflict
- Opened conflict.tsx and resolved conflicts manually
```txt
<<<<<<< main
Line from main branch
=======
Line from edit-text branch
>>>>>>> edit-text
```
- Edited to
```text
Both lines are merged successfully.
```
### Commit and Push the Resolved Version
```bash
git add conflict.txt
git commit -m "Resolve merge conflict"
git push origin main
```