# CharHub API Documentation/Information

### OpenAPI Documentation
The public-intended endpoints are documented at (https://api.characterhub.org/openapi)[https://api.characterhub.org/openapi]. 
Currently, the only endpoints intended for public use are read-only operations on publicly accessible characters and lorebooks.
This will change in the coming weeks.

### Usage
To recreate something similar to the homepage of the site, you would use:
- Something like https://api.characterhub.org/api/characters/search?first=30&page=1&sort=last_activity_at&asc=false&include_forks=false&nsfw=false
- Then for each tile, the download link would be something equivalent to:
```
curl -X 'POST'   'https://api.characterhub.org/api/characters/download'   -H 'accept: /'   -H 'Content-Type: application/json'   -d '{
  "format": "tavern",
  "fullPath": "Anonymous/example-character",
  "version": "main"
}' --output anonymous_example_char_main.png
```
