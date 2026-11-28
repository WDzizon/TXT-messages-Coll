cd ~/lod-server-support-lod-only &&
> git pull --ff-only origin feat/lod-only-preservation-1.21.1 &&
> git log -1 --oneline &&
> ./gradlew --console=plain :common:test :neoforge:test :neoforge:compileGametestJava :neoforge:runGameTestServer :neoforge:build
remote: Enumerating objects: 31, done.
remote: Counting objects: 100% (31/31), done.
remote: Compressing objects: 100% (12/12), done.
remote: Total 16 (delta 9), reused 0 (delta 0), pack-reused 0 (from 0)
Unpacking objects: 100% (16/16), 2.17 KiB | 61.00 KiB/s, done.
From https://github.com/WDzizon/lod-server-support-lod-only
 * branch                feat/lod-only-preservation-1.21.1 -> FETCH_HEAD
   ebe876efa..50b15ad96  feat/lod-only-preservation-1.21.1 -> origin/feat/lod-only-preservation-1.21.1
Updating ebe876efa..50b15ad96
Fast-forward
 docs/planning/lod-only-preservation-plan.md                                              | 24 ++++++++++++++++++++++++
 neoforge/build.gradle                                                                    |  2 ++
 .../src/test/java/dev/vox/lss/neoforge/lodonly/LodOnlyStagedAnvilPayloadReaderTest.java  | 18 ++++++++++++++----
 3 files changed, 40 insertions(+), 4 deletions(-)
50b15ad96 (HEAD -> feat/lod-only-preservation-1.21.1, origin/feat/lod-only-preservation-1.21.1) Fix staged payload decoder test fixture classpath

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
> Task :neoforge:compileJava UP-TO-DATE
> Task :neoforge:processResources UP-TO-DATE
> Task :neoforge:classes UP-TO-DATE
> Task :neoforge:jarJar NO-SOURCE
> Task :neoforge:jar SKIPPED
> Task :neoforge:generateJarJarMetadata
> Task :neoforge:shadowJar UP-TO-DATE

> Task :neoforge:compileTestJava FAILED
/home/wdzizon/lod-server-support-lod-only/neoforge/src/test/java/dev/vox/lss/neoforge/lodonly/LodOnlyStagedAnvilPayloadReaderTest.java:8: error: cannot find symbol
import java.io.GZIPOutputStream;
              ^
  symbol:   class GZIPOutputStream
  location: package java.io
/home/wdzizon/lod-server-support-lod-only/neoforge/src/test/java/dev/vox/lss/neoforge/lodonly/LodOnlyStagedAnvilPayloadReaderTest.java:161: error: cannot find symbol
            case 1 -> new GZIPOutputStream(bytes);
                          ^
  symbol:   class GZIPOutputStream
  location: class LodOnlyStagedAnvilPayloadReaderTest
2 errors

[Incubating] Problems report is available at: file:///home/wdzizon/lod-server-support-lod-only/build/reports/problems/problems-report.html

FAILURE: Build failed with an exception.

* What went wrong:
Execution failed for task ':neoforge:compileTestJava' (registered by plugin class 'org.gradle.api.plugins.JavaBasePlugin').
> Compilation failed; see the compiler output below.
  /home/wdzizon/lod-server-support-lod-only/neoforge/src/test/java/dev/vox/lss/neoforge/lodonly/LodOnlyStagedAnvilPayloadReaderTest.java:8: error: cannot find symbol
  import java.io.GZIPOutputStream;
                ^
    symbol:   class GZIPOutputStream
    location: package java.io
  /home/wdzizon/lod-server-support-lod-only/neoforge/src/test/java/dev/vox/lss/neoforge/lodonly/LodOnlyStagedAnvilPayloadReaderTest.java:161: error: cannot find symbol
              case 1 -> new GZIPOutputStream(bytes);
                            ^
    symbol:   class GZIPOutputStream
    location: class LodOnlyStagedAnvilPayloadReaderTest
  2 errors

* Try:
> Check your code and dependencies to fix the compilation error(s)
> Run with --scan to get full insights from a Build Scan (powered by Develocity).

BUILD FAILED in 9s
17 actionable tasks: 2 executed, 15 up-to-date
