# Game Icons [![Gem Version](https://badge.fury.io/rb/game_icons.svg)](https://rubygems.org/gems/game_icons) [![Build Status](https://travis-ci.org/andymeneely/game_icons.svg?branch=master)](https://travis-ci.org/andymeneely/game_icons) [![Dependency Status](https://gemnasium.com/andymeneely/game_icons.svg)](https://gemnasium.com/andymeneely/game_icons) [![Coverage Status](https://coveralls.io/repos/andymeneely/game_icons/badge.svg)](https://coveralls.io/r/andymeneely/game_icons) [![Inline docs](http://inch-ci.org/github/andymeneely/game_icons.png?branch=master)](http://inch-ci.org/github/andymeneely/game_icons)

RubyGem access to the SVGs on [game-icons.net](http://game-icons.net), an awesome library of free icons.

## Installation

Add this line to your application's Gemfile:

```ruby
gem 'game_icons'
```

And then execute:

    $ bundle

Or install it yourself as:

    $ gem install game_icons

## Usage

```ruby
require 'game_icons'

GameIcons.get('glass-heart').file     # absolute path to glass-heart.svg, black-on-white
GameIcons.get('glass-heart.svg').file # .svg extension allowed too
GameIcons.get(:flame).file            # symbols work too
GameIcons.get('glass-heart').string   # the SVG string
GameIcons.get('glass-heart').string   # the SVG string
GameIcons.get('glass-heart').recolor(fg: '333', bg: 'ccc').string # Recolor the foreground and background to different shades of gray
```

## Working With Squib

[Squib](http://andymeneely.github.io/squib) is my other pet project. Here's some example usage:

```ruby
require 'game_icons' # Be sure to also put this in your Gemfile and run "bundle install"
svg file: GameIcons.get('glass-heart').file
svg data: GameIcons.get('glass-heart').recolor(fg: '333', bg: 'ccc').string
```
Recoloring for Squib support is [coming soon](https://github.com/andymeneely/squib/issues/65)...

## We Are Not Game-Icons.net

This is not affiliated with [game-icons.net](http://game-icons.net). They are awesome, talented artists who give away their hard work. I'm not them.

That said, the Ruby code surroudning this Gem is MIT licensed. The icons themselves are under a [CC BY 3.0](https://creativecommons.org/licenses/by/3.0/). Be sure to attribute them in your work.

## Contributing

1. Fork it ( https://github.com/[my-github-username]/game_icons/fork )
2. Create your feature branch (`git checkout -b my-new-feature`)
3. Commit your changes (`git commit -am 'Add some feature'`)
4. Push to the branch (`git push origin my-new-feature`)
5. Create a new Pull Request
