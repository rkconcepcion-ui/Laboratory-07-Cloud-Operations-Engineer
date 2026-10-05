# Container Observability

## Checkpoint 4 - Application Logging

### Docker Logs

The following command was used to retrieve the application logs from the Nginx container:

```bash
docker logs client-website
```

### HTTP 404 Error

```text
172.17.0.1 - - [05/Oct/2026:12:51:07 +0000] "GET /hidden-admin-page HTTP/1.1" 404 153 "-" "curl/8.5.0" "-"
```

Application logs are vital for troubleshooting because they provide a record of requests and errors that occur inside the application. By examining the logs, a Cloud Operations Engineer can identify failed requests and determine the cause of an application problem.

![Docker Logs](screenshots/docker-logs.png)
