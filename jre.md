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
## Compatibility Notes

## Getting Started

A JRE is the standard runtime for a Java application. It is used for running an already developed, and packaged Java application. Generally you will combine your application with the Chainguard JRE image with Docker or a build tool like [Maven](https://apache.maven.org) or [Gradle](https://gradle.org/)

## Using JIB to build a JRE-based application image

Using Maven or Gradle you can compile and package your application. There is a great example application that works with Maven or Gradle here: [https://github.com/GoogleContainerTools/jib/tree/master/examples/spring-boot](https://github.com/GoogleContainerTools/jib/tree/master/examples/spring-boot)

There is an easy way shown in the example to use the `cgr.dev/chainguard/jre` image from the Maven or Gradle project.

## Using Helm to Deploy your Java Application

Using [Helm](https://helm.sh/) to deploy your JRE-based application image is relatively straight forward using either [https://github.com/gruntwork-io/helm-kubernetes-services/blob/main/charts/k8s-service](https://github.com/gruntwork-io/helm-kubernetes-services/blob/main/charts/k8s-service/README.md) or [https://artifacthub.io/packages/helm/kvalitetsit/service](https://artifacthub.io/packages/helm/kvalitetsit/service)

## Documentation and Resources

- [How to Migrate a Java Application to Chainguard Images](https://edu.chainguard.dev/chainguard/chainguard-images/videos/java-images/) (video)
- [Building Minimal Images for Applications with Runtimes](https://edu.chainguard.dev/chainguard/chainguard-images/videos/minimal-runtime-images/) (video)
- [Building minimal and low CVE images for Java](https://www.chainguard.dev/unchained/building-minimal-and-low-cve-images-for-java)

The latest builds of Chainguard's JRE image passes the TCK for OpenJDK Java 21.0.3 and Java 22.0.1 as provided by [Oracle under the OpenJDK Community TCK License Agreement](https://openjdk.org/groups/conformance/JckAccess/index.html) (OCTLA) and are [Java Compatibility Kit (JCK) conformant](https://www.chainguard.dev/unchained/chainguards-openjdk-java-images-are-now-jck-conformant).
<!--body:end-->
