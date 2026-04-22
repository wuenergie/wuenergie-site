source "https://rubygems.org"

# Dieser Gemfile ist ausschließlich für die **lokale Vorschau** gedacht.
# GitHub Pages liest ihn nicht — der produktive Build nutzt serverseitig
# die `github-pages`-Gem (Jekyll 3.9 + whitelisted Plugins).
#
# Lokal fahren wir das aktuelle Jekyll 4, weil der github-pages-Stack
# inzwischen inkompatibel mit modernem Ruby ist. Da wir weder ein Theme
# noch Blogposts haben und nur die beiden auf der GH-Pages-Whitelist
# stehenden Plugins nutzen, ist der Render-Output identisch.
#
# Updaten mit:  bundle update

gem "jekyll", "~> 4.3"

group :jekyll_plugins do
  gem "jekyll-sitemap"
  gem "jekyll-seo-tag"
end

# Standard-Library-Gems, die seit Ruby 3.4 nicht mehr mitkommen.
gem "webrick", "~> 1.8"
gem "csv"
gem "base64"
gem "bigdecimal"
gem "logger"
