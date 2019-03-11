# WK-test
Container trials:

This is a test of the CircleCI workspace feature, which allows a workflow composed of engines in different containers to 
communicate data through a workspace.

One workspace is allowed per workflow, and in this example, we create a 'loader' container that copies data into the workspace
in order to start the first engine.

One way this could work is to create canonical input and output directories (or flags to specify) for engines in containers.
Then this system of using a workflow would allow us to create a workflow by chaining these engines together.

THe workspace is implemented using an artifact, so it is not nearly as fast as a local filesystem (or possibly a volume).
