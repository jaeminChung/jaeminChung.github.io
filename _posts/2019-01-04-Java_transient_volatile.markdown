---
layout: post
title:  "Java의 transient와 volatile"
date:   2019-01-04 22:35:13
categories: programming
permalink: /archivers/java_transient_volatile
---
1. 컴퓨터 프로그래밍에서 transient는 "임시" 속성이라는 의미로 사용됨. Java에서는 필드의 접근자로 사용되는 키워드로, transient로 선언된 필드는 직렬화 대상에서 제외됨
```java
class User implements Serializable {
  private String userId;
  private transient String password;
}
```
2. volatile로 선언된 변수는 java에서 global ordering을 갖게 되어, 모든 쓰레드가 캐시가 아닌, 메모리에서 해당 값을 읽고 쓰게 됨. 