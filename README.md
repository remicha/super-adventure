# Super-adventure

Super-adventure is a project created to test out github features

## Features

* New files are created and committed
* New commits are tracked

## Rationale

Understand exactly how github works

##Playing with some formatting

Configure Redisse (e.g. in `config/initializers/redisse.rb`):

    require 'redisse'

    Redisse.channels do |env|
      %w[ global ]
    end

Use the endpoint in your main application (in config.ru or your router):

    # config.ru Rack
    map "/events" do
      run Redisse.redirect_endpoint
    end

    # config/routes.rb Rails
    get "/events" => Redisse.redirect_endpoint

Run the server:

    $ bundle exec redisse --stdout --verbos

## Next steps

Maybe create a cheat-sheet with all the commands seen so-far
