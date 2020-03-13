# EvoSuite-Jacoco-IDEA

### To set up test environment
1. Create a new Maven project
2. Create a peice of java code under `src/main/java`, e.g, `codeToTest.java`
3. Create a junit script under `src/test/java`, e.g, `codeToTestTest.java`
4. Modify your `pom.xml` like [pom.xml](https://github.com/Krystal97/EvoSuite-IDEA/blob/master/ideaj.example/pom.xml).
5. Dowload all dependencies

### To use `Jacoco` in IDEA
1. Click `Run` then click `Edit Configuration`
2. Find `Code Coverage`
3. Select `Jacoco`

### To run `EvoSuite` in Terminal
1. First get in the directory of your maven project
2. Run `mvn evosuite:generate`, you will find the generated tests under `.evosuite`
3. By running `mvn evosuite:generate evosuite:export`, the tests will be generated automatically under `src/test/java`

### To run `EvoSuite` in IDEA GUI
1. Go to Plugin Market and search EvoSuite
2. Install `EvoSuite Plugin` and restart IDEA IDE
3. Right click the junit script and select `Run EvoSuite`
4. Customize your configuration
  * Maven location: for ubuntu: `/usr/share/maven/bin/mvn` (apt install maven)
  * JAVA_HOME

After all these steps, you will get two java files
1. `*_ESTest`
2. `*_ESTest_scaffolding`
Just discard `*_ESTest_scaffolding`, it is useless.
And comment `@RunWith*` and `extends *_ESTest_scaffolding`.
Or copy the generated test scripts to your own file.

Environment requirement: Java 8

