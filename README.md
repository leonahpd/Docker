# Docker



1. How would you handle a situation where a container crashes immediately after starting?
   
**Expected Answer:**

---> Inspect logs using **docker logs <container_id>** to identify errors.

---> Use **docker inspect <container_id>** to check the container’s configuration.

---> Verify if dependencies or environment variables are missing.

---> Run the container interactively using **docker run -it** to debug.

---> Check the Dockerfile for misconfigurations, such as incorrect **CMD** or **ENTRYPOINT**



2. You notice that a Docker container is using excessive memory or CPU. What steps would you take to troubleshoot and fix the issue?

   **Expected Answer:**

---> Use **docker stats** to monitor resource usage.

---> Inspect the container’s logs (**docker logs <container_id>**) for signs of issues like memory leaks or infinite loops.

---> Limit resources in the future using flags like **--memory** and **--cpus** when running containers.

---> Check for inefficient code or misconfigured applications inside the container.

---> Restart the container if it’s unresponsive (**docker restart <container_id>**).



3. You need to update an application running in a Docker container without downtime. How would you approach this?

**Expected Answer:**

---> Use a **rolling update** strategy with **docker-compose** or an orchestrator like Docker Swarm or Kubernetes.

---> Run the new version of the container alongside the old one.

---> Test the new container before redirecting traffic to it.

---> Use a **load balancer** to gradually shift traffic from the old container to the new one.

---> Once the new container is verified, stop and remove the old container.



