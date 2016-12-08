# jekyll-theme-cypress

A portfolio theme for Jekyll and Siteleaf.

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
`show_title` | Boolean to show title | `true`
`title_image` | Custom title image URL to replace text title |
`show_description` | Boolean to show description below the title (description is specified in `description`) | `false`
`show_permalink_index` | Boolean to show index thumbnails on permalink pages | `true`
`show_date` | Boolean to show date on permalink pages | `true`
`date_format` | Date [format](https://shopify.github.io/liquid/filters/date/) | `"%b %-d, %Y"` (outputs to `Jun 7, 2016`)
`post_sort` | Sort order for posts in the index, such as by `'position'` (the drag and drop order in Siteleaf) or '`title`' | Date, reversed
`footer_text` | Markdown text to include in the footer; hidden if not specified |

### Navigation

Specify the navigation page links that appear below the title in `_config.yml`:

```
nav:
- title: About
  url: /about/
- title: Contact
  url: https://twitter.com/siteleaf
```

### Custom styles

The theme comes with a stylesheet, `/assets/styles.scss`, where you can edit color and typography variables.

TO DO: edit these when finalized
```
// colors

$color--primary:    #333;
$color--secondary:  #999;
$color--background: #fff;

// typography

$font-size--desktop: 16px;
$font-size--mobile:  14px;

$font-family--body:     monospace;
$font-weight--body:     400;
$line-height--body:     1.5;

$font-family--headings: sans-serif;
$font-weight--headings: 700;
$line-height--headings: 1.25;
```

### Google Analytics

You can enable Google Anaytics in production in your site's `_config.yml` by specifying the tracking code:

```yaml
google_analytics: UA-XXXXXXXX-X
```

## Development

To set up your environment to develop this theme, run `bundle install`.

You theme is setup just like a normal Jekyll site. To test your theme, run `bundle exec jekyll serve` and open your browser at `http://localhost:4000`. This starts a Jekyll server using your theme. Add pages, documents, data, etc. like normal to test your theme's contents. As you make modifications to your theme and to your content, your site will regenerate and you should see the changes in the browser after a refresh, just like normal.

When your theme is released, only the files in `_layouts`, `_includes`, and `_sass` tracked with Git will be released.

## License

The theme is available as open source under the terms of the [MIT License](http://opensource.org/licenses/MIT).
