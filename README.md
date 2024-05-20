# IoT CO2 Sensor Application
This project monitors CO2 levels using a CO2 sensor device, processes the data on a Spring boot backend, and provides a mobile app interface for users.
The system uses various Azure services for data storage, data messaging, and deployment.

## Overview

### Frontend:
Its a simple application written in Kotlin, features basic login/register functionalities, device info andbinding process. 

### Backend:
Its a standard Rest API for communication between the client and the database. Its also responsible for saving events from the broker so it is listening for events on the Azure Brooker and saving them to the database. The database is a Azure MSSQL database. The backend is contenarized and deployed as a container on Azure.

### Sensor:
It is a Raspberry with a CO2 sensor, that creates an acces point, that is used for pairing with the local network. After pairing it sends reading data to the Azure broker. Written mostly in C++
