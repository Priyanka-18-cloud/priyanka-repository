# Use the node:19.7.0-alpine base image
FROM node:19.7.0-alpine

# Set environment variable NODE_ENV to production
ENV NODE_ENV=production

# Create a directory called /labone
RUN mkdir /labone && chown -R node:node /labone

# Set /labone as the working directory
WORKDIR /labone

# Set the user to node
USER node

# Copy source files and change ownership to node
COPY --chown=node:node . .

# Install node.js packages
RUN npm install

# Expose port 3000
EXPOSE 3000

# Set default command to run the app
CMD ["node", "src/index.js"]
