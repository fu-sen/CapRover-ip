## Secure CapRover server IP address lookup

[CapRover](https://caprover.com/)

Outputs CapRover-specific HTML when referring to the IP address from a browser on the server on which CapRover is installed. It exposes the fact that CapRover is installed on the server, and can be the source of further probes within the server.

By assigning this simple app to an IP address, it will generate a blank HTML or TLS (SSL) error when browsed by IP address. It cannot verify the presence of the CapRover and keeps the server safe.

powered by [Caddy](https://caddyserver.com/)

## Usage

1. Create any App. Add your server's IP address as a custom domain to this App. Do not enable HTTPS. (Let's Encrypt does not issue certificates to IP addresses)
2. Clone this project into the CapRover operating environment.
3. Run `caprover deploy`. Select the App created here and apply the deployment.
4. Browse to the IP address in your web browser and confirm that you get a blank screen or a TLS (SSL) error.
