parameters:
  releases 
pools()
projects: ''
targetPaths''
articraftsNames: ''

jobs
   -job1-build
pools $({parameters.pool})
steps
-tasks DotnNetCoreCLI@2
  inputs:
command:'publish'
projects:$({parameters.projects})
arguments:"--configurtion $((parameters.release})"
-task: PublishPipelineArtifact@1

inputs:
targetPath:$({parameters.targetpath})
ArtifactName:$({parameters.artifactname})

