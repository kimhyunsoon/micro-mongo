![image](https://github.com/kimhyunsoon/micro-mongo/assets/60641694/b85f6c6e-1024-4e8f-bd9d-90abfc84c0f1)

# micro-mongo
MongoDB Docker container builder with applied replicaSet.

# How to Apply
1. Creating a key file.

```bash
openssl rand -base64 756 > mongodb.key
```

2. Create a `.env` file with the following content:

```bash
NFS_DIR=$your_nfs_dir
OUTER_PORT=$external_port
DB_ROOT_NAME=root
DB_ROOT_PASSWORD=$password
DB_MASTER_NAME=master
DB_MASTER_PASSWORD=$password
DB_DATABASE_NAME=$database_name
```

3. Execute `deploy.sh`.

```bash
bash deploy.sh
```

4. Access the Docker container and run `init.sh`. (For the initial execution or after data initialization.)
```bash
docker exec -it $container_id bash
```
```bash
bash init.sh
```
