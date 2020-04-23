#!/usr/bin/env groovy

pipeline {
  environment {
    CCACHE_DIR = '/opt/.ccache'
  }

  options {
    buildDiscarder(logRotator(numToKeepStr: '20'))
    timestamps()
  }

  agent any
  stages {
    stage ('All') {
      steps {
        script {
            sh "env"
          }
        }
      }
    }
  }


      
      
  
