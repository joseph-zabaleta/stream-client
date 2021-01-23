# Stream Project

## Table of Contents

---

-   [Stream Project](#stream-project)
    -   [Overview](#overview)
    -   [Installation](#installation)
        -   [Part 1 Client App](#part-1-installation)
        -   [Part 2 API Server](#part-2-installation)
        -   [Part 3 RTMP Server](#part-3-installation)
    -   [Authors](#authors)
    -   [Collaborations](#collaborations)
    -   [License](#license)
    -   [Acknowledgements / Resources](#acknowledgements-/-resources)

---

## Overview

This is REST-ful application that goes through the motions of login with Google OAuth, accesses an API that is making use of the CRUD operations, and a RTMP server to manage the streams. Overall this application allows users to create, edit, and delete streams.

### Part 1

[Client]()

A React application that makes use of Redux, Redux-form, URL-Based Selection with programmaic navigation, and Google Oauth for login. This is just a few highlights as there are many more features within.

### Part 2

[API Server]()

This piece is making use of the npm package `json-server`. Simple way to create, read, edit, and destroy data. This was chosen to quickly set up a server, that strictly follows RESTful conventions for the project.

### Part 3

[RTMP Server]()

Real Time Messaging Protocol (RTMP) Server. Utilizing the npm package `node-media-server` we create an RTMP server to handle the broadcasting of our stream locally.

## Installation

This application is designed to run with the API server and RTMP Server. To get this running on your local machine please follow the below instructions.

### Part 1 Installation

-   Repository: [stream-client](https://github.com/joseph-zabaleta/streams-client)

Client server is a React application follow the below code block on how to clone the repo, change into the root directory, and install all required dependencies.

```bash
git clone https://github.com/joseph-zabaleta/streams-client
cd streams-client
npm install
```

Before we can run the start script you will need to create an environment file in the root of the directory that will contain your personal Google Auth Client ID.

Since this application is utilizing Google OAuth for its login authentication, you will need a Google Auth Client ID. To acquire this, you will need to visit [console.developers.google.com](console.developers.google.com) and create a project/app. After creating a project, you can add credentials for Oauth 2.0 which will generate you a Client ID and Secret Key.

```bash
mkdir .env
```

Inside your `.env` file ensure the key name is `REACT_APP_GOOGLE_CLIENT_ID`

```
REACT_APP_GOOGLE_CLIENT_ID="your-key-goes-here"
```

Now the Client portion of this project is ready to start by default this project will run on localhost:3000, from the root directory you can run the following command

```bash
npm start
```

You will need to ensure that the API and RTMP servers are both running so please continue onto parts 2 and 3.

### Part 2 Installation

-   Repository: [stream-api-server](https://github.com/joseph-zabaleta/stream-api-server)

Above is the link to an API server using `json-server` for local deployment of this application.

### Part 3 Installation

-   Repository: [stream-rtmp-server](https://github.com/joseph-zabaleta/stream-rtmp-server)

Above is the link to a RTMP server using `node-media-server` for local deployment of this application.

## Authors

-   Software Developer: Joseph Zabaleta
    -   [Official Github](https://github.com/joseph-zabaleta)

## License

This project is under the MIT License.

## Acknowledgements / Resources

-   [Modern React with Redux](https://www.udemy.com/course/react-redux/)
-   [json-server Docs](https://www.npmjs.com/package/json-server)
-   [node-media-server Docs](https://github.com/illuspas/Node-Media-Server)
