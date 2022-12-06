# Commands

1. Create an image out of the dockerfile with a tag:

   ```CLI
   docker build -t fedjaw/simpleweb .
   ```

2. Run the new image:

   ```CLI
   docker run -p 8080:8080 fedjaw/simpleweb
   ```
