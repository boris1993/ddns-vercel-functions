# DDNS Vercel Functions

A DDNS updater hosted in Vercel Functions, aimed for providing a bridge for Synology DDNS, but also can be used in general ways.

[![Deploy with Vercel](https://vercel.com/button)](https://vercel.com/new/clone?repository-url=https%3A%2F%2Fgithub.com%2Fboris1993%2Fddns-vercel-functions)

## Current Supported Platform

[x] CloudFlare

## Endpoints

- `/api/ddns/cloudflare?zoneId=__USERNAME__&token=__PASSWORD__&domain=__HOSTNAME__&address=__MYIP__`

## Responses

- good - Update successfully.
- nochg - Update successfully but the IP address have not changed.
- nohost - The hostname specified does not exist in this user account.
- abuse - The hostname specified is blocked for update abuse.
- notfqdn - The hostname specified is not a fully-qualified domain name.
- badauth - Authenticate failed.
- 911 - There is a problem or scheduled maintenance on provider side
- badagent - The user agent sent bad request(like HTTP method/parameters is not permitted)
- badresolv - Failed to connect to because failed to resolve provider address.
- badconn - Failed to connect to provider because connection timeout.
