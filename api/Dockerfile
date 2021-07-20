FROM node:alpine
RUN apk add --no-cache libc6-compat
WORKDIR /api
# COPY package.json ./
COPY . ./
RUN npm ci --only=production

# COPY tsconfig.json ./
RUN yarn tsc
ENV NODE_ENV=production
CMD yarn start