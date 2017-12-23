# promote-nexus-artifact

Promote single artifact in Sonatype Nexus artifact management system from one repository to another repository using Gradle.

Forked from upstream [package-release](https://github.com/praqma/packagerelease) project, which supports multiple artifacts promotion.

## Prerequisites

* Sonatype Nexus 3 environment.

* Apache Maven environment.

* Update `~/.gradle/gradle.properties` file has similar content as shown below. As an alternative, update the current [gradle.properies](gradle.properties) file and use it directly. Note that this file cannot use the encrypted password generated from Apache Maven environment.

```
repositoryManagerUsername=username
repositoryManagerPassword=password
repositoryManagerUrl=http://localhost:8081/nexus3/repository
```

* Get artifact promotion project.

```
git clone git@github.com:praqma/promote-nexus-artifact.git
```

* Optional: Get example project.

```
git clone git@github.com:praqma/promote-nexus-artifact-gilded-rose.git
```

## Usage

*  Promote artifact.

    *nix:    `./gradlew ...`

    Windows: `gradlew ...`

```
    ./gradlew publish -P targetEnvironment=beta -P pomFile=pom.xml
```
