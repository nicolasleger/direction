# Direction

Enforce better encapsulation by returning self from commands.

Thanks to James Ladd for the inspiration.

## Usage

Provide a feature like the Forwardable library, but set the return value to self.

It provides a class level "command" method to do message forwarding.

```ruby
class SomeClass
  extend Direction

  command [:name, :id] => :collaborator, [:color, :type] => :partner
end
```

This will define methods on instances that forward to the provided receiver while enforcing encapsulation of the relationship between objects.


## Installation

Add this line to your application's Gemfile:

    gem 'direction'

And then execute:

    $ bundle

Or install it yourself as:

    $ gem install direction

## Contributing

1. Fork it ( http://github.com/saturnflyer/direction/fork )
2. Create your feature branch (`git checkout -b my-new-feature`)
3. Commit your changes (`git commit -am 'Add some feature'`)
4. Push to the branch (`git push origin my-new-feature`)
5. Create new Pull Request