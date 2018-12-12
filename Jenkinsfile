pipeline {
  agent any
  stages {
      
    stage ('Build') {
      step('Clone sources') {
        git url: 'https://github.com/jfrogdev/project-examples.git'
    }
      steps {
        echo 'Running Build Automation '
        sh './gradlew build --no-daemon'
        archiveArtifacts artifacts: 'dist/sampleapp.zip'
            }
          }
        }
      }
