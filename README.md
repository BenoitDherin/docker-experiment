# docker-experiment


```
curl -sSL https://get.docker.com/ubuntu/ | sudo sh
```

With [https://get.docker.com/ubuntu/](https://get.docker.com/ubuntu/) pointing to


```
# Check that HTTPS transport is available to APT
if [ ! -e /usr/lib/apt/methods/https ]; then
	apt-get update
	apt-get install -y apt-transport-https
fi

# Add the repository to your APT sources
echo deb https://get.docker.com/ubuntu docker main > /etc/apt/sources.list.d/docker.list

# Then import the repository key
apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 36A1D7869245C8950F966E92D8576A8BA88D21E9

# Install docker
apt-get update
apt-get install -y lxc-docker

#
# Alternatively, just use the curl-able install.sh script provided at https://get.docker.com
#
```
From `man docker` description:

```
     docker  has  two  distinct functions. It is used for starting the Docker daemon and to run the CLI
       (i.e., to command the daemon to manage images, containers etc.) So docker is both a server,  as  a
       daemon, and a client to the daemon, through the CLI.

       To  run the Docker daemon you do not specify any of the commands listed below but must specify the
       -d option.  The other options listed below are for the daemon only.

       The Docker CLI has over 30 commands. The commands are listed below and each has its own  man  page
       which explain usage and arguments.
 ```
