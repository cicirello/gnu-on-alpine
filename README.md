# gnu-on-alpine

[![gnu-on-alpine - A lightweight Docker container for shell scripting with GNU tools on Alpine Linux)](https://actions.cicirello.org/images/gnu-on-alpine640.png)](#gnu-on-alpine)

Website for our GitHub Actions and tools for developing them: https://actions.cicirello.org/


| __Docker Hub__ | [![Docker Image Version (latest by date)](https://img.shields.io/docker/v/cicirello/gnu-on-alpine?label=Docker%20Hub&logo=docker)](https://hub.docker.com/r/cicirello/gnu-on-alpine) [![Docker Pulls](https://img.shields.io/docker/pulls/cicirello/gnu-on-alpine?logo=docker)](https://hub.docker.com/r/cicirello/gnu-on-alpine) |
| :--- | :--- |
| __GitHub__ | [![GitHub release (latest by date)](https://img.shields.io/github/v/release/cicirello/gnu-on-alpine?logo=github)](https://github.com/cicirello/gnu-on-alpine/releases) |
| __Image Stats__ | [![Docker Image Size (latest by date)](https://img.shields.io/docker/image-size/cicirello/gnu-on-alpine?logo=docker)](https://hub.docker.com/r/cicirello/gnu-on-alpine) |
| __Build Status__ | [![build](https://github.com/cicirello/gnu-on-alpine/workflows/build/badge.svg)](https://github.com/cicirello/gnu-on-alpine/actions/workflows/docker-image.yml) |
| __License__ | [![License](https://img.shields.io/github/license/cicirello/gnu-on-alpine)](https://github.com/cicirello/gnu-on-alpine/blob/master/LICENSE) |
| __Support__ | [![GitHub Sponsors](https://img.shields.io/badge/sponsor-30363D?logo=GitHub-Sponsors&logoColor=#EA4AAA)](https://github.com/sponsors/cicirello) [![Liberapay](https://img.shields.io/badge/Liberapay-F6C915?logo=liberapay&logoColor=black)](https://liberapay.com/cicirello) [![Ko-Fi](https://img.shields.io/badge/Ko--fi-F16061?logo=ko-fi&logoColor=white)](https://ko-fi.com/cicirello) |

## Summary
The gnu-on-alpine Docker image is designed
to support shell scripting using GNU tools,
such as the bash shell, gawk, coreutils, and
findutils, while keeping the image size relatively 
small. Alpine Linux is used as the base 
image. The gnu-on-alpine image adds 
bash, findutils, coreutils, and gawk on top 
of Alpine Linux.

For more information, see my blog post on DEV: [gnu-on-alpine and alpine-plus-plus: Two Lightweight Containers for Implementing GitHub Container Actions with Shell Scripting](https://dev.to/cicirello/gnu-on-alpine-and-alpine-plus-plus-two-lightweight-containers-for-implementing-github-container-actions-with-shell-scripting-360i).

## Multiplatform Image

gnu-on-alpine has the following platforms available:
* linux/386
* linux/amd64
* linux/arm/v6
* linux/arm/v7
* linux/arm64
* linux/ppc64le
* linux/s390x

## Source Repository and Builds

The [source repository](https://github.com/cicirello/gnu-on-alpine) is maintained on GitHub.  The images are built on Github and pushed to [Docker Hub](https://hub.docker.com/r/cicirello/gnu-on-alpine), as well as the [Github Container Registry](https://github.com/cicirello?ecosystem=container&tab=packages) using Github Actions.


## Docker Tags and Versioning Scheme

Each image pushed to Docker Hub and the Github Container Registry is tagged as follows:
* The tag `latest` indicates, well, the latest image.
* Tags of the form MAJOR.MINOR.PATCH (such as 3.13.5) indicate the SemVer of 
  the __Alpine__ image used as the base.
* Tags of the form MAJOR.MINOR (e.g., 3.13) correspond to the most recent patch level of
  the __Alpine__ image used as the base. For example, if 3.13.5 is the latest
  release, then 3.13 maps to this as well.
* Tags of the form MAJOR (e.g., 3) correspond to the most recent patch level of
  the __Alpine__ image used as the base, with major corresponding major version. 
  For example, if 3.13.5 is the latest release, then 3 maps to this as well.

[Semantic Versioning](https://semver.org/) uses version numbers 
of the form: MAJOR.MINOR.PATCH, where differences in 
MAJOR correspond to incompatible changes, differences in MINOR 
correspond to introduction of backwards compatible new functionality, 
and PATCH corresponds to backwards compatible bug fixes.


## Installation and Usage

The pre-built image is hosted on both Docker Hub and the Github Container Registry. You can use it in the following ways.

### Docker Pull Command

Pull the latest image from Docker Hub with the following (replace `latest` with 
a specific version number if you prefer):

```
docker pull cicirello/gnu-on-alpine:latest
```

Pull from the Github Container Registry with:

```
docker pull ghcr.io/cicirello/gnu-on-alpine:latest
```


### Use as a base image in a Dockerfile

Use as a base image in a Dockerfile (replace `latest` with 
a specific version number if you prefer):

```Dockerfile
FROM cicirello/gnu-on-alpine:latest

# The rest of your Dockerfile would go here.
```

Or you can use as a base image (via the Github Container Registry) with:

```Dockerfile
FROM ghcr.io/cicirello/gnu-on-alpine:latest

# The rest of your Dockerfile would go here.
```

## License
### Source Code License
The source code, including the Dockerfile and anything
else within the [Github repository for gnu-on-alpine](https://github.com/cicirello/gnu-on-alpine), is licensed under the
[MIT License](https://github.com/cicirello/gnu-on-alpine/blob/master/LICENSE).

### Image Licenses
As with all pre-built Docker images, the image itself (once built, or obtained from
Docker Hub or the Github Container Registry) contains software that is covered by a
variety of licenses. Since the base image is Alpine, this would include
the [licenses of the components of Alpine](https://pkgs.alpinelinux.org/);
and also includes the [licenses of the GNU tools added to the image](https://www.gnu.org/licenses/gpl-3.0.en.html).  

If you build and distribute an image containing your software, 
using gnu-on-alpine as the base image, it
is your responsibility to follow the licenses of all of the
software contained within the image.  At the time that this documentation
is written, one of the effects of the combination of those licenses is
a constraint on the licensing of such a pre-built image containing 
your software to the GPL 3.0 or later (derived from the inclusion of bash 
and the other GNU tools).  If you desire a more permissive license
for your software, one approach would be to instead distribute a
Dockerfile that builds the image containing your software, 
rather than a pre-built image of your software, which should circumvent the
issue since you would no longer be distributing a derivative of 
GPL licensed software.

