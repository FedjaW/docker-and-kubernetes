# Commands

1. Create an image out of the dockerfile with a tag:

   ```CLI
   docker build -t fedjaw/visits .
   ```

2. Run the new image:

   ```CLI
   docker run -p 8081:8081 fedjaw/visits
   ```
