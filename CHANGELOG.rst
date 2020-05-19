pelican-bootstrap3-nero
-----------------------

This theme is copied from pelican-bootstrap3 with some customization.

I could not update the related changes that should be made for translation (foreign languages).

Use it at your own risk.

Changes, newer changes on top
-----------------------------

* Version 1.1
  - Disable loading of (unused) fonts from https://fonts.googleapis.com in static/tipuesearch.css

* Version 1.0
* Release date: 2020-May

- Enabled Google Analytics with consent_cookies2

  - Need to update parameters and enable it
  - GOOGLE_ANALYTICS_UNIVERSAL = 'UA-XXXXXXX-Y'
  - GOOGLE_ANALYTICS_UNIVERSAL_PROPERTY = 'auto'
  - GOOGLE_ANALYTICS_UNIVERSAL_CHECK_CONSENT = True

- static/tipuesearch/tipuesearch.css

  - Changing default fonts

- Customization for plugin neighbor articles

  - includes/articles.html updated for displaying previous/next article (same category only)
  - New file: includes/neighbour_same_category.html

- Customized template for plugin share_post (updated includes/articles.html)

  - New file: includes/share_posts.html

- Tweaks to templates/footer.html

  - HTTPS for the links and adding "nofollow"

- Upgrade jsquery from 3.4.1 to 3.5.1 with SRI

- If you enabled plugin pelican-ert (estimated read time).

  - It would add info for the ert in the article_info.html

- includes/categories.html

  - id="categories" -> id="sidebar_categories"
  - For fixing duplicated id=categories (same id was also included from base.html) in the same html

- includes/social.html. Adding reddit so that it could display the icon correctly

- Adding a section for bottom of sidebar. Use case could be displaying disclaimer

- Options for sidebar bottom

  - OPTIONAL_SIDEBAR_BOTTOM = True
  - OPTIONAL_SIDEBAR_BOTTOM_TITLE = 'Disclaimer'
  - OPTIONAL_SIDEBAR_BOTTOM_ID= 'disclaimer'
  - OPTIONAL_SIDEBAR_BOTTOM_TEXT = 'Replace by your text for disclaimer'

- Adding a file 'templates/includes/twitter_custom.html' for Twitter recent tweet list

  - Displayed at bottom of articles
  - If you have ad-block software it may not be displayed
  - Enable it in pelicanconf.py
  - TWITTER_CUSTOM = True

- Adding support for IntenseDebate in new template file templates/includes/comments_intensedebate.html

  - Include the IntenseDebate comment system in 'templates/article.html'
  - Enable it in pelicanconf.py
  - INTENSEDEBATE_ACCOUNT = 'Your account id from IntenseDebate'

- Adding support for cookie_consent2 with SRI

  - New template file templates/includes/cookie_consent2.html
  - Included the banner in 'templates/base.html'
  - Enable it in pelicanconf.py
  - COOKIE_CONSENT2 = True
  - Set your URL to privacy policy with COOKIE_CONSENT2_PRIVACY_URL

- Adding new html file for similar_posts and include it in articles.html

  - New file: includes/similar_posts.html
  - You need to enable 'similar_posts' plugin

- Cloned from pelican-themes 2020-Mar-16

  - From commit dcfb5cd30708576bf41866740ba26d0b2843eaba
  - This theme is copied from pelican-bootstrap3 to become a new customized theme