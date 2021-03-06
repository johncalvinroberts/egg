
| [<img src="https://raw.githubusercontent.com/alrra/browser-logos/master/src/edge/edge_48x48.png" alt="IE / Edge" width="24px" height="24px" />](http://godban.github.io/browsers-support-badges/)</br>IE / Edge | [<img src="https://raw.githubusercontent.com/alrra/browser-logos/master/src/firefox/firefox_48x48.png" alt="Firefox" width="24px" height="24px" />](http://godban.github.io/browsers-support-badges/)</br>Firefox | [<img src="https://raw.githubusercontent.com/alrra/browser-logos/master/src/chrome/chrome_48x48.png" alt="Chrome" width="24px" height="24px" />](http://godban.github.io/browsers-support-badges/)</br>Chrome | [<img src="https://raw.githubusercontent.com/alrra/browser-logos/master/src/safari/safari_48x48.png" alt="Safari" width="24px" height="24px" />](http://godban.github.io/browsers-support-badges/)</br>Safari | [<img src="https://raw.githubusercontent.com/alrra/browser-logos/master/src/safari-ios/safari-ios_48x48.png" alt="iOS Safari" width="24px" height="24px" />](http://godban.github.io/browsers-support-badges/)</br>iOS Safari | [<img src="https://raw.githubusercontent.com/alrra/browser-logos/master/src/samsung-internet/samsung-internet_48x48.png" alt="Samsung" width="24px" height="24px" />](http://godban.github.io/browsers-support-badges/)</br>Samsung | [<img src="https://raw.githubusercontent.com/alrra/browser-logos/master/src/opera/opera_48x48.png" alt="Opera" width="24px" height="24px" />](http://godban.github.io/browsers-support-badges/)</br>Opera |
| --------- | --------- | --------- | --------- | --------- | --------- | --------- |
| IE11, Edge| last 2 versions| last 4 versions| last 2 versions| last 3 versions| last 2 versions| last 3 versions

# egg

*egg* is a flexible, minimal, and beautiful CSS/SCSS framework. It was developed originally for building Web apps at [Wiredcraft](https://wiredcraft.com) (things like [devo.ps](http://devo.ps)).

**More on the official page: http://wiredcraft.github.io/egg/#about**.

### What is egg?

You're probaly asking yourself: what do we mean by a *flexible* CSS framework? 

*egg* is designed to be compatible with several workflows in mind. We don't care if you're using React, Vue, Jekyll, or whatever is the hottest framework the kool kids are using these days. We are here for you regardless of your subjectively foolish choice of tooling.

Furthermore: egg is designed to be *minimal*. Around ~10kb gzipped, this framework is lightweight and unobtrusive. CSS frameworks often try to provide too much, resulting in a lot of unused CSS bloating your bundles. We try to stay out of YOUR CSS by just providing developers with the basic defaults and toolkit, allowing you to write custom CSS quickly and easily. Let's face it: you're going to end up writing a lot of CSS anyways to fulfill the design spec 😘.

**Tl;dr** The mental model of *egg* is to be compatible **and** extensible within your existing workflow/framework/platform. We are opinionated about how our CSS design systems are composed, but we're not dogmatic about it.

### How to Use
With these goals in mind, there are (for now) three main ways you can use *egg*

1. [**Out of The Box™**](#out-of-the-box) - Drop it in as a stylesheet and start prototyping, sans config headaches
2. [**Built from source**](#built-from-source) - If you want to customize *egg* without creating CSS bloat, you can build it into your existing SASS/SCSS workflow.
3. [**Component-based**](#component-based) - Import CSS for the components you need, to use as styles alongside your existing frontend framework. **coming soon**

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

From here, you can build this in to whatever SCSS/SASS framework you may need.

Also, *egg* offers a bunch of neat mixins and functions for SASS/SCSS workflows, [check them out here](https://wiredcraft.com).


**More details at http://wiredcraft.github.io/egg/#how-to/**.


## Support for Tree-shaking

When we get there, will put this ehre

## /docs

To build the styles for the public page (in `docs/`):

    cd docs
    sass --sourcemap=none --style compressed --watch styles.scss:styles.css

Obviously, drop the `--watch` option if you're not actively working on it.
