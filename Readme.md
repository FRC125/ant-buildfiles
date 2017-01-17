# Nutrons Basepom

Maven allows you to specify 1 pom that you pull in settings from. This is the
"basepom" for all Nutrons projects, from this pom you pull in most of the
non-project specific settings you need in order to build a Nutrons project using
maven. [Maven doc](https://maven.apache.org/pom.html#Inheritance)

* Our basepom uses the `sortpom-maven-plugin` to enforce a sort on all child poms (so that they're easier to read and
understand).
* Our basepom uses the `maven-checkstyle-plugin` to enforce java style according
  to the [Google Style Guide](https://raw.githubusercontent.com/checkstyle/checkstyle/master/src/main/resources/google_checks.xml)
* This pom sets up the local repository to find the WPILibs in, which requires that this project is configured as a sub-module.



This project is published on [jitpack](https://jitpack.io/#FRC125/ant-buildfiles) an awesome site
that makes it super easy to turn a repository into a downloadable jar for use as
a dependency.

## Release
To cut a release:
1. bump the version in `pom.xml` to `1.0.x`.
2. Push to master
3. Make a release [here](https://github.com/FRC125/maven-build-files/releases)
   using the version # that you bumped to.
4. Go to jitpack https://jitpack.io/#FRC125/maven-build-files, and log in.
5. Click `get it` next to the version that you just cut a release for.
6. Wait for jitpack to build it... Congratulations now you can depend on this in
   other projects.
