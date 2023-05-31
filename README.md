# Personal Website

A fawncy personal website for goingforbrooke.

## Installation

[Install Zola](https://www.getzola.org/documentation/getting-started/installation/)

```console
$ brew install zola
```

Clone the repo.

```console
$ git clone git@github.com:goingforbrooke/personal_blog.git
```

## Contributing

Preview the site locally.

```console
$ zola serve
```

Make changes in `templates/*.html`. Zola will automatically reload with each new change.

### Update Devicons

Download the [newest icon set](https://github.com/devicons/devicon/archive/master.zip) from Devicons.

Extract `devicon-base.css`, `devicon.ttf`, and `devicon.woff`.

Ensure that Sass is installed so we can convert Devicon's *.css to *.scss.

```console
$ where sass
```

If it's not, then you can install it with `brew install sass/sass/sass`.

Convert `devicon-base.css` to `_devicon.scss`

```console
$ sass devicon-base.css _devicon.scss
```

Overwrite the existing Devicon files.

```console
$ mv _devicon.scss personal_website/sass/lib/_devicon.scss
$ mv devicon.woff static/fonts/devicon.woff
$ mv devicon.ttf static/fonts/devicon.ttf
```

If `zola serve` is active, then Zola will detect the changes and generate a new site.

Commit the changes to VCS.

### Update Fontawesome Icons

1. Download the [latest icon pack](https://fontawesome.com/download).
2. Add to project and follow Font Awesome's [integration instructions](https://fontawesome.com/docs/web/use-with/scss).

### Add Verified Link to Mastodon

https://docs.joinmastodon.org/user/profile/#verification

### Check Favicon Status

https://realfavicongenerator.net/favicon_checker?protocol=http&site=www.goingforbrooke.com