# egg

*egg* is a flexible, minimal, and beautiful css/scss framework. It was developed originally for building Web apps at [Wiredcraft](https://wiredcraft.com) (things like [devo.ps](http://devo.ps)).

**More on the official page: http://wiredcraft.github.io/egg/#about**.

### What is egg?

You're probaly asking yourself: what do we mean by a *flexible* css framework? 

*egg* is designed to be compatible with several workflows in mind. We don't care if you're using React, Vue, Jekyll, or whatever is the hottest framework the kool kids are using these days. As they say: *Every fool has his tool*. We are here for you regardless of your subjectively foolish choice of tooling.

Furthermore: egg is designed to be *minimal*. Around ~10kb gzipped, this framework is lightweight and unobtrusive. CSS frameworks often try to provide too much, resulting in a lot of unused css bloating your bundles. We also hate css specificity battles, so we try to stay out of YOUR css by just providing developers with the basic defaults and toolkit, allowing you to write your best custom css quickly and easily. Let's face it: you're going to end up writing a lot of css anyways to fulfill the design spec.

The mental model of *egg* is to be compatible **and** extensible within your existing workflow/framework/platform. We are opinionated about how our CSS design systems are composed, but we're not dogmatic about it.

### How to Use
With the mental model behind being stated, there are (for now) three main ways you can use *egg*

1. [**Out of The Box™**](#out-of-the-box) - Drop it in as a stylesheet and start prototyping, sans config headaches
2. [**Built from source**](#built-from-source) - If you want to customize *egg* without creating CSS bloat, you can build it into your existing SASS/SCSS workflow.
3. [**Component-based**](#component-based) - Import css for the components you need, to use as styles alongside your existing frontend framework. 

## Out of The Box™
You just came here for CSS styles, right? Here:

```
npm install eggcss --save
```
After install, the distribution stylesheet is available in `node_modules/egcss/dist/egg.min.css`

Alternatively, include it in your website's head through unpkg

```
<link src="LINK_HERE" rel="stylesheet">
```
Now start prototyping stuff and never come back to this github readme!

## Built from source

First, you'll need to install it of course

```
npm install eggcss --save
```

Next, to extend *egg* you can customize by providing a `_variables.scss` file, with which you can write custom colors, fonts, etc. to override defaults.
[Put a link here to a description in the docs about these variables](https://wiredcraft.com)

Now, create a file for which will be your entry point to your custom stylesheet, e.g. `styles.scss`. In this file, import your new `_variables.scss` along with `node_modules/eggcss/scss/lib.scss`. 

From here, you can build this in to whatever scss/sass framework you may need.

For a SASS/SCSS workflow, *egg* offers a bunch of neat mixins and functions, [check them out here](https://wiredcraft.com).


**More details at http://wiredcraft.github.io/egg/#how-to/**.

## Browser Support

## Support for Tree-shaking

When we get there, will put this ehre

## /docs

To build the styles for the public page (in `docs/`):

    cd docs
    sass --sourcemap=none --style compressed --watch styles.scss:styles.css

Obviously, drop the `--watch` option if you're not actively working on it.
