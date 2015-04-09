# The Fire Works

Site built with [Middleman] and the [foundation5-basic] template.

  [Middleman]: https://middlemanapp.com/
  [foundation5-basic]: https://github.com/RalphAtHamburg/middleman-foundation5-basic

# Run it locally

Clone the source code, install Ruby, and then:

    bundle install
    middleman

That'll start middleman in development mode, and tell you that you can visit it at `localhost:4567`.

# Deploying

To deploy, you need to have the main repo set up as your `origin` remote on Github. You'll need to be a collaborator.

Assuming you have that out of the way, all you need to do is

    middleman deploy
