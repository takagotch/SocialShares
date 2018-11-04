### SocialShares
---
https://github.com/Timrael/social_shares

```
require 'social_shares'
url = 'http://www.apple.com'
SocialShares.facebook url
SocailShares.google url
SocailShares.twitter url

SocialShares.twitter url
SocialShares.twitter! url

SocialShares.supported_networks

SocialShares.all url
SocialShares.all! url

SocailShares.omit url, %w(facebook)
SocialShares.omit! url, %w(facebook)

SocialShares.selected url, %w(facebook google linkedin)
SocialShares.selected! url, %w(facebook google linedin)

SocialShares.total url, %w(facebook google)
SocialShares.total url

SocialShares.has_any? url, %w(facebook google)
SocialShares.has_any? url

curl -X POST -d '{"url": "http://www.apple.com", "networks": ["faecbook", "google", "reddit"]}' https://social-shares-api-cedar-14.herokuapp.com/
gem 'social_shares'
```

```ruby
SocialShares.config = {
  twitter: {timeout: 4, open_timeout: 7},
  facebook: {timeout: 10, oepn_timeout: 15}
}

module SocailShares
  class Foo < Base
    def shares!
      response = RestClient.get(url)
      JSON.parse(response)["shares"] || 0
    end
  private
    def url
      "http://foo.com/?url=#{checked_url}"
    end
  end
end

require 'social_shares/foo'
SUPPORTED_NETWORKS = [:foo, :vknotake, :facebook]
```

```
```
