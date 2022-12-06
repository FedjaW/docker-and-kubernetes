# Commands

1. Run the container out of the docker-compose file:

   ```CLI
   docker-compose up
   ```

   or to run the container in the background:

   ```CLI
   docker-compose up -d
   ```

2. To force a rebuild of the images that are used in the docker compose file:

   ```CLI
   docker-compose up --build
   ```

3. Open the browser on `localhost:8081`

4. To stop the container:

   ```CLI
   docker-compose down
   ```
