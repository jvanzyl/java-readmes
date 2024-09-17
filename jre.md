<!--monopod:start-->
# jre
| | |
| - | - |
| **OCI Reference** | `cgr.dev/chainguard/jre` |


* [View Image in the Chainguard Images Directory](https://images.chainguard.dev/directory/image/jre/overview).
* [View the Image Catalog](https://console.chainguard.dev/images/catalog) for a full list of available tags.
* [Contact Chainguard](https://www.chainguard.dev/chainguard-images) for enterprise support, SLAs, and access to older tags.

---
<!--monopod:end-->

<!--overview:start-->
Minimalist Wolfi-based Java JRE image using [OpenJDK](https://openjdk.org/projects/jdk/). Used for running Java applications.
<!--overview:end-->

<!--getting:start-->
## Download this Image
The image is available on `cgr.dev`:

```
docker pull cgr.dev/chainguard/jre:latest
```
<!--getting:end-->

<!--body:start-->

The latest builds of Chainguard's JRE image passes the TCK for OpenJDK Java 21.0.3 and Java 22.0.1 as provided by [Oracle under the OpenJDK Community TCK License Agreement](https://openjdk.org/groups/conformance/JckAccess/index.html) (OCTLA) and are Java Compatibility Kit (JCK) conformant.

## Purpose

A JRE is the standard runtime for a Java application. It is used for running an already developed Java application.

## Running a Java Application 

- Show an example of packaging a SpringBoot application with the JRE base image and running.

<!--body:end-->
