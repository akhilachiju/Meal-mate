# Build stage (Debian-based: better compatibility with Prisma/native deps)
FROM node:18-slim AS builder

WORKDIR /app

# Install dependencies
COPY package.json package-lock.json ./
RUN npm ci

# Copy source and build
COPY . .
RUN npx prisma generate
RUN npm run build

# Production stage
FROM node:18-slim

WORKDIR /app

# Install production dependencies only
COPY package.json package-lock.json ./
RUN npm ci --omit=dev

# Copy built output from builder
COPY --from=builder /app/dist ./dist

# Server should listen on all interfaces inside the container
ENV NODE_ENV=production

EXPOSE 5000

CMD ["node", "dist/index.js"]
