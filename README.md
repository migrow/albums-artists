# Music API

The Music API is a RESTful API utilizing JSON with information on certain albums and the artists that created them.  There will be another piece of documentation that gives information on the artists themselves.  There will be `/artists` and `/albums` endpoints

## Getting Started

## HTTP Verbs
The Music API uses the following commands:
- `GET`
- `POST`
- `PUT`
- `DELETE`

## Endpoints

## Music

## Albums

## Create an Album
Create an album via `POST` to the `/albums` route passing in an album JSON object in the request body.
```
POST /albums

{
  "name": "Send Away the Tigers",
  "genre": "rock",
  "year": "2007",
  "artistId": "artist_manic-street-preachers",
  "type": "album"
}
```
When this is created, a successfully-created album will result in a `201 - Created` response and the album will be returned in the response body.  The response body will include `_id` and `_rev` properties:
```
{
  "_id": "album_send-away-the-tigers",
  "_rev": "1-aldk645shfa893258235hadf",
  "name": "Send Away the Tigers",
  "genre": "rock",
  "year": "2007",
  "artistId": "artist_manic-street-preachers",
  "type": "album"
}
```

## Get an Album
Get an album via `GET` from the `/albums/:id` route, passing in the ID.
```
GET /albums/album_send-away-the-tigers
```
When this is called, a successfully-found item will result in a `200 - OK` response and the album will be returned in the response body.  The response body will include the `_id` and `_rev` properties.

```
{
  "_id": "album_send-away-the-tigers",
  "_rev": "1-aldk645shfa893258235hadf",
  "name": "Send Away the Tigers",
  "genre": "rock",
  "year": "2007",
  "artistId": "artist_manic-street-preachers",
  "type": "album"
}
```

## Delete an Album
Delete an album from the collection of albums via `DELETE` to the `/albums/:id` path.
```
 DELETE /albums/album_send-away-the-tigers
 ```
 When this is called, a successfully-deleted item will result in a `200 - OK` response. The response body will contain a JSON object with properties `ok`, `id`, and `rev`.
 ```
 {
    "ok": true,
    "id": "album_send-away-the-tigers",
    "rev": "1-aldk645shfa893258235hadf"
 }   
 ```
 
 ## Artists

## Create an Artist
Create an artist via `POST` to the `/artists` route passing in an album JSON object in the request body.
```
POST /artists

{
  "name": "Manic Street Preachers",
  "country": "Wales",
  "founded": "1986",
  "description": "A Welsh rock band, formed in 1986 in Blackwood, Caerphilly and consisting of James Dean Bradfield (lead vocals, lead guitar), Nicky Wire (bass guitar, lyrics) and Sean Moore (drums, percussion, soundscapes). They are often colloquially known as the Manics.",
  "type": "artist"
}
```
When this is created, a successfully-created album will result in a `201 - Created` response and the album will be returned in the response body.  The response body will include `_id` and `_rev` properties:
```
{
  "_id": "artist_manic-street-preachers",
  "_rev": "1-lkik645shfa893258235hadf",
   "name": "Manic Street Preachers",
  "country": "Wales",
  "founded": "1986",
  "description": "A Welsh rock band, formed in 1986 in Blackwood, Caerphilly and consisting of James Dean Bradfield (lead vocals, lead guitar), Nicky Wire (bass guitar, lyrics) and Sean Moore (drums, percussion, soundscapes). They are often colloquially known as the Manics.",
  "type": "artist"
}
```

## Get an Artist
Get an artist via `GET` from the `/artists/:id` route, passing in the ID.
```
GET /artists/artists_manic-street-preachers
```
When this is called, a successfully-found item will result in a `200 - OK` response and the album will be returned in the response body.  The response body will include the `_id` and `_rev` properties.

```
{
  "_id": "artist_manic-street-preachers",
  "_rev": "1-lkik645shfa893258235hadf",
  "name": "Manic Street Preachers",
  "country": "Wales",
  "founded": "1986",
  "description": "A Welsh rock band, formed in 1986 in Blackwood, Caerphilly and consisting of James Dean Bradfield (lead vocals, lead guitar), Nicky Wire (bass guitar, lyrics) and Sean Moore (drums, percussion, soundscapes). They are often colloquially known as the Manics.",
  "type": "artist"
}
```

 ## Delete an Artist
 Delete an artist from the collection of artists via `DELETE` to the `/artists/:id` path.
```
 DELETE /artists/artists_manic-street-preachers
 ```
 When this is called, a successfully-deleted item will result in a `200 - OK` response. The response body will contain a JSON object with properties `ok`, `id`, and `rev`.
 ```
  {
    "ok": true,
    "id": "artist_manic-street-preachers",
    "rev": "1-lkik645shfa893258235hadf"
 } 
 ```
