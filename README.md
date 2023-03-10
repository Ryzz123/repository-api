<h3>API REPOSITORY</h3>
<p>Api repository adalah sebuah rest api dimana ada data dummy dan lainnya, kamu dapat menggunakannya di program kamu dan dapat membantu kamu untuk menggunakannya.</p>
<p>Link Api <br> <a href="https://api-repository.vercel.app">https://api-repository.vercel.app</a></p>
<h4><a href="">V 1.1.6</a></h4>

| API | Description | Versi |
|-----------|-------------|-----------|
| Anime | Search dan Ambil anime favorit mu     | <a href="">1.1.6</a>
| Products | Ini adalah sebuah data dummy yang cocok buat kamu pakai di website mu | <a href="">1.1.0</a>
| Movie | Ini adalah movie film kamu dapat mencari film yang terbaru dan terupdate| <a href="">1.1.4</a>
| Ai | Ini adalah api Ai yang dapat kamu pakai untuk kebutuhan development kamu | <a href="">1.1.6</a>

<h3>LIST API</h3>
<h4><a href="">Anime</a></h4>

<p>Search Anime</p>

```http
GET /api/v1/anime
```
| Parameter | Type   | Description    |
|-----------|--------|---------------|
| `q`| string | Search anime |

<p>Response</p>

```json
{
  "pagination": {
    "last_visible_page": 2,
    "has_next_page": true,
    "current_page": 1,
    "items": {
      "count": 25,
      "total": 34,
      "per_page": 25
    }
  },
  "data": [
    {
```

<hr>

<p>Get Anime By Id</p>

```http
GET /api/v1/anime/{id}
```
| Parameter | Type   | Description    |
|-----------|--------|---------------|
| `id`| string | Get anime by Id |

<p>Response</p>

```json
{
  "data": {
    "mal_id": 24,
    "url": "https://myanimelist.net/anime/24/School_Rumble",
    "images": {
      "jpg": {
        "image_url": "https://cdn.myanimelist.net/images/anime/4/75488.jpg",
        "small_image_url": "https://cdn.myanimelist.net/images/anime/4/75488t.jpg",
        "large_image_url": "https://cdn.myanimelist.net/images/anime/4/75488l.jpg"
      },
      "webp": {
        "image_url": "https://cdn.myanimelist.net/images/anime/4/75488.webp",
        "small_image_url": "https://cdn.myanimelist.net/images/anime/4/75488t.webp",
        "large_image_url": "https://cdn.myanimelist.net/images/anime/4/75488l.webp"
      }
    }
```

<hr>

<p>Get Anime By Id Characters</p>

```http
GET /api/v1/anime/{id}/characters
```
| Parameter | Type   | Description    |
|-----------|--------|---------------|
| `id`| string | Get anime by Id characters |

<p>Response</p>

```json
{
  "data": [
    {
      "character": {
        "mal_id": 199,
        "url": "https://myanimelist.net/character/199/Kenji_Harima",
        "images": {
          "jpg": {
            "image_url": "https://cdn.myanimelist.net/images/characters/10/29703.jpg?s=00548c794bdaea53a9ebaac70681bebf"
          },
          "webp": {
            "image_url": "https://cdn.myanimelist.net/images/characters/10/29703.webp?s=00548c794bdaea53a9ebaac70681bebf",
            "small_image_url": "https://cdn.myanimelist.net/images/characters/10/29703t.webp?s=00548c794bdaea53a9ebaac70681bebf"
          }
        },
        "name": "Harima, Kenji"
      }
```

<hr>

<p>Get Anime By Id Episodes</p>

```http
GET /api/v1/anime/{id}/episodes
```
| Parameter | Type   | Description    |
|-----------|--------|---------------|
| `id`| string | Get anime by Id Episodes |

<p>Response</p>

```json
{
  "pagination": {
    "last_visible_page": 1,
    "has_next_page": true
  },
  "data": [
    {
      "mal_id": 1,
      "url": "https://myanimelist.net/anime/24/School_Rumble/episode/1",
      "title": "The New School Year! Be Still My Heart! / Love Letter Mayhem! / Warp Speed on a Bike!",
      "title_japanese": "????????????????????????! / ??????????????????????????????! / ???????????????????????????!",
      "title_romanji": "Shingakki de Dokidoki! / Love Letter de Jitabata! / Jitensha de Dokyuun!??",
      "aired": "2004-10-05T00:00:00+00:00",
      "score": 4.4,
      "filler": false,
      "recap": false,
      "forum_url": "https://myanimelist.net/forum/?topicid=37357"
    }
```

