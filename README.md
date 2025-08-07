# alx-project-0x14

## API Overview
The MoviesDatabase API provides access to a comprehensive database of movies, allowing users to search, retrieve, and manage movie-related information. Key features include searching for movies by title, retrieving detailed information about specific movies, and accessing user ratings and reviews.

## Version
1.0.0

## Available Endpoints
- **GET /movies**: Retrieve a list of movies based on search criteria.
- **GET /movies/{id}**: Get detailed information about a specific movie by its ID.
- **POST /movies**: Add a new movie to the database.
- **PUT /movies/{id}**: Update information for an existing movie.
- **DELETE /movies/{id}**: Remove a movie from the database.

## Request and Response Format
### Request Format
- **GET /movies**
  - Query Parameters: `title`, `genre`, `year`
  
### Response Format
- **200 OK**
  ```json
  {
    "movies": [
      {
        "id": "1",
        "title": "Inception",
        "year": "2010",
        "genre": "Sci-Fi"
      }
    ]
  }
  ```

## Authentication
To authenticate requests to the MoviesDatabase API, include an API key in the request headers:
```
Authorization: Bearer YOUR_API_KEY
```

## Error Handling
Common error responses include:
- **400 Bad Request**: The request was invalid. Check the request parameters.
- **401 Unauthorized**: Authentication failed. Ensure the API key is valid.
- **404 Not Found**: The requested resource could not be found.

## Usage Limits and Best Practices
- Rate Limit: 100 requests per hour.
- Best Practices: Cache responses where possible to reduce the number of requests made to the API, and handle errors gracefully to improve user experience.