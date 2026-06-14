# Google Search API (Custom Search JSON API Wrapper)

Live Demo: https://google-search.vercel.app/

This project is a simple wrapper around the **Google Custom Search JSON API** that allows users to perform Google-like searches and receive structured JSON responses.

---

## ⚠️ IMPORTANT WARNING

This project is:

- ❌ Not actively maintained
- ❌ May break at any time due to API or dependency changes
- ❌ Not guaranteed to work consistently
- ❌ Not suitable for production environments
- ⚠️ Should be used with caution

If the API fails, returns errors, or behaves unexpectedly, it is likely due to external changes in Google's API or quota limitations.

---

## 🎓 PURPOSE

This project is created strictly for:

- Educational purposes
- Learning how APIs work
- Understanding JSON responses
- Practicing frontend/backend integration
- Experimenting with search APIs

---

## 🚫 USAGE RESTRICTIONS

You MUST NOT use this project for:

- Production applications
- Commercial services
- Large-scale automation or scraping
- Spam or abusive requests
- Any activity that violates Google API Terms of Service

---

## 🔗 API ENDPOINT

```
GET https://www.googleapis.com/customsearch/v1
```

### 📌 EXAMPLE REQUEST

```
GET https://www.googleapis.com/customsearch/v1?key=AIzaSyCNNgFq67GsLtCH18fHPHbsyDWXER1zcG0&cx=b3afb02f3f21a4152&q=hello&start=1
```

### ⚙️ REQUIRED PARAMETERS

| Parameter | Type   | Required | Description               |
|-----------|--------|----------|---------------------------|
| key       | string | Yes      | Google API key            |
| cx        | string | Yes      | Custom Search Engine ID   |
| q         | string | Yes      | Search query              |
| start     | number | No       | Pagination start index (default = 1) |

---

## 📤 RESPONSE FORMAT OVERVIEW

The API returns a JSON object containing metadata, pagination details, and search results.

### 🧾 SAMPLE RESPONSE

