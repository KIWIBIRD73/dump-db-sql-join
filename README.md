# Get started
1. Install dependencies
    ```shell
    npm install
    ```
2. Start database in docker container
    ```shell
    docker-compose up --build -d
    ```
3. Start server
    ```shell
    npm run start:dev
    ```

# Load db dump file into docker container
1. Migrate dump `assets/db-dump.sql` into container
    ```shell
    docker exec -i <CONTAINER> psql -U <USER> <DB-NAME> < <PATH-TO-DUMP>
    ```

# Migrate to prisma orm
1. Check database schema location in GUI for postgresql
2. Generate prisma schema
    ```shell
    npx prisma db pull
    ```
3. Генерация типов
    ```shell
    npx prisma generate
    ```
