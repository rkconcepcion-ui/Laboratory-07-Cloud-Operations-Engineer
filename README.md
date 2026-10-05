# Laboratory 07 - Cloud Operations Engineer

## Mission Overview

In this laboratory activity, I took on the role of a Cloud Operations Engineer for CloudNova Technologies. I established a baseline of the Linux host system, deployed an Nginx web server using Docker, generated test web traffic, analyzed application logs, and monitored the container's resource usage. The activity focused on observability, which helps engineers use logs and metrics to verify the health and performance of cloud applications.

## Objectives

- Monitor Linux host memory and disk resources.
- Use the `top` command to observe CPU load and running processes.
- Deploy an Nginx web server using Docker.
- Generate successful and failed HTTP requests using `curl`.
- Analyze application logs using `docker logs`.
- Monitor container CPU, memory, and network usage using `docker stats`.
- Document monitoring results using Markdown.

## Monitoring Commands Executed

### Check Memory Usage

```bash
free -h
```

### Check Disk Usage

```bash
df -h
```

### Monitor CPU and Processes

```bash
top
```

### Deploy Nginx

```bash
docker run -d -p 8080:80 --name client-website nginx
```

### Generate Web Traffic

```bash
curl http://localhost:8080
```

Three successful HTTP requests were generated to verify that the website was accessible.

### Generate an HTTP 404 Error

```bash
curl http://localhost:8080/hidden-admin-page
```

This request intentionally accessed a page that does not exist and generated a `404 Not Found` response.

### View Application Logs

```bash
docker logs client-website
```

This command displayed the Nginx startup information and HTTP request logs, including the successful `200` responses and the intentional `404` error.

### Monitor Container Metrics

```bash
docker stats
```

This command displayed the real-time CPU, memory, network, block I/O, and process usage of the container.

## Skills Learned

Through this activity, I learned how to establish a basic health baseline for a Linux server and how to monitor resources using native Linux commands. I also learned how to deploy and observe a Docker container, generate test traffic, identify HTTP errors from application logs, and examine real-time container metrics. Most importantly, I learned that logs and metrics provide evidence that can help Cloud Operations Engineers troubleshoot problems and verify that applications are running properly.
