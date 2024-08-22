# MDandMe-Take-Home-Backend

This project is a backend service developed as part of the MDandMe take-home assignment. It uses `json-server` to provide a simple REST API for the frontend application.

## Note for Reviewers

The `data.json` file has been modified from its original format to be compatible with `json-server`. Specifically, `data.json` was changed from an array format to an object format. The contents of the original array have been encapsulated within a property `posts` of the new object. For example:

```json
{
  "posts": [
    // The original data here
  ]
}
```

This modification allows `json-server` to correctly interpret and serve the data.

## Prerequisites

Before you start, make sure you have the following tools installed:

1. **[Node.js](https://nodejs.org/)**: A JavaScript runtime that lets you run JavaScript on the server side. Download and install it from the official website.

2. **[MDandMe-Take-Home-Frontend](https://github.com/kjmj/MDandMe-Take-Home-Frontend)**: This project requires a frontend application. Clone or download this repository and follow its instructions to set up the frontend.

## Getting Started

Follow these steps to set up and run the backend server:

1. **Install Dependencies**

   First, install the necessary Node.js packages by running:

   ```bash
   npm install
   ```

2. **Start the JSON Server**

   Launch the JSON server to serve the API endpoints:

   ```bash
   npx json-server data.json --id post_url --host 0.0.0.0
   ```

   This command starts the server with the following parameters:

   - `data.json`: The file containing the mock data for the API.
   - `--id post_url`: Specifies the field to use as the unique identifier for each record.
   - `--host 0.0.0.0`: Allows the server to accept requests from any IP address.

   Once the server is running, you will see requests being logged in the terminal.
