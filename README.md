cd ~/lod-server-support-lod-only &&
> git pull --ff-only origin feat/lod-only-preservation-1.21.1 &&
> git log -1 --oneline &&
> ./gradlew --console=plain :common:test :neoforge:test :neoforge:compileGametestJava :neoforge:runGameTestServer :neoforge:build
remote: Enumerating objects: 67, done.
remote: Counting objects: 100% (67/67), done.
remote: Compressing objects: 100% (34/34), done.
remote: Total 48 (delta 18), reused 0 (delta 0), pack-reused 0 (from 0)
Unpacking objects: 100% (48/48), 9.37 KiB | 309.00 KiB/s, done.
From https://github.com/WDzizon/lod-server-support-lod-only
 * branch                feat/lod-only-preservation-1.21.1 -> FETCH_HEAD
   d2d45acb6..08f22e28f  feat/lod-only-preservation-1.21.1 -> origin/feat/lod-only-preservation-1.21.1
Updating d2d45acb6..08f22e28f
Fast-forward
 docs/planning/lod-only-preservation-plan.md                                                |  67 +++++++++++-
 .../src/gametest/java/dev/vox/lss/neoforge/gametest/LodOnlyStagedAnvilPayloadGameTest.java | 153 ++++++++++++++++++++++++++++
 .../src/main/java/dev/vox/lss/neoforge/lodonly/LodOnlyStagedAnvilMetadataInspector.java    | 241 ++++++++++++++++++++++++++++++++++++++++++++
 3 files changed, 459 insertions(+), 2 deletions(-)
 create mode 100644 neoforge/src/main/java/dev/vox/lss/neoforge/lodonly/LodOnlyStagedAnvilMetadataInspector.java
08f22e28f (HEAD -> feat/lod-only-preservation-1.21.1, origin/feat/lod-only-preservation-1.21.1) Keep local metadata observations separate from deletion decisions

> Configure project :fabric
Fabric Loom: 1.17.13

> Configure project :sponge
SpongePowered Plugin 'GRADLE' Toolset Version '2.3.0'
Targeting Minecraft '1.21.1' on a 'SERVER' platform

> Task :common:compileJava UP-TO-DATE
> Task :common:compileSqliteBridgeJava UP-TO-DATE
> Task :common:generateSqliteRuntime UP-TO-DATE
> Task :common:processResources UP-TO-DATE
> Task :common:classes UP-TO-DATE
> Task :common:shadowJar UP-TO-DATE
> Task :common:compileTestFixturesJava UP-TO-DATE
> Task :common:processTestFixturesResources UP-TO-DATE
> Task :common:testFixturesClasses UP-TO-DATE
> Task :common:testFixturesJar UP-TO-DATE
> Task :common:compileTestJava UP-TO-DATE
> Task :common:processTestResources UP-TO-DATE
> Task :common:testClasses UP-TO-DATE
> Task :common:test UP-TO-DATE
> Task :neoforge:createMinecraftArtifacts UP-TO-DATE
> Task :neoforge:compileJava
> Task :neoforge:processResources UP-TO-DATE
> Task :neoforge:classes
> Task :neoforge:jarJar NO-SOURCE
> Task :neoforge:jar SKIPPED
> Task :neoforge:generateJarJarMetadata UP-TO-DATE
> Task :neoforge:shadowJar
> Task :neoforge:compileTestJava UP-TO-DATE
> Task :neoforge:processTestResources NO-SOURCE
> Task :neoforge:testClasses UP-TO-DATE
> Task :neoforge:test

> Task :neoforge:compileGametestJava FAILED
/home/wdzizon/lod-server-support-lod-only/neoforge/src/gametest/java/dev/vox/lss/neoforge/gametest/LodOnlyStagedAnvilPayloadGameTest.java:399: error: cannot find symbol
        check(result.mustPreserve(), message + ": unknown metadata must require preservation");
                    ^
  symbol:   method mustPreserve()
  location: variable result of type Inspection
/home/wdzizon/lod-server-support-lod-only/neoforge/src/gametest/java/dev/vox/lss/neoforge/gametest/LSSNeoGameTests.java:292: warning: [removal] makeMockServerPlayerInLevel() in GameTestHelper has been deprecated and marked for removal
            var firstPlayer = helper.makeMockServerPlayerInLevel();
                                    ^
