# Remote isolation probe

Christian's manual, harmless GitHub-hosted runner probe. It checks operating system, user, home directory listing, Rust tooling, public HTTPS access, mount metadata and environment variable names.

The workflow uses a standard Ubuntu runner and `permissions: {}`. It does not check out a repository, run third-party actions, reference repository secrets, upload artifacts or execute target-project code. Runs are manual only.

The absence of the macOS `/Users` tree, absence of inherited assistant configuration directories, runner identity and mount information are separate witnesses. A successful run proves only the observations in its logs. GitHub still creates a native job token; an empty permissions mapping does not prove that the service creates no credentials.

Public repository with standard GitHub-hosted runner: [official billing documentation](https://docs.github.com/en/actions/concepts/billing-and-usage). No paid runner or private-repository minutes are requested.
