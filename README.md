# Kaggle Scraper API

[![Oxylabs promo code](https://user-images.githubusercontent.com/129506779/250792357-8289e25e-9c36-4dc0-a5e2-2706db797bb5.png)](https://oxylabs.go2cloud.org/aff_c?offer_id=7&aff_id=877&url_id=112)

Oxylabs’ [Kaggle Scraper](https://oxylabs.io/products/scraper-api/web/kaggle?utm_source=github&utm_medium=repositories&utm_campaign=product) is a data gathering solution allowing you to extract real-time information from an Kaggle website effortlessly. This brief guide explains how an Kaggle Scraper works and provides code examples to understand better how you can use it hassle-free.

### How it works

You can get Kaggle results by providing your own URLs to our service. We can return the HTML for any Kaggle page you like.

#### Python code example

The example below illustrates how you can get HTML of Kaggle page.

```python
import requests
from pprint import pprint

# Structure payload.
payload = {
    'source': 'universal',
    'url': 'https://www.kaggle.com/competitions'
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
Find code examples for other programming languages [**here**](https://github.com/oxylabs/kaggle-scraper/tree/main/code%20examples)

#### Output Example
```json
{
  "results": [
    {
      "content": "\r\n\r\n<!DOCTYPE html>\r\n<html lang=\"en\">\r\n\r\n<head>\r\n  <title>Kaggle Competitions</title>\r\n  <meta chars ... </html>",
      "created_at": "2023-12-18 11:16:52",
      "updated_at": "2023-12-18 11:16:54",
      "page": 1,
      "url": "https://www.kaggle.com/competitions",
      "job_id": "7142472785195965441",
      "status_code": 200
    }
  ]
}
```
With our Kaggle Scraper, you can easily extract public data from any Kaggle web page. Gather the essential information related to machine learning datasets, open-source code, and competitions, to leverage your data science knowledge and stay ahead in the field. If you have any queries, reach out to our support team via live chat or email us at hello@oxylabs.io.