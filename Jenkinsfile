pipeline {
  agent any
  stages {
    checkout([$class: 'GitSCM', branches: [[name: '*/master']], doGenerateSubmoduleConfigurations: false, extensions: [], submoduleCfg: [],
              userRemoteConfigs: [[credentialsId: 'GITHUB', url: 'https://github.com/Anish0210/cicd-pipeline-gradle']]])
    stage ('Build') {
      steps {
        echo 'Running Build Automation '
        sh './gradlew build --no-daemon'
        archiveArtifacts artifacts: 'dist/sampleapp.zip'
            }
          }
        }
      }
