# Commands

1. Build the image:

   ```CLI
   docker build -t frontend -f Dockerfile.dev .
   ```

2. Run the image:

   ```CLI
   docker run -p 3000:3000 frontend
   ```

3. Open the browser on `localhost:3000`
