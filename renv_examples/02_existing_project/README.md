# Adding renv to an existing project

In this example, we have a project that has already been started. There are only two files in the directory, our `.Rproj` file and `spirograph_shiny.R` which holds the Shiny application we have been working on. To add renv to this project, we'll start by calling `renv::init()` to perform the initialization.

```
> renv::init()
* Initializing project ...
* Discovering package dependencies ... Done!
* Copying packages into the cache ... Done!
The following package(s) will be updated in the lockfile:

# CRAN ===============================
- BH             [* -> 1.72.0-3]
- MASS           [* -> 7.3-51.4]
- Matrix         [* -> 1.2-18]
...

* Lockfile written to '…/02_existing_project/renv.lock'.

Restarting R session...

* Project '…/02_existing_project' loaded. [renv 0.9.3]
```

renv will find all of the source files and scan them, looking for packages to
include in the `renv.lock` file. Notice that we didn't need to take a snapshot
to update the lockfile. At this point, we are ready to save and share our
`renv.lock` file.
