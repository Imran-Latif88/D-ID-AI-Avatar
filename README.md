# D-ID AI Avatar

This repository contains a Fastify-based API server that integrates with D-ID's API to create AI avatars with voice. It allows users to generate talking avatars using an image and an audio file.

## Features

- Create AI avatars using images and voice recordings.
- Polling mechanism to check avatar generation status.
- Webhook integration for status updates.
- Swagger documentation for API endpoints.
- JWT authentication for security.
- CORS support for cross-origin requests.

## Prerequisites

Before running the application, ensure you have the following:

- Node.js installed (latest LTS recommended)
- D-ID API Key
- Fastify framework
- HTTPS certificates for secure communication

## Installation

1. Clone the repository:
   ```sh
   git clone https://github.com/yourusername/d-id-ai-avatar.git
   cd d-id-ai-avatar
   ```
2. Install dependencies:
   ```sh
   npm install
   ```
3. Create a `.env` file and set your API key:
   ```sh
   API_KEY=your_did_api_key
   ```
4. Add your HTTPS certificates (for local testing, use self-signed certs):
   ```sh
   key.pem
   cert.pem
   ```

## Usage

### Start the Server

Run the following command to start the Fastify server:

```sh
npm start
```

The server will run on `https://0.0.0.0:443`.

### API Endpoints

#### Create AI Avatar with Voice

**POST** `/standardavatar/create-avatar-with-voice`

**Request Body:**

```json
{
  "imgFileUrl": "https://example.com/image.jpg",
  "audioFileUrl": "https://example.com/audio.mp3",
  "userId": "user123"
}
```

**Response:**

```json
{
  "id": "talkId",
  "status": "processing",
  "result_url": "https://api.d-id.com/video/result.mp4"
}
```

### Swagger API Docs

API documentation is available at:

```
https://127.0.0.1:443/docs
```

## Security

- JWT authentication is implemented for secure access.
- Fastify CORS is enabled to allow API calls from different origins.

## License

This project is licensed under the MIT License.

## Contributing

Feel free to open issues and contribute to this project.

## Author

[Imran Latif](https://github.com/Imran-Latif88)

