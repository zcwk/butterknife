Butter Knife
============

![Logo](website/static/logo.png)

Field and method binding for Android views which uses annotation processing to generate boilerplate
code for you.

 * Eliminate `findViewById` calls by using `@FindView` on fields.
 * Group multiple views in a list using `@FindViews`. Operate on all of them at once with actions,
   setters, or properties.
 * Eliminate anonymous inner-classes for listeners by annotating methods with `@OnClick` and others.

```java
class ExampleActivity extends Activity {
  @FindView(R.id.user) EditText username;
  @FindView(R.id.pass) EditText password;

  @OnClick(R.id.submit) void submit() {
    // TODO call server...
  }

  @Override public void onCreate(Bundle savedInstanceState) {
    super.onCreate(savedInstanceState);
    setContentView(R.layout.simple_activity);
    ButterKnife.bind(this);
    // TODO Use fields...
  }
}
```

For documentation and additional information see [the website][3].

__Remember: A butter knife is like [a dagger][1] only infinitely less sharp.__



Download
--------

Download [the latest JAR][2] or grab via Maven:
```xml
<dependency>
  <groupId>com.jakewharton</groupId>
  <artifactId>butterknife</artifactId>
  <version>6.1.0</version>
</dependency>
```
or Gradle:
```groovy
compile 'com.jakewharton:butterknife:6.1.0'
```

Snapshots of the development version are available in [Sonatype's `snapshots` repository][snap].

报了空指针异常就是IDEA要配置一下Annotation Processing  -》勾选 Enable annotation processing 选择processor path 就是你的ButterKnife.jar 就好了

License
-------

    Copyright 2013 Jake Wharton

    Licensed under the Apache License, Version 2.0 (the "License");
    you may not use this file except in compliance with the License.
    You may obtain a copy of the License at

       http://www.apache.org/licenses/LICENSE-2.0

    Unless required by applicable law or agreed to in writing, software
    distributed under the License is distributed on an "AS IS" BASIS,
    WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
    See the License for the specific language governing permissions and
    limitations under the License.



 [1]: http://square.github.com/dagger/
 [2]: https://search.maven.org/remote_content?g=com.jakewharton&a=butterknife&v=LATEST
 [3]: http://jakewharton.github.com/butterknife/
 [snap]: https://oss.sonatype.org/content/repositories/snapshots/
