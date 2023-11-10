# Traefik Mkcert

Enables https for local traefik usage.

## Generate Mkcert certificates

Overwrite key.pem & cert.pem file

```bash
mkcert -key-file ./certs/key.pem -cert-file ./certs/cert.pem whoami.loc
```

Generate key.pem & cert.pem file from domains.txt

```bash
mkcert -key-file ./certs/key.pem -cert-file ./certs/cert.pem $(cat certs/domains.txt)
```

Add domain to domains.txt

```txt
yourdomain.de example.loc ... [new domain]
```

## Links

https://github.com/soulweblab/docker4localdev/tree/main