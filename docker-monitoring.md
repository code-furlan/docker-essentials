# Docker Monitoring Guide
--- 
# Docker Inspect  

The docker inspect command is used to display detailed information about a container, image, network, or volume.  

Parameters  
--format or -f: Format the output using a Go template.  

---
## Code Examples  
- Display detailed information about a container  

`docker inspect $(docker ps -lq)`  

```sh
[
    {
        "Id": "d33b11d13d644d387a2dafc06a27189890f46ed53159683ef9de311a7e308d5b",
        "Created": "2023-04-03T18:18:49.925252924Z",
        "Path": "/docker-entrypoint.sh",
        "Args": [
            "apache2-foreground"
        ],
        "State": {
            "Status": "running",
            "Running": true,
            "Paused": false,
            "Restarting": false,
            "OOMKilled": false,
            "Dead": false,
            "Pid": 3016,
            "ExitCode": 0,
            "Error": "",
            "StartedAt": "2023-04-26T17:32:39.137996427Z",
            "FinishedAt": "2023-04-26T14:32:37.58858659-03:00"
        },
        "Image": "sha256:b2c631705a0e18f82fc4699a4be85f98046b9594282308599449f38b87f3bcb8",
        "ResolvConfPath": "/var/lib/docker/containers/d33b11d13d644d387a2dafc06a27189890f46ed53159683ef9de311a7e308d5b/resolv.conf",
        "HostnamePath": "/var/lib/docker/containers/d33b11d13d644d387a2dafc06a27189890f46ed53159683ef9de311a7e308d5b/hostname",
        "HostsPath": "/var/lib/docker/containers/d33b11d13d644d387a2dafc06a27189890f46ed53159683ef9de311a7e308d5b/hosts",
        "LogPath": "/var/lib/docker/containers/d33b11d13d644d387a2dafc06a27189890f46ed53159683ef9de311a7e308d5b/d33b11d13d644d387a2dafc06a27189890f46ed53159683ef9de311a7e308d5b-json.log",
        "Name": "/docker-phpmyadmin-1",
        "RestartCount": 0,
        "Driver": "overlay2",
        "Platform": "linux",
        "MountLabel": "",
        "ProcessLabel": "",
        "AppArmorProfile": "docker-default",
        "ExecIDs": null,
        "HostConfig": {
            "Binds": null,
            "ContainerIDFile": "",
            "LogConfig": {
                "Type": "json-file",
                "Config": {}
            },
            "NetworkMode": "docker_ihtmapps",
            "PortBindings": {
                "80/tcp": [
                    {
                        "HostIp": "",
                        "HostPort": "33333"
                    }
                ]
            },
            "RestartPolicy": {
                "Name": "always",
                "MaximumRetryCount": 0
            },
            "AutoRemove": false,
            "VolumeDriver": "",
            "VolumesFrom": null,
            "ConsoleSize": [
                0,
                0
            ],
            "CapAdd": null,
            "CapDrop": null,
            "CgroupnsMode": "private",
            "Dns": [],
            "DnsOptions": [],
            "DnsSearch": [],
            "ExtraHosts": [],
            "GroupAdd": null,
            "IpcMode": "private",
            "Cgroup": "",
            "Links": null,
            "OomScoreAdj": 0,
            "PidMode": "",
            "Privileged": false,
            "PublishAllPorts": false,
            "ReadonlyRootfs": false,
            "SecurityOpt": null,
            "UTSMode": "",
            "UsernsMode": "",
            "ShmSize": 67108864,
            "Runtime": "runc",
            "Isolation": "",
            "CpuShares": 0,
            "Memory": 0,
            "NanoCpus": 0,
            "CgroupParent": "",
            "BlkioWeight": 0,
            "BlkioWeightDevice": null,
            "BlkioDeviceReadBps": null,
            "BlkioDeviceWriteBps": null,
            "BlkioDeviceReadIOps": null,
            "BlkioDeviceWriteIOps": null,
            "CpuPeriod": 0,
            "CpuQuota": 0,
            "CpuRealtimePeriod": 0,
            "CpuRealtimeRuntime": 0,
            "CpusetCpus": "",
            "CpusetMems": "",
            "Devices": null,
            "DeviceCgroupRules": null,
            "DeviceRequests": null,
            "MemoryReservation": 0,
            "MemorySwap": 0,
            "MemorySwappiness": null,
            "OomKillDisable": null,
            "PidsLimit": null,
            "Ulimits": null,
            "CpuCount": 0,
            "CpuPercent": 0,
            "IOMaximumIOps": 0,
            "IOMaximumBandwidth": 0,
            "MaskedPaths": [
                "/proc/asound",
                "/proc/acpi",
                "/proc/kcore",
                "/proc/keys",
                "/proc/latency_stats",
                "/proc/timer_list",
                "/proc/timer_stats",
                "/proc/sched_debug",
                "/proc/scsi",
                "/sys/firmware"
            ],
            "ReadonlyPaths": [
                "/proc/bus",
                "/proc/fs",
                "/proc/irq",
                "/proc/sys",
                "/proc/sysrq-trigger"
            ]
        },
        "GraphDriver": {
            "Data": {
                "LowerDir": "/var/lib/docker/overlay2/6795d2e0bebae2f22a048828ca5e45a6fc01ad9e31336cc76a1365f44cb27c49-init/diff:/var/lib/docker/overlay2/e40aac029c10163cf12b341424cc3ca1c5b9560eea859427ee1abcb4bf7779df/diff:/var/lib/docker/overlay2/2e075318c4b26f078eac6a39286b9137b02fe895db04b07a6bf2e49253e7a691/diff:/var/lib/docker/overlay2/ad9e9400055818fc731541f7f4e042ac2544d956b7445b27f555651ce5e556f8/diff:/var/lib/docker/overlay2/d7991c0c174e42895877ca1679752d6adea753b289d41b848ad51cf7bb71d078/diff:/var/lib/docker/overlay2/f2197460275ec45b518bc166824d14ff838eb3b9360f03fbcab748465420ec44/diff:/var/lib/docker/overlay2/c160176d6d37fc92cbf758e81a0d0d82fe3ff81b5ad7bc5a337d18f1c4c536d7/diff:/var/lib/docker/overlay2/ecc937b98d7a9e1e60fe91cf8e504572cb508472dfd845dedb6de44517998175/diff:/var/lib/docker/overlay2/e530d1e67065c09037d18fe2995012d8950961d56c8c247ebf88a884e6c8d1de/diff:/var/lib/docker/overlay2/05dd01c1d014df662c9cc251f519f40aa9f5ad508f9d3d1d840624b113ff789a/diff:/var/lib/docker/overlay2/cd130959819357f55a938ff3d9805198aa95f28e644916304ad2f9f50fad95c7/diff:/var/lib/docker/overlay2/9f819527d4eb76554005e0ad6a0e37937e1d6f1dd3c0e443848a9788461b5e42/diff:/var/lib/docker/overlay2/9ef9b5871ec0bca42a5d34c7e09b46bef85b7ee1aef71fe2dd76eca21b3577aa/diff:/var/lib/docker/overlay2/c9167d79ba236b001faa748d766b27aa9f77642d9401700bd480cf12f94ce62c/diff:/var/lib/docker/overlay2/7c1ba4f9bc28f4de8ae3e33b140c5433450d081bd03dda32dfb4dd3fc2f2e0fc/diff:/var/lib/docker/overlay2/5cb9e1966c601ed316f10f5c24b8dca45c888f027f792ec0c94abd5ea431def7/diff:/var/lib/docker/overlay2/5a81a478cf9a19a58a8c0e5bbe4efffedd3770ced9e799c8ddafa33b70c3b9f4/diff:/var/lib/docker/overlay2/73bc974bbb6f0490ad07b2d0ff7a56aa18d1d9ff8cf0c83cbb1877ac0d658cae/diff:/var/lib/docker/overlay2/9ce619a2845c0a11e11b273181ddc19185629fc78f643f70a10ab14acde0e933/diff",
                "MergedDir": "/var/lib/docker/overlay2/6795d2e0bebae2f22a048828ca5e45a6fc01ad9e31336cc76a1365f44cb27c49/merged",
                "UpperDir": "/var/lib/docker/overlay2/6795d2e0bebae2f22a048828ca5e45a6fc01ad9e31336cc76a1365f44cb27c49/diff",
                "WorkDir": "/var/lib/docker/overlay2/6795d2e0bebae2f22a048828ca5e45a6fc01ad9e31336cc76a1365f44cb27c49/work"
            },
            "Name": "overlay2"
        },
        "Mounts": [],
        "Config": {
            "Hostname": "d33b11d13d64",
            "Domainname": "",
            "User": "",
            "AttachStdin": false,
            "AttachStdout": true,
            "AttachStderr": true,
            "ExposedPorts": {
                "80/tcp": {}
            },
            "Tty": false,
            "OpenStdin": false,
            "StdinOnce": false,
            "Env": [
                "PMA_HOSTS=db,eoc-db",
                "PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin",
                "PHPIZE_DEPS=autoconf \t\tdpkg-dev \t\tfile \t\tg++ \t\tgcc \t\tlibc-dev \t\tmake \t\tpkg-config \t\tre2c",
                "PHP_INI_DIR=/usr/local/etc/php",
                "APACHE_CONFDIR=/etc/apache2",
                "APACHE_ENVVARS=/etc/apache2/envvars",
                "PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64",
                "PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64",
                "PHP_LDFLAGS=-Wl,-O1 -pie",
                "GPG_KEYS=528995BFEDFBA7191D46839EF9BA0ADA31CBD89E 39B641343D8C104B2B146DC3F9C39DC0B9698544 F1F692238FBC1666E5A5CCD4199F9DFEF6FFBAFD",
                "PHP_VERSION=8.1.16",
                "PHP_URL=https://www.php.net/distributions/php-8.1.16.tar.xz",
                "PHP_ASC_URL=https://www.php.net/distributions/php-8.1.16.tar.xz.asc",
                "PHP_SHA256=d61f13d96a58b93c39672b58f25e1ee4ce88500f4acb1430cb01a514875c1258",
                "MAX_EXECUTION_TIME=600",
                "MEMORY_LIMIT=512M",
                "UPLOAD_LIMIT=2048K",
                "VERSION=5.2.1",
                "SHA256=373f9599dfbd96d6fe75316d5dad189e68c305f297edf42377db9dd6b41b2557",
                "URL=https://files.phpmyadmin.net/phpMyAdmin/5.2.1/phpMyAdmin-5.2.1-all-languages.tar.xz"
            ],
            "Cmd": [
                "apache2-foreground"
            ],
            "Image": "phpmyadmin",
            "Volumes": null,
            "WorkingDir": "/var/www/html",
            "Entrypoint": [
                "/docker-entrypoint.sh"
            ],
            "OnBuild": null,
            "Labels": {
                "com.docker.compose.config-hash": "1efa1cdc4c84bc6c425b862e892293e020191026ca437c147f4172bc082d1c0f",
                "com.docker.compose.container-number": "1",
                "com.docker.compose.depends_on": "db:service_started:false,eoc-db:service_started:false",
                "com.docker.compose.image": "sha256:b2c631705a0e18f82fc4699a4be85f98046b9594282308599449f38b87f3bcb8",
                "com.docker.compose.oneoff": "False",
                "com.docker.compose.project": "docker",
                "com.docker.compose.project.config_files": "/home/furlan/iHM/repos/ihtmapps/docker/docker-compose.app.yml",
                "com.docker.compose.project.working_dir": "/home/furlan/iHM/repos/ihtmapps/docker",
                "com.docker.compose.service": "phpmyadmin",
                "com.docker.compose.version": "2.17.2",
                "org.opencontainers.image.authors": "The phpMyAdmin Team <developers@phpmyadmin.net>",
                "org.opencontainers.image.description": "Run phpMyAdmin with Alpine, Apache and PHP FPM.",
                "org.opencontainers.image.documentation": "https://github.com/phpmyadmin/docker#readme",
                "org.opencontainers.image.licenses": "GPL-2.0-only",
                "org.opencontainers.image.source": "https://github.com/phpmyadmin/docker.git",
                "org.opencontainers.image.title": "Official phpMyAdmin Docker image",
                "org.opencontainers.image.url": "https://github.com/phpmyadmin/docker#readme",
                "org.opencontainers.image.vendor": "phpMyAdmin",
                "org.opencontainers.image.version": "5.2.1"
            },
            "StopSignal": "SIGWINCH"
        },
        "NetworkSettings": {
            "Bridge": "",
            "SandboxID": "59d62a2e1cea6a9df570dd1ae5da5e64d65737348b240d2825880ce743739c15",
            "HairpinMode": false,
            "LinkLocalIPv6Address": "",
            "LinkLocalIPv6PrefixLen": 0,
            "Ports": {
                "80/tcp": [
                    {
                        "HostIp": "0.0.0.0",
                        "HostPort": "33333"
                    },
                    {
                        "HostIp": "::",
                        "HostPort": "33333"
                    }
                ]
            },
            "SandboxKey": "/var/run/docker/netns/59d62a2e1cea",
            "SecondaryIPAddresses": null,
            "SecondaryIPv6Addresses": null,
            "EndpointID": "",
            "Gateway": "",
            "GlobalIPv6Address": "",
            "GlobalIPv6PrefixLen": 0,
            "IPAddress": "",
            "IPPrefixLen": 0,
            "IPv6Gateway": "",
            "MacAddress": "",
            "Networks": {
                "docker_ihtmapps": {
                    "IPAMConfig": null,
                    "Links": null,
                    "Aliases": [
                        "docker-phpmyadmin-1",
                        "phpmyadmin",
                        "d33b11d13d64"
                    ],
                    "NetworkID": "7e987bb868c58af6dda478537fb43170da58d7bef6735e3d2f277b6df41c0208",
                    "EndpointID": "9d85a0251dc00cf3ccc52ddd6d08569dbfa4fa123a7e10e0eb5e5b754e52fc7c",
                    "Gateway": "172.21.0.1",
                    "IPAddress": "172.21.0.4",
                    "IPPrefixLen": 16,
                    "IPv6Gateway": "",
                    "GlobalIPv6Address": "",
                    "GlobalIPv6PrefixLen": 0,
                    "MacAddress": "02:42:ac:15:00:04",
                    "DriverOpts": null
                }
            }
        }
    }
]
```

