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

## To Github (as a pre-screen)

To deploy, you need to have the main repo set up as your `origin` remote on Github. You'll need to be a collaborator.

Assuming you have that out of the way, all you need to do is

    middleman deploy

## To AWS (the real deal)

You'll need these gems:

    gem install aws mime-types simple-cloudfront-invalidator

You'll also need my S3 credentials in a config.yml file. Which I won't give
you, probably! I guess these are just my notes. :wink:

Run `rake -T` to see the available rake commands. Check the Rakefile to see
what they do (or, read [this excellent article] that I stole it all from.)

  [this excellent article]: http://spin.atomicobject.com/2013/09/23/deploy-aws-s3-rake/

Once it's deployed fo reals, [check it out on the open
internet](http://thefireworks.works) to make sure it works! Woo!
