# Jobs

A job is a set of steps in a workflow that is executed on the same runner.

Each step is either a shell script that will be executed, or an action that will be run.

Steps are executed in order and are dependent on each other.

Since each step is executed on the same runner, you can share data from one step to another.

For example, you can have a step that builds your application followed by a step that tests the application that was built.

You can configure a job's dependencies with other jobs; by default, jobs have no dependencies and run in parallel with each other.

When a job takes a dependency on another job, it will wait for the dependent job to complete before it can run.

For example, you may have multiple build jobs for different architectures that have no dependencies, and a packaging job that is dependent on those jobs.

The build jobs will run in parallel, and when they have all completed successfully, the packaging job will run.
