# Commands

## Development

1. Build the image:

   ```CLI
   docker build -t frontend -f Dockerfile.dev .
   ```

2. **(See 4.)** Run the container based on the image:

   ```CLI
   docker run -p 3000:3000 -v /app/node_modules -v $(pwd):/app frontend
   ```

   Explanation:

   - `-p 3000:3000` map the port from the host to the container
   - `-v /app/node_modules` map a volume from inside the container dir /app/node_modules to nothing.
   - `-v $(pwd):/app` map a volume from inside the container dir /app to outside the container present working directory (pwd)

3. To run unit tests within the container:

   ```CLI
   docker run -it frontend npm run test
   ```

   Notice that the `npm run test` will override the default CMD in the Dockerfile.dev

4. **Or** run the application and also execute tests via docker-compose:

   ```CLI
   docker-compose up
   ```

5. Open the browser on `localhost:3000`

## Production

1. Build the image:

   ```CLI
   docker build -t fedjaw/frontend .
   ```

2. Run the container based on the image:

   ```CLI
   docker run -p 8080:80 fedjaw/frontend
   ```

3. Open the browser on `localhost:8080`
