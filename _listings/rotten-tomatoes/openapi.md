swagger: "2.0"
x-collection-name: Rotten Tomatoes
x-complete: 1
info:
  title: Rotten Tomatoes
  description: test-our-api-services-using-io-docs-
  contact:
    name: Mike Ralphson
    url: https://github.com/mermade/mashery2openapi
    email: mike.ralphson@gmail.com
  version: "1.0"
host: api.rottentomatoes.com
basePath: /api/public/v1.0
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /lists/movies.json:
    get:
      summary: Get Lists Movies
      description: Get lists movies.json.
      operationId: getListsMovies.json
      x-api-path-slug: listsmovies-json-get
      responses:
        200:
          description: OK
      tags:
      - Lists
      - Movies
  /lists/movies/box_office.json:
    get:
      summary: Get Lists Movies Box Office
      description: Get lists movies box office.json.
      operationId: getListsMoviesBoxOffice.json
      x-api-path-slug: listsmoviesbox-office-json-get
      parameters:
      - in: query
        name: country
        description: Provides localized data for the selected country (ISO 3166-1
          alpha-2) if available
      - in: query
        name: limit
        description: Limits the number of movies returned
      responses:
        200:
          description: OK
      tags:
      - Lists
      - Movies
      - Box
      - Office
  /lists/movies/in_theaters.json:
    get:
      summary: Get Lists Movies In Theaters
      description: Get lists movies in theaters.json.
      operationId: getListsMoviesInTheaters.json
      x-api-path-slug: listsmoviesin-theaters-json-get
      parameters:
      - in: query
        name: country
        description: Provides localized data for the selected country (ISO 3166-1
          alpha-2) if available
      - in: query
        name: page
        description: The selected page of in theaters movies
      - in: query
        name: page_limit
        description: The amount of movies in theaters to show per page
      responses:
        200:
          description: OK
      tags:
      - Lists
      - Movies
      - In
      - Theaters
  /lists/movies/opening.json:
    get:
      summary: Get Lists Movies Opening
      description: Get lists movies opening.json.
      operationId: getListsMoviesOpening.json
      x-api-path-slug: listsmoviesopening-json-get
      parameters:
      - in: query
        name: country
        description: Provides localized data for the selected country (ISO 3166-1
          alpha-2) if available
      - in: query
        name: limit
        description: Limits the number of opening movies returned
      responses:
        200:
          description: OK
      tags:
      - Lists
      - Movies
      - Opening
  /lists/movies/upcoming.json:
    get:
      summary: Get Lists Movies Upcoming
      description: Get lists movies upcoming.json.
      operationId: getListsMoviesUpcoming.json
      x-api-path-slug: listsmoviesupcoming-json-get
      parameters:
      - in: query
        name: country
        description: Provides localized data for the selected country (ISO 3166-1
          alpha-2) if available
      - in: query
        name: page
        description: The selected page of upcoming movies
      - in: query
        name: page_limit
        description: The amount of upcoming movies to show per page
      responses:
        200:
          description: OK
      tags:
      - Lists
      - Movies
      - Upcoming
  /movies.json:
    get:
      summary: Get Movies
      description: Get movies.json.
      operationId: getMovies.json
      x-api-path-slug: movies-json-get
      parameters:
      - in: query
        name: page
        description: The selected page of movie search results
      - in: query
        name: page_limit
        description: The amount of movie search results to show per page
      - in: query
        name: q
        description: The plain text search query to search for a movie
      responses:
        200:
          description: OK
      tags:
      - Movies
  /movies/{id}.json:
    get:
      summary: Get Movies
      description: Get movies .json.
      operationId: getMovies.json
      x-api-path-slug: moviesid-json-get
      parameters:
      - in: path
        name: id
        description: Movie ID
      responses:
        200:
          description: OK
      tags:
      - Movies
  /movies/{id}/cast.json:
    get:
      summary: Get Movies Cast
      description: Get movies cast.json.
      operationId: getMoviesCast.json
      x-api-path-slug: moviesidcast-json-get
      parameters:
      - in: path
        name: id
        description: Movie ID
      responses:
        200:
          description: OK
      tags:
      - Movies
      - Cast
  /movies/{id}/clips.json:
    get:
      summary: Get Movies Clips
      description: Get movies clips.json.
      operationId: getMoviesClips.json
      x-api-path-slug: moviesidclips-json-get
      parameters:
      - in: path
        name: id
        description: Movie ID
      responses:
        200:
          description: OK
      tags:
      - Movies
      - Clips
  /movies/{id}/reviews.json:
    get:
      summary: Get Movies Reviews
      description: Get movies reviews.json.
      operationId: getMoviesReviews.json
      x-api-path-slug: moviesidreviews-json-get
      parameters:
      - in: query
        name: country
        description: Provides localized data for the selected country (ISO 3166-1
          alpha-2) if available
      - in: path
        name: id
        description: Movie ID
      - in: query
        name: page
        description: The selected page of reviews
      - in: query
        name: page_limit
        description: The number of reviews to show per page
      - in: query
        name: review_type
        description: '3 different review types are possible: all, top_critic and dvd'
      responses:
        200:
          description: OK
      tags:
      - Movies
      - Reviews
  /movies/{id}/similar.json:
    get:
      summary: Get Movies Similar
      description: Get movies similar.json.
      operationId: getMoviesSimilar.json
      x-api-path-slug: moviesidsimilar-json-get
      parameters:
      - in: path
        name: id
        description: Movie ID
      - in: query
        name: limit
        description: Limit the number of similar movies to show
      responses:
        200:
          description: OK
      tags:
      - Movies
      - Similar