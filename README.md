# app-mod-workshop
IBM CSM Application Modernization on Red Hat OpenShift Workshop

**Pre-reqs:** Make sure you have completed the environment installation described [here](https://github.ibm.com/CSM-SPGI/workshopDevOps).

## Publishing

This repo is private to IBM. However, the tutorial it contains needs to be published externally to the public since it will be carried out by clients.
Therefore, there is a public github repository [here](https://github.com/IBM/CSM-SPGI-app-mod) where the mkdocs pages from this reporistory are published to.

As a result, changes to the source code (that is the instructions) must be done to this private repository but the mkdocs pages publishing is done into the public repository.
To do so, you need to:

1. Clone this private repo:

   ```
   git clone git@github.ibm.com:CSM-SPGI/app-mod-workshop.git   
   ```

1. Clone the public repo https://github.com/IBM/CSM-SPGI-app-mod

   ```
   git clone git@github.com:IBM/CSM-SPGI-app-mod.git
   ```

1. Change directory into the public repo:

   ```
   cd CSM-SPGI-app-mod
   ```

1. Build the private repo but publish it into the public repo

   ```
   mkdocs gh-deploy --config-file ../app-mod-workshop/mkdocs.yml  --remote-branch gh-pages
   ```

1. Check that your changes have been published into the `gh-pages` branch of the public repo: https://github.com/IBM/CSM-SPGI-app-mod/tree/gh-pages
1. Check that the tutorial with your latest changes are available at https://ibm.github.io/CSM-SPGI-app-mod/
