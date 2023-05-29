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

### Changelog

23-5-29 switching from [devicons](https://devicon.dev) to [material design icons](https://pictogrammers.com/library/mdi/) because devicons doesn't have Mastodon. Meanwhile, [Fontawesome](https://fontawesome.com/icons) seems to have gone the corpo route and only 2,020 of their icons are free.