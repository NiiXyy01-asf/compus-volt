
nano Dockerfille
docker build -t getting-started .
[+] Building 188.8s (11/12)                                                                                                      docker:default
 => [internal] load build definition from Dockerfile                                                                                       0.0s
 => => transferring dockerfile: 181B                                                                                                       0.0s
 => resolve image config for docker-image://docker.io/docker/dockerfile:1                                                                  8.7s
 => [auth] docker/dockerfile:pull token for registry-1.docker.io                                                                           0.0s
 => docker-image://docker.io/docker/dockerfile:1@sha256:4edf897a3ffa55b89f906fc8cc78afdb3f1834cc9c7083565e611a8a7d5fe99e                  29.4s
[+] Building 223.8s (13/13) FINISHED                                                                                             docker:default
 => [internal] load build definition from Dockerfile                                                                                       0.0s
 => => transferring dockerfile: 181B                                                                                                       0.0s
 => resolve image config for docker-image://docker.io/docker/dockerfile:1                                                                  8.7s
 => [auth] docker/dockerfile:pull token for registry-1.docker.io                                                                           0.0s
 => docker-image://docker.io/docker/dockerfile:1@sha256:4edf897a3ffa55b89f906fc8cc78afdb3f1834cc9c7083565e611a8a7d5fe99e                  29.4s
 => => resolve docker.io/docker/dockerfile:1@sha256:4edf897a3ffa55b89f906fc8cc78afdb3f1834cc9c7083565e611a8a7d5fe99e                       0.0s
 => => sha256:9d2b4f57f9e20f33279375ce25c6ff14f30f64270ed5c7b613b2b30256754f62 14.28MB / 14.28MB                                          28.9s
 => => extracting sha256:9d2b4f57f9e20f33279375ce25c6ff14f30f64270ed5c7b613b2b30256754f62                                                  0.4s
 => [internal] load metadata for docker.io/library/node:22-alpine                                                                          2.9s
 => [auth] library/node:pull token for registry-1.docker.io                                                                                0.0s
 => [internal] load .dockerignore                                                                                                          0.1s
 => => transferring context: 59B                                                                                                           0.0s
 => [1/4] FROM docker.io/library/node:22-alpine@sha256:fe4f6d74e20370acb04ad889077d14d0f64a9c8ea6a42bc60cddf1e844699914                  134.3s
 => => resolve docker.io/library/node:22-alpine@sha256:fe4f6d74e20370acb04ad889077d14d0f64a9c8ea6a42bc60cddf1e844699914                    0.1s
 => => sha256:304511616d6a6d472222f696b9045e20dc90e8043b2a8ba2acb61746595781f3 442B / 442B                                                 0.5s
 => => sha256:7246d4c6a55dd0f8dd00d2e63aece3a68d91e6a5d04c4e748fc2706897d96312 1.26MB / 1.26MB                                             5.8s
 => => sha256:8776aa3d2ba7247a375d06dcec03856b99dbb0e16e904a5672d3bf08c852d4f1 56.22MB / 56.22MB                                         132.3s
 => => sha256:7b229517ed222597277036d94892173207d01a731ab3a88eeb1de2e963a2c788 3.85MB / 3.85MB                                            14.2s
 => => extracting sha256:7b229517ed222597277036d94892173207d01a731ab3a88eeb1de2e963a2c788                                                  0.1s
 => => extracting sha256:8776aa3d2ba7247a375d06dcec03856b99dbb0e16e904a5672d3bf08c852d4f1                                                  1.6s
 => => extracting sha256:7246d4c6a55dd0f8dd00d2e63aece3a68d91e6a5d04c4e748fc2706897d96312                                                  0.1s
 => => extracting sha256:304511616d6a6d472222f696b9045e20dc90e8043b2a8ba2acb61746595781f3                                                  0.0s
 => [internal] load build context                                                                                                          0.2s
 => => transferring context: 4.57MB                                                                                                        0.1s
 => [2/4] WORKDIR /app                                                                                                                     0.4s
 => [3/4] COPY . .                                                                                                                         0.1s
 => [4/4] RUN yarn install --production                                                                                                   41.9s
 => exporting to image                                                                                                                     5.5s
 => => exporting layers                                                                                                                    2.1s
 => => exporting manifest sha256:2c61a3983e94e7512b6ef4acbbe70a790cbc5a853bb2e7dc257c0dec42db51e3                                          0.0s
 => => exporting config sha256:39b88a5f8d3234a60641dbfc19105191d3ed2cb55cbbaa65b223dbabda28285f                                            0.0s
 => => exporting attestation manifest sha256:5944d0145e43283df028cf51dd27b0d89e2cd9694c3f222a791d98208bc2fb2b                              0.1s
 => => exporting manifest list sha256:c71080705bfc84f0c1179c6cdce67c263b2343a30f2d9c8535ef3bd638601aa3                                     0.0s
 => => naming to docker.io/library/getting-started:latest                                                                                  0.0s
 => => unpacking to docker.io/library/getting-started:latest    

docker run -d --name todo -p 127.0.0.1:3000:3000 getting-started
74598313a4605bdcab10a49968ee71e7dd0c8f2549a05a1a11c5f4b9b97f6d72
docker ps
CONTAINER ID   IMAGE             COMMAND                  CREATED         STATUS         PORTS                      NAMES
74598313a460   getting-started   "docker-entrypoint.s…"   8 minutes ago   Up 8 minutes   127.0.0.1:3000->3000/tcp   todo
docker exec todo ps aux
PID   USER     TIME  COMMAND
    1 root      0:00 node src/index.js
   18 root      0:00 ps aux

docker exec todo hostname
74598313a460

docker exec todo cat /etc/os-release
NAME="Alpine Linux"
ID=alpine
VERSION_ID=3.24.3
PRETTY_NAME="Alpine Linux v3.24"
HOME_URL="https://alpinelinux.org/"
BUG_REPORT_URL="https://gitlab.alpinelinux.org/alpine/aports/-/issues"
 
docker inspect -f '{{.State.Pid}}' todo
826

 
