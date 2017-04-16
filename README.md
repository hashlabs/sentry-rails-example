# Sentry Rails custom exception context

This is an example application describing how you can send custom
context payloads for Exceptions in sentry-rails.

## Installation

You will need to have a `SENTRY_DSN` to receive events in Sentry. You
can signup for a free trial in their website (https://sentry.io)

1. `bundle install`
2. `env SENTRY_DSN=<your-sentry-dsn-here> rails s`
3. In your browser, go to **https://localhost:3000/errors**

## Files to look at

* [lib/exceptions/exceptions.rb](lib/exceptions/exceptions.rb) - Exceptions definitions
* [app/controllers/errors_controller.rb](app/controllers/errors_controller.rb) - Triggering an exception
* [config/application.rb](config/application.rb) - Adding `lib/exceptions` to autoload paths
