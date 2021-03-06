# Rails Programming Task

### Please complete the following task.
*Note: This task should take no longer than 1-2 hours at the most to complete.*


### Prerequisites

- Please note that this will require that you have basic [Ruby on Rails](http://rubyonrails.org/) and [RSpec](https://github.com/rspec/rspec-rails) knowledge.

- You will need to have [Ruby on Rails 4](https://www.tutorialspoint.com/ruby-on-rails/rails-installation.htm) installed to complete this task.

*Important: We require that the application uses Rails 4.2.4 and Ruby 2.2.3.*

As part of your setup, you should add the following to your Gemfile:

```ruby
...
ruby '2.2.3'
gem 'rails', '4.2.4'
...
```
*Note: This requires that you have installed ruby 2.2.3 and Rails 4.2.4 before bundle install will work.*

## Task

- Fork this repository.
- Create a *source* directory.
- In the *source* directory, scaffold a simple Rails 4 web app that models `complaints`. JSON data structure below:

```
  {
    "id": 9923,
    "created": 1389618241,
    "user_email": "jake@bluesbrothers.com",
    "content": "I would like to report Joe, for what he did."
  }
```

    *Note: Content may contain between 1 and 4 paragraphs of text in a real use case.*

It is important to us that our users have the best possible support. For this reason, we need an email address and some content for every single complaint. Under no circumstances do we want to have empty complaints or complaints without an email address for us to use.

##### Create a form to submit complaints:

- This should be on its own view (most likely `GET /complaints/new` route).
- Include the following fields:
  - Email address
  - Complaint (*content text box*)
- The form should be functional. You should be able to submit complaints via this form (most likely `POST /complaints` route).
- Use Bootstrap to style this page.

##### Create a dashboard to review the complaints:

- This should be on its own view (most likely `GET /complaints` route).
- Complaints should be displayed in a list with the following information for each item:
  - Email address
  - Complaint (*content text box*)
- Use Bootstrap to style this page.


##### Seed 10 complaints into the system:

    5 should have the same email address.

    5 should have content that is at least 1000 characters long. (Lorem Ipsum works fine)

    5 should have content that is at most 100 characters long. (Lorem Ipsum works fine)

    No complaint should have content that is at most 3000 characters long. (Lorem Ipsum works fine)

### Tests

Create the following tests:

*Constraint: Use RSpec for creating the following tests.*

  1. `Submission form`:
      1. Verify that the form is on screen.
  2. `Complaints dashboard`:
      1. Verify that there are 10 complaints in total.
      2. Verify that 5 complaints have the same address.
  3. Create 1 short test of your own. The question you should ask yourself is, "what would I test for if I was building this application and the client did not specify any particular tests for me to write?" You may be asked questions about the test you created via a Github pull request review.

## Git commit structure

For your submission to be reviewed as quickly as possible, we ask that you commit your code in 4 to 5 steps.

1. `New Rails application`: Once you generate a new rails application, please create a commit that only creates the standard Rails Application files.
2. `Scaffolds and setup`: Your second commit should contain all of the code generated by using scaffolds and any changes you have made to the standard Rails Application files to get the application started. This includes: modifications to the Gemfile, secrets.yml, database.yml, and schema.rb.
3. `Rspec tests`: Please make sure to write your Rspec tests in their own independent commit.
4. `Project logic`: For this commit you will add all of the logic related changes to your application. This is where you would fill out your controllers, models, views, stylesheets, javascript files, routes, initializers, and seed files.
5. `Cleaning up tests`: After committing your logic, you might need to make a few slight changes to your Rspec tests to better test the logic you've created.

    *Note 1: Our team uses the above development process (TDD) internally.*
    *Note 2: Please use the above labels in your commit messages for clearer documentation.*

## Once Complete
1. Commit and Push your code to your new repository.
2. Send us a pull request, we will review your code and get back to you.
      1. Please add screenshot images of the two views we requested to your pull request.
