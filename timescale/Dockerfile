FROM node

## Create app directory
WORKDIR /app

## Copy Emulator
COPY emulator.ts .

## Add Postgres package
RUN yarn add pg

## Add the wait script to the image
ADD https://github.com/ufoscout/docker-compose-wait/releases/download/2.9.0/wait /wait
RUN chmod +x /wait

EXPOSE 3008

CMD /wait && node emulator.ts