```json
{
  "kind": "customsearch#search",
  "url": {
    "type": "application/json",
    "template": "https://www.googleapis.com/customsearch/v1?q={searchTerms}&num={count?}&start={startIndex?}&lr={language?}&safe={safe?}&cx={cx?}&sort={sort?}&filter={filter?}&gl={gl?}&cr={cr?}&googlehost={googleHost?}&c2coff={disableCnTwTranslation?}&hq={hq?}&hl={hl?}&siteSearch={siteSearch?}&siteSearchFilter={siteSearchFilter?}&exactTerms={exactTerms?}&excludeTerms={excludeTerms?}&linkSite={linkSite?}&orTerms={orTerms?}&dateRestrict={dateRestrict?}&lowRange={lowRange?}&highRange={highRange?}&searchType={searchType}&fileType={fileType?}&rights={rights?}&imgSize={imgSize?}&imgType={imgType?}&imgColorType={imgColorType?}&imgDominantColor={imgDominantColor?}&alt=json"
  },
  "queries": {
    "request": [
      {
        "title": "Google Custom Search - hello",
        "totalResults": "2410000000",
        "searchTerms": "hello",
        "count": 10,
        "startIndex": 1,
        "inputEncoding": "utf8",
        "outputEncoding": "utf8",
        "safe": "off",
        "cx": "b3afb02f3f21a4152"
      }
    ],
    "nextPage": [
      {
        "title": "Google Custom Search - hello",
        "totalResults": "2410000000",
        "searchTerms": "hello",
        "count": 10,
        "startIndex": 11,
        "inputEncoding": "utf8",
        "outputEncoding": "utf8",
        "safe": "off",
        "cx": "b3afb02f3f21a4152"
      }
    ]
  },
  "context": {
    "title": "inizio-react"
  },
  "searchInformation": {
    "searchTime": 0.420458,
    "formattedSearchTime": "0.42",
    "totalResults": "2410000000",
    "formattedTotalResults": "2,410,000,000"
  },
  "items": [
    {
      "kind": "customsearch#result",
      "title": "Adele - Hello (Official Music Video) - YouTube",
      "htmlTitle": "Adele - \u003cb\u003eHello\u003c/b\u003e (Official Music Video) - YouTube",
      "link": "https://www.youtube.com/watch?v=YQHsXMglC9A",
      "displayLink": "www.youtube.com",
      "snippet": "Oct 22, 2015 ... Listen to \"Easy On Me\" here: http://Adele.lnk.to/EOM Pre-order Adele's new album \"30\" before its release on November 19: ...",
      "htmlSnippet": "Oct 22, 2015 \u003cb\u003e...\u003c/b\u003e Listen to &quot;Easy On Me&quot; here: http://Adele.lnk.to/EOM Pre-order Adele&#39;s new album &quot;30&quot; before its release on November 19:&nbsp;...",
      "formattedUrl": "https://www.youtube.com/watch?v=YQHsXMglC9A",
      "htmlFormattedUrl": "https://www.youtube.com/watch?v=YQHsXMglC9A",
      "pagemap": {
        "cse_thumbnail": [
          {
            "src": "https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcRW1bvAZugZom5o2dnQB0kgGCcpQvUV4jpFdjMohUMr1CS9RG2B-BUin6M&s",
            "width": "300",
            "height": "168"
          }
        ],
        "imageobject": [
          {
            "width": "1280",
            "url": "https://i.ytimg.com/vi/YQHsXMglC9A/maxresdefault.jpg",
            "height": "720"
          }
        ],
        "person": [
          {
            "name": "Adele",
            "url": "http://www.youtube.com/@adele"
          }
        ],
        "interactioncounter": [
          {
            "userinteractioncount": "19334517",
            "interactiontype": "https://schema.org/LikeAction"
          },
          {
            "userinteractioncount": "3265032181",
            "interactiontype": "https://schema.org/WatchAction"
          }
        ],
        "metatags": [
          {
            "og:image": "https://i.ytimg.com/vi/YQHsXMglC9A/maxresdefault.jpg",
            "twitter:app:url:iphone": "vnd.youtube://m.youtube.com/watch?v=YQHsXMglC9A&feature=applinks",
            "twitter:app:id:googleplay": "com.google.android.youtube",
            "theme-color": "rgba(0, 0, 0, 0)",
            "og:image:width": "1280",
            "twitter:card": "player",
            "og:site_name": "YouTube",
            "twitter:url": "https://www.youtube.com/watch?v=YQHsXMglC9A",
            "twitter:app:url:ipad": "vnd.youtube://m.youtube.com/watch?v=YQHsXMglC9A&feature=applinks",
            "al:android:package": "com.google.android.youtube",
            "twitter:app:name:googleplay": "YouTube",
            "title": "Adele - Hello (Official Music Video)",
            "al:ios:url": "vnd.youtube://m.youtube.com/watch?v=YQHsXMglC9A&feature=applinks",
            "twitter:app:id:iphone": "544007664",
            "og:description": "Listen to \"Easy On Me\" here: http://Adele.lnk.to/EOM Pre-order Adele's new album \"30\" before its release on November 19: https://www.adele.com Shop the \"Adele\" collection here: http://shop.adele.com\n\n'Hello' is taken from the new album, 25, out November 20. http://adele.com\nAvailable now from iTunes http://smarturl.it/itunes25 \nAvailable now from Amazon http://smarturl.it/25amazon \nAvailable now from Google Play http://smarturl.it/25gplay\nAvailable now at Target (US Only): http://smarturl.it/target25\n\nDirected by Xavier Dolan, @XDolan\n\nFollow Adele on:\n\nFacebook - https://www.facebook.com/Adele\nTwitter - https://twitter.com/Adele \nInstagram - http://instagram.com/Adele\n\nhttp://vevo.ly/jzAuJ1\n\nCommissioner: Phil Lee\nProduction Company: Believe Media/Sons of Manual/Metafilms\nDirector: Xavier Dolan\nExecutive Producer: Jannie McInnes\nProducer: Nancy Grant/Xavier Dolan\nCinematographer: André Turpin\nProduction design: Colombe Raby\nEditor: Xavier Dolan\nAdele's lover: Tristan Wilds",
            "al:ios:app_store_id": "544007664",
            "twitter:image": "https://i.ytimg.com/vi/YQHsXMglC9A/maxresdefault.jpg",
            "twitter:player": "https://www.youtube.com/embed/YQHsXMglC9A",
            "twitter:player:height": "720",
            "twitter:site": "@youtube",
            "og:video:type": "text/html",
            "og:video:height": "720",
            "og:video:url": "https://www.youtube.com/embed/YQHsXMglC9A",
            "og:type": "video.other",
            "twitter:title": "Adele - Hello (Official Music Video)",
            "al:ios:app_name": "YouTube",
            "og:title": "Adele - Hello (Official Music Video)",
            "og:image:height": "720",
            "twitter:app:id:ipad": "544007664",
            "al:web:url": "http://m.youtube.com/watch?v=YQHsXMglC9A&feature=applinks",
            "og:video:secure_url": "https://www.youtube.com/embed/YQHsXMglC9A",
            "og:video:tag": "Adele",
            "og:video:width": "1280",
            "al:android:url": "vnd.youtube://m.youtube.com/watch?v=YQHsXMglC9A&feature=applinks",
            "fb:app_id": "87741124305",
            "twitter:app:url:googleplay": "https://www.youtube.com/watch?v=YQHsXMglC9A",
            "twitter:app:name:ipad": "YouTube",
            "viewport": "width=device-width, initial-scale=1.0, minimum-scale=1.0, maximum-scale=1.0, user-scalable=no,",
            "twitter:description": "Listen to \"Easy On Me\" here: http://Adele.lnk.to/EOM Pre-order Adele's new album \"30\" before its release on November 19: https://www.adele.com Shop the \"Adele\" collection here: http://shop.adele.com\n\n'Hello' is taken from the new album, 25, out November 20. http://adele.com\nAvailable now from iTunes http://smarturl.it/itunes25 \nAvailable now from Amazon http://smarturl.it/25amazon \nAvailable now from Google Play http://smarturl.it/25gplay\nAvailable now at Target (US Only): http://smarturl.it/target25\n\nDirected by Xavier Dolan, @XDolan\n\nFollow Adele on:\n\nFacebook - https://www.facebook.com/Adele\nTwitter - https://twitter.com/Adele \nInstagram - http://instagram.com/Adele\n\nhttp://vevo.ly/jzAuJ1\n\nCommissioner: Phil Lee\nProduction Company: Believe Media/Sons of Manual/Metafilms\nDirector: Xavier Dolan\nExecutive Producer: Jannie McInnes\nProducer: Nancy Grant/Xavier Dolan\nCinematographer: André Turpin\nProduction design: Colombe Raby\nEditor: Xavier Dolan\nAdele's lover: Tristan Wilds",
            "og:url": "https://www.youtube.com/watch?v=YQHsXMglC9A",
            "twitter:player:width": "1280",
            "al:android:app_name": "YouTube",
            "twitter:app:name:iphone": "YouTube"
          }
        ],
        "videoobject": [
          {
            "identifier": "YQHsXMglC9A",
            "embedurl": "https://www.youtube.com/embed/YQHsXMglC9A",
            "playertype": "HTML5 Flash",
            "isfamilyfriendly": "true",
            "keywords": "Adele,Someone Like You,Chasing Pavements,Set Fire to the Rain,Rolling in the Deep,XL Recordings",
            "uploaddate": "2015-10-22T23:54:18-07:00",
            "requiressubscription": "False",
            "description": "Listen to \"Easy On Me\" here: http://Adele.lnk.to/EOM Pre-order Adele's new album \"30\" before its release on November 19: https://www.adele.com Shop the \"Adele\" collection here: http://shop.adele.co...",
            "url": "https://www.youtube.com/watch?v=YQHsXMglC9A",
            "duration": "PT6M7S",
            "name": "Adele - Hello (Official Music Video)",
            "width": "1280",
            "regionsallowed": "AD,AE,AF,AG,AI,AL,AM,AO,AQ,AR,AS,AT,AU,AW,AX,AZ,BA,BB,BD,BE,BF,BG,BH,BI,BJ,BL,BM,BN,BO,BQ,BR,BS,BT,BV,BW,BY,BZ,CA,CC,CD,CF,CG,CH,CI,CK,CL,CM,CN,CO,CR,CU,CV,CW,CX,CY,CZ,DE,DJ,DK,DM,DO,DZ,EC,EE,EG,EH...",
            "genre": "Music",
            "datepublished": "2015-10-22T23:54:18-07:00",
            "thumbnailurl": "https://i.ytimg.com/vi/YQHsXMglC9A/maxresdefault.jpg",
            "height": "720"
          }
        ],
        "cse_image": [
          {
            "src": "https://i.ytimg.com/vi/YQHsXMglC9A/maxresdefault.jpg"
          }
        ],
        "thing": [
          {
            "name": "Adele"
          }
        ],
        "listitem": [
          {
            "position": "1"
          }
        ]
      }
    },
    {
      "kind": "customsearch#result",
      "title": "Hello Products",
      "htmlTitle": "\u003cb\u003eHello\u003c/b\u003e Products",
      "link": "https://www.hello-products.com/",
      "displayLink": "www.hello-products.com",
      "snippet": "friendly products for friendly people. vegan, cruelty free, and thoughtfully formulated for everyone.",
      "htmlSnippet": "friendly products for friendly people. vegan, cruelty free, and thoughtfully formulated for everyone.",
      "formattedUrl": "https://www.hello-products.com/",
      "htmlFormattedUrl": "https://www.\u003cb\u003ehello\u003c/b\u003e-products.com/",
      "pagemap": {
        "cse_thumbnail": [
          {
            "src": "https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcRJxMNQJOaYIS0DjFBpaHIFgijr9JUDyHElekaPKysN7q-Uy_8wHLPn0Q&s",
            "width": "426",
            "height": "118"
          }
        ],
        "metatags": [
          {
            "og:image": "https://cdn.shopify.com/s/files/1/0672/2909/0040/files/NEW-homepage-header_Medium_Banner.webp?v=1710339593",
            "og:image:width": "2000",
            "viewport": "width=device-width,initial-scale=1",
            "shopify-digital-wallet": "/67229090040/digital_wallets/dialog",
            "shopify-checkout-api-token": "cf338dc4ff02a56a7d583a520a9151c8",
            "og:image:height": "556",
            "og:image:secure_url": "https://cdn.shopify.com/s/files/1/0672/2909/0040/files/NEW-homepage-header_Medium_Banner.webp?v=1710339593"
          }
        ],
        "cse_image": [
          {
            "src": "https://cdn.shopify.com/s/files/1/0672/2909/0040/files/NEW-homepage-header_Medium_Banner.webp?v=1710339593"
          }
        ]
      }
    },
    {
      "kind": "customsearch#result",
      "title": "no hello",
      "htmlTitle": "no \u003cb\u003ehello\u003c/b\u003e",
      "link": "https://nohello.net/en",
      "displayLink": "nohello.net",
      "snippet": "If you feel it's a bit brusque to simply say \"Hi\" and ask the question, you can still preface your message with as many pleasantries as you see fit.",
      "htmlSnippet": "If you feel it&#39;s a bit brusque to simply say &quot;Hi&quot; and ask the question, you can still preface your message with as many pleasantries as you see fit.",
      "formattedUrl": "https://nohello.net/en",
      "htmlFormattedUrl": "https://no\u003cb\u003ehello\u003c/b\u003e.net/en",
      "pagemap": {
        "cse_thumbnail": [
          {
            "src": "https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcQeoeulfqmB-Z8gxhO22a1bhZM1AHKLGZJZFAjgYm9LJBHn8pTdeyg7ZSk&s",
            "width": "225",
            "height": "225"
          }
        ],
        "metatags": [
          {
            "og:image": "https://nohello.net/img/XzfE_FYNGc-500.webp",
            "og:type": "website",
            "twitter:card": "summary",
            "twitter:title": "no hello",
            "viewport": "width=device-width, initial-scale=1.0",
            "twitter:url": "https://nohello.net/",
            "twitter:description": "please don't say just hello in chat",
            "og:title": "no hello",
            "title": "no hello",
            "og:url": "https://nohello.net/",
            "og:description": "please don't say just hello in chat",
            "twitter:image": "https://nohello.net/img/XzfE_FYNGc-500.webp"
          }
        ],
        "cse_image": [
          {
            "src": "https://nohello.net/img/XzfE_FYNGc-500.webp"
          }
        ]
      }
    },
    {
      "kind": "customsearch#result",
      "title": "Hello Game (Home Edition) - Common Practice",
      "htmlTitle": "\u003cb\u003eHello\u003c/b\u003e Game (Home Edition) - Common Practice",
      "link": "https://commonpractice.com/products/hello-game",
      "displayLink": "commonpractice.com",
      "snippet": "Hello is a conversation game. It's the easy, non-threatening way to start a conversation with your family and friends about what matters most to you.",
      "htmlSnippet": "\u003cb\u003eHello\u003c/b\u003e is a conversation game. It&#39;s the easy, non-threatening way to start a conversation with your family and friends about what matters most to you.",
      "formattedUrl": "https://commonpractice.com/products/hello-game",
      "htmlFormattedUrl": "https://commonpractice.com/products/\u003cb\u003ehello\u003c/b\u003e-game",
      "pagemap": {
        "offer": [
          {
            "seller": "Common Practice",
            "pricecurrency": "USD",
            "price": "24.95",
            "availability": "http://schema.org/InStock",
            "itemcondition": "New"
          },
          {
            "seller": "Common Practice",
            "pricecurrency": "USD",
            "price": "4.99",
            "availability": "http://schema.org/InStock",
            "itemcondition": "New"
          },
          {
            "seller": "Common Practice",
            "pricecurrency": "USD",
            "price": "124.75",
            "availability": "http://schema.org/InStock",
            "itemcondition": "New"
          },
          {
            "seller": "Common Practice",
            "pricecurrency": "USD",
            "price": "124.75",
            "availability": "http://schema.org/InStock",
            "itemcondition": "New"
          }
        ],
        "cse_thumbnail": [
          {
            "src": "https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcTsLZPtzHnlPgeZsCnvs6qoDQbgtaL6n9uDL8UQu-eXZJEH_WeaP0jN-UFv&s",
            "width": "225",
            "height": "225"
          }
        ],
        "product": [
          {
            "name": "Hello Game (Home Edition)",
            "description": "Hello is a conversation game. It's the easy, non-threatening way to start a conversation with your family and friends about what matters most to you. 2-5 PlayersAges 13+ Contents: 5 Questions..."
          },
          {
            "name": "Extra Player Pack",
            "url": "Extra Player Pack $ 4.99"
          },
          {
            "name": "Hello Event Kit",
            "url": "Hello Event Kit from $ 124.75"
          },
          {
            "name": "Spanish Conversation Event Kit",
            "url": "Spanish Conversation Event Kit from $ 124.75"
          }
        ],
        "metatags": [
          {
            "og:image": "http://commonpractice.com/cdn/shop/products/3650_DissentPins091018-12_600x.jpg?v=1628871906",
            "og:type": "product",
            "twitter:card": "summary",
            "twitter:title": "Hello Game (Home Edition)",
            "theme-color": "#fff3d8",
            "og:site_name": "Common Practice",
            "og:price:amount": "24.95",
            "handheldfriendly": "True",
            "author": "Common Practice",
            "og:title": "Hello Game (Home Edition)",
            "og:price:currency": "USD",
            "twitter:image:height": "240",
            "shopify-checkout-api-token": "05ad6db112f855a7b2697c0ea506657e",
            "og:description": "A conversation game for living and dying well",
            "og:image:secure_url": "https://commonpractice.com/cdn/shop/products/3650_DissentPins091018-12_600x.jpg?v=1628871906",
            "twitter:image": "https://commonpractice.com/cdn/shop/products/3650_DissentPins091018-12_240x.jpg?v=1628871906",
            "twitter:site": "@copractice",
            "twitter:image:width": "240",
            "viewport": "width=device-width,initial-scale=1",
            "twitter:description": "Hello is a conversation game. It's the easy, non-threatening way to start a conversation with your family and friends about what matters most to you.\n2-5 PlayersAges 13+\nContents: \n5 Questions Booklets 30 Thank-you chips Instruction Sheet Tips for inviting your friends and family to play",
            "shopify-digital-wallet": "/12397018/digital_wallets/dialog",
            "mobileoptimized": "320",
            "og:url": "https://commonpractice.com/products/hello-game"
          }
        ],
        "cse_image": [
          {
            "src": "http://commonpractice.com/cdn/shop/products/3650_DissentPins091018-12_600x.jpg?v=1628871906"
          }
        ],
        "hproduct": [
          {
            "fn": "Hello Game (Home Edition)",
            "description": "Hello is a conversation game. It's the easy, non-threatening way to start a conversation with your family and friends about what matters most to you. 2-5 PlayersAges 13+ Contents: 5 Questions...",
            "currency": "USD",
            "currency_iso4217": "840"
          },
          {
            "fn": "Extra Player Pack",
            "currency": "USD",
            "currency_iso4217": "840",
            "url": "https://commonpractice.com/products/extra-player-pack"
          },
          {
            "fn": "Hello Event Kit",
            "currency": "USD",
            "currency_iso4217": "840",
            "url": "https://commonpractice.com/products/hello-event-kit"
          },
          {
            "fn": "Spanish Conversation Event Kit",
            "currency": "USD",
            "currency_iso4217": "840",
            "url": "https://commonpractice.com/products/event-kit-spanish"
          }
        ]
      }
    },
    {
      "kind": "customsearch#result",
      "title": "Hello - song and lyrics by Adele - Spotify",
      "htmlTitle": "\u003cb\u003eHello\u003c/b\u003e - song and lyrics by Adele - Spotify",
      "link": "https://open.spotify.com/track/62PaSfnXSMyLshYJrlTuL3",
      "displayLink": "open.spotify.com",
      "snippet": "Lyrics. Hello, it's me. I was wondering if after all these years you'd like to meet. To go over everything. They say that time's supposed to heal ya, ...",
      "htmlSnippet": "Lyrics. \u003cb\u003eHello\u003c/b\u003e, it&#39;s me. I was wondering if after all these years you&#39;d like to meet. To go over everything. They say that time&#39;s supposed to heal ya,&nbsp;...",
      "formattedUrl": "https://open.spotify.com/track/62PaSfnXSMyLshYJrlTuL3",
      "htmlFormattedUrl": "https://open.spotify.com/track/62PaSfnXSMyLshYJrlTuL3",
      "pagemap": {
        "cse_thumbnail": [
          {
            "src": "https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcSh9vMzp8aTy2gV6n9BhhzjZx_x1-rxMmUAdBgwRWtWoXVp3QdWHFsnri8&s",
            "width": "225",
            "height": "225"
          }
        ],
        "metatags": [
          {
            "og:image": "https://i.scdn.co/image/ab67616d0000b27347ce408fb4926d69da6713c2",
            "twitter:card": "summary",
            "og:site_name": "Spotify",
            "al:android:package": "com.spotify.music",
            "al:ios:url": "spotify://track/62PaSfnXSMyLshYJrlTuL3",
            "og:description": "Adele · 25 · Song · 2015",
            "twitter:image": "https://i.scdn.co/image/ab67616d0000b27347ce408fb4926d69da6713c2",
            "al:ios:app_store_id": "324684580",
            "music:album": "https://open.spotify.com/album/3AvPX1B1HiFROvYjLb5Qwi",
            "twitter:site": "@spotify",
            "music:release_date": "2015-11-20",
            "music:duration": "296",
            "og:restrictions:country:allowed": "AR",
            "og:type": "music.song",
            "twitter:title": "Hello",
            "music:album:track": "1",
            "al:ios:app_name": "Spotify",
            "music:musician": "https://open.spotify.com/artist/4dpARuHxo51G3z768sgnrY",
            "og:title": "Hello",
            "og:audio:type": "audio/mpeg",
            "al:android:url": "spotify://track/62PaSfnXSMyLshYJrlTuL3",
            "fb:app_id": "174829003346",
            "viewport": "width=device-width, initial-scale=1",
            "twitter:description": "Adele · 25 · Song · 2015",
            "og:url": "https://open.spotify.com/track/62PaSfnXSMyLshYJrlTuL3",
            "og:audio": "https://p.scdn.co/mp3-preview/27069a2e4ff7be549a241052b7e3233ac835e1f6",
            "al:android:app_name": "Spotify"
          }
        ],
        "cse_image": [
          {
            "src": "https://i.scdn.co/image/ab67616d0000b27347ce408fb4926d69da6713c2"
          }
        ]
      }
    },
    {
      "kind": "customsearch#result",
      "title": "Hello | µ-Ziq - Mike Paradinas - Bandcamp",
      "htmlTitle": "\u003cb\u003eHello\u003c/b\u003e | µ-Ziq - Mike Paradinas - Bandcamp",
      "link": "https://mikeparadinas.bandcamp.com/album/hello",
      "displayLink": "mikeparadinas.bandcamp.com",
      "snippet": "15-track CD \"Hello/Goodbye\" · Compact Disc is fulfilled by Planet Mu and ships out within 5 days · Includes unlimited streaming via the Bandcamp app, plus ...",
      "htmlSnippet": "15-track CD &quot;\u003cb\u003eHello\u003c/b\u003e/Goodbye&quot; &middot; Compact Disc is fulfilled by Planet Mu and ships out within 5 days &middot; Includes unlimited streaming via the Bandcamp app, plus&nbsp;...",
      "formattedUrl": "https://mikeparadinas.bandcamp.com/album/hello",
      "htmlFormattedUrl": "https://mikeparadinas.bandcamp.com/album/\u003cb\u003ehello\u003c/b\u003e",
      "pagemap": {
        "cse_thumbnail": [
          {
            "src": "https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcQ4jwTCdRenGXyNZJUGTfBXZ41T3KcJWKg1j5Gxv5egMvXT1aLV1N2wUtTo&s",
            "width": "194",
            "height": "259"
          }
        ],
        "metatags": [
          {
            "bc-page-properties": "{\"item_type\":\"a\",\"item_id\":3990094370,\"tralbum_page_version\":1,\"page_load\":1781224962}",
            "og:image": "https://f4.bcbits.com/img/a3759043233_5.jpg",
            "video_height": "120",
            "theme-color": "#ffffff",
            "og:type": "album",
            "twitter:card": "player",
            "og:site_name": "Mike Paradinas",
            "og:title": "Hello, by µ-Ziq",
            "video_width": "400",
            "medium": "video",
            "title": "Hello, by µ-Ziq",
            "og:video:secure_url": "https://bandcamp.com/EmbeddedPlayer/v=2/album=3990094370/size=large/tracklist=false/artwork=small/",
            "og:description": "9 track album",
            "og:video:width": "400",
            "video_type": "application/x-shockwave-flash",
            "twitter:player": "https://bandcamp.com/EmbeddedPlayer/v=2/album=3990094370/size=large/linkcol=0084B4/notracklist=true/twittercard=true/",
            "twitter:player:height": "467",
            "twitter:site": "@bandcamp",
            "og:video": "https://bandcamp.com/EmbeddedPlayer/v=2/album=3990094370/size=large/tracklist=false/artwork=small/",
            "viewport": "width=device-width, initial-scale=1",
            "og:video:type": "text/html",
            "og:video:height": "120",
            "og:url": "https://mikeparadinas.bandcamp.com/album/hello",
            "twitter:player:width": "350"
          }
        ],
        "cse_image": [
          {
            "src": "https://f4.bcbits.com/img/0029895606_71.jpg"
          }
        ]
      }
    },
    {
      "kind": "customsearch#result",
      "title": "Hello - Wikipedia",
      "htmlTitle": "\u003cb\u003eHello\u003c/b\u003e - Wikipedia",
      "link": "https://en.wikipedia.org/wiki/Hello",
      "displayLink": "en.wikipedia.org",
      "snippet": "Hello is a salutation or greeting in the English language. It is first attested in writing from 1826.",
      "htmlSnippet": "\u003cb\u003eHello\u003c/b\u003e is a salutation or greeting in the English language. It is first attested in writing from 1826.",
      "formattedUrl": "https://en.wikipedia.org/wiki/Hello",
      "htmlFormattedUrl": "https://en.wikipedia.org/wiki/\u003cb\u003eHello\u003c/b\u003e",
      "pagemap": {
        "metatags": [
          {
            "referrer": "origin",
            "og:image": "https://upload.wikimedia.org/wikipedia/commons/b/b3/TelephoneHelloNellie.jpg",
            "theme-color": "#eaecf0",
            "og:image:width": "705",
            "og:type": "website",
            "viewport": "width=device-width, initial-scale=1.0, user-scalable=yes, minimum-scale=0.25, maximum-scale=5.0",
            "og:title": "Hello - Wikipedia",
            "og:image:height": "1200",
            "format-detection": "telephone=no"
          }
        ]
      }
    },
    {
      "kind": "customsearch#result",
      "title": "Hello Magazine - Highlights for Children",
      "htmlTitle": "\u003cb\u003eHello\u003c/b\u003e Magazine - Highlights for Children",
      "link": "https://shop.highlights.com/hello-magazines-subscription",
      "displayLink": "shop.highlights.com",
      "snippet": "Highlights Hello Magazine is a special baby and toddler magazine filled with fun stories and baby activities. Subscribe today and share the joy of reading.",
      "htmlSnippet": "Highlights \u003cb\u003eHello\u003c/b\u003e Magazine is a special baby and toddler magazine filled with fun stories and baby activities. Subscribe today and share the joy of reading.",
      "formattedUrl": "https://shop.highlights.com/hello-magazines-subscription",
      "htmlFormattedUrl": "https://shop.highlights.com/\u003cb\u003ehello\u003c/b\u003e-magazines-subscription",
      "pagemap": {
        "offer": [
          {
            "pricecurrency": "USD",
            "price": "48",
            "availability": "http://schema.org/InStock"
          }
        ],
        "cse_thumbnail": [
          {
            "src": "https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcTbGXir0_eJMycIwmg87VELr8Gv2ik82XQfaodNiYj9z3KpCD4wakcP5dg&s",
            "width": "264",
            "height": "191"
          }
        ],
        "thumbnail": [
          {
            "src": "https://shop.highlights.com/media/catalog/product/0/0/001-st-pdpmi-10950_pdp-main-images-evergreen_hello.jpg?optimize=low&fit=bounds&height=&width=",
            "name": "Hello Magazine - 1 Year"
          }
        ],
        "product": [
          {
            "image": "https://shop.highlights.com/media/catalog/product/f/y/fy27722-st-pdpmi-12416_main-image-pdps-magazines_hello.jpg?optimize=low&fit=bounds&height=&width=",
            "name": "Hello Magazine - 1 Year",
            "description": "Highlights Hello Magazine is filled with fun stories and baby activities for ages 0-2. Highlights magazines for kids are expertly crafted to show little ones the joy of reading.",
            "sku": "HHO2020SP",
            "brand": "highlights"
          }
        ],
        "aggregaterating": [
          {
            "ratingvalue": "4.8",
            "reviewcount": "2333"
          }
        ],
        "metatags": [
          {
            "p:domain_verify": "isqcl7j72dAGPYrrl6TaYLWgtpL7nA64",
            "og:image": "https://shop.highlights.com/media/catalog/product/f/y/fy27722-st-pdpmi-12416_main-image-pdps-magazines_hello.jpg?optimize=low&fit=bounds&height=265&width=265",
            "og:type": "product",
            "viewport": "width=device-width, initial-scale=1",
            "og:title": "Hello Magazine - 1 Year",
            "product:price:currency": "USD",
            "product:price:amount": "48",
            "title": "Highlights Hello Magazine | Highlights for Children",
            "og:url": "https://shop.highlights.com/hello-magazines-subscription",
            "og:description": "Highlights Hello Magazine is filled with fun stories and baby activities for ages 0-2. Highlights magazines for kids are expertly crafted to show little ones the joy of reading.",
            "format-detection": "telephone=no"
          }
        ],
        "pricespecification": [
          {
            "pricecurrency": "USD",
            "price": "48.000000"
          }
        ],
        "cse_image": [
          {
            "src": "https://shop.highlights.com/static/version1781176748/frontend/Highlightsp2/shop/en_US/images/cart.svg"
          }
        ],
        "hproduct": [
          {
            "fn": "Hello Magazine - 1 Year",
            "description": "Highlights Hello Magazine is filled with fun stories and baby activities for ages 0-2. Highlights magazines for kids are expertly crafted to show little ones the joy of reading.",
            "photo": "https://shop.highlights.com/media/catalog/product/f/y/fy27722-st-pdpmi-12416_main-image-pdps-magazines_hello.jpg?optimize=low&fit=bounds&height=&width=",
            "currency": "USD",
            "currency_iso4217": "840"
          }
        ]
      }
    },
    {
      "kind": "customsearch#result",
      "title": "Hello (Adele song) - Wikipedia",
      "htmlTitle": "\u003cb\u003eHello\u003c/b\u003e (Adele song) - Wikipedia",
      "link": "https://en.wikipedia.org/wiki/Hello_(Adele_song)",
      "displayLink": "en.wikipedia.org",
      "snippet": "\"Hello\" is a song recorded by British singer-songwriter Adele, released on 23 October 2015 by XL Recordings as the lead single from her third studio album, 25 ...",
      "htmlSnippet": "&quot;\u003cb\u003eHello\u003c/b\u003e&quot; is a song recorded by British singer-songwriter Adele, released on 23 October 2015 by XL Recordings as the lead single from her third studio album, 25&nbsp;...",
      "formattedUrl": "https://en.wikipedia.org/wiki/Hello_(Adele_song)",
      "htmlFormattedUrl": "https://en.wikipedia.org/wiki/\u003cb\u003eHello\u003c/b\u003e_(Adele_song)",
      "pagemap": {
        "metatags": [
          {
            "referrer": "origin",
            "og:image": "https://upload.wikimedia.org/wikipedia/en/8/85/Adele_-_Hello_%28Official_Single_Cover%29.png",
            "theme-color": "#eaecf0",
            "og:image:width": "1200",
            "og:type": "website",
            "viewport": "width=device-width, initial-scale=1.0, user-scalable=yes, minimum-scale=0.25, maximum-scale=5.0",
            "og:title": "Hello (Adele song) - Wikipedia",
            "og:image:height": "1200",
            "format-detection": "telephone=no"
          }
        ]
      }
    },
    {
      "kind": "customsearch#result",
      "title": "Confused about Windows Hello as MFA, how does it protect account?",
      "htmlTitle": "Confused about Windows \u003cb\u003eHello\u003c/b\u003e as MFA, how does it protect account?",
      "link": "https://www.reddit.com/r/sysadmin/comments/1jm6bbt/confused_about_windows_hello_as_mfa_how_does_it/",
      "displayLink": "www.reddit.com",
      "snippet": "Mar 28, 2025 ... When you enable hello it adds another layer of protection using biometrics to make a trusted passkey that does not require the password/MFA ...",
      "htmlSnippet": "Mar 28, 2025 \u003cb\u003e...\u003c/b\u003e When you enable \u003cb\u003ehello\u003c/b\u003e it adds another layer of protection using biometrics to make a trusted passkey that does not require the password/MFA&nbsp;...",
      "formattedUrl": "https://www.reddit.com/.../confused_about_windows_hello_as_mfa_how_d...",
      "htmlFormattedUrl": "https://www.reddit.com/.../confused_about_windows_\u003cb\u003ehello\u003c/b\u003e_as_mfa_how_d...",
      "pagemap": {
        "metatags": [
          {
            "og:image": "https://share.redd.it/preview/post/1jm6bbt",
            "theme-color": "#000000",
            "og:image:width": "1200",
            "og:type": "website",
            "og:image:alt": "An image containing a preview of the post",
            "twitter:card": "summary_large_image",
            "twitter:title": "r/sysadmin on Reddit: Confused about Windows Hello as MFA, how does it protect account?",
            "og:site_name": "Reddit",
            "og:title": "r/sysadmin on Reddit: Confused about Windows Hello as MFA, how does it protect account?",
            "og:image:height": "630",
            "msapplication-navbutton-color": "#000000",
            "og:description": "Posted by u/I3igAl - 52 votes and 35 comments",
            "twitter:image": "https://share.redd.it/preview/post/1jm6bbt",
            "apple-mobile-web-app-status-bar-style": "black",
            "twitter:site": "@reddit",
            "viewport": "width=device-width, initial-scale=1, viewport-fit=cover",
            "apple-mobile-web-app-capable": "yes",
            "og:ttl": "600",
            "og:url": "https://www.reddit.com/r/sysadmin/comments/1jm6bbt/confused_about_windows_hello_as_mfa_how_does_it/?seeker-session=true"
          }
        ]
      }
    }
  ]
}
```

