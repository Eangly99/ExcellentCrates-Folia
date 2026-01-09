I will initialize Folia support using `FoliaLib` as requested.

**1. Update `pom.xml`**
- Add the `FoliaLib` repository: `https://repo.tcoded.com/releases`
- Add the `FoliaLib` dependency (version `0.5.1`).
- Configure `maven-shade-plugin` to relocate `com.tcoded.folialib` to `su.nightexpress.excellentcrates.lib.folialib` to prevent conflicts.

**2. Update `CratesPlugin.java`**
- Add the `FoliaLib` field and initialize it in the plugin startup logic.
- Add a getter method `getFoliaLib()` to expose the library instance for use in other parts of the plugin.

This setup will provide the foundation for Folia support, allowing you to replace Bukkit schedulers with `foliaLib.getScheduler()` calls in the future.