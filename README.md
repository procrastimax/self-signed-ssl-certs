# Self-Signed-SSL-Cert Scripts

The repo contains two scripts to:
1. Create a certificate authority (CA) certificate
2. Create a server certificate and a certificate sign request for this server certificate
3. Sign the server's certificate with the CA's certificate
4. Convert the server certificate and server key to DER format
5. Create a C-style file containing the servers certificate and key in bytes

One script creates the CA certificate (step 1), the other script executed the other steps (2-5).

## Usage
Use these scripts if you i.e., want to setup a dev HTTPS server.
Call these scripts, assign the server's certificate and private key to you HTTPS server and import the CA certificate to your device/ browser, to validate and trust the HTTPS requests.

The server certificate uses Subject Alternative Names (SAN), to be used for DNS names or IP-Adresses. To sign a certificate for specific DNS entry or IP Adress, please change the related fields in the `certs.ext` file.

## Warning
These certificates are not encrypted nor securited for production usage!
Only use the generated certificates for development use cases!
