---
layout: page
title: experiments.json
navigation_source: docs_nav
---

This is the template that [rush init]({% link pages/commands/rush_init.md %})
generates for **common/config/rush/experiments.json**:

```js
/**
 * This configuration file allows repo maintainers to enable and disable experimental
 * Rush features.  More documentation is available on the Rush website: https://rushjs.io
 */
{
  "$schema": "https://developer.microsoft.com/json-schemas/rush/v5/experiments.schema.json",

  /**
   * Rush 5.14.0 improved incremental builds to ignore spurious changes in the pnpm-lock.json file.
   * This optimization is enabled by default. If you encounter a problem where "rush build" is neglecting
   * to build some projects, please open a GitHub issue. As a workaround you can uncomment this line
   * to temporarily restore the old behavior where everything must be rebuilt whenever pnpm-lock.json
   * is modified.
   */
  // "legacyIncrementalBuildDependencyDetection": true,

  /**
   * By default, rush passes --no-prefer-frozen-lockfile to 'pnpm install'.
   * Set this option to true to pass '--frozen-lockfile' instead.
   */
  // "usePnpmFrozenLockfileForRushInstall": true,

  /**
   * If true, the chmod field in temporary project tar headers will not be normalized.
   * This normalization can help ensure consistent tarball integrity across platforms.
   */
  // "noChmodFieldInTarHeaderNormalization": true,

  /**
   * If true, the build cache feature is enabled. To use this feature, a common/config/rush/build-cache.json
   * file must be created with configuration options.
   *
   * See https://github.com/microsoft/rushstack/issues/2393 for details about this experimental feature.
   */
  // "buildCache": true
}
```
