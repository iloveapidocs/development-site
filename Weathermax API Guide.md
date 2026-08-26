**1. Prerequisites**

Before you begin, ensure you have:
* A **Weathermax Developer Account**
* An active **API Key** (retrieved from your Acconunt Dashboard)
* **cURL** installed on your system (built into most modern terminals)

**2. Authenticate your requests**

The Weathermax API uses API keys for authentication. You must include your key in the `X-API-Key` HTTP header of every request.

[!WARNING]
Important Keep your API key secure. Do not hardcode it into public client-side code or commit it to GitHub.`

**3. Make your First API Call**

To verify your conenction, request the current weather for a spepcific location using `/current` endpoint.

Open your terminal and run the following **cURL command**. Replace `YOUR_API_KEY` with your actual token:

**bash**
```bash
curl -X GET "https://weathermax.com" \
-H "X-API-Key: YOUR_API_KEY" \
-H "Accept: application/json"`
```
**4. Expected Response**

A successful connection returns a `200 OK` HTTP status code and a JSON payload containing the location's current weather data:

**json**
```js
{
    "location:" {
        "name": "Seattle",
        "region": "Washington",
        "country": "USA"
    },
    "current": {
        "temperature_f": 62.4,
        "condition": "Partly Cloudy",
        "humidity": 71,
        "wind_mph": 8.5
    }
}
```
## Troubleshooting Common Errors
* `401 Unauthorized`: Your `X-API-Key` header is missing, malformed, or inactive. Cheeck your dazshboard to ensure your key is valid.

* `400 Bad Request`: The `location` parameter is missing or improperly formatted.

## Next Steps
* Explore our full API Reference Documentation.
* Download our offical Python and JavaScript SDKs to start building.

Would you like to see how a tech writer would adapt this guide for a **different language** (like Python or Javascript), or do you want to explore the **OpenAPI specification** used to generate it?