#### 🔹 kind
Type of response returned by Google API. Always: `customsearch#search`

#### 🔹 url
Contains internal request template used by Google.

```json
{
  "type": "application/json",
  "template": "https://www.googleapis.com/customsearch/v1?q={searchTerms}"
}
```

#### 🔹 queries
Contains pagination and query metadata.

```json
{
  "request": [],
  "nextPage": []
}
```

**request** - Information about current query:
- `searchTerms` → user query
- `totalResults` → estimated results count
- `startIndex` → current page index

**nextPage** - Used for pagination:
- `startIndex` → next page starting index

#### 🔹 context

```json
{
  "title": "Search Engine Name"
}
```

Represents custom search engine title.

#### 🔹 searchInformation

```json
{
  "searchTime": 0.42,
  "formattedSearchTime": "0.42",
  "totalResults": "2410000000",
  "formattedTotalResults": "2,410,000,000"
}
```

- `searchTime` → time taken for query
- `totalResults` → estimated number of results

#### 🔹 items (SEARCH RESULTS)

Each item represents a search result.

```json
{
  "kind": "customsearch#result",
  "title": "Result Title",
  "link": "https://example.com",
  "displayLink": "example.com",
  "snippet": "Short description",
  "htmlSnippet": "HTML formatted description",
  "formattedUrl": "https://example.com",
  "pagemap": {}
}
```

