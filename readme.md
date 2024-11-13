# Open-WebUI with self-signed SSL certificate

This is a simple docker compose project for running [Open-WebUI](https://github.com/open-webui/open-webui) under https using an Nginx reverse proxy with a self-signed SSL certificate.

## Generating the certificate

To generate the self-signed certificate, you just run the command:

```bash
mkdir -p nginx/certificates
openssl req -x509 -nodes -days 365 -newkey rsa:2048 -keyout nginx/certificates/selfsigned.key -out nginx/certificates/selfsigned.crt
```

## Running the stack

Execute the following command

```bash
docker compose up -d
```

Check if the application is running by accessing https://localhost on your browser.
