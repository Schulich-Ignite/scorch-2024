# Day 6; Basic networking & Deploying sites

We can create sites now, but how do we get them on the internet, and for that matter how does the internet work? In this session we will cover the basics of networking on the internet, and how to deploy a website. We will also look into CI/CD (automation) to help make these processes easier.

## Resources

Here are a list of the additional resources from the [slides](https://docs.google.com/presentation/d/16miIc0UGVLDbKlSoBHTC3bLk78eb3AAqmhmWSQNdMzk/edit?usp=sharing)

### Table of contents
- [Git](#git)
- [Other static site hosts](#other-static-site-hosts)
- [Virtual Machines/containers](#virtual-machinescontainers)
- [Some other CI/CD Systems](#some-other-cicd-systems)
- [Some other CI/CD or github actions Uses](#some-other-cicd-or-github-actions-uses)
- [Examples in action](#examples-in-action)
- [If you want more detail](#if-you-want-more-detail)
- [Some interesting commands](#some-interesting-commands)
- [Using a custom domain with github pages](#using-a-custom-domain-with-github-pages)


### Git

If you are interested in learning more about git you can check out a video recorded on the topic [here](https://www.youtube.com/watch?v=NwASRGFz5Wg)


### Other static site hosts

Some alternatives to github pages for those who are interested

-   [Cloudflare pages](https://pages.cloudflare.com/)
-   [AWS (Amazon Web Services) Amplify](https://aws.amazon.com/amplify/hosting/)
-   [AWS (Amazon Web Services) S3](https://aws.amazon.com/s3/)
-   [GitLab Pages](https://docs.gitlab.com/ee/user/project/pages/)
-   [FireBase](https://firebase.google.com/products/hosting)

### Virtual Machines/containers


Here is some additional information about VM’s and containers for those interested:

-   [Introduction to VM’s](https://www.youtube.com/watch?v=wX75Z-4MEoM)
-   [Introduction to containers](https://www.youtube.com/watch?v=eGz9DS-aIeY)
-   Software to make VM’s
    -   [Virtualbox](https://www.virtualbox.org/)
    -   [vmware](https://www.vmware.com/ca.html)
    -   [proxmox](https://www.proxmox.com/en/)
-   Software to make containers
    -   [Docker](https://www.docker.com/)

### Some other CI/CD Systems


Here are some other CI/CD Systems to check out

-   [Ansible](https://www.ansible.com/)
    
-   [Azure](https://azure.microsoft.com/en-us/products/devops/pipelines/)
    
-   [Travis CI](https://www.travis-ci.com/)
    
-   [Gitlab](https://docs.gitlab.com/ee/ci/)
    
-   [Jenkins](https://www.jenkins.io/)
    
-   [Nox](https://nox.thea.codes/en/stable/) (local python CI/CD)


### Some other CI/CD or github actions Uses

-   [Minify HTML/CSS/JS](https://github.com/marketplace/actions/minify-css-js-and-html-files-in-github-action)
    
-   [Format your code](https://github.com/marketplace/actions/prettier-action)
    
-   [Optimize images](https://github.com/calibreapp/image-actions)
    
-   [Check if dependencies are up to date](https://docs.github.com/en/code-security/dependabot/working-with-dependabot/automating-dependabot-with-github-actions)
    
-   [Security Auditing](https://github.com/apps/mend-bolt-for-github)
    
-   [Building assets](https://github.com/QU-UP/ezcv-themes/blob/main/.github/workflows/release.yml#L18-L31)
    
-   [Checking for password leaks in code](https://github.com/marketplace/actions/gitleaks)
    
-   [Static Code analysis](https://deepsource.io/) (lots of the above all in one)
    

  

Used to build everything from a static site to entire [operating systems!](https://www.linuxmint.com)

### Examples in action


-   [Schulich ignite](https://github.com/Schulich-Ignite/website)
    
-   [Ezcv included themes builder](https://github.com/QU-UP/ezcv-themes/blob/main/.github/workflows/release.yml)
    
-   [ahd automated testing + documentation](https://github.com/Descent098/ahd/tree/master/.github/workflows)
    
-   [Bootstrap for a ton of stuff](https://github.com/twbs/bootstrap/tree/main/.github/workflows)
    
-   [PokeAPI using it to create new containers](https://github.com/PokeAPI/pokeapi/tree/master/.github/workflows) (CD)
    
-   [Most of my websites](https://canadiancoding.ca/)


### If you want more detail

You can find a slideshow with more details about HTTP, DNS and everything else [here](https://kieranwood.ca/basic-networking-infastructure/#slide=58)

### Some interesting commands

Watch a request:

```bash
Windows: tracert <hostname>
*nix: tracepath <hostname>
```

Get IP of domain:

```bash
	ping <domain>
```

### Using a custom domain with github pages

Steps:

1.  Buy a domain
2.  Point the nameservers to a DNS provider or use the built in one
3.  On the DNS side you will need to add 4 [A records](https://docs.github.com/en/pages/configuring-a-custom-domain-for-your-github-pages-site/managing-a-custom-domain-for-your-github-pages-site#configuring-an-apex-domain:~:text=185.199.108.153%0A185.199.109.153%0A185.199.110.153%0A185.199.111.153), or A[AA records](https://docs.github.com/en/pages/configuring-a-custom-domain-for-your-github-pages-site/managing-a-custom-domain-for-your-github-pages-site#configuring-an-apex-domain:~:text=2606%3A50c0%3A8000%3A%3A153%0A2606%3A50c0%3A8001%3A%3A153%0A2606%3A50c0%3A8002%3A%3A153%0A2606%3A50c0%3A8003%3A%3A153) for the correct IP addresses
4.  Go into the github pages setting and add a field to the [custom domain setting](https://docs.github.com/en/pages/configuring-a-custom-domain-for-your-github-pages-site/managing-a-custom-domain-for-your-github-pages-site#configuring-an-apex-domain:~:text=a%20subdomain.%22-,On%20GitHub%2C%20navigate%20to%20your%20site%27s%20repository.,see%20%22Configuring%20a%20publishing%20source%20for%20your%20GitHub%20Pages%20site.%22,-Navigate%20to%20your)

