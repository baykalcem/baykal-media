title: "Baykal Media"
description: "Documentary, cinematic photography capturing authentic moments"
logo: "/assets/images/logo.png"
url: "https://www.baykalmedia.com"
baseurl: ""

remote_theme: mmistakes/minimal-mistakes
minimal_mistakes_skin: "air"

# Site Settings
locale: "en-US"
search: true
breadcrumbs: true
words_per_minute: 200

# Social Sharing
twitter:
  username: ""
facebook:
  username: "yourhandle"
  app_id:
  publisher:
og_image: "/assets/images/logo.png"
social:
  type: Person
  links:
    - "https://instagram.com/yourhandle"
    - "https://facebook.com/yourhandle"

# Analytics
analytics:
  provider: false # false (default), "google", "google-universal", "google-gtag", "custom"
  google:
    tracking_id:
    anonymize_ip: false # true, false (default)

# Site Author
author:
  name: "Baykal Media"
  avatar: "/assets/images/profile.jpg"
  bio: "Documentary photographer specializing in landscapes and portraits"
  location: "Your Location"
  links:
    - label: "Instagram"
      icon: "fab fa-fw fa-instagram"
      url: "https://instagram.com/yourhandle"
    - label: "Facebook"
      icon: "fab fa-fw fa-facebook"
      url: "https://facebook.com/yourhandle"
    - label: "Email"
      icon: "fas fa-fw fa-envelope"
      url: "mailto:hello@baykalmedia.com"

# Site Footer
footer:
  links:
    - label: "Instagram"
      icon: "fab fa-fw fa-instagram"
      url: "https://instagram.com/yourhandle"
    - label: "Facebook"
      icon: "fab fa-fw fa-facebook"
      url: "https://facebook.com/yourhandle"

# Collections
collections:
  portfolio:
    output: true
    permalink: /:collection/:path/
  posts:
    output: true
    permalink: /:categories/:title/

# Defaults
defaults:
  # _posts
  - scope:
      path: ""
      type: posts
    values:
      layout: single
      author_profile: true
      read_time: true
      comments: false
      share: true
      related: true
  # _pages
  - scope:
      path: "_pages"
      type: pages
    values:
      layout: single
      author_profile: false
  # _portfolio
  - scope:
      path: ""
      type: portfolio
    values:
      layout: single
      author_profile: false
      share: true

# Plugins
plugins:
  - jekyll-paginate
  - jekyll-sitemap
  - jekyll-gist
  - jekyll-feed
  - jekyll-include-cache

category_archive:
  type: liquid
  path: /categories/
tag_archive:
  type: liquid
  path: /tags/