<hr>

<p>Get Anime By Id Videos</p>

```http
GET /api/v1/anime/{id}/videos
```
| Parameter | Type   | Description    |
|-----------|--------|---------------|
| `id`| string | Get anime by Id Videos |

<p>Response</p>

```json
{
  "data": {
    "promo": [
      {
        "title": "PV English dub version",
        "trailer": {
          "youtube_id": "0Uv3_zjM448",
          "url": "https://www.youtube.com/watch?v=0Uv3_zjM448",
          "embed_url": "https://www.youtube.com/embed/0Uv3_zjM448?enablejsapi=1&wmode=opaque&autoplay=1",
          "images": {
            "image_url": "https://img.youtube.com/vi/0Uv3_zjM448/default.jpg",
            "small_image_url": "https://img.youtube.com/vi/0Uv3_zjM448/sddefault.jpg",
            "medium_image_url": "https://img.youtube.com/vi/0Uv3_zjM448/mqdefault.jpg",
            "large_image_url": "https://img.youtube.com/vi/0Uv3_zjM448/hqdefault.jpg",
            "maximum_image_url": "https://img.youtube.com/vi/0Uv3_zjM448/maxresdefault.jpg"
          }
        }
      }
```

<hr>

<p>Get Anime By Id Videos episodes</p>

```http
GET /api/v1/anime/{id}/videos/episodes
```
| Parameter | Type   | Description    |
|-----------|--------|---------------|
| `id`| string | Get anime by Id Videos episodes |

<p>Response</p>

```json
{
  "pagination": {
    "last_visible_page": 1,
    "has_next_page": false
  },
  "data": [
    {
      "mal_id": 26,
      "title": "School Rumble Forever!",
      "episode": "Episode 26",
      "url": "https://myanimelist.net/anime/24/School_Rumble/episode/26",
      "images": {
        "jpg": {
          "image_url": null
        }
      }
    }
```

<hr>

<p>Get Anime By Id Pictures</p>

```http
GET /api/v1/anime/{id}/pictures
```
| Parameter | Type   | Description    |
|-----------|--------|---------------|
| `id`| string | Get anime by Id pictures |

<p>Response</p>

```json
{
  "data": [
    {
      "jpg": {
        "image_url": "https://cdn.myanimelist.net/images/anime/9/20417.jpg",
        "small_image_url": "https://cdn.myanimelist.net/images/anime/9/20417t.jpg",
        "large_image_url": "https://cdn.myanimelist.net/images/anime/9/20417l.jpg"
      },
      "webp": {
        "image_url": "https://cdn.myanimelist.net/images/anime/9/20417.webp",
        "small_image_url": "https://cdn.myanimelist.net/images/anime/9/20417t.webp",
        "large_image_url": "https://cdn.myanimelist.net/images/anime/9/20417l.webp"
      }
    }
```

<hr>

<p>Get Anime By Id Recommendations</p>

```http
GET /api/v1/anime/{id}/recommendations
```
| Parameter | Type   | Description    |
|-----------|--------|---------------|
| `id`| string | Get anime by Id recommendations |

<p>Response</p>

```json
{
  "data": [
    {
      "entry": {
        "mal_id": 4224,
        "url": "https://myanimelist.net/anime/4224/Toradora",
        "images": {
          "jpg": {
            "image_url": "https://cdn.myanimelist.net/images/anime/13/22128.jpg?s=08c2b1b4a465fc43cbe15aae4a425b78",
            "small_image_url": "https://cdn.myanimelist.net/images/anime/13/22128t.jpg?s=08c2b1b4a465fc43cbe15aae4a425b78",
            "large_image_url": "https://cdn.myanimelist.net/images/anime/13/22128l.jpg?s=08c2b1b4a465fc43cbe15aae4a425b78"
          }
```

<hr>

<p>Search Anime Karakter</p>

```http
GET /api/v1/character
```
| Parameter | Type   | Description    |
|-----------|--------|---------------|
| `q`| string | Search karakter |

<p>Response</p>

```json
{
  "pagination": {
    "last_visible_page": 1,
    "has_next_page": false,
    "current_page": 1,
    "items": {
      "count": 8,
      "total": 8,
      "per_page": 25
    }
  },
  "data": [
    {
```

<hr>

<p>Search Clubs</p>

```http
GET /api/v1/clubs
```
| Parameter | Type   | Description    |
|-----------|--------|---------------|
| `q`| string | Search Clubs |

<p>Response</p>

