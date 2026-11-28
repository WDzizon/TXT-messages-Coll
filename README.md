cd ~/lod-server-support-lod-only &&
> git pull --ff-only origin feat/lod-only-preservation-1.21.1 &&
> git log -1 --oneline &&
> ./gradlew --console=plain :common:test :neoforge:test :neoforge:compileGametestJava :neoforge:runGameTestServer :neoforge:build
remote: Enumerating objects: 29, done.
remote: Counting objects: 100% (29/29), done.
remote: Compressing objects: 100% (11/11), done.
remote: Total 15 (delta 8), reused 0 (delta 0), pack-reused 0 (from 0)
Unpacking objects: 100% (15/15), 1.41 KiB | 111.00 KiB/s, done.
From https://github.com/WDzizon/lod-server-support-lod-only
 * branch                feat/lod-only-preservation-1.21.1 -> FETCH_HEAD
   50b15ad96..3f457a81e  feat/lod-only-preservation-1.21.1 -> origin/feat/lod-only-preservation-1.21.1
Updating 50b15ad96..3f457a81e
Fast-forward
 docs/planning/lod-only-preservation-plan.md                                                  | 15 +++++++++++++++
 neoforge/src/test/java/dev/vox/lss/neoforge/lodonly/LodOnlyStagedAnvilPayloadReaderTest.java |  2 +-
 2 files changed, 16 insertions(+), 1 deletion(-)
3f457a81e (HEAD -> feat/lod-only-preservation-1.21.1, origin/feat/lod-only-preservation-1.21.1) Fix GZIP stream import in staged payload tests

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
> Task :neoforge:generateJarJarMetadata UP-TO-DATE
> Task :neoforge:shadowJar UP-TO-DATE
> Task :neoforge:compileTestJava
> Task :neoforge:processTestResources NO-SOURCE
> Task :neoforge:testClasses

> Task :neoforge:test FAILED

LodOnlyStagedAnvilPayloadReaderTest > rejectsCompressedAndExpandedPayloadsOverTheirIndependentLimits() FAILED
    org.opentest4j.AssertionFailedError at LodOnlyStagedAnvilPayloadReaderTest.java:85
        Caused by: java.lang.NoClassDefFoundError at LodOnlyStagedAnvilPayloadReaderTest.java:86
            Caused by: java.lang.ClassNotFoundException at LodOnlyStagedAnvilPayloadReaderTest.java:86

LodOnlyStagedAnvilPayloadReaderTest > decodesAllBuiltInMinecraftCompressionFormatsWithoutChangingSourceOrStage() FAILED
    java.lang.NoClassDefFoundError at LodOnlyStagedAnvilPayloadReaderTest.java:40
        Caused by: java.lang.ClassNotFoundException at LodOnlyStagedAnvilPayloadReaderTest.java:40

LodOnlyStagedAnvilPayloadReaderTest > decodesExternalMccPayloadUsingTheRegionCompressionMarker() FAILED
    java.lang.NoClassDefFoundError at LodOnlyStagedAnvilPayloadReaderTest.java:65
        Caused by: java.lang.ClassNotFoundException at LodOnlyStagedAnvilPayloadReaderTest.java:65

87 tests completed, 3 failed

FAILURE: Build failed with an exception.

* What went wrong:
Execution failed for task ':neoforge:test'.
> There were failing tests. See the report at: file:///home/wdzizon/lod-server-support-lod-only/neoforge/build/reports/tests/test/index.html

* Try:
> Run with --scan to get full insights from a Build Scan (powered by Develocity).

BUILD FAILED in 4s
18 actionable tasks: 2 executed, 16 up-to-date
