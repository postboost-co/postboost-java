# PostBoost Java SDK

Official Java client for the [PostBoost API](https://postboost.co/docs/api).

## Install

**Maven:**

```xml
<repositories>
  <repository>
    <id>github</id>
    <url>https://maven.pkg.github.com/postboost-co/postboost-java</url>
  </repository>
</repositories>

<dependency>
  <groupId>com.postboost</groupId>
  <artifactId>postboost-java-sdk</artifactId>
  <version>1.1.0</version>
</dependency>
```

**Gradle:**

```groovy
repositories {
    maven { url 'https://maven.pkg.github.com/postboost-co/postboost-java' }
}
dependencies {
    implementation 'com.postboost:postboost-java-sdk:1.1.0'
}
```

| | |
|---|---|
| **GitHub Packages** | [github.com/postboost-co/postboost-java/packages](https://github.com/postboost-co/postboost-java/packages) |
| **GitHub** | [postboost-co/postboost-java](https://github.com/postboost-co/postboost-java) |
| **Docs** | [postboost.co/docs/api](https://postboost.co/docs/api) |
| **Version** | v1.1.0 |

## Quick start

```java
ApiClient client = new ApiClient();
client.setBearerToken(apiToken);

PostsApi api = new PostsApi(client);
List<Post> posts = api.listPosts("YOUR_WORKSPACE_UUID");
posts.forEach(p -> System.out.println(p.getUuid()));
```

## License

MIT
