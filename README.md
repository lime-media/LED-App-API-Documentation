# LED App API Documentation

Interactive API documentation for the Lime Media LED App, built with [Swagger UI](https://swagger.io/tools/swagger-ui/).

## Endpoints

The API covers four main areas:

- **Authentication** — login with AES-encrypted credentials to receive a JWT
- **Client Programs** — list and retrieve client programs and their associated markets
- **Trucks** — list and retrieve trucks with issue history
- **Program Schedule** — query shifts, schedule details, and date ranges

## Servers

| Environment | URL |
|-------------|-----|
| Production | `https://app.lime-media.com` |
| Local | `http://localhost:3000` |

## Viewing the Docs

Open `index.html` in a browser — it loads the `swagger.yaml` spec into Swagger UI. No build step or server required.

To serve locally:

```bash
npx serve .
```

## Authentication

1. `POST /api/v1/authentication/authenticate` with AES-encrypted credentials
2. Copy the `token` from the response
3. Use `Authorization: Bearer <token>` on all subsequent requests
