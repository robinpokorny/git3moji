source 'https://rubygems.org'

require 'json'
require 'open-uri'
versions = JSON.parse(open('https://pages.github.com/versions.json').read)

gem 'github-pages', versions['github-pages']
gem "jekyll-readme-index"

# Security related version fixes
gem "jekyll", ">= 3.6.3"
gem "nokogiri", ">= 1.10.8"
gem "ffi", ">= 1.9.24"
