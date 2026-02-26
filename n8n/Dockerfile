FROM n8nio/n8n:2.9.4

# Switch to root for installation
USER root

# Create isolated directory for custom deps
WORKDIR /home/node/custom

# Initialize a tiny Node project and install exiftool locally
RUN npm init -y \
    && npm install exiftool-vendored \
    && chown -R node:node /home/node/custom

# Switch back to non-root user for runtime
USER node
