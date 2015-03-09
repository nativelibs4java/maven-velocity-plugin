`maven-velocity-plugin` is a [Velocity template](https://velocity.apache.org/) plugin for Maven.

It interprets any template file in `src/main/velocity` (resp. `src/test/velocity`) and outputs the result to the appropriate locations: `*.java` files end up in `target/generated-sources/{main,test}` so that they can be compiled, while other files end up in `target/generated-resources/{main,test}`.

It is licensed under a BSD license.

# Usage

```
  <build>
    <plugins>
      <plugin>
        <groupId>com.nativelibs4java</groupId>
        <artifactId>maven-velocity-plugin</artifactId>
        <version>0.9</version>
        <configuration>
          <properties>
            <foo>bar</foo>
          </properties>
        </configuration>
      </plugin>
      ...
    </plugins>
  </build>
```

For a complete example of use of this plugin in production, have a look at BridJ's [source templates](https://github.com/ochafik/BridJ/tree/master/src/main/velocity/) and [test templates](https://github.com/ochafik/BridJ/tree/master/src/test/velocity/).

# Predefined properties

Every project property defined in the POM are reflected as Velocity variables, and the POM itself is accessible through the `pom` property.

There are also a couple of predefined BridJ-specific properties that are available (TODO: remove them?).

