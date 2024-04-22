# Superpages Scraper API

[![Oxylabs promo code](https://user-images.githubusercontent.com/129506779/250792357-8289e25e-9c36-4dc0-a5e2-2706db797bb5.png)](https://oxylabs.go2cloud.org/aff_c?offer_id=7&aff_id=877&url_id=112)

[![](https://dcbadge.vercel.app/api/server/eWsVUJrnG5)](https://discord.gg/GbxmdGhZjq)

Oxylabs' [Superpages Scraper](https://oxylabs.io/products/scraper-api/web/superpages?utm_source=github&utm_medium=repositories&utm_campaign=product) is a data gathering solution allowing you to extract real-time information from an Superpages website effortlessly. This brief guide showcases how Superpages Scraper works, along with code examples to help you better understand how to use it hassle-free.

### How it works

You can get Superpages results by providing your own URLs to our service. We can return the HTML for any page you like.

#### Python code example

The example below illustrates how you can get HTML of Superpages page.

```python
import requests
from pprint import pprint

# Structure payload.
payload = {
    'source': 'universal_ecommerce',
    'url': 'https://www.superpages.com/oakland-ca/auto-services'
}

# Get response.
response = requests.request(
    'POST',
    'https://realtime.oxylabs.io/v1/queries',
    auth=('user', 'pass1'),
    json=payload,
)

# Instead of response with job status and results url, this will return the
# JSON response with the result.
pprint(response.json())
```
Find code examples for other programming languages [**here**](https://github.com/oxylabs/superpages-scraper/tree/main/code%20examples)

#### Output Example
```json
{
  "results": [
    {
      "content": "<!DOCTYPE html><html lang=\"en\"><head><meta name=\"charset\" content=\"utf-8\"><meta http-equiv=\"X-UA-Com ... </html>",
      "created_at": "2024-02-20 12:35:02",
      "updated_at": "2024-02-20 12:35:06",
      "page": 1,
      "url": "https://www.superpages.com/oakland-ca/auto-services",
      "job_id": "7165685280832227329",
      "status_code": 200
    }
  ]
}
```
With our Superpages Scraper, you can seamlessly obtain public data from any Superpages webpage. Gather vital business information like contact details, business profiles, or customer ratings to understand your market landscape and stay competitive. If you need assistance, reach out to our support team directly through live chat or send an email to hello@oxylabs.io.
