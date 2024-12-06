# Git Sync

This repository shows a simple example of seeting up [git-sync](https://github.com/kubernetes/git-sync) to fetch and serve HTML pages.  

The docker-compose file runs two containers that share a volume between themselves. The container running git-sync syncs a git repository which contains a static HTML page that's served by the container running the server. This demonstrates how fetching the HTML content and serving it can be decoupled. In large-scale deployments, this allows updating the HTML pages without having to redeploy the webservers.  

To see this in action, execute the following commands.  

First, bring up the containers.

```
docker compose up -d
```  

Next, open the following URL in your web browser. 

http://localhost:8080  

This serves the static content that was synced from the repository.
