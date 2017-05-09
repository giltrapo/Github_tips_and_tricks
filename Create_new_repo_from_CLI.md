### Create new repo from CLI
Imagine that you have just started a project...

1. You have created the folder where the project will be and you have started the repository.

```bash
mkdir project_folder
```

2. And you have added files to the project.
```bash
echo "This is the first line of my project" > first_file_project.txt
git add .
git commit -m "The first commit"
```

3. Now you are ready to make push... but where? Using the [Github API](https://developer.github.com/v3/repos/#create "Github's Developer site") you can create the repository from your terminal:

```bash
curl -u 'YOUR_USER' https://api.github.com/user/repos -d '{"name":"YOUR_REPO"}'
```

4. And finally you only have to add the remote repository that you have just created and push the project.

```bash
git remote add origin https://github.com/YOUR_USER/YOUR_REPO.git

# if you have a trusted ssh keypair with github you can use:
# git remote add origin git@github.com:YOUR_USER/YOUR_REPO.git

git push origin master
```
