# Mission Reflection

This laboratory activity helped me understand why monitoring is an important part of cloud operations. First, it is important to check the host server's resources even if the containers are running perfectly because containers still depend on the physical or virtual host. If the server runs out of memory, disk space, or CPU resources, the containers can become slow or stop working. Checking the host baseline helps identify resource problems before they affect the applications.

If a user complains that they cannot log into a web application, the `docker logs` command can help investigate what is happening inside the container. I would run `docker logs client-website` and examine the messages for errors, failed requests, or other information related to the login problem. This can help determine whether the issue is coming from the application or another part of the system.

Monitoring logs and monitoring metrics are different but complementary. Logs provide detailed records of events and requests, such as the HTTP 200 responses and the 404 error I generated during this activity. Metrics provide numerical information about system performance, such as CPU usage, memory usage, and network activity. In my `docker stats` output, the client website used 0.00% CPU and 2.723MiB of memory.

Large enterprise companies can monitor thousands of containers by using centralized monitoring and observability tools such as Prometheus and Grafana. Prometheus can collect and store metrics from many systems, while Grafana can display those metrics in dashboards that make problems easier to identify.

Finally, this activity improved my ability to troubleshoot Linux environments because I learned to use commands such as `top`, `docker logs`, and `docker stats` to investigate system and container health. Instead of simply assuming that an application is working, I can now use actual logs and performance data as evidence.
