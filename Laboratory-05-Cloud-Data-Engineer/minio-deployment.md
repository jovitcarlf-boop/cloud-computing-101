## MinIO Deployment Documentation

### Docker Command Used
[docker run -d -p 9000:9000 -p 9001:9001 --name minio-server \
-e "MINIO_ROOT_USER=cloudadmin" \
-e "MINIO_ROOT_PASSWORD=CloudNova2026!" \
cgr.dev/chainguard/minio:latest server /data --console-address ":9001"

## Web Console Access

- **Port Number Used:** 9001
- **Access Method:** KillerCoda "Traffic / Ports" or "Custom Ports" feature
- **Login Credentials:**
  - Username: `cloudadmin`
  - Password: `CloudNova2026!`

## Bucket Details

- **Bucket Name Created:** client-photos
- **Purpose:** Store user-uploaded photos for the client's photo-sharing application
- **Storage Location:** /data directory inside the container

## Environment Variables (-e Flags) Explanation

The `-e` flags in the Docker command set environment variables that configure MinIO's behavior:

- **MINIO_ROOT_USER:** Defines the administrator username used to log into the MinIO Web Console and API. Set to `cloudadmin` for this deployment.

- **MINIO_ROOT_PASSWORD:** Defines the password for the root/admin user account. Set to `CloudNova2026!` to secure access to the storage system.

These environment variables allow you to configure MinIO's authentication without modifying configuration files, making the deployment portable and repeatable.

## Port Mapping Explanation

- **Port 9000 (-p 9000:9000):** MinIO API port. Applications and clients connect to this port to perform storage operations (upload, download, delete files).

- **Port 9001 (-p 9001:9001):** MinIO Web Console port. Administrators use a web browser to access the graphical management interface for creating buckets, managing users, and monitoring storage.

## Deployment Verification Command

To verify the container is running, use:
```bash
docker ps
```

Look for the `minio-server` container with status "Up" to confirm successful deployment.

## What the -d Flag Does

The `-d` flag runs the container in detached mode, meaning it runs in the background and returns control of the terminal to you immediately.
