# How to deploy the project (on GitHub pages)

## Method : 

1. Open github and create a repo. (No need to add readme or license at this moment)

2. Run the commands that are showing on the screen to your git command line.
     - `git init`
     - `git add .`
     - `git commit -m "first commit"`
     - `git remote add origin https://github.com//example.git`
     - `git push -u origin main`
  
   Now we should be able to see our code in the github repository.

## Start Deplyoing

This is how your website will look: (your_github_name.github.io/repo_name)

1. We have to change our Vite config! : Update `vite.config.js` base property to match the name of the repository. For example, `base: "/your_portfolio"`

2. Open your git terminal:
   - `npm run build`
   - `git add dist -f` (We need -f because, Vite's default .gitignore, ignores /dist, but we need this 
      folder, so we need to to overwrite that)
   - `git commit -m "adding dist"`
   - `git subtree push --prefix dist origin gh-pages` (This creates gh-pages a subtree of our master branch)

Now we can see gh-pages branch in your github repository.

3. Go to setting of that repo > go to pages > you can see the URL there.

