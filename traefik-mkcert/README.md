# Traefik Mkcert

Enables https for local traefik usage.

## Install Mkcert

```bash
$ apt get install libnss3-tools

$ wget https://github.com/FiloSottile/mkcert/releases/download/v1.4.3/mkcert-v1.4.3-linux-amd64

$ mv mkcert-v1.4.3-linux-amd64 /usr/bin/mkcert

$ chmod +x /usr/bin/mkcert
```

## Generate Mkcert certificates

Overwrite key.pem & cert.pem file

```bash
$ mkcert -key-file ./certs/key.pem -cert-file ./certs/cert.pem whoami.loc
```

Generate key.pem & cert.pem file from domains.txt

```bash
$ mkcert -key-file ./certs/key.pem -cert-file ./certs/cert.pem $(cat certs/domains.txt)
```

Add domain to domains.txt

```txt
yourdomain.de example.loc ... [new domain]
```

## Links

https://github.com/soulweblab/docker4localdev/tree/main