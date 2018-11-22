# egg

*egg* is a flexible, universal, and beautiful CSS/SCSS framework. It was developed originally for building Web apps at [Wiredcraft](https://wiredcraft.com) (things like [devo.ps](http://devo.ps)).

**More on the official page: http://wiredcraft.github.io/egg/#about**.

## Mental Model

You're probaly asking yourself: what do we mean by a *flexible* css framework? *egg* is designed to be compatible with several workflows in mind. We don't care if you're using React, Vue, Jekyll, or whatever is the hottest compile-to-source bullshit framework the kool kids are using these days. As they say: *Every fool has his tool*. It's okay, we are here for you regardless of your choice of tooling.

The mental model of *egg* is to be compatible **and** extensible within your existing workflow/framework/platform. We are opinionated about how our CSS classes and design system are composed, but we're not dogmatic about it.

## How to Use
With the goal of this "Mental Model" being stated, there are (for now) three main ways you can use *egg*

1. **Out of The Box™** - Drop it in as a stylesheet and start prototyping, sans config headaches
2. **Built from source** - If you want to customize *egg* without creating CSS bloat, you can build it into your existing SASS/SCSS workflow.
3. **Component-based** - Import css for the components you need, to use as styles alongside your existing frontend framework. 

## Getting started
1. **Dependencies**; `bower install` to add bourbon and normalize (scss version) or edit the `egg.scss` to change the import path for these dependencies.
2. **Hack**; you could simply `@import egg.scss` and override the styles, or start
modifying the files. `partials/` is definitely fair game, `modules/` too if you
know what you're doing.

**More details at http://wiredcraft.github.io/egg/#how-to/**.

## Support for Tree-shaking

When we get there, will put this ehre

## /docs

To build the styles for the public page (in `docs/`):

    cd docs
    sass --sourcemap=none --style compressed --watch styles.scss:styles.css

Obviously, drop the `--watch` option if you're not actively working on it.
