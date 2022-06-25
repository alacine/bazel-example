## 自定义 JDK 版本

主机版本
```bash
java -version
```

output
```
openjdk version "18.0.1.1" 2022-04-22
OpenJDK Runtime Environment (build 18.0.1.1+2)
OpenJDK 64-Bit Server VM (build 18.0.1.1+2, mixed mode)
```

编译时使用的版本
```bash
bazel build --config=java11 //src/main/java:main
javap -verbose bazel-bin/src/main/java/_javac/main/main_classes/Main.class | grep major
```

output
```
major version: 55
```

[版本对应表参考](https://en.wikipedia.org/wiki/Java_class_file#General_layout)
> Java SE 11 = 55 (0x37 hex)

运行时使用的版本
```bash
bazel run --config=java11 //src/main/java:main
```

output
```
INFO: ...
...
Hello World
11.0.2
```

同理可以尝试一下其他的版本
```bash
bazel run --config=java15 //src/main/java:main
bazel run --config=java17 //src/main/java:main
bazel run --config=java18 //src/main/java:main
```
