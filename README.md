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

#### Github

Create a new repository.

[https://help.github.com/articles/create-a-repo/](https://help.github.com/articles/create-a-repo/)

Add a new remote and push your new code.

    git remote add github https://github.com/<user>/<repo>.git
    git push -u github master

#### Heroku

Add a new app.

    heroku apps:create <new-project>
    git push heroku

Add redis.

    heroku addons:create heroku-redis

Add a worker.

    heroku ps:scale worker=1

### Start making something awesome. 🎉
