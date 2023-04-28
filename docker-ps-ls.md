# Docker PS&LS Guide
---
## Code Examples  
---
### Display first container  

`docker ps -l`  

```sh
CONTAINER ID   IMAGE        COMMAND                  CREATED       STATUS        PORTS                                     NAMES
d33b11d13d64   phpmyadmin   "/docker-entrypoint.…"   3 weeks ago   Up 18 hours   0.0.0.0:33333->80/tcp, :::33333->80/tcp   docker-phpmyadmin-1
```
---
### **Display running containers**  

`docker ps`  

```bash
CONTAINER ID   IMAGE              COMMAND                  CREATED         STATUS         PORTS     NAMES
52e16a6eb9d2   nginx              "/docker-entrypoint.…"   6 seconds ago   Up 5 seconds   80/tcp    web
```
---
### **Display all containers**  

`docker ps -a`  

```bash
CONTAINER ID   IMAGE              COMMAND                  CREATED       STATUS                   PORTS                                       NAMES
d33b11d13d64   phpmyadmin         "/docker-entrypoint.…"   3 weeks ago   Up 42 minutes            0.0.0.0:33333->80/tcp, :::33333->80/tcp     docker-phpmyadmin-1
653cf2404db6   91d4d2bd0a07       "docker-php-entrypoi…"   3 weeks ago   Exited (0) 3 weeks ago                                               docker-web-1
8046e86708ab   91d4d2bd0a07       "docker-php-entrypoi…"   3 weeks ago   Exited (0) 3 weeks ago                                               docker-eoc-app-1
95b175636f9f   ihtmapps2/apache   "docker-php-entrypoi…"   3 weeks ago   Exited (0) 3 weeks ago                                               docker-webv2-1
34d7b0a1190e   mariadb:10.2.44    "docker-entrypoint.s…"   3 weeks ago   Up 42 minutes            3306/tcp                                    docker-eoc-db-1
824861f0071f   mariadb:10.2.44    "docker-entrypoint.s…"   3 weeks ago   Up 42 minutes            0.0.0.0:3306->3306/tcp, :::3306->3306/tcp   docker-db-1
1617786ee00c   mailhog/mailhog    "MailHog"                3 weeks ago   Exited (2) 3 weeks ago                                               docker-mailhog-1
```
---
### **Display running container IDs**  

`docker ps -q`  

```bash
d33b11d13d64
34d7b0a1190e
824861f0071f
```
---
### **Display container sizes**  

`docker ps -s`  

```bash
CONTAINER ID   IMAGE             COMMAND                  CREATED       STATUS          PORTS                                       NAMES                 SIZE
d33b11d13d64   phpmyadmin        "/docker-entrypoint.…"   3 weeks ago   Up 43 minutes   0.0.0.0:33333->80/tcp, :::33333->80/tcp     docker-phpmyadmin-1   70B (virtual 517MB)
34d7b0a1190e   mariadb:10.2.44   "docker-entrypoint.s…"   3 weeks ago   Up 43 minutes   3306/tcp                                    docker-eoc-db-1       2B (virtual 338MB)
824861f0071f   mariadb:10.2.44   "docker-entrypoint.s…"   3 weeks ago   Up 43 minutes   0.0.0.0:3306->3306/tcp, :::3306->3306/tcp   docker-db-1           2B (virtual 338MB)
```
---
### **Pretty-print containers using a Go template**  

`docker ps --format "table {{.ID}}\t{{.Names}}"`

```bash
CONTAINER ID   NAMES
d33b11d13d64   docker-phpmyadmin-1
34d7b0a1190e   docker-eoc-db-1
824861f0071f   docker-db-1
```
### Available Options
- {{.Command}}
- {{.CreatedAt}}
- {{.ID}}
- {{.Image}}
- {{.Labels}}
- {{.LocalVolumes}}
- {{.Mounts}}
- {{.Names}}
- {{.Networks}}
- {{.Ports}}
- {{.RunningFor}}
- {{.Size}}
- {{.State}}
- {{.Status}}  
 ---
### **Docker ls**  
- An alias for `docker ps`, but with shorter name  

`docker container ls -a`  

```bash
CONTAINER ID   IMAGE              COMMAND                  CREATED          STATUS                      PORTS     NAMES
52e16a6eb9d2   nginx              "/docker-entrypoint.…"   6 minutes ago    Up 6 minutes                80/tcp    web
bca231456a7f   hello-world        "/hello"                 15 minutes ago   Exited (0) 15 minutes ago             agitated_shirley
```
---