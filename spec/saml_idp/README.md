# Show internal XML

``` ruby
require 'ruby-saml-idp'
require 'uuid'
include SamlIdp::Controller
saml_response = encode_SAMLResponse("foo@example.com", :audience_uri => 'xxx')
xml = Base64.decode64(saml_response)
require 'nokogiri'
n = Nokogiri.parse(xml)
puts n.to_xml
```