- Display State Information in  using Json schema  

`docker inspect --format '{{json .State}}' $(docker ps -lq)`

```sh
{"Status":"running","Running":true,"Paused":false,"Restarting":false,"OOMKilled":false,"Dead":false,"Pid":3016,"ExitCode":0,"Error":"","StartedAt":"2023-04-26T17:32:39.137996427Z","FinishedAt":"2023-04-26T14:32:37.58858659-03:00"}
```
---
- Display the running processes of a container  

`docker top $(docker ps -lq)`

```sh
UID                 PID                 PPID                C                   STIME               TTY                 TIME                CMD
root                3016                2977                0                   abr26               ?                   00:00:01            apache2 -DFOREGROUND
www-data            3253                3016                0                   abr26               ?                   00:00:00            apache2 -DFOREGROUND
www-data            3254                3016                0                   abr26               ?                   00:00:00            apache2 -DFOREGROUND
www-data            3255                3016                0                   abr26               ?                   00:00:00            apache2 -DFOREGROUND
www-data            3256                3016                0                   abr26               ?                   00:00:00            apache2 -DFOREGROUND
www-data            3257                3016                0                   abr26               ?                   00:00:00            apache2 -DFOREGROUND
```

---
# Docker Stats  
---

The docker stats command is used to display a live stream of container resource usage statistics. This includes CPU usage, memory usage, network input/output, and block I/O.