/home/wdzizon/lod-server-support-lod-only/neoforge/src/gametest/java/dev/vox/lss/neoforge/gametest/LSSNeoGameTests.java:313: warning: [removal] makeMockServerPlayerInLevel() in GameTestHelper has been deprecated and marked for removal
            var secondPlayer = helper.makeMockServerPlayerInLevel();
                                     ^
/home/wdzizon/lod-server-support-lod-only/neoforge/src/gametest/java/dev/vox/lss/neoforge/gametest/LSSNeoGameTests.java:430: warning: [removal] makeMockServerPlayerInLevel() in GameTestHelper has been deprecated and marked for removal
        var player = helper.makeMockServerPlayerInLevel();
                           ^
/home/wdzizon/lod-server-support-lod-only/neoforge/src/gametest/java/dev/vox/lss/neoforge/gametest/LSSNeoGameTests.java:446: warning: [removal] makeMockServerPlayerInLevel() in GameTestHelper has been deprecated and marked for removal
        var player = helper.makeMockServerPlayerInLevel();
                           ^
/home/wdzizon/lod-server-support-lod-only/neoforge/src/gametest/java/dev/vox/lss/neoforge/gametest/LSSNeoGameTests.java:463: warning: [removal] makeMockServerPlayerInLevel() in GameTestHelper has been deprecated and marked for removal
        var player = helper.makeMockServerPlayerInLevel();
                           ^
1 error
5 warnings

[Incubating] Problems report is available at: file:///home/wdzizon/lod-server-support-lod-only/build/reports/problems/problems-report.html

FAILURE: Build failed with an exception.

* What went wrong:
Execution failed for task ':neoforge:compileGametestJava' (registered by plugin class 'org.gradle.api.plugins.JavaBasePlugin').
> Compilation failed; see the compiler output below.
  /home/wdzizon/lod-server-support-lod-only/neoforge/src/gametest/java/dev/vox/lss/neoforge/gametest/LSSNeoGameTests.java:292: warning: [removal] makeMockServerPlayerInLevel() in GameTestHelper has been deprecated and marked for removal
              var firstPlayer = helper.makeMockServerPlayerInLevel();
                                      ^
  /home/wdzizon/lod-server-support-lod-only/neoforge/src/gametest/java/dev/vox/lss/neoforge/gametest/LSSNeoGameTests.java:313: warning: [removal] makeMockServerPlayerInLevel() in GameTestHelper has been deprecated and marked for removal
              var secondPlayer = helper.makeMockServerPlayerInLevel();
                                       ^
  /home/wdzizon/lod-server-support-lod-only/neoforge/src/gametest/java/dev/vox/lss/neoforge/gametest/LSSNeoGameTests.java:430: warning: [removal] makeMockServerPlayerInLevel() in GameTestHelper has been deprecated and marked for removal
          var player = helper.makeMockServerPlayerInLevel();
                             ^
  /home/wdzizon/lod-server-support-lod-only/neoforge/src/gametest/java/dev/vox/lss/neoforge/gametest/LSSNeoGameTests.java:446: warning: [removal] makeMockServerPlayerInLevel() in GameTestHelper has been deprecated and marked for removal
          var player = helper.makeMockServerPlayerInLevel();
                             ^
  /home/wdzizon/lod-server-support-lod-only/neoforge/src/gametest/java/dev/vox/lss/neoforge/gametest/LSSNeoGameTests.java:463: warning: [removal] makeMockServerPlayerInLevel() in GameTestHelper has been deprecated and marked for removal
          var player = helper.makeMockServerPlayerInLevel();
                             ^
  /home/wdzizon/lod-server-support-lod-only/neoforge/src/gametest/java/dev/vox/lss/neoforge/gametest/LodOnlyStagedAnvilPayloadGameTest.java:399: error: cannot find symbol
          check(result.mustPreserve(), message + ": unknown metadata must require preservation");
                      ^
    symbol:   method mustPreserve()
    location: variable result of type Inspection
  1 error
  5 warnings

* Try:
> Check your code and dependencies to fix the compilation error(s)
> Run with --scan to get full insights from a Build Scan (powered by Develocity).

BUILD FAILED in 25s
19 actionable tasks: 4 executed, 15 up-to-date
