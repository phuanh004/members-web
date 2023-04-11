# members-web

Public website for CSE 135 project team

## Deploy

GitHub Actions is used to deploy changes to the droplet.
Whenever a new commit is pushed to GitHub, our workflow triggers and checks out the repository.
Then it removes the .git folder and copies it to our droplet via SCP.

We have a dedicated user account (github-actions) on the droplet which is part of the www-data group.
This group has write access to the /var/www directory, where the /root/public_html directory which our main site is hosted in resides.