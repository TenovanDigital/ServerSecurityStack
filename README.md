<!-- PROJECT SHIELDS -->
[![Contributors][contributors-shield]][contributors-url]
[![Forks][forks-shield]][forks-url]
[![Stargazers][stars-shield]][stars-url]
[![Issues][issues-shield]][issues-url]
[![License][license-shield]][license-url]

<!-- PROJECT LOGO -->
<div align="center">
  <h3 align="center">Server Security Stack</h3>

  <p align="center">
    A comprehensive Docker Compose stack for securing home servers with Authelia, CrowdSec, Traefik, and more.
    <br />
    <a href="https://www.youtube.com/playlist?list=PLTZ_YGxx-Igtf6L-2AfQ-dhkpXeR5aN2N">View YouTube Tutorial Series</a>
    &middot;
    <a href="https://github.com/TenovanDigital/ServerSecurityStack/issues/new?labels=bug&template=bug-report---.md">Report Bug</a>
    &middot;
    <a href="https://github.com/TenovanDigital/ServerSecurityStack/issues/new?labels=enhancement&template=feature-request---.md">Request Feature</a>
  </p>
</div>

<!-- TABLE OF CONTENTS -->
<details>
  <summary>Table of Contents</summary>
  <ol>
    <li><a href="#about-the-project">About The Project</a></li>
    <li><a href="#built-with">Built With</a></li>
    <li><a href="#getting-started">Getting Started</a></li>
    <li><a href="#usage">Usage</a></li>
    <li><a href="#license">License</a></li>
    <li><a href="#contact">Contact</a></li>
  </ol>
</details>

<!-- ABOUT THE PROJECT -->
## About The Project

![Server Security Stack Screen Shot][product-screenshot]

ServerSecurityStack is a comprehensive Docker Compose stack designed to help home server owners secure their environment. This stack combines several best-in-class security applications that work together seamlessly to protect your server from unauthorized access and malicious activities.

This stack provides:
- Secure authentication with Authelia
- Real-time threat detection with CrowdSec
- Automated container updates with Watchtower
- Reverse proxy with SSL/TLS using Traefik
- Monitoring and management through Portainer and Diun
- A customizable dashboard with Homepage

You can use this stack as a foundation and add your favorite applications while maintaining strong security controls. The comprehensive security layer ensures that only authorized users and services can access your server, even when exposed to the internet.

### Built With

The following applications are included in this stack:

[![Authelia][authelia-shield]][authelia-url]
[![CrowdSec][crowdsec-shield]][crowdsec-url]
[![Traefik][traefik-shield]][traefik-url]
[![Socket Proxy][socket-proxy-shield]][socket-proxy-url]
[![Portainer][portainer-shield]][portainer-url]
[![Watchtower][watchtower-shield]][watchtower-url]
[![DIUN][diun-shield]][diun-url]
[![Homepage][homepage-shield]][homepage-url]

<!-- GETTING STARTED -->
## Getting Started

This repository contains the complete Docker Compose stack for server security, but it doesn't contain all of the extra steps to secure your server such as:

- Setting a Static IP
- Installing and configuring Uncomplicated Firewall (UFW)
- Generating Authelia encryption secrets
- Setting up Authelia user account
- Adding Traefik as a CrowdSec bouncer
- Updating Traefik `config.yml` and `traefik.yml` (See "# TODO:" comments)
- Getting various api keys / access tokens for everything to report to Homepage

For a walkthrough setting all these up, please refer to our YouTube tutorial series:

<a href="https://www.youtube.com/playlist?list=PLTZ_YGxx-Igtf6L-2AfQ-dhkpXeR5aN2N">Server Security Series on YouTube</a>

