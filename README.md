# Port-Knocking Server and Client Application

## Overview
This project implements a port-knocking mechanism on UNIX systems. It includes a server that requires a sequence of correct "knocks" on dynamically determined ports before delivering a secret message to an authenticated client. The aim of this project is to demonstrate practical applications of TCP/IP sockets in network security.

## Features
- **Dynamic Port Knocking**: Server listens for a pre-defined number of knocks on changing ports.
- **Secret Transmission**: Upon successful port knocking, the server transmits a secret message to the client.
- **Error Handling**: Both the server and client include basic error handling for robustness.
- **Timeout Implementation**: The server uses timeouts to improve security and efficiency.

