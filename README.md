# jekyll-theme-cypress

A theme for portfolios, for Jekyll and Siteleaf.

## Installation

Add the theme's gem to your site's `Gemfile`:

```ruby
gem "jekyll-theme-cypress"
```

Specify the `theme` in your site's `_config.yml`:

```yaml
theme: jekyll-theme-cypress
```

Install:

```
$ bundle
```

## Usage

### Configuration

You can set the following options in your site's `_config.yml`:

Setting | Description | Default
--- | --- | ---
`layout` | Layout of index thumbnail items: `shelf`, `tile`, or `short-tile` | `shelf`
`title_image` | URL to an optional custom title image to replace text title |
`is_description_hidden` | Hide description below the title | `false`
`is_nav_hidden` | Hide navigation links below the title | `false`
`sort_by` | Sort order for posts in the index, including: `'date'`, `'title'`, `'position'` (sorted by drag-and-drop in Siteleaf) | `'date'` 
`is_sort_reversed` | Reverse the `sort_by` order | `false`
`is_index_hidden` | Hide index thumbnails on permalink pages | `false`
`is_date_hidden` | Hide date on permalink pages | `false`
`date_format` | Date [format](https://shopify.github.io/liquid/filters/date/) | `"%b %-d, %Y"` (outputs to `Jun 7, 2016`)

### Custom styles

The theme comes with a stylesheet, `/assets/styles.scss`, where you can edit variables, including font sizes and colors.

### Additional pages

You can create additional pages, like an About page (`about.markdown`), which will be compiled at the URL `/about/`.

```
---
title: About
layout: page
---

This is the body of the page.
```

### Navigation

Any pages you add will get added to the navigation by default. You can override these with your own navigation links (both internal and external) in a horizontal list below the title. Add these in `_config.yml`:

```yaml
nav:
- title: About
  url: /about/
- title: GitHub
  url: https://github.com/justinjaywang/jekyll-theme-cypress
```

### Google Analytics

Enable Google Anaytics in production by specifying the tracking code in your site's `_config.yml`:

```yaml
google_analytics: UA-XXXXXXXX-X
```

## Development

To set up your environment to develop this theme, run `bundle install`.

You theme is setup just like a normal Jekyll site. To test your theme, run `bundle exec jekyll serve` and open your browser at `http://localhost:4000`. This starts a Jekyll server using your theme. Add pages, documents, data, etc. like normal to test your theme's contents. As you make modifications to your theme and to your content, your site will regenerate and you should see the changes in the browser after a refresh, just like normal.

When your theme is released, only the files in `_layouts`, `_includes`, and `_sass` tracked with Git will be released.

## License

The theme is available as open source under the terms of the [MIT License](http://opensource.org/licenses/MIT).
