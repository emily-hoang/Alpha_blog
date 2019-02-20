# README

Production Deploy - Text directions, references and code

Prepartion for heroku deploy:

- Remove sqlite3 gem from top of application to within group :development, :test do block

- Create a group production ->

group :production do

gem 'pg', '~> 0.11'

end

- Save Gemfile

- Run bundle install --without production to update Gemfile.lock file

- Commit your changes to git repo ->

git add -A

git commit -m "Make app production ready"

wget -qO- https://toolbelt.heroku.com/install-ubuntu.sh | sh

Check heroku:

heroku -v

heroku version

heroku # for list of common heroku commands

From your app directory:

To login to your heroku account from your env ->

heroku login

To add your SSH key to your heroku account so you don't have to use username and password everytime ->

heroku keys:add

To create a new production version of your app hosted in heroku ->

heroku create

To push your application code to heroku (deploy your app) ->

git push heroku master

Ensure you have committed all your local changes to your git repo prior to pushing to heroku by checking git status

To change the name of your application ->

heroku rename newnameofyourapp
