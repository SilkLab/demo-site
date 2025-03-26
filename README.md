# Silk Demo Website

This is a website used to demo the capabilities of [Silk](https://silklab.io). It is deployed to AWS and the data is ingested into Silk for analysis and q&a.

## Building

This is based on NextJS and Payload. After cloning, running the following build command will produce an image suitable for ECS and Lightsail.

```
docker build --build-arg PAYLOAD_SECRET=<secret> --build-arg DATABASE_URI=<secret> -t silklab/demo-site:latest --platform linux/amd64 --no-cache .
```

## Running

To run the dev server fill out a `.env` file in the root similar to the `env.example`. Then run `npm start`

