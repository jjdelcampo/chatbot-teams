pipeline {
  agent any

  tools {nodejs "node-13"}

  stages {

    stage('Cloning Git') {
      steps {
        git 'https://github.com/jjdelcampo/chatbot-teams.git'
      }
    }

    stage('Install dependencies') {
      steps {
        sh 'npm install'
      }
    }

    stage('Test') {
      steps {
         sh './node_modules/.bin/mocha ./test/test.js'
      }
    }
  }
}
