# Database for hydra compatible cores
Please add cores to the `cores/` folder in .json format, as described below.

Define these fields as necessary:

`CoreName`: Set this to the name of the core.

`CoreSubName`: The sub-name of the core. If there's multiple versions of this CoreName, it will be a description of the core specialization such as "Accuracy" or "Efficiency" etc. Can be empty.

`SystemNames`: Comma separated list of the systems this core supports.    

`Versioning`: Used to check for updates. Set this to `Github`. In the future there may be added different ways to check if a core needs an update.    

`VersioningURL`: If using `Github` as `Versioning`, set this to `https://api.github.com/repos/<author>/<repo>/branches/master` (by replacing `<author>` and `<repo>` accordingly).    

`Downloads`: A map of systems to their core download links in the form of `"<System> <Architecture>:"<URL>"`. Cores must be saved either in `.zip` or their native shared library format (`.dll/.dylib/.so`).    

Available systems: `Windows` `MacOS` `Linux` `Android` `iOS`    
Available architectures: `x64`, `x86`, `arm64`, `arm32`

---

See `Panda3DS-nightly.json` for an example of a core.