---

## 📦 PAGEMAP (EXTRA DATA)

The `pagemap` field may contain additional structured metadata such as:

- `cse_image` → preview image
- `cse_thumbnail` → thumbnail image
- `metatags` → OpenGraph / SEO metadata
- `videoobject` → video information (if available)
- `product` → product-related data (if available)

This field varies depending on the type of search result.

---

## 🔁 PAGINATION

Google returns results in pages of 10 items.

| Page | start |
|------|-------|
| 1    | 1     |
| 2    | 11    |
| 3    | 21    |

Example usage:

```
?q=hello&start=1
?q=hello&start=11
?q=hello&start=21
```

---

## 🐍 PYTHON EXAMPLE

```python
import requests

def search(query):
    url = "https://www.googleapis.com/customsearch/v1"
    params = {
        "key": "AIzaSyCNNgFq67GsLtCH18fHPHbsyDWXER1zcG0",
        "cx": "b3afb02f3f21a4152",
        "q": query
    }

    response = requests.get(url, params=params)
    return response.json()

data = search("hello")

for item in data.get("items", []):
    print(item["title"])
    print(item["link"])
```

---

## 🌐 JAVASCRIPT EXAMPLE

```javascript
async function search(query) {
  const url = `https://www.googleapis.com/customsearch/v1?key=AIzaSyCNNgFq67GsLtCH18fHPHbsyDWXER1zcG0&cx=b3afb02f3f21a4152&q=${query}`;
  const res = await fetch(url);
  return res.json();
}

search("hello").then(console.log);
```

---

## 🔐 SECURITY WARNING

- Never expose API keys in frontend code
- Always use environment variables in real projects
- Restrict API keys in Google Cloud Console
- Rotate keys if they are exposed

---

## 🌍 REFERENCE

- **Live Demo:** https://google-search.vercel.app/
- **Google Custom Search API Documentation:** https://developers.google.com/custom-search/v1/overview

---

## FINAL NOTE

This project is experimental and educational.
Use it responsibly and understand that it may stop working without notice due to external API changes or restrictions.
