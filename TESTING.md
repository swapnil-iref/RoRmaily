# Testing

## Preparations

Before you run the tests for the first time you need to load the test database with the empty structure:

```
RAILS_ENV=test rake db:setup
rspec
guard # execute specs interactively

```

This is useful command also in reseting the test DB to empty and clean state.

## Running tests

Run all the tests suites:

* run `rspec spec`

## Rails unit testing (RSpec)

In addition to running all the spec tests with rake spec you can also run a single file with for example `rspec ./spec/helpers/locations_helper_spec.rb` or even a single tests inside a file by pointing it with the line number: `rspec ./spec/helpers/locations_helper_spec.rb:23` That makes it faster to test a single feature that you are changing. However, it's good practice to run the whole test set before sending your code for other people to use (or to develop on).

### Guard

To speed up tests, you can use guard. It watches the file system and runs tests automatically when files change:

Run `guard` and start coding. Saving a file triggers the change.