Reading:
Chapter 1 - Section 1.1 on Bundler
Chapter 3 REST, Resources, andRails - Sections 3.1 - 3.6

Code:
Create new rails app
Add a ruby version and gemset to it
Add one page of static content
Create one Resource with Scaffolding
Put it on Github

# Questions:
## 1. What is the difference between Bundler and RVM?

RVM manages ruby versions. Bundler installs the gems you want for your project to work. With gemsets, RVM lets you isolate certain setups. When used with Bundler, you can automagically keep your gems for one project from mixing with the gems from other projects. Just rvm into your setup, then list the gems in the Gemfile and run bundler install.

## 2. What is REST and why is it useful?

It's been said that without REST, no one really knows where to put anything.

You need an endpoint for the resources (models) that your app consumes, particularly if you are using AJAX. REST will give you a guide for how to lay everything out. It typically works with HTTP verbs which, more or less, correspond to database actions.

## 3. What does CRUD stand for?  

Database verbs.

Create, Retrieve, Update, and Destroy

It is all you need, isn't it?

## 4. What does this line of code do, and what file in my rails app would it go in?

   resources :students, except: :destroy

   It sets up REST endpoints for the student model, so you can CRU, but not D, From the http endpoints.

   You can find it in config/routes.rb

## Project Description:

I'd like to do multiple projects.

A quick first project: I have some static content that teaches students how to install and use a podcatcher on their mobile phones. I want to add a small amount of dynamic content to customize it for different classes. It should be very easy to get it done quickly, and would be useful to me. Then I will move on to another project. The second project might be a soundcloud.com app for language learning.

## Link to code on Github:

This is for the week 1 homework: https://github.com/psytau/hello-rails

I'll put the app here when I start work on it. https://github.com/psytau/how-to-podcatch

