## OpenShift

### 安装完应用后的文字

What about ~/data folder?

> https://www.openshift.com/page/openshift-environment-variables

A persistent directory for your data

What about app-deployments folder?

> https://www.openshift.com/forums/openshift/deployments

app-deployments contains 1 or more complete deployments for your application. A complete deployment is the combination of build-dependencies (currently really only applies to Java-based applications and is the .m2 directory for Maven), dependencies (runtime dependencies such as node_modules, pear libraries for php, your .war files for Java, etc.), and the repo (a copy of the contents of your application's git repo).

If you configure your application to keep more than 1 deployment around, you now get the ability to roll back to a previous deployment. That's why we now have the app-deployments directory as well as why we keep a complete copy of the build-dependencies, dependencies, and repo for each deployment.

When you deploy something from git (either via "git push" or "rhc deploy"):

your code is copied from the bare git repo in your gear into app-root/runtime/repo using the "git archive" command we run the cartridge's build method and application's relevant hooks (if they exists) we run the application's prepare hook (if it exists) we calculate the checksum of the deployment's contents (in case we want to verify later) we distribute the deployment to child gears (if they exist) we activate the deployment on all gears (run deploy method/hook, start cartridges, etc) If you want to deploy a binary artifact, you'll need to switch your application's deployment type from git to binary (rhc app configure -a myapp --deployment-type=binary). You can create a binary artifact by running the following command against a live application: rhc snapshot save -a myapp --deployment. Or, alternatively, you can create a binary artifact by creating a tar.gz file containing build-dependencies, dependencies, and repo. You can deploy a binary artifact by doing "rhc deploy -a myapp /path/to/artifact.tar.gz"

Finally, to answer your question about Jenkins, we have made it so existing jobs should continue to function, but with some limitations. New jobs:

reset the deployment metadata.json for each build, giving you clean information about each build create a new deployment directory under app-deployments on the upstream (actual) gear sync the metadata.json about the jenkins build upstream (otherwise the information about git ref, git sha1, etc. never changes to reflect what was built on jenkins) And re cartridge authors having control over the process, what were you thinking?
