# Chattering Teeth

A Go web application with automatic deployment to Google Cloud Platform.

## Project Structure

```
Chattering_teeth/
├── main.go          # Application entry point
├── go.mod           # Go module definition
├── .gitignore       # Git ignore file
├── app.yaml         # App Engine configuration
├── Dockerfile       # For containerized deployment
└── README.md        # This file
```

## Getting Started

### Local Development

1. Install Go (version 1.20 or later)
2. Clone the repository
3. Run the application locally:

```bash
go run main.go
```

4. Access the application at http://localhost:8080

### Deployment to GCP

#### Option 1: App Engine

```bash
gcloud app deploy app.yaml
```

#### Option 2: Cloud Run

```bash
# Build and push the container
gcloud builds submit --tag gcr.io/[YOUR_PROJECT_ID]/chattering-teeth

# Deploy to Cloud Run
gcloud run deploy chattering-teeth --image gcr.io/[YOUR_PROJECT_ID]/chattering-teeth --platform managed
```

## Future Expansion

As this project grows, consider organizing it using the standard Go project layout:

```
Chattering_teeth/
├── cmd/               # Main applications
├── internal/          # Private application code
├── pkg/               # Public libraries
├── api/               # API definitions
├── web/               # Web assets
└── configs/           # Configuration files
```