### Alternative: Automated Setup with Citadel
If you prefer a more streamlined and automated process, consider using **Citadel**, our automated setup script. Citadel handles the tedious configuration steps for you, reducing errors and saving time. All you need to do is:
- Complete a few initial configurations
- Create Portainer Access Token for Homepage to use (Couldn't automate this)
- Import CrowdSec Cyber Threat Insights dashboard into Grafana (Couldn't automate this)

Plus Citadel sets up a bonus Grafana dashboard for CrowdSec that is not included in this repository. While you'll have to do the final import, Citadel sets up everything the dashboard needs for you.

#### Learn More About Citadel:
<a href="https://go.digital.tenovan.com/citadel">Citadel: Your Fortress for Home Server Security</a>

### Prerequisites

- Configurations for the server to use:
    - **Custom domain name** to access the server
    - **Email address(es)** for notifications and SSL certification generation
    - **Email Relay** to send emails
- Basic understanding of Docker and Docker Compose
- Basic familiarity with terminal usage
- A server with internet access

<!-- USAGE -->
## Usage

This Server Security Stack is designed to help you protect your home server while maintaining accessibility and functionality. Here are some common use cases and reasons why you'd want to use this stack:

### Why Secure Your Server?
- **Access from anywhere**: Safely access your server resources from any location using secure authentication and encryption.
- **Protect sensitive data**: Keep your personal files, media, and applications safe from unauthorized access and malicious attacks.
- **Host multiple services**: Add additional applications like:
  - Media servers (Plex, Emby)
  - Automation tools (N8n, Home Assistant)
  - Local AI services
  - Custom web pages and apps
  - File servers (Nextcloud, Filebrowser)
- **Peace of mind**: Know that your server is protected by enterprise-grade security tools while still being accessible for legitimate use.

<!-- LICENSE -->
## License

Distributed under the MIT License. See [LICENSE][license-url] for more information.

<!-- CONTACT -->
## Contact

Tenovan Digital LLC - [https://digital.tenovan.com](https://digital.tenovan.com) - success@digital.tenovan.com

Project Link: [https://github.com/TenovanDigital/ServerSecurityStack](https://github.com/TenovanDigital/ServerSecurityStack)

If you have questions or need help, feel free to ask in the repository's Discussions section or refer to our YouTube tutorials.

<!-- ACKNOWLEDGMENTS -->
## Acknowledgments

Special thanks to:
- The Docker community
- Authelia team
- CrowdSec developers
- Traefik maintainers
- And all other open-source contributors who made this stack possible

<!-- MARKDOWN LINKS & IMAGES -->
[contributors-shield]: https://img.shields.io/github/contributors/TenovanDigital/ServerSecurityStack.svg?style=for-the-badge
[contributors-url]: https://github.com/TenovanDigital/ServerSecurityStack/graphs/contributors
[forks-shield]: https://img.shields.io/github/forks/TenovanDigital/ServerSecurityStack.svg?style=for-the-badge
[forks-url]: https://github.com/TenovanDigital/ServerSecurityStack/network/members
[stars-shield]: https://img.shields.io/github/stars/TenovanDigital/ServerSecurityStack.svg?style=for-the-badge
[stars-url]: https://github.com/TenovanDigital/ServerSecurityStack/stargazers
[issues-shield]: https://img.shields.io/github/issues/TenovanDigital/ServerSecurityStack.svg?style=for-the-badge
[issues-url]: https://github.com/TenovanDigital/ServerSecurityStack/issues
[license-shield]: https://img.shields.io/github/license/TenovanDigital/ServerSecurityStack.svg?style=for-the-badge
[license-url]: https://github.com/TenovanDigital/ServerSecurityStack/blob/main/LICENSE
[product-screenshot]: screenshot.png
[authelia-shield]: https://img.shields.io/badge/Authelia-3f51b5?style=for-the-badge
[authelia-url]: https://www.authelia.com/
[crowdsec-shield]: https://img.shields.io/badge/CrowdSec-f8ab13?style=for-the-badge
[crowdsec-url]: https://www.crowdsec.net/
[traefik-shield]: https://img.shields.io/badge/Traefik-37abc8?style=for-the-badge
[traefik-url]: https://traefik.io/
[socket-proxy-shield]: https://img.shields.io/badge/Socket%20Proxy-94398d?style=for-the-badge
[socket-proxy-url]: https://hub.docker.com/r/linuxserver/socket-proxy
[portainer-shield]: https://img.shields.io/badge/Portainer-3abbed?style=for-the-badge
[portainer-url]: https://www.portainer.io/
[watchtower-shield]: https://img.shields.io/badge/Watchtower-416271?style=for-the-badge
[watchtower-url]: https://containrrr.dev/watchtower/
[diun-shield]: https://img.shields.io/badge/Diun-02a6f2?style=for-the-badge
[diun-url]: https://crazymax.dev/diun/
[homepage-shield]: https://img.shields.io/badge/Homepage-555555?style=for-the-badge
[homepage-url]: https://gethomepage.dev/