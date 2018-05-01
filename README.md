This is the repository of the Alpha Blog app of the Rails JavaScript Development course.

- This was built using Ruby on Rails

**Text- directions for the course**

Getting Started with Alpha Blog - Text Directions and Code
Section 1, Lecture 5

On the command line run

    git clone https://github.com/railsjavascriptcourse/alpha-blog.git

    cd alpha-blog/
    ruby -v
    gem install bundler
    bundle install
    rails -v
    bundle exec rails db:migrate
    bundle exec rails server
    git status

**Installing Webpacker and React - Text Directions and Code
Section 1, Lecture 7**

In the Gemfile  add

    #Adding webpacker for Javascript library management
    gem 'webpacker', '~> 3.3'

On the command line run

    bundle install
    bundle exec rails webpacker:install
    bundle exec rails server

**Quiz**


What you know

    React is a framework for ___________
    What is the name of the gem that lets us add front end dependencies in Rails applications?
    What is the name of the JavaScript class that all React components must extend?




**React-Rails and Pushing to GitHub - Text Directions and Code
Section 1, Lecture 9**

In the Gemfile  add

    #React gem for Rails
    gem 'react-rails'

On the command line run

    bundle install
    bundle exec rails generate react:install

    rails g react:component HelloWorld greeting:string

In app/views/layouts/application.html.erb  add

<%= javascript_pack_tag %>

right below

<%= javascript_pack_tag 'application' %>

and then inside the <body>  add

<%= react_component("HelloWorld", {greeting: "Hello"}) %>

On the command line run

bundle exec rails server

Change the react_component  call from before to

<%= react_component("HelloWorld", {greeting: "Hi"}) %>

On the command line run

    git status
    git diff
    git add .
    git status
    git commit -m "Adding react and webpacker to the blog app"

Create a git repository in GitHub

    git remote -v
    git remote set-url origin <your_github_repo_url>
    git remote -v
    git push




