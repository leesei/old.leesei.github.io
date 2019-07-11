---
title: Ansible
categories:
  - app
tags:
  - devops
  - ansible
toc: true
date: 2016-02-17 23:27:12
---

Ansible runs over SSH so there is no need for agent in slave nodes. This reduces dependency of the management toolchain, eliminates the possibility of the agent are down or out of date. Ansible is acquired by Red Hat in 2015.

> see `Ansible_in_Depth.pdf`

[Ansible is Simple IT Automation](https://www.ansible.com/) [github](https://github.com/ansible/ansible)
[Ansible Galaxy | Find, reuse, and share the best Ansible content](https://galaxy.ansible.com/) repository for Ansible roles
[Why use Ansible for automation and orchestration | InfoWorld](https://www.infoworld.com/article/3269748/devops/why-use-ansible-for-automation-and-orchestration.html)

[Ansible Documentation](http://docs.ansible.com/)
[Ansible Resources - Videos](https://www.ansubsible.com/videos)
[Ansible Blog | Ansible.com | Ansible](https://www.ansible.com/blog/topic/ansible)
[Ansible Blog | Ansible.com | Getting Started](https://www.ansible.com/blog/topic/getting-started)

[Ansible Webinar On Demand Introduction To Ansible](https://www.ansible.com/webinar-on-demand-ansible-introduction) !important
[Ansible Resources - AnsibleFest San Francisco 2017 Videos](https://www.ansible.com/videos-ansiblefest-sanfran-2017)
[Ansible Tutorial](https://codereviewvideos.com/course/ansible-tutorial)

[Ansible » ADMIN Magazine](http://www.admin-magazine.com/Articles/Automation-with-Ansible)
[Jan-Piet Mens :: Configuration management with Ansible](http://jpmens.net/2012/06/06/configuration-management-with-ansible/) a bit old, links are dead
[Review: Ansible shows the beef | InfoWorld](http://www.infoworld.com/article/3119346/data-center/review-ansible-shows-the-beef.html)
[Lessons from using Ansible exclusively for 2 years.](https://blog.serverdensity.com/what-ive-learnt-from-using-ansible-exclusively-for-2-years/)

[afroisalreadyinu/practical-ansible-intro: A practical guide to Ansible](https://github.com/afroisalreadyinu/practical-ansible-intro)
[ansible/ansible-examples: A few starter examples of ansible playbooks, to show features and how they work together.](https://github.com/ansible/ansible-examples)
[geerlingguy/ansible-for-devops: Ansible examples from Ansible for DevOps.](https://github.com/geerlingguy/ansible-for-devops)
[Servers For Hackers](https://github.com/Servers-for-Hackers)

```
YAML truthy
  true , True* , TRUE , yes , Yes , YES , on , On , ON , y , Y
YAML falsey
  false , False* , FALSE , no , No , NO , off , Off , OFF , n , N

module arg truthy
yes* , on , 1 , true
module arg falsey
no* , off , 0 , false

* recommended
```

## Blog

[Ansible | Best practices, tips and more](https://ansiblemaster.wordpress.com/)

## Beginners

[What is Ansible? A short DevOps Introduction - YouTube](https://www.youtube.com/watch?v=xMHVvHZ-Zn4)
[Configuration Management With Ansible: A Whirlwind Tour - YouTube](https://www.youtube.com/watch?v=fYd_KQpfBs8)
[Learn you some Ansible for great good! - YouTube](https://www.youtube.com/watch?v=qEuk65few9I)
[Michael DeHaan: Ansible - Python-Powered Radically Simple IT Automation - PyCon 2014 - YouTube](https://www.youtube.com/watch?v=Qi0AhK7PMCI)
[James Cammarata - Achieving Continuous Delivery: An Automation Story - PyCon 2015 - YouTube](https://www.youtube.com/watch?v=7tfTR42iNSs)
[Ansible for the Absolute Beginners - YouTube](https://www.youtube.com/playlist?list=PL2We04F3Y_42_PN52bT_U5o_lt6uPQqqq)

[Ansible basic usage and common issues encountered](http://www.kernel-overload.com/ansible-basic-usage-and-common-issues-encountered/)
[An Ansible Tutorial - Servers for Hackers](https://serversforhackers.com/an-ansible-tutorial)
[Ansible 101 — Medium](https://medium.com/@denot/ansible-101-d6dc9f86df0a#.1ojrwyk0w)
[Ansible 101 | zaiste.net](http://zaiste.net/2014/05/ansible_101/)
[Configuration Management 101: Writing Ansible Playbooks | DigitalOcean](https://www.digitalocean.com/community/tutorials/configuration-management-101-writing-ansible-playbooks)

[Ansible 2.0 & Beyond - YouTube](https://www.youtube.com/watch?v=sy8i4VXIVEE)
[V2 and beyond](http://www.slideshare.net/jimi-c/v2-and-beyond)
[Ansible 2.0 Has Arrived](https://www.ansible.com/blog/ansible-2.0-launch)

[Getting Started with Ansible | Ansible.com](https://www.ansible.com/get-started)
[Ansible Simply Kicks Ass | devo.ps](http://devo.ps/blog/ansible-simply-kicks-ass/)
[Automation made simple with Ansible // Speaker Deck](https://speakerdeck.com/erikaheidi/automation-made-simple-with-ansible-1)
[Ansible - The configuration management tool for humans](http://theodorosploumis.github.io/ansible-python/#/)
[Ansible from Introduction to Amazon AWS](http://www.slideshare.net/GiovanniAlbero/ansible-49674704)
[Top 5 Best and Worst Attributes of Ansible](https://www.upguard.com/articles/top-5-best-and-worst-attributes-of-ansible)

[Ansible Workshop](http://vfarcic.github.io/ansible-workshop/#/cover)
[Ansible Q&A: It Can't Make Your Breakfast Yet - CenturyLink Cloud Developer Center](https://www.ctl.io/developers/blog/post/ansible-cant-make-breakfast)

## Admin UI

[Ansible Tower | Ansible.com](https://www.ansible.com/tower) (commercial) web UI for Ansible, with logging and status
[ansible/awx: AWX Project](https://github.com/ansible/awx) upstream project for Tower

[AWX Project FAQ | Ansible.com](https://www.ansible.com/products/awx-project/faq)
[AWX » ADMIN Magazine](http://www.admin-magazine.com/Archive/2018/46/AWX)

[ansible-semaphore/semaphore: Open Source Alternative to Ansible Tower](https://github.com/ansible-semaphore/semaphore)

## Best Practices

[Playbook Best Practices — Ansible Documentation](http://docs.ansible.com/ansible/playbooks_best_practices.html)
[Ansible Best Practices: The Essentials](https://www.ansible.com/blog/ansible-best-practices-essentials)
[6 practices for super smooth Ansible experience by Maxim Chernyak](http://hakunin.com/six-ansible-practices)
[Best practices to build great Ansible playbooks | Theodo](https://www.theodo.fr/blog/2015/10/best-practices-to-build-great-ansible-playbooks/)
[fdavis/ansible-best-practices: This is my working example of Ansible best practices](https://github.com/fdavis/ansible-best-practices)

[Jan-Piet Mens :: Validate Ansible templates!](http://jpmens.net/2015/02/26/validate-ansible-templates/)

[15 Things You Should Know About Ansible](http://codeheaven.io/15-things-you-should-know-about-ansible/)

[How to use Vagrant provision with Ansible for playbook development – Linuxserver.io](https://www.linuxserver.io/index.php/2016/02/08/how-to-use-vagrant-provision-with-ansible-for-playbook-development/) !important

## Testing

[How We Test Our Ansible Roles with Molecule - The Zapier Engineering Blog - Zapier](https://zapier.com/engineering/ansible-molecule/)
[Molecule — Molecule 1.24.0 documentation](https://molecule.readthedocs.io/en/stable-1.24/)

## Inventory

Inventory is an INI-like file that describes the servers to manages, the grouping of them and the parameters for connection.

Ansible loads `/etc/ansible/hosts` by default. It's recommended to use `-i` option to pass different inventory files per use case.

The inventory file can be a program as long as it emits the correct JSON upon invocation.

[Using Ansible’s in-memory inventory to create a variable number of instances — Catalyst Cloud 1.0 documentation](https://docs.catalystcloud.io/tutorials/ansible-create-x-servers-using-in-memory-inventory.html)

## Connection Modes

> see `Scaling_and_Performance_of_the_Ansible_Management_Toolchain.pdf`

Local: affects the local system only, used for "pull" and "push-pull" topology
Paramiko: Python SSH module (obsolete since 1.2)
SSH with Control Persist: default mode, SSH connection is kept alive for a timeout (say 30 minutes)
Accelerated: temporary daemon will be created that only allows connections only from the initiating user, the communication is encrypted with AES keys exchanged in SSH, 2.5x faster than SSH

[Jan-Piet Mens :: Ansible: pull instead of push](http://jpmens.net/2012/07/14/ansible-pull-instead-of-push/)

## Variables

[Variables — Ansible Documentation](http://docs.ansible.com/ansible/playbooks_variables.html)
[Jinja2 filters — Ansible Documentation](http://docs.ansible.com/ansible/playbooks_filters.html)
[Jinja2 tests — Ansible Documentation](https://docs.ansible.com/ansible/playbooks_tests.html)
[List of Builtin Filters](http://jinja.pocoo.org/docs/dev/templates/#builtin-filters)
[Simplifying JSON Response Mocks With Jinja - sasheldon.com](http://sasheldon.com/blog/2013/12/14/simplifying-json-response-mocks-with-jinja/)

[Jinja2 for better Ansible playbooks and templates - codecentric Blog : codecentric Blog](https://blog.codecentric.de/en/2014/08/jinja2-better-ansible-playbooks-templates/)
[[Howto] Introduction to Ansible variables – /home/liquidat](https://liquidat.wordpress.com/2016/01/26/howto-introduction-to-ansible-variables/)

## Fact

[Jan-Piet Mens :: Ansible: it's a fact](http://jpmens.net/2012/07/15/ansible-it-s-a-fact/)

You can use `set_fact` to dynamically create variables:

```yml
- set_fact: 
    myvar: "{{ result.stdout | from_json }}"
```

[set_fact - Set host facts from a task — Ansible Documentation](http://docs.ansible.com/ansible/set_fact_module.html)

[Variables — Ansible Documentation](http://docs.ansible.com/ansible/playbooks_variables.html#fact-caching) fact caching
[Fast Caching facts ansible – Erik's Blog](https://blog.bytework.eu/fast-caching-facts-ansible/)

## Modules

[About Modules — Ansible Documentation](http://docs.ansible.com/ansible/modules.html)
[All Modules — Ansible Documentation](http://docs.ansible.com/ansible/list_of_all_modules.html)

[Command Module Deep Dive for Networks](https://www.ansible.com/blog/command-module-deep-dive-for-networks)

## Playbooks

[Playbooks — Ansible Documentation](http://docs.ansible.com/ansible/playbooks.html)

Playbooks contain Plays; Plays contain Tasks; Tasks invoke modules.
Handlers are tasks that can be run once after tasks.

[sed - Ansible playbook shell output - Stack Overflow](http://stackoverflow.com/questions/20563639/ansible-playbook-shell-output)
[debug - Print statements during execution — Ansible Documentation](http://docs.ansible.com/ansible/debug_module.html)

[Amon - What I learned from a year using Ansible extensively](https://www.amon.cx/blog/one-year-with-ansible/#) install, test playbook with docker

[Insanely complete Ansible playbook, showing off all the options](https://gist.github.com/phred/2897937)
[How To Create Ansible Playbooks to Automate System Configuration on Ubuntu | DigitalOcean](https://www.digitalocean.com/community/tutorials/how-to-create-ansible-playbooks-to-automate-system-configuration-on-ubuntu)

## Jinja templates

[Jinja2: lstrip_blocks to manage indentation | Ansible](https://ansiblemaster.wordpress.com/2016/07/29/jinja2-lstrip_blocks-to-manage-indentation/)
[Jinja2 for better Ansible playbooks and templates - codecentric Blog : codecentric Blog](https://blog.codecentric.de/en/2014/08/jinja2-better-ansible-playbooks-templates/)

## Docker

[Managing Docker Containers with Ansible - Linux Academy](https://linuxacademy.com/cp/socialize/index/type/community_post/id/13750)

## Alternatives

[pstadler/flightplan: Run sequences of shell commands against local and remote hosts.](https://github.com/pstadler/flightplan)
[Welcome to Fabric!](http://www.fabfile.org/) [documentation](http://docs.fabfile.org/en/latest/)

### `pdsh`

[chaos/pdsh: A high performance, parallel remote shell utility](https://github.com/chaos/pdsh)
[pdsh Parallel Shell » ADMIN Magazine](http://www.admin-magazine.com/HPC/Articles/pdsh-Parallel-Shell)

### Parallel SSH

```sh
sudo apt-get install pssh
parallel-ssh -h pssh-hosts -A -P -I < pssh-command
```

> Note: cannot `sudo`

[How to run remote commands on multiple Linux servers with Parallel-SSH - TechRepublic](https://www.techrepublic.com/google-amp/article/how-to-run-remote-commands-on-multiple-linux-servers-with-parallel-ssh/)

---

## unsorted notes

Play
  target
  vars
  handlers
  tasks

Variable hierarchy
inventory
cli
playbook
module facts

directive
vars, vars_files, vars_prompt
module 
local_action
script

async, poll

In pull mode, each managed node pull the config from git and run locally, without connecting to any controlling host machine.

AnsibleModule class, lib/ansible/module_common.py

### Role

Breakdown a playbook into a predefined directory structure for better modularization.
[Playbook Roles and Include Statements — Ansible Documentation](http://docs.ansible.com/ansible/playbooks_roles.html#roles)

Point of entry: `meta/main.yml`
Can declare dependency for other roles here.

The easiest way to create a role is with `ansible-galaxy`:
```sh
ansible-galaxy init <role>
```

[A Worked Example of Role Versioning](http://willthames.github.io/2015/04/03/worked-example-of-versioning.html)
[Ansible roles explained in practice](http://www.kernel-overload.com/ansible-roles-explained-in-practice/)
[Evan Stoner — Ansible Pattern: Using Wrappers to Parameterize...](http://blog.evanstoner.net/post/116143629247/ansible-pattern-wrapper-roles)
[Being a Star in Galaxy ● Future500 B.V.](http://www.future500.nl/articles/2015/04/being-a-star-in-galaxy/)

[Creating Ansible Roles from Scratch: Part 1 | Azavea Labs](http://www.azavea.com/blogs/labs/2014/10/creating-ansible-roles-from-scratch-part-1/)
[Creating Ansible Roles from Scratch: Part 2 | Azavea Labs](http://www.azavea.com/blogs/labs/2014/10/creating-ansible-roles-from-scratch-part-2/)

[Ansible: Roles - Servers for Hackers](https://serversforhackers.com/video/ansible-roles)

### Error Handling

[Error Handling In Playbooks — Ansible Documentation](http://docs.ansible.com/ansible/playbooks_error_handling.html)
[Error Catching in Ansible — Hey There Fancy Pants](http://www.erickenney.io/Blog//2015/02/20/handling-ansible-errors/)
[deployment - How to do proper error handling in ansible? - Server Fault](http://serverfault.com/questions/748844/how-to-do-proper-error-handling-in-ansible)

## 葉秉哲 (William Yeh)

[softarch-school/ansible-workshop: Ansible Workshop - Hands-On Materials.](https://github.com/softarch-school/ansible-workshop)
[William-Yeh/build-docker-with-ansible: Build Docker images with Ansible - A half-blood approach](https://github.com/William-Yeh/build-docker-with-ansible)

## Ansible Vault

[Vault — Ansible Documentation](http://docs.ansible.com/ansible/playbooks_vault.html)

[ansible vault - alessandromazzoli.comalessandromazzoli.com](http://www.alessandromazzoli.com/ansible-vault/)
[Safely storing Ansible playbook secrets | On Web Security](https://www.onwebsecurity.com/devops/safely-storing-ansible-playbook-secrets)
[OpenSSL the Ansible vault.. using PBKDF2 | On Web Security](https://www.onwebsecurity.com/tools/openssl-the-ansible-vault-using-pbkdf2)
[Python for Network Engineers | Articles](https://pynet.twb-tech.com/blog/ansible/vault.html)
[Specify sudo password for Ansible - Stack Overflow](http://stackoverflow.com/questions/21870083/specify-sudo-password-for-ansible)

[Ansible: Using Vault - Servers for Hackers](https://serversforhackers.com/video/ansible-using-vault)

## Ansible Container

[Container Management with Ansible](https://www.ansible.com/containers)
[5 Reasons We Started the Ansible Container Project](https://www.ansible.com/blog/ansible-container-project)
[Announcing Ansible Container 0.9](https://www.ansible.com/blog/ansible-container-0-9) 
> 0.9 revamped the commands and internal

[Ansible Container - Container Automation with Ansible](https://www.ansible.com/ansible-container)
[ansible/ansible-container: Ansible Container is a tool to build Docker images and orchestrate containers using only Ansible playbooks.](https://github.com/ansible/ansible-container)
[Ansible Container Documentation](http://docs.ansible.com/ansible-container/)

`Dockerfile` replacement with Ansible awesomeness

## Edguim

Use Ansible as a cross-platform package manager
[Edgium](http://martinrusev.github.io/edgium/#)
[Edgium packages](http://martinrusev.github.io/edgium/#packages)

[martinrusev/edgium: Collection of Ansible playbooks to quickly install up todate Linux packages](https://github.com/martinrusev/edgium)

## API

[Python API — Ansible Documentation](http://docs.ansible.com/ansible/developing_api.html)
[Jan-Piet Mens :: Obtaining remote data with Ansible's API](http://jpmens.net/2012/12/13/obtaining-remote-data-with-ansible-s-api/)
[Running Ansible Programmatically - Servers for Hackers](https://serversforhackers.com/running-ansible-programmatically)
[Running Ansible 2 Programmatically - Servers for Hackers](https://serversforhackers.com/running-ansible-2-programmatically)
[Extending Ansible – Tyler Turk's Blog](http://tylerturk.com/extending-ansible/)

---

[Ansible: Post-Install Setup](https://valdhaus.co/writings/ansible-post-install/)
[Puppet to Ansible - Big Bubbles (no troubles)](http://www.big-bubbles.fluff.org/blogs/bubbles/blog/2015/06/16/puppet-to-ansible/)

[Part 1: Getting Started with Ansible](http://tomoconnor.eu/blogish/getting-started-ansible/)
[Part 2: Deploying Applications with Ansible](http://tomoconnor.eu/blogish/part-2-deploying-applications-ansible/)
[Part 3: Ansible and Amazon Web Services](http://tomoconnor.eu/blogish/part-3-ansible-and-amazon-web-services/)
[Part 4: Ansible Tower](http://tomoconnor.eu/blogish/part-4-ansible-tower/)
[Part 5: Ansible Galaxy](http://tomoconnor.eu/blogish/part-5-ansible-galaxy/)
[tomoconnor/parallax: My collection of ansible templates, sensible defaults and an example of where to start from.](https://github.com/tomoconnor/parallax)

[Briefs on Ansible Newsletter](https://valdhaus.co/newsletters/ansible/) (ended)
[ansible | Search Results | Technology Conversations](http://technologyconversations.com/?s=ansible)

[Ansible vs. Ansible Tower](https://www.upguard.com/articles/ansible-vs.-ansible-tower)
[Shell Scripts vs Ansible: Fight!](https://valdhaus.co/writings/ansible-vs-shell-scripts/)

## #perfmatters

[Making Ansible a Bit Faster · Adam’s Tech Blog](https://adamj.eu/tech/2015/05/18/making-ansible-a-bit-faster/)
[How to accelerate your Ansible Playbooks](http://acalustra.com/acelerate-your-ansible-playbooks-with-async-tasks.html)

[Tuning Ansible » ADMIN Magazine](http://www.admin-magazine.com/Archive/2018/45/Tuning-Ansible)
[Ansible Performance Tuning (for Fun and Profit)](https://www.ansible.com/blog/ansible-performance-tuning)
[Ansible Configuration Settings — Ansible Documentation](https://docs.ansible.com/ansible/latest/reference_appendices/config.html)

```
forks = 10
callback_whitelist = timer, profile_tasks
pipelining = True
```

## Docker

[Getting Started with Docker — Ansible Documentation](http://docs.ansible.com/ansible/guide_docker.html) major updates in 2.1

[Managing Docker · Billie Thompson](https://purplebooth.co.uk/blog/2015/05/31/managing-docker/)
[Ansible and Docker](https://developer.rackspace.com/blog/ansible-and-docker/)
[Docker + Ansible = Happiness! – Alex Madrossan – Just a humble geek](http://madrossan.github.io/docker_ansible/)
[Testing Ansible Roles with Docker](https://www.ansible.com/blog/testing-ansible-roles-with-docker)
[Six Ways Ansible Makes Docker-Compose Better](https://www.ansible.com/blog/six-ways-ansible-makes-docker-compose-better)
[How Ansible and Docker Fit: Using Ansible to Bootstrap and Coordinate Docker Containers - DZone DevOps](https://dzone.com/articles/how-ansible-and-docker-fit)
[Managing Docker Containers with Ansible](https://linuxacademy.com/howtoguides/posts/show/topic/13750-managing-docker-containers-with-ansible)

['ansible docker' on SlideShare](http://www.slideshare.net/search/slideshow?searchfrom=header&q=ansible+docker)

## Monitoring

[Agile Testing: Deploying monitoring tools with ansible](http://agiletesting.blogspot.hk/2015/06/deploying-monitoring-tools-with-ansible.html)
[Ansible for Server Monitoring | Cambridge Web Design and Development by Will Hall Online](http://www.willhallonline.co.uk/blog/ansible-server-monitoring)

Ansible + Nagios/Monit + Collectd = EPIC WIN

## Tips and Tricks

[Ansible tips & tricks](http://www.slideshare.net/bcoca/ansible-tips-tricks)
[Ansible Tips and Tricks](https://ansible-tips-and-tricks.readthedocs.io/en/latest/)

[Studio Cliffano](http://blog.cliffano.com/2014/04/06/human-readable-ansible-playbook-log-output-using-callback-plugin/)

[Make Your Life Easier by Creating Utilities and Delegating Playbooks](https://www.ansible.com/blog/make-your-life-easier-by-creating-utilities-and-delegating-playbooks)

[Outage Recovery With Ansible](http://devnull.guru/outage-recovery-ansible/)
[A Shiny New Way to Manage VMware Guests](https://www.ansible.com/blog/managing
-vmware-guests)

[Graduating Past Playbooks](https://nylas.com/blog/graduating-past-playbooks)
[reinteractive | Blog | Ansible (Real Life) Good Practices](https://reinteractive.com/posts/167-ansible-real-life-good-practices)
[6 practices for super smooth Ansible experience by Maxim Chernyak](http://hakunin.com/six-ansible-practices)
`group_vars/all` can be a folder, create `group_vars/all/{config,secret}`, add the latter to `.gitignore` FTW
[Best practices to build great Ansible playbooks - Theodo](https://blog.theodo.com/2015/10/best-practices-to-build-great-ansible-playbooks/)
[10 Things you should start using in your Ansible Playbook](https://medium.com/@abhijeet.kamble619/10-things-you-should-start-using-in-your-ansible-playbook-808daff76b65)

[Deploying a GlusterFS Storage Cluster withf Ansible on DigitalOcean — Medium](https://medium.com/@jmarhee/deploying-a-glusterfs-storage-cluster-with-ansible-on-digitalocean-14dacd721e23#.whqwo6a35)
[Provisioning Gluster Servers with Ansible](http://rnowling.github.io/devops/2015/04/21/ansible-gluster.html)

## Videos

[Ansible Webinars and Training I Ansible](https://www.ansible.com/resources/webinars-training)
[Ansible Resources - Videos](https://www.ansible.com/resources/videos)

[Ansible Essentials](https://www.ansible.com/resources/webinars-training/introduction-to-ansible)

[Ansible Trips and Tricks Webinar #1 - YouTube](https://www.youtube.com/watch?v=ekpjX3_1wY4)
[Ansible Tips & Tricks Webinar #2 - YouTube](https://www.youtube.com/watch?v=k0nUa9eQWak)
[tips n tricks webinar #3 - YouTube](https://www.youtube.com/watch?v=b3PMcINjqX4)
[Ansible Tips & Tricks webinar #4 - YouTube](https://www.youtube.com/watch?v=gBZ0WrdAsqA)
[Ansible Tips & Tricks webinar #5 - YouTube](https://www.youtube.com/watch?v=F5iFGWRSG-4)

## CLI Example

```sh
ansible HOST --become -m MODULE -a MODULE_ARGS
```

```sh
ansible HOST -m setup | grep release
```

## Playbook example

[Your Debian-based data center in a box](https://debops.org/)
[pigmonkey/spark: Arch Linux Provisioning with Ansible](https://github.com/pigmonkey/spark)
[wardviaene/ansible-demo](https://github.com/wardviaene/ansible-demo)

```sh
ansible-playbook PLAYBOOK -i HOSTS --user root --ask-pass
```

```yaml
- hosts: all    
   user: root   # server user
   sudo: yes    # is it super user
- name: With module and args as keys
  apt:
    name: "{{ item }}"
    update_cache: yes
    cache_valid_time: 3600
  with_items:
    - htop
    - ngrep
    - vim
- name: With action YAML multiline
  action: apt >
    pkg={{ item }} 
    state=installed 
    update-cache=yes
  with_items:
    - python-dev
    - gcc
    - python-setuptools
    - git-core
- name: Single line
  apt: pkg={{ item }} state=installed update-cache=yes
  with_items:
    - libmysqlclient-dev
    - mysql-server
    - redis-server
    - mysql-client
    - nginx
    - apache2
```

---

## Notes for ansible-for-devops

Pretask
Ad hoc command
Apt cache valid time 
--force-handlers
Mywiki.Wooldridge.org/dotfiles
Magic variable

Precedence
-e
Inventory, connection
Play, include
Inventory, others
Facts
Role default

119
Digital ocean
122， 125
Dynamic inventory scripts
addhost, groupby
Doc, leanpub
124
Custom inventory

www.sudo.ws
245,246 selinux link

248 tower user guide,free?
260 debug

265 rolespec, ci
266 Serverspec

267 vagrant
Vagrant commands except init expects a vagrantfile in the current folder
Up, halt, suspend, ssh, sshconfig 
current folder is mapped to /vagrant
