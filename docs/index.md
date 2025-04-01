<a href="https://www.threatpatrols.com">
<img src="assets/img/threatpatrols-eyeprint-banner-black-344×90.png#only-light" style="height: 70px; float: right; margin-left: 24px; margin-bottom: 24px">
<img src="assets/img/threatpatrols-eyeprint-banner-white-344×90.png#only-dark" style="height: 70px; float: right; margin-left: 24px; margin-bottom: 24px">
</a>

# Threat Patrols Projects

## Threat Patrols Action

**[threatpatrols.github.io/threatpatrols-action](https://threatpatrols.github.io/threatpatrols-action/)**

Threat Patrols Action (TPAS) is our primary open-source framework for SecOps automation turning 
security-practitioners into security automation super-heroes.

Threat Patrols Actions are **[well known tools](https://threatpatrols.github.io/threatpatrols-action/actions/)** that 
have been containerized, are kept up-to-date and wrapped with **callback features** that makes their use in continuous 
security automation pipelines a delight.

  * Want to run `<favorite security tool here>` on a regular basis, store the results in a S3-bucket, get 
    a Slack-notification and send the results to some other workflow?  TPAS makes this easy.

  * Want to use `<favorite security tool here>` as a simple Github Action definition and send results to another
    workflow?  TPAS makes this easy.

  * Want a ready-to-go API endpoint to invoke `<favorite security tool here>` with background tasks and 
    callbacks?  TPAS makes this really easy.


## OPNsense Resources

**[threatpatrols.github.io/opnsense-resources](https://threatpatrols.github.io/opnsense-resources)**

Threat Patrols really loves OPNsense, and we produce and support resources for it.

 * **Autossh**: an OPNsense plugin that wraps the well-known autossh package for maintaining and keeping alive 
   outbound SSH tunnels.  
 * **Configuration Sync**: an OPNsense plugin that saves all system configurations changes to an S3 bucket that 
   ensures off-system config backup.
 * **Cloudflare Mirror**: we provide an OPNsense mirror that is backed by Cloudflare CDN using a CF worker, some 
   caching and a requests to origin.


## Env Alias

**[threatpatrols.github.io/env-alias](https://threatpatrols.github.io/env-alias)**

Env Alias is a tool we had always wanted for improving operational security when working with environment 
variables that frequently contain sensitive secrets.  Env-alias makes it fast and practical to store 
sensitive variables in password vaults and load them just-in-time for specific tasks.

Provides bonus special handling for Keepass and Ansible Vault Password files but most vaults should be adaptable.


## HIBP Downloader

**[threatpatrols.github.io/hibp-downloader](https://threatpatrols.github.io/hibp-downloader)**

HIBP Downloader is a CLI tool to efficiently download a local copy of the pwned password hash data from the 
very awesome HIBP pwned passwords api-endpoint using all the good bits; multiprocessing, async-processes, 
local-caching, content-etags and http2-connection pooling to (probably) make things as fast as is Python-ly 
possible.

## HLID

**[github.com/threatpatrols/hlid](https://github.com/threatpatrols/hlid)**

HLID: a Human Lexicographically (sortable) identifier that borrows similar concepts from -

 * ULID (Universally-Unique, Lexicographically-Sortable Identifier) - github.com/ulid
 * UUID7 (Time-ordered UUID with millisecond precision) - ietf.org

HLIDs can be swapped with UUID-type or ULID-type values, and we use them among our tooling as we
find them really very useful when dealing with data that updates over time.


## Fresh Resolvers

**[github.com/threatpatrols/fresh-resolvers](https://github.com/threatpatrols/fresh-resolvers)**

Provides daily up-to-date lists of reliable public DNS resolvers using source-data from `public-dns.info` filtered 
for -

 * servers that pass DNS Validator for correctness.
 * servers that have high reported uptime.
 * servers that support DNSSEC.


## Docker Containers

**[hub.docker.com/u/threatpatrols](https://hub.docker.com/u/threatpatrols)**

Threat Patrols produces a good many containers for TPAS where we use the Github Container Registry `ghcr.io` to make 
those containers publicly available.

Additionally, we maintain a collection of other Docker containers via Docker Hub.  A sample of these -  

* **[threatpatrols/sshjumphost](https://hub.docker.com/r/threatpatrols/sshjumphost)** - much as the name suggests, a container for easily deploying an SSH 
  jumphost (bastion host) using environment variables for setup and configuration.
* **[threatpatrols/autossh](https://hub.docker.com/r/threatpatrols/autossh)** - Autossh with pre-command injection  useful for declaring container 
  routes before `autossh` is invoked.
* **[threatpatrols/cfwarp-syncthing](https://hub.docker.com/r/threatpatrols/cfwarp-syncthing)** - Run an instance of Syncthing in Docker with traffic via 
  Cloudflare WARP.
* **[threatpatrols/gophish-ducknweave](https://hub.docker.com/r/threatpatrols/gophish-ducknweave)** - Provides a dockerized Gophish instance with updates 
  and modifications to avoid common spam/phish filtering triggers.

We publish plenty of others too, please check the Docker Hub repo.
