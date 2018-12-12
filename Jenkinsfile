pipeline {
  agent any
  stages {
      stage('Clone sources') {
        git url: 'https://github.com/jfrogdev/project-examples.git'
    }
    stage ('Build') {
      steps {
        echo 'Running Build Automation '
        sh './gradlew build --no-daemon'
        archiveArtifacts artifacts: 'dist/sampleapp.zip'
            }
          }
        }
      }
