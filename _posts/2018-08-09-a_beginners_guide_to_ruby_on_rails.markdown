---
layout: post
title:      "A Beginner's Guide to Ruby on Rails"
date:       2018-08-09 19:39:56 -0400
permalink:  a_beginners_guide_to_ruby_on_rails
---


<img src="https://www.onlinebooksreview.com/uploads/blog_images/2017/08/20_rails_5.png" alt="rails" width="300px"/> 


The Rails framework, DHH's beloved brainchild, is expansive. The thought that went into creating it is simply baffling. With a healthy introduction to the framework under my belt I decided to create this reference guide to help me, and hopefully others who have a basic Rails understanding, further grasp and navigate the powerful Rails framework. [Learn.co's](http://learn.co/) incredible curriculum was a great resource when putting this together.

<br>
### What is Rails?

1. **A Framework** - Rails is a web development framework that provides standardized tools and protocols to help developers build web applications quickly and effectively. 
2. **A Ruby Gem** - You can implement the Rails framework by simply downloading the codebase, packaged as a Ruby Gem.
3. **MVC Oriented** - Rails honors the popular application architecture of Model-View-Controller, separating the concerns of logic, application flow, and displaying content. 

<br>
### The Rails File System

* **app** – Contains the models, views, and controllers, along with the the rest of the core functionality of the application. This is where developers will spend most of their time.

* **bin** – Contains built in Rails tasks that will largely be untouched, but enable some of Rails' "magic".

* **config** – Manages settings that control the default behavior of your application, including: the environment settings, a set of modules that are initialized when the application starts, the ability to set language values, the application settings, the database settings, the application routes, and lastly the secret key base.
 
* **db** – Contains important files related to the database, including the schema, migrations and seed file.
 
* **lib** – You can complete a project without touching this folder, but it can be helpful as the home of custom rake tasks to help developers automate certain processes. 

* **log** – Houses the application's logs, which help developers debug, but it is recommend to employ a third party service to take advantage of more advanced logging services. 

* **public** – this directory contains some of the custom error pages, such as 404 errors, along with the robots.txt file which will let developers control how search engines index the application on the web.
 
* **test** – The home of all of specs, factories, test helpers, and test configuration files.
 
* **tmp** – Stores temporary items and is rarely accessed by developers.
 
* **vendor** – This directory has been utilized for varying purposes in the past. In Rails 4+, its main purpose is for integrating client-side MVC frameworks, such as AngularJS.
 
* **Gemfile** – the Gemfile contains all of the gems that are included in the application; this is where you will place outside libraries that are utilized in the application.
 
* **Gemfile.lock** – This file displays all of the dependencies that each of the Gems contain and should not be edited.
 
* **README.rdoc** – Assuming an open-source project, this is where developers place instructions to other developers, such as how to get the app up and running locally.

<br>
### The Rails Request Flow

<img src="https://s3.amazonaws.com/flatiron-bucket/readme-lessons/mvc_flow_updated.png" alt="rails" width="600px"/> Credit: [Learn.co](http://learn.co/) 


<br>
### Rails Routing - Static vs. Dynamic

Routes, established in `config/routes.rb`, come in two forms:
1. **Static Route** - Renders a view that will not change based on User or inputs. (i.e. 'About', 'Contact')

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Typical Format: `the http verb 'the URL path', to: 'controller#action'`
<br>
<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Example: `get 'about', to: 'static#about'`
<br>
2. **Dynamic Route** - Renders different data based on params that are communicated through the route and interpreted by the controller before rendering a view. Dynamic Routes allow developers to create custom routes for, say, every blog post in their application, without hardcoding a route for each one.

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Typical Format: `the http verb 'the URL path/**param**', to: 'controller#action'`
<br>
<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Example: `get 'posts/:id', to: 'posts#show'`

<br>
### Rails + Active Record

[Active Record](https://guides.rubyonrails.org/active_record_basics.html) is an Object Relational Mapping system that allows developers to reference and pull from the database more easily. 
<br>
<br>
What does that mean?
<br>
<br>
Active Record is the Rails built-in ORM that helps developers make abstract SQL queries on their models. This functionality allows developers to use methods such as `.all`, `.last`, and `.create!` without coding SQL manually.

<br>
### Overwhelmed by the above information? Time for some REST.

**REST** stands for REpresentational State Transfer. But, that isn't important.
<br>
What is important is the implementation of REST. 'RESTful' conventions look like this:

| Method | Action | Description |
| ----------- | ----------- | ----------- |
| GET     | /newsletters      | Show all newsletters     |
| POST     | /newsletters    | 	Create a new newsletter   |
| GET     | /newsletters/new      | Render the form for creating a new newsletter     |
| GET     | /newsletters/:id/edit    | Render the form for editing a newsletter   |
| GET     | /newsletters/:id      | Show a single newsletter     |
| PATCH     | /newsletters/:id    | Update a newsletter   |
| DELETE     | 	/newsletters/:id    | Delete a newsletter   |


Using these standard, 'RESTful' paths results in a more organized web application that plays more nicely with other applications through APIs and other methods. Rails was built with REST in mind, so it will more easily allow developers to follow these conventions. Below is a final REST-related visual:

<img src="https://curriculum-content.s3.amazonaws.com/web-development/rails-intro-to-rest/rails_routes.png" alt="rails" width="600px"/> Credit: [Learn.co](http://learn.co/) 

<br>
### A developer's journey is long and winding. Enter Route Helpers.

In Sinatra, a lot of Controller actions end with a redirect to a dynamic path that looks like this:
<br>
<br>
`/posts/#{@post.id}`
<br>
<br>
**Route Helpers** allow developers to simplify this path and offer a more elegant, non-hardcoded path:
<br>
<br>
`post_path(@post)`
<br>
<br>
The main benefits of Route Helpers are:
1. Readability
2. More Dynamic
3. Direct HTML-friendly translation

Below is a full Route Helper utilizing a `link_to` tag to auto generate HTML:
<br>
```
link_to post.title, post_path(post)
```

### Rails Forms

There are two basic form types in Rails:

1. **form_tag** - A Rails helper method that helps developers easily generate more secure HTML forms. This tag is better for simpler forms.

```
<%= form_tag posts_path do %>
  <label>Post title:</label><br>
  <%= text_field_tag :'post[title]' %><br>
 
  <label>Post description:</label><br>
  <%= text_area_tag :'post[description]' %><br>
 
  <%= submit_tag "Submit Post" %>
<% end %>
```

The above results in the following HTML:

```
<form action="/posts" accept-charset="UTF-8" method="post"><input name="utf8" type="hidden" value="&#x2713;" /><input type="hidden" name="authenticity_token" value="vq9SMVNk0CjwgZmYomFRhwbo5dfu7tI/2FiR7jOtlVgbj8r/zOO5oL+arU9N4PMm7WqxbUbXg4wqneW02ZfpMw==" />
  <label>Post title:</label><br>
  <input type="text" name="post[title]" id="post_title" /><br>
 
  <label>Post description:</label><br>
  <textarea name="post[description]" id="post_description">
</textarea><br>
 
  <input type="submit" name="commit" value="Submit Post" />
</form>
```


2.**form_for** - The main differences between a form_tag and the more powerful form_for tag are below. Generally, this tag is better for directly interacting with a model and database.

<br>
* The form_for method accepts the instance of the model as an argument. Using this argument, form_for is able to make a bunch of assumptions for you.
* form_for yields an object of class FormBuilder
* form_for automatically knows the standard route (it follows RESTful conventions) for the form data as opposed to having to manually declare it
* form_for gives the option to dynamically change the submit button text (this comes in very handy when you're using a form partial and the new and edit pages will share the same form, but more on that in a later lesson)

```
<%= form_for(@post) do |f| %>
  <label>Post title:</label><br>
  <%= f.text_field :title %><br>
 
  <label>Post description</label><br>
  <%= f.text_area :description %><br>
 
  <%= f.submit %>
<% end %>
```
<br>
<br>
### Strong Params keep our code LEAN.

On a basic level, **Strong Params** tell our forms what data to require, accept, and reject. We can abstract the data, or params, into a private controller method we can use when Creating, and Updating an object. 

```
def create
  @post = Post.new(post_params)
  @post.save
  redirect_to post_path(@post)
end
 
def update
  @post = Post.find(params[:id])
  @post.update(post_params)
  redirect_to post_path(@post)
end
 
private
 
def post_params
  params.require(:post).permit(:title, :description)
end
```

<br>
### Rails Generators.

Developers use Rails Generators to quickly generate necessary files for new models, controllers, resources, or migrations. Developers should be tactical with generators and avoid generating too many extra files. A typical generator command can be seen below:
<br>
```
rails g <name of generator> <options> --no-test-framework
```
**Resource** is a helpful generator that doesn't cause to much "code-bloat" or unnecessary files. 
<br>
**Scaffolds** are to be avoided because the generator creates both front end and back end code for CRUD features. This can result in a lot of extraneous files that are unnecessary. 

<br>
### Validations. The bouncers of Rails.

**Validations** are methods contained in the model class that "protect" the database from bad data. They inhibit the ability to run `.save` if the instance is not valid.

A basic Validation and a few other Validating methods:

```
class Person < ActiveRecord::Base
  validates :name, presence: true
end
```

```
class Person < ActiveRecord::Base
  validates(:name, { :length => { :minimum => 2 } })
  validates(:bio, { :length => { :maximum => 500 } })
  validates(:password, { :length => { :in => 6..20 } })
  validates(:registration_number, { :length => { :is => 6 } })
end
```
<br>
### Rails Testing. Keeping ourselves in check. 

There are three types of Rails Tests:

1. **Models** (RSpec) - The easist to test. Model tests use the least amount of special features, since all you really need is the model class itself. The most common usage for model tests is to make sure you have set up your validations correctly.

Example:
```
  let(:missing_name) { attributes.except(:name) }
  let(:invalid_size) { attributes.merge(size: "not that big") }
  let(:missing_species) { attributes.merge(taxonomy: "Abradacus") }
 
  it "is invalid without a name" do
    expect(Monster.new(missing_name)).not_to be_valid
  end
 
  it "is invalid with an unusual size" do
    expect(Monster.new(invalid_size)).not_to be_valid
  end
 
  it "is invalid with a missing species" do
    expect(Monster.new(missing_species)).not_to be_valid
  end
```
<br>
<br>
2.**Controllers** (RSpec) - These tests  are great, especially while we're still getting used to how controllers are wired. However, almost these exact tests could be copied for any controller set up according to Rails' RESTish conventions.

```
# spec/controllers/monsters_controller_spec.rb
 
describe MonstersController, type: :controller do
  let(:attributes) do
    {
      name: "Dustwing",
      size: "tiny",
      taxonomy: "Abradacus nonexistus"
    }
  end
 
  it "renders the show template" do
    monster = Monster.create!(attributes)
    get :show, id: monster.id
    expect(response).to render_template(:show)
  end
 
  describe "creation" do
    before { post :create, monster: attributes }
    let(:monster) { Monster.find_by(name: "Dustwing") }
 
    it "creates a new monster" do
      expect(monster).to_not be_nil
    end
 
    it "redirects to the monster's show page" do
      expect(response).to redirect_to(monster_path(monster))
    end
  end
end
```
<br>
<br>

3.**Features** (RSpec/Capybara)

One example of a feature test would be: *"When the steering wheel is rotated to the left, the tires rotate to the left."*

This is called an acceptance test. We don't really care how it gets done, but the result is there. This is **too general**.

Another option is: *"When the steering column's flange rotates, the steering shaft transmits the rotation to the steering box."*

This is called a unit test. This is way too specific.

The best option is called a **feature test**. They let developers think like a user, but consider the functions underneath the hood: *"When the steering wheel is rotated to the left, the steering column transmits the rotation to the steering box."* Tests like these are achieved with Capybara.

<br>
### Layouts & Partials & Helpers in Rails. Keep it DRY.

**Layouts** allow developers to spend more time coding the unique parts of each view and skip over the repetitive bits (navigation, header etc.). A layout can be established for specific actions but generally it is called at the top of a controller: 

```
  class ShoppingCartController < ApplicationController
    layout "products"
  end
```

**Partials** allow developers to easily add common parts of a view. For example, developers can create a conditional form that can be inserted into multiple views, instead of repeating the form across different views. 

```
Information About the Post
<%= render partial: "authors/author", locals: {post_author: @author} %>
<%= @post.title %>
<%= @post.content %>
```

**Helpers** are methods located in the 'app/helpers' folder and associated with a controller. They provide devs with a great way to extract common presentation logic from multiple views. Its all about keeping the logic OUT of the views.
```
<% @posts.each do |post| %>
  <div>
    <%= post.title %> - <%= post.updated_at.strftime("Last updated %A, %b %e, at %l:%M %p") %>
  </div>
<% end %>
```
compared to:

```
<% @posts.each do |post| %>
  <div>
    <%= post.title %> - <%= last_updated post %>
  </div>
<% end %>
```
```
# app/helpers/posts_helper.rb
 
def last_updated(post)
  post.updated_at.strftime("Last updated %A, %b %e, at %l:%M %p")
end
```

-------------------------------------------------------------------------------------------------------

Whew. Thanks for sticking with me. This guide is just a start and I look forward to referencing it in the future. Maybe even adding to it as I learn new things. 

Until then, party on.






