# NUPANO Maven Repository

Define your `~/.m2/settings.xml` as follows. Set your GitHub username and token properly. Ensure that your token has access to packages.

```
<settings xmlns="http://maven.apache.org/SETTINGS/1.0.0"
  xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
  xsi:schemaLocation="http://maven.apache.org/SETTINGS/1.0.0
                      http://maven.apache.org/xsd/settings-1.0.0.xsd">

  <activeProfiles>
    <activeProfile>github</activeProfile>
  </activeProfiles>

  <profiles>
    <profile>
      <id>github</id>
      <repositories>
        <repository>
          <id>nupano</id>
          <name>GitHub NUPANO Maven Packages</name>
          <url>https://maven.pkg.github.com/nupano/maven-repository</url>
          <releases><enabled>true</enabled></releases>
          <snapshots><enabled>true</enabled></snapshots>
        </repository>  
        <repository>
          <id>central</id>
          <url>https://repo1.maven.org/maven2</url>
          <releases><enabled>true</enabled></releases>
          <snapshots><enabled>true</enabled></snapshots>
        </repository>  
      </repositories>
    </profile>
  </profiles>

  <servers>
    <server>
      <id>nupano</id>
      <username>GITHUB_USERNAME</username>
      <password>GITHUB_TOKEN</password>
    </server>
  </servers>
</settings>
```