```json
{
  "pagination": {
    "last_visible_page": 21,
    "has_next_page": true
  },
  "data": [
    {
      "mal_id": 1,
      "url": "https://myanimelist.net/clubs.php?cid=1",
      "images": {
        "jpg": {
          "image_url": "https://cdn.myanimelist.net/images/clubs/16/222057.jpg"
        }
      },
      "name": "Cowboy Bebop",
      "members": 1384,
      "category": "anime",
      "created": "2007-03-29T00:00:00+00:00",
      "access": "public"
    },
```

<hr>

<p>Search Manga</p>

```http
GET /api/v1/manga
```
| Parameter | Type   | Description    |
|-----------|--------|---------------|
| `q`| string | Search anime manga |

<p>Response</p>

```json
{
  "pagination": {
    "last_visible_page": 2503,
    "has_next_page": true,
    "current_page": 1,
    "items": {
      "count": 25,
      "total": 62557,
      "per_page": 25
    }
  },
  "data": [
    {
```

<hr>

<p>Search People</p>

```http
GET /api/v1/people
```
| Parameter | Type   | Description    |
|-----------|--------|---------------|
| `q`| string | Search people |

<p>Response</p>

```json
{
  "pagination": {
    "last_visible_page": 1925,
    "has_next_page": true
  },
  "data": [
    {
      "mal_id": 1,
      "url": "https://myanimelist.net/people/1/Tomokazu_Seki",
      "website_url": null,
      "images": {
        "jpg": {
          "image_url": "https://cdn.myanimelist.net/images/voiceactors/1/55486.jpg"
        }
      },
      "name": "Tomokazu Seki",
      "given_name": "??????",
      "family_name": "???",
      "alternate_names": [
        "Seki Mondoya",
        "?????? ???",
        "Monto Hiraku"
      ],
```

<hr>

<p>Get Anime Genres</p>

```http
GET /api/v1/genres/anime
```
| Parameter | Type   | Description    |
|-----------|--------|---------------|
| `null`| null | Get anime dan genres |

<p>Response</p>

```json
{
  "data": [
    {
      "mal_id": 1,
      "name": "Action",
      "url": "https://myanimelist.net/anime/genre/1/Action",
      "count": 4520
    },
    {
      "mal_id": 2,
      "name": "Adventure",
      "url": "https://myanimelist.net/anime/genre/2/Adventure",
      "count": 3752
    },
```

<hr>

<p>Get Manga genres</p>

```http
GET /api/v1/genres/manga
```
| Parameter | Type   | Description    |
|-----------|--------|---------------|
| `null`| null | Get genres manga |

<p>Response</p>

```json
{
  "data": [
    {
      "mal_id": 1,
      "name": "Action",
      "url": "https://myanimelist.net/anime/genre/1/Action",
      "count": 4520
    },
    {
      "mal_id": 2,
      "name": "Adventure",
      "url": "https://myanimelist.net/anime/genre/2/Adventure",
      "count": 3752
    },
```

<hr>

<p>Get Magazines</p>

```http
GET /api/v1/magazines
```
| Parameter | Type   | Description    |
|-----------|--------|---------------|
| `q`| string | Get magazines |

<p>Response</p>

```json
"data": [
    {
      "mal_id": 1,
      "name": "Big Comic Original",
      "url": "https://myanimelist.net/manga/magazine/1/Big_Comic_Original",
      "count": 69
    },
    {
      "mal_id": 2,
      "name": "Young Animal",
      "url": "https://myanimelist.net/manga/magazine/2/Young_Animal",
      "count": 145
    },
```

<h4><a href="">Products Store</a></h4>

<p>Get All Products</p>

```http
GET /api/v1/products
```
| Parameter | Type   | Description    |
|-----------|--------|---------------|
| `null`| null | Get Products dummy |

<p>Response</p>

```json
[
  {
    "id": 1,
    "title": "Fjallraven - Foldsack No. 1 Backpack, Fits 15 Laptops",
    "price": 109.95,
    "description": "Your perfect pack for everyday use and walks in the forest. Stash your laptop (up to 15 inches) in the padded sleeve, your everyday",
    "category": "men's clothing",
    "image": "https://fakestoreapi.com/img/81fPKd-2AYL._AC_SL1500_.jpg",
    "rating": {
      "rate": 3.9,
      "count": 120
    }
  },
```

<hr>

<p>Get Products By Id</p>

```http
GET /api/v1/products/{id}
```
| Parameter | Type   | Description    |
|-----------|--------|---------------|
| `id`| string | Get Products dummy by id |

