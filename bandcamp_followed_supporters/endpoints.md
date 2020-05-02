- HTML selector `#collectors-data[data-blob]`

```json
{
  "thumbs": [
    {
      "username": "fanusername",
      "image_id": 8669314,
      "name": "example fan",
    }
  ],
  "band_thanks_text": "supported by",
  "more_reviews_available": false,
  "shown_reviews": [],
  "reviews": [],
  "more_thumbs_available": true,
  "shown_thumbs": [
    {
      "username": "fanusername",
      "image_id": 8669314,
      "name": "example fan",
    }
  ]
}
```

---

- POST: `https://bandcamp.com/api/tralbumcollectors/2/thumbs`
- POST data: `{"tralbum_type":"a","tralbum_id":3724680000,"token":"1:1570960703:437713:0:0:0","count":80}`
  + token is of the format `token_version:timestamp:fan_id:?:?:?`
  + token_version should be 1, 0 is rejected by the endpoint
  + to get the first page, token should be omitted: `{"tralbum_type":"a","tralbum_id":3724680000,"count":80}`

```json
{
  "results":[
    {"featured_track_id":null,"fan_id":305634,"username":"fanusername","fav_track_title":null,"url":"https://bandcamp.com/fanusername","token":"1:1570940724:305634:0:0:0","image_id":3385566,"mod_date":"13 Oct 2019 04:25:24 GMT","name":"example fan","is_montage_image":true,"item_type":"a","item_id":3724680000,"why":null}
  ],
  "more_available":false
}
```

---

- GET: `https://bandcamp.com/api/fan/2/collection_summary`

```json
{
  "collection_summary": {
    "fan_id": 1847,
    "username": "fanusername",
    "url": "https://bandcamp.com/fanusername",
    "follows": {
      "following": {
        "674": true,
        "1146": true,
        "1284": true
      }
    }
  }
}
```
