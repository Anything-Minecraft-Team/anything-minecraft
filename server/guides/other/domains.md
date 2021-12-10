# Domains

This article aims to provide you with the knowledge to connect your own domains to your own Minecraft servers.

## Obtaining a Domain

Domains can be purchased from a wide range of venders some of these include; [Godaddy](https://godaddy.com), [Namecheap](https://www.namecheap.com) and [Google](https://domains.google/). You can also purchase your domain from any vender you prefer.

## DDOS Protection (Optional)

DDOS (Distributed Denial of Service) attacks flood the router/modem with so many requests that it cant respond to all of them causing your Minecraft server and sometimes the rest of your internet to go down. Some domain vendors offer a DDOS protection service for free or an added item at checkout.

### Cloudflare

To prevent this proxies route the traffic through their servers taking the load off your network. To protect your server from DDOS attacks you can use a service like [cloudflare](https://www.cloudflare.com/) which offers free and paid tiers, to protect a Minecraft server the free tier is adequate. After you have created a cloudflare account you can add your domain to the free tier using the "Add a Site" button.

### Changing Nameservers

Different venders have different methods to change the nameservers for your domain. Some venders offer a free service to change the nameservers for your domain, some offer a paid service. If you are not sure which vender to use you can always contact them to find out. Because the specifics change from vender to vender you will need to look up their documentation to find out how to change the nameservers. 

## DNS Records

DNS records is the way that the domain points to different ip's. In the case of the Minecraft server domain, the domain will need to point to the ip of the Minecraft server. To do this you will need to create an 'A' record, this redirects a subdomain to an ip address (for example 'example.anythingmc.org' can be pointed to xxx.xxx.xxx.xxx). There are two fields, the name and IPv4 address, the name is the subdomain you want to point to the IPv4 address, the ip address you want to point to, this only works if you public ip is numbers (IPv4).