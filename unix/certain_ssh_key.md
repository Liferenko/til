### Using a specific SSH key when using Git command

Need to specify an ssh key for certain `git clone`?

Try:
```
ssh-agent bash -c "ssh-add ~/.ssh/mykeyhere; git clone ...."
```
