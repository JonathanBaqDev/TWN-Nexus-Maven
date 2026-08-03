# Nexus Repository Manager Installation and Maven Setup

Checkout [TWN-Nexus-Gradle](https://github.com/JonathanBaqDev/TWN-Nexus-Gradle) for steps on how to install Java and Nexus on a server and how to create a Nexus user with permissions to upload artifacts.

## Publish an Artifact

- Configure the project for deployment (see [commit](https://github.com/JonathanBaqDev/TWN-Nexus-Maven/commit/1eef026b129a34f79edf3158e1d42de4822734a5))
- Create a `settings.xml` file in your local profile's `.m2` directory
- Add your Nexus repository credentials:

```xml
<settings>
  <servers>
    <server>
      <id>nexus-snapshots</id>
      <username>NEXUS_USERNAME</username>
      <password>NEXUS_PASSWORD</password>
    </server>
  </servers>
</settings>
```

## Build and Publish
- Build the project using `mvn package`
- Publish the artifact using `mvn deploy`
