## Sinatra versus Rails Exploration

### Setup:

First, clone down the Rails project:

```terminal
git clone https://github.com/turingschool/job-tracker.git rails_project
```

And then clone down the Sinatra project:

```terminal
git clone https://github.com/turingschool/bike-share.git sinatra_project
```
Now cd into each project, run `bundle` on each project, and you're ready to go. We will only be looking at the code base and not interacting with the app. If you wanted to run the server and interact with the app, you would need to create your database, migrate your migrations, etc.

### Exercise:

1. Take a look at this stripped down Sinatra app and this stripped down Rails app. How are they different and how are they similar? Identify 5 differences, and for each one describe 1-2 implications. What effect does that difference have for each framework? If you don't know exactly, draw on your knowledge and experience and make some educated guesses/inferences. Also, practice your research skills to look into the differences.

1. rails_helper.rb file
> It looks like the rails_helper.rb file pulls the environment setting logic out of the spec_helper file. The file will not run if the environment is in production mode. The file requires spec_helper so they must work in accordance with each other.

2. vendor folder
> The vendor has two subfolders for javascripts and stylesheets. The vendor folder must hold and organize all external js and css files.

3. multiple controllers
> This rails project has three controller files. This must allow rails apps to scale in size much larger than Sinatra apps.

4. different environment files in config
> Each environment(dev, prod, test) have their own files. This probably helps keep functionality of different environments more organized

5. bin folder
> Looks like the bin folder runs all the gems when bundle install is called

1. Consulting blogs and commentary you find online, identify 3 similarities between Rails and Sinatra.
> Both built for the Ruby language
> Both use ActiveRecord
> Both follow MVC convention

1. Consulting blogs and commentary you find online, identify 3 things that distinguish Rails, advantages.
> Rails is better for larger applications with more endpoint. A general range for a using. Sinatra is if the app has 5-10 endpoints where as a rails app will have 15-20 end points.
> Rails has a better community following and more documentation online. Rails includes ActionView/ActionPack which works all the magic.

1. In your Rails project, what does the `routes.rb` file inside of the `/config` directory do? What does this correlate to in our Sinatra app?
> The routes.rb file corresponds to the paths we defined in our controller in Sinatra.

1. We teach Sinatra by adding some structures that Sinatra doesn’t need, but help you make the transition between Sinatra and Rails. What does a stripped down implementation of Sinatra look like, and what are the pieces we’ve added for educational purposes?
>The MVC folder structure isn't necessary in a Sinatra application. Using this structure helps us organize many files and gets us accustomed to how rails is going to organize files.
