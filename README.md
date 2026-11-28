cd ~/lod-server-support-lod-only &&
> git pull --ff-only origin feat/lod-only-preservation-1.21.1 &&
> git log -1 --oneline &&
> ./gradlew --console=plain :common:test :neoforge:test :neoforge:compileGametestJava :neoforge:runGameTestServer :neoforge:build
remote: Enumerating objects: 40, done.
remote: Counting objects: 100% (40/40), done.
remote: Compressing objects: 100% (17/17), done.
remote: Total 23 (delta 7), reused 0 (delta 0), pack-reused 0 (from 0)
Unpacking objects: 100% (23/23), 10.14 KiB | 741.00 KiB/s, done.
From https://github.com/WDzizon/lod-server-support-lod-only
 * branch                feat/lod-only-preservation-1.21.1 -> FETCH_HEAD
   477685e97..ebe876efa  feat/lod-only-preservation-1.21.1 -> origin/feat/lod-only-preservation-1.21.1
Updating 477685e97..ebe876efa
Fast-forward
 docs/planning/lod-only-preservation-plan.md                                 | 102 +++++++++++++
 .../java/dev/vox/lss/neoforge/lodonly/LodOnlyStagedAnvilPayloadReader.java  | 294 ++++++++++++++++++++++++++++++++++++
 .../dev/vox/lss/neoforge/lodonly/LodOnlyStagedAnvilPayloadReaderTest.java   | 192 +++++++++++++++++++++++
 3 files changed, 588 insertions(+)
 create mode 100644 neoforge/src/main/java/dev/vox/lss/neoforge/lodonly/LodOnlyStagedAnvilPayloadReader.java
 create mode 100644 neoforge/src/test/java/dev/vox/lss/neoforge/lodonly/LodOnlyStagedAnvilPayloadReaderTest.java
ebe876efa (HEAD -> feat/lod-only-preservation-1.21.1, origin/feat/lod-only-preservation-1.21.1) Add bounded read-only staged Anvil payload decoder
Starting a Gradle Daemon, 1 incompatible and 1 stopped Daemons could not be reused, use --status for details

> Configure project :fabric
Fabric Loom: 1.17.13

> Configure project :sponge
SpongePowered Plugin 'GRADLE' Toolset Version '2.3.0'
SpongePowered Vanilla 'GRADLE' Toolset Version '0.2.2'
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
> Task :neoforge:createMinecraftArtifacts UP-TO-DATE
> Task :common:test UP-TO-DATE
> Task :neoforge:compileJava
> Task :neoforge:processResources UP-TO-DATE
> Task :neoforge:classes
> Task :neoforge:jarJar NO-SOURCE
> Task :neoforge:jar SKIPPED
> Task :neoforge:generateJarJarMetadata UP-TO-DATE
> Task :neoforge:shadowJar

> Task :neoforge:compileTestJava FAILED
/home/wdzizon/lod-server-support-lod-only/neoforge/src/test/java/dev/vox/lss/neoforge/lodonly/LodOnlyStagedAnvilPayloadReaderTest.java:4: error: package net.minecraft.world.level.chunk.storage does not exist
import net.minecraft.world.level.chunk.storage.RegionFileVersion;
                                              ^
/home/wdzizon/lod-server-support-lod-only/neoforge/src/test/java/dev/vox/lss/neoforge/lodonly/LodOnlyStagedAnvilPayloadReaderTest.java:154: error: cannot find symbol
        RegionFileVersion version = RegionFileVersion.fromId(compressionId);
        ^
  symbol:   class RegionFileVersion
  location: class LodOnlyStagedAnvilPayloadReaderTest
/home/wdzizon/lod-server-support-lod-only/neoforge/src/test/java/dev/vox/lss/neoforge/lodonly/LodOnlyStagedAnvilPayloadReaderTest.java:154: error: cannot find symbol
        RegionFileVersion version = RegionFileVersion.fromId(compressionId);
                                    ^
  symbol:   variable RegionFileVersion
  location: class LodOnlyStagedAnvilPayloadReaderTest
3 errors

[Incubating] Problems report is available at: file:///home/wdzizon/lod-server-support-lod-only/build/reports/problems/problems-report.html

FAILURE: Build failed with an exception.

* What went wrong:
Execution failed for task ':neoforge:compileTestJava' (registered by plugin class 'org.gradle.api.plugins.JavaBasePlugin').
> Compilation failed; see the compiler output below.
  /home/wdzizon/lod-server-support-lod-only/neoforge/src/test/java/dev/vox/lss/neoforge/lodonly/LodOnlyStagedAnvilPayloadReaderTest.java:154: error: cannot find symbol
          RegionFileVersion version = RegionFileVersion.fromId(compressionId);
          ^
    symbol:   class RegionFileVersion
    location: class LodOnlyStagedAnvilPayloadReaderTest
  /home/wdzizon/lod-server-support-lod-only/neoforge/src/test/java/dev/vox/lss/neoforge/lodonly/LodOnlyStagedAnvilPayloadReaderTest.java:154: error: cannot find symbol
          RegionFileVersion version = RegionFileVersion.fromId(compressionId);
                                      ^
    symbol:   variable RegionFileVersion
    location: class LodOnlyStagedAnvilPayloadReaderTest
  /home/wdzizon/lod-server-support-lod-only/neoforge/src/test/java/dev/vox/lss/neoforge/lodonly/LodOnlyStagedAnvilPayloadReaderTest.java:4: error: package net.minecraft.world.level.chunk.storage does not exist
  import net.minecraft.world.level.chunk.storage.RegionFileVersion;
                                                ^
  3 errors

* Try:
> Check your code and dependencies to fix the compilation error(s)
> Run with --scan to get full insights from a Build Scan (powered by Develocity).

BUILD FAILED in 18s
17 actionable tasks: 3 executed, 14 up-to-date
