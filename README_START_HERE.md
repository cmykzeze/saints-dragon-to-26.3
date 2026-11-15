# Saint's Dragons -> Minecraft 26.3 (Fabric only)

This is the work-in-progress port. Round 1 only sets up the build. The code itself is
NOT ported yet, so the first build is EXPECTED to fail with lots of errors. That's the plan:
those errors are the to-do list.

## How to test it on GitHub (no coding needed)

1. Install **GitHub Desktop** (desktop.github.com) and sign in. (Ask a grown-up to help.)
2. Unzip this folder somewhere easy, like your Documents.
3. In GitHub Desktop: **File > Add local repository...**, pick this folder.
   If it says "this isn't a git repository", click **create a repository**.
4. Click **Commit to main**, then **Publish repository**. (Private is fine.)
5. On github.com open your repository, click the **Actions** tab, click the newest run.
   It takes about 5 minutes.
6. When it finishes (red X is expected for now) open the run and scroll down:
   - The **Summary** shows the first errors.
   - Under **Artifacts** download **build-logs**. It holds `build-log.txt` and `errors.txt`.
7. Send me `errors.txt` (or paste what it says). I fix the code and send you a new zip.
   Repeat from step 2. (Copy my new files over the old ones, then commit + publish again.)

When the build turns green, the Artifacts will also include the finished `.jar`.
Put it in your Minecraft 26.3 Fabric `mods` folder together with Fabric API and GeckoLib.

## What was changed in round 1

- Forge removed. `common` and `fabric` merged into one normal Fabric project.
- Architectury removed (not needed for Fabric only).
- Build moved to Minecraft 26.3 tools: Java 25, Gradle 9.6, Fabric Loom 1.17.
- Mojang's code names are used directly now (26.x isn't scrambled anymore).
- Parked in `_parked/` for later (not deleted): JEI, EMI, Jade and ModMenu add-ons.
- Cloth Config (the config screen library) and reach-entity-attributes are switched off.
  The config code and the Dragonheart weapon reach code will show errors. I'll rewrite those.
