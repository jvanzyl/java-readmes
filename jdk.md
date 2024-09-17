<!--monopod:start-->
# jdk
| | |
| - | - |
| **OCI Reference** | `cgr.dev/chainguard/jdk` |


* [View Image in the Chainguard Images Directory](https://images.chainguard.dev/directory/image/jdk/overview).
* [View the Image Catalog](https://console.chainguard.dev/images/catalog) for a full list of available tags.
* [Contact Chainguard](https://www.chainguard.dev/chainguard-images) for enterprise support, SLAs, and access to older tags.

---
<!--monopod:end-->

<!--overview:start-->
Minimalist Wolfi-based Java JDK image using using [OpenJDK](https://openjdk.org/projects/jdk/).  Used for developing Java applications.
<!--overview:end-->

<!--getting:start-->
## Download this Image
The image is available on `cgr.dev`:

```
docker pull cgr.dev/chainguard/jdk:latest
```
<!--getting:end-->

<!--body:start-->

The latest builds of Chainguard's JDK image passes the TCK for OpenJDK Java 21.0.3 and Java 22.0.1 as provided by [Oracle under the OpenJDK Community TCK License Agreement](https://openjdk.org/groups/conformance/JckAccess/index.html) (OCTLA) and are Java Compatibility Kit (JCK) conformant.

## Purpose

A JDK is the standard development system for a Java application. It is used for compiling and packaging Java application, which is then subsequently run on a JRE.

## Compiling a Minimal Java Application Example

This section outlines how you can build a Java application with the Chainguard JDK Image.

Start by creating a sample Java class named `HelloWolfi.java`:

```sh
cat >HelloWolfi.java <<EOL
class HelloWolfi
{
    public static void main(String args[])
    {
        System.out.println("Hello Wolfi users!");
    }
}
EOL
```

Then create a multistage Dockerfile, adding the Java class you just created:

```sh
cat >Dockerfile <<EOL
FROM cgr.dev/chainguard/jdk

COPY HelloWolfi.java /home/build/
RUN javac HelloWolfi.java

FROM cgr.dev/chainguard/jre

COPY --from=0 /home/build/HelloWolfi.class /app/
CMD ["HelloWolfi"]
EOL
```

Following that, you can build the image:

```sh
docker build -t my-java-app .
```

Note that this example tags the image with `my-java-app`. You can now run the image by referencing this tag, as in the following command:

```sh
docker run my-java-app
```
```
Hello Wolfi users!
```

## Using the JDK to create a custom JRE

- [Creating your own runtime using jlink](https://adoptium.net/en-GB/blog/2021/10/jlink-to-produce-own-runtime/)
- https://adriankodja.com/creating-a-custom-jre-for-your-java-applications

<!--body:end-->