<p>Response</p>

```json
{
  "id": 7,
  "title": "White Gold Plated Princess",
  "price": 9.99,
  "description": "Classic Created Wedding Engagement Solitaire Diamond Promise Ring for Her. Gifts to spoil your love more for Engagement, Wedding, Anniversary, Valentine's Day...",
  "category": "jewelery",
  "image": "https://fakestoreapi.com/img/71YAIFU48IL._AC_UL640_QL65_ML3_.jpg",
  "rating": {
    "rate": 3,
    "count": 400
  }
}
```

<hr>

<p>Get Products Limit</p>

```http
GET /api/v1/short/products
```
| Parameter | Type   | Description    |
|-----------|--------|---------------|
| `limit`| int | Set limit data |

<p>Response</p>

```json
{
    "id": 2,
    "title": "Mens Casual Premium Slim Fit T-Shirts ",
    "price": 22.3,
    "description": "Slim-fitting style, contrast raglan long sleeve, three-button henley placket, light weight & soft fabric for breathable and comfortable wearing. And Solid stitched shirts with round neck made for durability and a great fit for casual fashion wear and diehard baseball fans. The Henley style round neckline includes a three-button placket.",
    "category": "men's clothing",
    "image": "https://fakestoreapi.com/img/71-3HjGNDUL._AC_SY879._SX._UX._SY._UY_.jpg",
    "rating": {
      "rate": 4.1,
      "count": 259
    }
  }
```

<hr>

<p>Get All Categories</p>

```http
GET /api/v1/categories
```
| Parameter | Type   | Description    |
|-----------|--------|---------------|
| `null`| null | Get all categories Products |

<p>Response</p>

```json
[
  "electronics",
  "jewelery",
  "men's clothing",
  "women's clothing"
]
```

<hr>

<p>Get Products where categories</p>

```http
GET /api/v1/categories/electronics
```
| Parameter | Type   | Description    |
|-----------|--------|---------------|
| `null`| null | Get Products where categories |

<p>Response</p>

```json
[
  {
    "id": 9,
    "title": "WD 2TB Elements Portable External Hard Drive - USB 3.0 ",
    "price": 64,
    "description": "USB 3.0 and USB 2.0 Compatibility Fast data transfers Improve PC Performance High Capacity; Compatibility Formatted NTFS for Windows 10, Windows 8.1, Windows 7; Reformatting may be required for other operating systems; Compatibility may vary depending on user???s hardware configuration and operating system",
    "category": "electronics",
    "image": "https://fakestoreapi.com/img/61IBBVJvSDL._AC_SY879_.jpg",
    "rating": {
      "rate": 3.3,
      "count": 203
    }
  },
```

<h4><a href="">Movies</a></h4>

<p>Search movies</p>

```http
GET /api/v1/search/movie
```
| Parameter | Type   | Description    |
|-----------|--------|---------------|
| `query`| string | Search your movies |

<p>Response</p>

```json
{
  "page": 1,
  "results": [
    {
      "adult": false,
      "backdrop_path": "/rH3jY9JN9krUyE0Q3WLNtujMs8.jpg",
      "genre_ids": [
        28,
        12,
        878
      ],
      "id": 667538,
      "original_language": "en",
      "original_title": "Transformers: Rise of the Beasts",
      "overview": "A ???90s globetrotting adventure that introduces the Maximals, Predacons, and Terrorcons to the existing battle on earth between Autobots and Decepticons.",
      "popularity": 185.686,
      "poster_path": "/qBcIUgJmDGrcAKbhRwCd6AmO0ZW.jpg",
      "release_date": "2023-06-07",
      "title": "Transformers: Rise of the Beasts",
      "video": false,
      "vote_average": 0,
      "vote_count": 0
    },
```

<hr>

<p>Get Movies Yang lagi tayang</p>

```http
GET /api/v1/movie/now_playing
```
| Parameter | Type   | Description    |
|-----------|--------|---------------|
| `null`| null | Get Movies Now Playing |

<p>Response</p>

```json 
{
  "dates": {
    "maximum": "2023-02-03",
    "minimum": "2022-12-17"
  },
  "page": 1,
  "results": [
    {
      "adult": false,
      "backdrop_path": "/faXT8V80JRhnArTAeYXz0Eutpv9.jpg",
      "genre_ids": [
        16,
        28,
        12,
        35,
        10751,
        14
      ],
      "id": 315162,
      "original_language": "en",
      "original_title": "Puss in Boots: The Last Wish",
```

