## Description

This Python script is designed to wait for a service to become available, mostly before initiating the application. It utilizes socket connections to check if a specified host and port are accessible. If the service is not available within the defined timeout period, it exits with a failure status.

## Usage

To use this script, simply execute it with the required parameters: `<host>` and `<port>`. 

```bash
python wait_for_db.py <host> <port> && <your next action>
```

For example (I used it with Docker):

```bash
python wait_for_db.py postgres 5432 && python manage.py runserver 0.0.0.0:8000
