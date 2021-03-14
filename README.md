# Event Driven Node Proof of Concept

This is a POC that allows HTTP to communicate with TCP sockets, forming the basis of and event driven system.

My goal in this repo is to have a sample HTTP client (Browser, Postman, Etc) be able to send a request to an HTTP server (`index.js`). The node.js event loop will hand off the request to the TCP client and then the TCP server should respond, eventually making its way back through the HTTP server.

To do this, I am utilizing Node's `Net` and `Event` modules.

This project is not hosted, and to run locally I am using Windows Terminal with 3 separate tabs. I recommend an approach like this.

## Requirements:

1. Node.js is installed
2. NPM is installed (I am using `yarn`)
3. PuTTy is installed (or Mac/Linux equivalent)
4. A terminal is installed (For this project I recommend one with tabs like Windows Terminal or cmder).

## To Run Locally:

1. Clone repo
2. `yarn install`
3. `yarn start:tcpserver`
4. In another terminal or tab, `yarn start:tcpclient`
5. In another terminal or tab, `yarn start:httpserver`
6. Make a `GET` request to the `/` endpoint with a query param of status code (400,500, or other).