<hr>

<p>Get Movies Yang paling populer </p>

```http
GET /api/v1/movie/popular
```
| Parameter | Type   | Description    |
|-----------|--------|---------------|
| `null`| null | Get Movies popular  |

<p>Response</p>

```json
{
      "adult": false,
      "backdrop_path": "/s16H6tpK2utvwDtzZ8Qy4qm5Emw.jpg",
      "genre_ids": [
        878,
        12,
        28
      ],
      "id": 76600,
      "original_language": "en",
      "original_title": "Avatar: The Way of Water",
      "overview": "Set more than a decade after the events of the first film, learn the story of the Sully family (Jake, Neytiri, and their kids), the trouble that follows them, the lengths they go to keep each other safe, the battles they fight to stay alive, and the tragedies they endure.",
      "popularity": 2598.476,
      "poster_path": "/t6HIqrRAclMCA60NsSmeqe9RmNV.jpg",
      "release_date": "2022-12-14",
      "title": "Avatar: The Way of Water",
      "video": false,
      "vote_average": 7.7,
      "vote_count": 4759
    }
```

<hr>

<p>Get Movies Yang akan datang</p>

```http
GET /api/v1/movie/upcoming
```
| Parameter | Type   | Description    |
|-----------|--------|---------------|
| `null`| null | Get movies up coming |

<p>Response</p>

```json
    {
"id": 980078,
      "original_language": "en",
      "original_title": "Winnie-the-Pooh: Blood and Honey",
      "overview": "Christopher Robin is headed off to college and he has abandoned his old friends, Pooh and Piglet, which then leads to the duo embracing their inner monsters.",
      "popularity": 474.692,
      "poster_path": "/wtFwgFFk1ze789ghcadWGEVjj3N.jpg",
      "release_date": "2023-01-27",
      "title": "Winnie-the-Pooh: Blood and Honey",
      "video": false,
      "vote_average": 6,
      "vote_count": 1
    }
```

<hr>

<p>Get Movies berdasarkan genres</p>

```http
GET /api/v1/genre/movie/list
```
| Parameter | Type   | Description    |
|-----------|--------|---------------|
| `null`| null | Get Movies berdasarkan genres |

<p>Response</p>

```json
    {
      "id": 1024546,
      "original_language": "en",
      "original_title": "Detective Knight: Rogue",
      "overview": "As Los Angeles prepares for Halloween, mask-wearing armed robbers critically wound detective James Knight???s partner in a shootout following a heist. With Knight in hot pursuit, the bandits flee L.A. for New York, where the detective???s dark past collides with his present case and threatens to tear his world apart???unless redemption can claim Knight first.",
      "popularity": 767.968,
      "poster_path": "/2wj5iUJ2B5AQ1lFctJgUrHHsp9B.jpg",
      "release_date": "2022-10-21",
      "title": "Detective Knight: Rogue",
      "video": false,
      "vote_average": 6.8,
      "vote_count": 59
    }
```

<h4><a href="">Ai</a></h4>

<p>Post sebuah kata ke ai</p>

```http
POST /api/v1/response/text
```
| Body | Type   | Description    |
|-----------|--------|---------------|
| `request`| string | Terima response dari ai bot |

<p>Response</p>

```json
{
  "result": " Christopher Columbus"
}
```

<hr>

<p>Post sebuah kata ke ai untuk meminta gambar</p>

```http
POST /api/v1/response/image
```
| Body | Type   | Description    |
|-----------|--------|---------------|
| `request`| string | Terima response gambar dari ai bot |

<p>Response</p>

```json
{
  "result": "https:\/\/oaidalleapiprodscus.blob.core.windows.net\/private\/org-aIzlAKPyzUxd6VfuzHt8Mzti\/user-VGw9ermKPdvywwNjce4BVSsP\/img-pa2SWXWMmyu1M7aIo2SGdzTu.png?st=2023-01-29T23%3A02%3A19Z&se=2023-01-30T01%3A02%3A19Z&sp=r&sv=2021-08-06&sr=b&rscd=inline&rsct=image\/png&skoid=6aaadede-4fb3-4698-a8f6-684d7786b067&sktid=a48cca56-e6da-484e-a814-9c849652bcb3&skt=2023-01-29T18%3A26%3A17Z&ske=2023-01-30T18%3A26%3A17Z&sks=b&skv=2021-08-06&sig=53tIUmxIWjt6MoXlKLMebAyQ0AV9WdwlQCdLyOKbQZg%3D"
}
```