Parameters
--all or -a: Show stats for all containers, including stopped containers.  
--format or -f: Format the output using a Go template.  
--no-stream or --no-trunc: Disable the streaming output and disable truncation of the container IDs.  
--no-stream and --no-trunc together will display a single output of the container stats.  

---
## Code Examples  

- Display real-time statistics about a container  

`docker stats $(docker ps -lq)`

```sh
CONTAINER ID   NAME                  CPU %     MEM USAGE / LIMIT     MEM %     NET I/O      BLOCK I/O       PIDS
d33b11d13d64   docker-phpmyadmin-1   0.01%     15.64MiB / 15.37GiB   0.10%     329kB / 0B   105MB / 4.1kB   6
```

- Display the resource usage statistics for all containers (including stopped containers) in a table format.  

`docker stats --all --format "table {{.Name}}\t{{.CPUPerc}}\t{{.MemUsage}}\t{{.NetIO}}\t{{.BlockIO}}"`

```sh
NAME                  CPU %     MEM USAGE / LIMIT     NET I/O      BLOCK I/O
docker-phpmyadmin-1   0.00%     15.64MiB / 15.37GiB   342kB / 0B   105MB / 4.1kB
docker-web-1          0.00%     0B / 0B               0B / 0B      0B / 0B
docker-eoc-app-1      0.00%     0B / 0B               0B / 0B      0B / 0B
docker-webv2-1        0.00%     0B / 0B               0B / 0B      0B / 0B
docker-eoc-db-1       0.06%     85.05MiB / 15.37GiB   342kB / 0B   81MB / 4.46MB
docker-db-1           0.05%     135.2MiB / 15.37GiB   342kB / 0B   225MB / 4.46MB
docker-mailhog-1      0.00%     0B / 0B               0B / 0B      0B / 0B
```

