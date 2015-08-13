# Gite Glaise

Static website for Gite de Glaise.
Uses [this boilerplate](https://github.com/clairezed/static_site_starter)

## Included

* jade
* sass
* coffeescript
* bootstrap3

Powered by [harp](http://harpjs.com/). Dig here for docs.

## Development principles and wishes
- Use of [BEM syntax](http://csswizardry.com/2013/01/mindbemding-getting-your-head-round-bem-syntax/) for css

## Possible tools
- http://scrollrevealjs.org : Easily reveal elements as they enter the viewport.
- 

## Commands

Install harp and bower globally :
```ssh
$ npm install -g harp
$ npm install -g bower
```

Clone this repository and install stuff
```ssh
$ git clone git@github.com:Trebouzul/gite-glaise.git
$ cd gite-glaise
$ bower install
````

Launch app :
```ssh
$ harp server
```
Server default to http://localhost:9000/

If you want to use another port :
```ssh
$ harp server --port 3000
```

Update harp :
```ssh
npm update -g harp
```

## Deployement on github pages

todo
<!-- if needed :
```ssh
$ git branch -D gh-pages
```
From master :
```ssh
$ git checkout --orphan gh-pages
$ cd _src
$ harp compile ./ ../
$ cd ../
$ git push origin gh-pages
```

Or, if needed:
```ssh
$ git push --set-upstream origin gh-pages --force
``` -->


## Anatomy of the application

```
gite-glaise/          <-- root of your application
   |- .bowerrc                <-- Bower config
   |- README.md               <-- Hello, reader !
   |- bower.json              <-- declaration of application dependencies (enables `bower install`)
   |- harp.json               <-- configuration, globals goes here.
   +- public/                 <-- your application belong in the public dir
<!--       |- _layout.jade         <-- optional layout file
      |- index.jade           <-- app must have an index.html or index.jade file
      |- 404.jade             <-- default 404 page
      +- assets/              <-- here are js, css and other public stuff
         +- fonts             <-- fonts
         +- images            <-- images
         +- scripts           <-- coffeescript / javascript
         +- styles            <-- sass / scss / css
      +- _shared/             <-- arbitrary directory for shared partials
         |- nav.jade          <-- a partial example
      +- items/               <-- pages in here will have "/items/" in URL
         |- _data.json        <-- items metadata goes here
         |- _layout.jade      <-- items layout, extending base layout & composed with jade blocks
         |- index.jade        <-- base /items file. You land here if url is "/items"
         |- item-one.jade     <-- should have at least one .html,  .jade, .md or .ejs file. -->
   +- vendor/                 <-- third party libs
```
Files and folders beginning with underscores won't be read

Good examples of how to use harp can be found in [the github repo of their website](https://github.com/harp/harpjs.com)


## To do
- [ ] improve dependencies automation (make script ?)
- [ ] check what is in bower.json (as it was made automatically without me understanding anything I was doing)
- [ ] continuous integration and deployment ?


## Inspiration and improvements

Check the following repos :
- https://github.com/isidrorg/hbbp : make script use
- https://github.com/jvandemo/hb-bootstrap : basic boilerplate
