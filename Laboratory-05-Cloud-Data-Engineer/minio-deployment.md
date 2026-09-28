## MinIO Deployment Documentation

### Docker Command Used
[docker run -d -p 9000:9000 -p 9001:9001 --name minio-server \
-e "MINIO_ROOT_USER=cloudadmin" \
-e "MINIO_ROOT_PASSWORD=CloudNova2026!" \
cgr.dev/chainguard/minio:latest server /data --console-address ":9001"

### Web Console Access
- **Port Number:** 9001
- **Access Method:** KillerCoda "Custom Ports" feature

### Bucket Details
- **Bucket Name:** client-photos
- **Purpose:** Store user-uploaded photos

### Environment Variables Explanation
- **MINIO_ROOT_USER:** Sets the administrator username for console login
- **MINIO_ROOT_PASSWORD:** Sets the password for the root user account
- Both flags (-e) configure how MinIO authenticates users to the web interface

### Port Mapping
- Port 9000: MinIO API (for applications to interact with storage)
- Port 9001: MinIO Web Console (for administrators)
