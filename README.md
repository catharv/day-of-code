# Day of Code

## WEEEE WOOO

This project is meant to provide a setup that can be used to build a Ruby on Rails application from scratch using GitHub Codespaces.
This is being used to organise Day of Code, an event based on tutorials provided by Rails Girls.

## Day of Code Instructions
### Step 1: Fork this repository
Forking means creating a personal copy of someone else’s project.
You can do that by selecting **Fork** on the top-right of the current repository page. 
It’s OK to leave all the default settings for the fork and you could enter an optional description if you would like to reference back to this project later on.

### Step 2: Run the codespace
Navigate to `Code > Codespaces` in the upper right and click `Create codespace on main`. 
A Codespace is a convenient development environment hosted in the cloud that you can use from your browser without the need to install anything (like the Ruby language, Rails framework or any coding editors) on your computer.

### Step 3: Chat with your coach
While you wait for your codespace to be ready your coach will explain the processes that are going on and how your environment is being set up.
This setup will take a bit over five minutes, so grab a cup of tea!

### Step 4: You’re ready to go
Congratulations, you’re up and running! You will see your own copy of Visual Studio Code (VS Code) which is an IDE (Integrated Development Environment) where you can write and run code.

Ask your coach to explain what the different components of VS Code are: the editor, project navigation, the Terminal.

Now you're ready to move on to the next step in the Day of Code Guides!

### A note for when you run your Rails server for the first time
This will become important after you've completed the first few steps in the Rails Girls guides and created your app with `rails new` - 
the official Rails Girls guides assume that you are installing and running Ruby and Rails locally on your computer.

This has been skipped with the current setup, so before you run `rails server` for the first time you will need to add one small bit of configuration to allow web requests to the non-local codespace:

```
# Insert the following code at the bottom of config/environments/development.rb, before the final `end`

config.hosts << "<codespace_subdomain>-3000.preview.app.github.dev"
```
Where `<codespace_subdomain>` is the first part of your codespace URL. Check the browser's address bar to find it, it will look like this:
```
https://<codespace_subdomain>.github.dev
```

Note that `https://<codespace_subdomain>-3000.preview.app.github.dev` will be the host URL we will use in this workshop, and not `http://localhost:3000 ` as indicated in the Rails Girls instructions.
### Find out more
- [Forking a repository explained](https://docs.github.com/en/get-started/quickstart/fork-a-repo)
- [GitHub codespaces overview](https://docs.github.com/en/codespaces/overview)