# Sharing the renv.lock file with others

To share your project with others, make sure they have a copy of your project's
source code and the `renv.lock` file. If you are working in a source code
repository, this means that you need to commit the `renv.lock` file to the
source code repository. The `renv` directory is not needed in the source code
repository.

When others checkout a local copy of the project's source code repository, they
can call the `renv::restore()` function to download, compile, and install the
correct versions of the packages needed by the source code.

This has the advantage of having the source code repository as the single
source of truth, telling which packages your project depends on and at what
versions. If the package information needs to be updated, you can follow good
software development practices of creating a branch, updating the `renv.lock`
file in the branch, testing to make sure it works, then merging the branch to
master, and asking everyone to update their computers from the master branch.

