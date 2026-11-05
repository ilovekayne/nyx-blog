# nyx-blog

nyx.ilovekayne.xyz, built with [jekyll-theme-nyx](https://github.com/Slavetomints/jekyll-theme-nyx). It deploys with GitHub Actions because Nyx needs Jekyll 4 and custom plugins, and the classic Pages builder supports neither.

What a gem theme does NOT bring with it, and this repo has to supply itself:

- `jekyll-toc` in the Gemfile and `plugins:` (the post layout calls `toc_only`)
- the `tabs` collection and the `_tabs/` folder (the header nav loops over `site.tabs`)
- `_plugins/taxonomy_pages.rb` (generates the tag and category pages)
- `_layouts/category.html` and `_layouts/tag.html` (the taxonomy plugin reads layouts from the site source, not the gem)
- the posts `defaults` block (layout, permalink, toc, author)

