### Starting commands
[[Linux]]

```bash
docker ps
```

```bash
docker start <container_id>
```

```bash
docker exec -it <container_id> sh
```

```bash
docker run --restart=always --name issabel --privileged -v /sys/fs/cgroup:/sys/fs/cgroup:ro -v issabel-etc:/etc -v issabel-data:/var/lib -dti --hostname pbx.saiyans.com.ve --network host deathmetall/issabel:live
```

Current stable
```powershell
docker run --privileged -dp 8283:443 issabel:live
```

Change image name 
```bash
docker image tag repo/user:tag name:tag
```

Create a imge from a dockerfiel

```bash
docker build -t . 
```