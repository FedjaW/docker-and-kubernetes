# Commands

1. Build the image:

   ```CLI
   docker build -t frontend -f Dockerfile.dev .
   ```

2. Run the container based on the image:

   ```CLI
   docker run -p 3000:3000 -v /app/node_modules -v $(pwd):/app frontend
   ```

   Explanation:

   - `-p 3000:3000` map the port from the host to the container
   - `-v /app/node_modules` map a volume from inside the container dir /app/node_modules to nothing.
   - `-v $(pwd):/app` map a volume from inside the container dir /app to outside the container present working directory (pwd)

3. Or run the container via docker-compose:

   ```CLI
   docker-compose up
   ```

4. Open the browser on `localhost:3000`

5. To run unit tests within the container:

   ```CLI
   docker run -it frontend npm run test
   ```

   Notice that the `npm run test` will override the default CMD in the Dockerfile.dev
