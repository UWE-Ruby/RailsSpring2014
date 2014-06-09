Reading:
Chapter 4 Working with Controllers: 4.3 - 4.7  (Skip the rack console exercise - unless you really want to do it)
Chapter 2 Routing: 2.1, 2.2, 2.4, 2.6, 2.7 

Code:
Setup a root route to a home or welcome controller
Have a link on your homepage to your scaffolded resource from last week
Have a link on your homepage that triggers a change on your homepage (wording change, expansion of text, change a color, etc...)
Create a view helper that will generate different content on your homepage based on a param value

#Questions:
##1. Why does a Rails app have routing? 

  It maps a route and a the parameters in a url to a controller and describes how the controller should interpret the url.

##2. How would you render the same view for two different controllers? (code example is fine)
You can use the render method to specifically set a view for the controller to render. For example:
    render "my_view"

##3. If you wanted to check a parameter before calling any controller action, what would you do? (code example is fine)
You could use the 'before_action' method to do any needed processing before the controller gets to work. For example:

```
class MyController < ApplicationController
    before_action :check_x_param

    def check_x_param
       logger.info 'x is not digit' if params['x'] =~ /^[0-9]+$/
    end
```

###Link to code on Github:
https://github.com/psytau/week2_rails