---
# Docker Diff
---

- Display changes made to a container  

`docker diff $(docker ps -lq)`

---
# Docker History
---

- Display the history of an image  

`docker history ihtmapps/apache:latest`  

- Display image IDs  

`docker history -q ihtmapps/apache:latest`  

---
# Docker Events  
---

- The docker events command is used to display real-time events from the Docker daemon. This includes events related to containers, images, volumes, and networks.

Parameters  
--since or -s: Show events created since a specific timestamp or ID.  
--until or -u: Show events created until a specific timestamp or ID.  
--filter or -f: Filter events based on specific criteria.  
--format or -format: Format the output using a Go template.  

## Code Examples  

- Display all real-time events from the Docker daemon  

`docker events`

- Display all container-related events between January 1, 2022 and January 2, 2022, and format the output to display the event type, action, and container ID  

`docker events --since "2022-01-01T00:00:00Z" --until "2022-01-02T00:00:00Z" --filter 'type=container' --format "{{.Type}} {{.Action}} {{.Actor.ID}}"`

---
# Docker top
---

- Display the running processes of a container

Parameters
--no-stream: Disable the streaming output and display the process list as a single output.  

## Code Examples  

- Display the running processes of the container named container_name  

`docker top container_name  

- Display the running processes of the container named container_name in a single output

`docker top --no-stream container_name`  

---
# Docker logs
--- 
- Display the logs of a container

Parameters
--follow or -f:

## Code Examples  

`docker logs $(docker ps -lq)`