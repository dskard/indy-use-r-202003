# New Project

With a new project, developers can initiate renv with `renv::init()`. This will
add the renv infrastructure to the project directory, including the `renv.lock`
lockfile.

When new packages are added to the project, renv attempts to install the
packages from its own package cache that is stored on the developer's computer.
This helps make installation fast for packages that are commonly used and saves
on disk space.

If new R packages are added to the project, they won't necessarily be
added to the lockfile. renv first tries to determine whether the package is
being used by the source code. If renv determines that the source code uses the
package, it will be included in the lockfile when the next time a snapshot is
taken with the `renv::snapshot()` function.

As the developer writes their source code and builds their project, they can
occasionally take snapshots of the packages in use with the `renv::snapshot()`
function. At this time, new packages will be added to the lockfile and packages
no longer in use will be removed.
