# The Fire Works

Site built with [Middleman] and the [foundation5-basic] template.

  [Middleman]: https://middlemanapp.com/
  [foundation5-basic]: https://github.com/RalphAtHamburg/middleman-foundation5-basic

# Run it locally

Clone the source code, install Ruby. You might already have it&mdash;check with `ruby -v`. On new versions of OSX, it should say that you have version 2.0.0. That'll do. Once you verify you have it:

    bundle install
    middleman

That'll start middleman in development mode, and tell you that you can visit it at `localhost:4567`.

# Deploying

## To Github (as a pre-screen)

To deploy, you need to have the main repo set up as your `origin` remote on Github. You'll need to be a collaborator.

Assuming you have that out of the way, all you need to do is

    middleman deploy

## To AWS (the real deal)

The `middleman deploy` command automatically runs `middleman build` before pushing to the `gh-pages` branch on Github. But if you don't run it, you'll need to make sure you run `middleman build` yourself before kicking off a deploy to AWS. The rest of this will just push the built files from the `.build` directory up to an S3 bucket fronted by a Cloudfront distribution.

You'll need these gems:

    gem install aws mime-types simple-cloudfront-invalidator

You'll also need my S3 credentials in a config.yml file. Which I won't give
you, probably! I guess these are just my notes. :wink:

Run `rake -T` to see the available rake commands. Check the Rakefile to see
what they do (or, read [this excellent article] that I stole it all from.)

  [this excellent article]: http://spin.atomicobject.com/2013/09/23/deploy-aws-s3-rake/

Once it's deployed fo reals, [check it out on the open
internet](http://thefireworks.works) to make sure it works! Woo!
