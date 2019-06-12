# LibDNSJson

Encoder/decoder for [google's JSON DNS message format](https://developers.google.com/speed/public-dns/docs/dns-over-https) based on [libdns](https://github.com/DaveRandom/LibDNS/).  

The API consists of a `QueryEncoderFactory` that creates `QueryEncoder` objects, that can encode libdns `Message` objects to a query string that can be used both with google's and cloudflare's DNS-over-HTTPS APIs (for cloudflare, using directly UDP wireformat with `libdns`'s `Encoder` is recommended).  

The `JsonDecoderFactory` creates `JsonDecoder` objects, that accept JSON strings and decode them back to `Message` objects.  
