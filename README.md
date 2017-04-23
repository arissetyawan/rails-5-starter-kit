# Quickly get a new Rails 5 up and running on Heroku

Including some options I enjoy. Adjust to suit your needs.

- Slim
- Bootstrap
- Sidekiq

## Instructions

Navigate to the location of your new project.

`cd ~/projects/new-project`

Copy the repo from Github to your local directory.

`git clone https://github.com/ryanstrickler/rails-5-starter-kit.git`

Rename the application folder.

`mv rails-5-starter-kit new-project`

Navigate into the new project folder.

`cd new-project`

Remove the old git information.

`rm -rf .git`

Start a fresh git repository.

    git init
    git add .
    git commit -m 'Initial commit'

Install the necessary gems.

`bundle install`

Run with foreman.

`foreman start`

### Optional

Create a new repository on Github.

[https://help.github.com/articles/create-a-repo/](https://help.github.com/articles/create-a-repo/)

Add a remote that points to Github and push your new repo.

    git remote add github https://github.com/<user>/<repo>.git
    git push -u github master

Add a new app on Heroku.

    heroku apps:create <new-project>
    git push heroku

Add redis to Heroku.

    heroku addons:create heroku-redis

Add a worker to Heroku.

    heroku ps:scale worker=1

### Start making something awesome. 🎉
