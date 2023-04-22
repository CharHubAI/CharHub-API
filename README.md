# CharHub API Documentation/Information

### OpenAPI Documentation
The public-intended endpoints are documented at https://api.characterhub.org/openapi. 
Currently, the only endpoints intended for public use are read-only operations on the latest version of publicly accessible characters and lorebooks.
This will change in the coming weeks.

### Usage
To recreate something similar to the homepage of the site, you would use:
- Something like https://api.characterhub.org/api/characters/search?first=30&page=1&sort=last_activity_at&asc=false&include_forks=false&nsfw=false
- Then for each tile, the download link would be something equivalent to:
```
curl -X 'POST'   'https://api.characterhub.org/api/characters/download' 
-H 'accept: /'   -H 'Content-Type: application/json'   -d '{
  "format": "tavern",
  "fullPath": "Anonymous/example-character",
  "version": "main"
}' --output anonymous_example_char_main.png
```

The process for lorebooks would be virtually the same. 


### Terms/Conditions of Usage
To use the API, you agree that:
1. You won't be bulk-downloading definitions and re-serving them from a different server.
2. The API and definitions will not be used for any commercial purpose whatsoever.
3. If used in an application, there will be some type of icon or indicator with a link to the site (e.g. 'Courtesy of [CharHub](https://www.characterhub.org/)') in the portions of your application using the API.
4. You agree to the Terms and Conditions and Privacy Policy of the site itself.
5. You will not use any endpoint not explicitly documented in the OpenAPI specification (obviously I can't fully prevent this, but it's annoying and can cause data integrity issues).

### Feedback/Questions/Requests
Email: [lore@characterhub.org](mailto:lore@characterhub.org)

Discord: [CharHub Server](https://discord.gg/5byUMguqDA) or [lloorree#4237](https://discordapp.com/users/lloorree#4237)
