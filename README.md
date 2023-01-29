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

`
GET /api/v1/anime
`
| Parameter | Type   | Description    |
|-----------|--------|---------------|
| `q`| string | Search anime |

<hr>

<p>Search Anime Karakter</p>

`
GET /api/v1/character
`
| Parameter | Type   | Description    |
|-----------|--------|---------------|
| `q`| string | Search karakter |

<hr>

<p>Search Clubs</p>

`
GET /api/v1/clubs
`
| Parameter | Type   | Description    |
|-----------|--------|---------------|
| `q`| string | Search Clubs |

<hr>

<p>Search Manga</p>

`
GET /api/v1/manga
`
| Parameter | Type   | Description    |
|-----------|--------|---------------|
| `q`| string | Search anime manga |

<hr>

<p>Search People</p>

`
GET /api/v1/people
`
| Parameter | Type   | Description    |
|-----------|--------|---------------|
| `q`| string | Search people |

<hr>

<p>Get Anime Genres</p>

`
GET /api/v1/genres/anime
`
| Parameter | Type   | Description    |
|-----------|--------|---------------|
| `null`| null | Get anime dan genres |

<hr>

<p>Get Manga genres</p>

`
GET /api/v1/genres/manga
`
| Parameter | Type   | Description    |
|-----------|--------|---------------|
| `null`| null | Get genres manga |

<hr>

<p>Get Magazines</p>

`
GET /api/v1/magazines
`
| Parameter | Type   | Description    |
|-----------|--------|---------------|
| `null`| null | Get magazines |

<h4><a href="">Products Store</a></h4>

<p>Get All Products</p>

`
GET /api/v1/products
`
| Parameter | Type   | Description    |
|-----------|--------|---------------|
| `null`| null | Get Products dummy |

<hr>

<p>Get Products By Id</p>

`
GET /api/v1/products/1
`
| Parameter | Type   | Description    |
|-----------|--------|---------------|
| `null`| null | Get Products dummy by id |

<hr>

<p>Get Products Limit</p>

`
GET /api/v1/short/products
`
| Parameter | Type   | Description    |
|-----------|--------|---------------|
| `limit`| int | Set limit data |

<hr>

<p>Get All Categories</p>

`
GET /api/v1/categories
`
| Parameter | Type   | Description    |
|-----------|--------|---------------|
| `null`| null | Get all categories Products |

<hr>

<p>Get Products where categories</p>

`
GET /api/v1/categories/jrewel
`
| Parameter | Type   | Description    |
|-----------|--------|---------------|
| `null`| null | Get Products where categories |

<h4><a href="">Movies</a></h4>

<p>Search movies</p>

`
GET /api/v1/search/movie
`
| Parameter | Type   | Description    |
|-----------|--------|---------------|
| `query`| string | Search your movies |

<hr>

<p>Get Movies Yang lagi tayang</p>

`
GET /api/v1/movie/now_playing
`
| Parameter | Type   | Description    |
|-----------|--------|---------------|
| `null`| null | Get Movies Now Playing |

<hr>

<p>Get Movies Yang paling populer </p>

`
GET /api/v1/movie/popular
`
| Parameter | Type   | Description    |
|-----------|--------|---------------|
| `null`| null | Get Movies popular  |

<hr>

<p>Get Movies Yang akan datang</p>

`
GET /api/v1/movie/upcoming
`
| Parameter | Type   | Description    |
|-----------|--------|---------------|
| `null`| null | Get movies up coming |

<hr>

<p>Get Movies berdasarkan genres</p>

`
GET /api/v1/genre/movie/list
`
| Parameter | Type   | Description    |
|-----------|--------|---------------|
| `null`| null | Get Movies berdasarkan genres |

<h4><a href="">Ai</a></h4>

<p>Post sebuah kata ke ai</p>

`
POST /api/v1/response/text
`
| Body | Type   | Description    |
|-----------|--------|---------------|
| `request`| string | Terima response dari ai bot |

<hr>

<p>Post sebuah kata ke ai untuk meminta gambar</p>

`
POST /api/v1/response/image
`
| Body | Type   | Description    |
|-----------|--------|---------------|
| `request`| string | Terima response gambar dari ai bot |
