pipeline {
  agent {
    node { label 'workstation' }
  }

  environment {
    SAMPLE_URL = "https://cricbuzz.com"
    SSH = credentials("ssh")
  }

  options {
    ansiColor('xterm')
  }

  parameters {
    string(name: 'PERSON', defaultValue: 'Mr Jenkins', description: 'Who should I say hello to?')

    text(name: 'BIOGRAPHY', defaultValue: '', description: 'Enter some information about the person')

    booleanParam(name: 'TOGGLE', defaultValue: true, description: 'Toggle this value')

    choice(name: 'CHOICE', choices: ['One', 'Two', 'Three'], description: 'Pick something')

    password(name: 'PASSWORD', defaultValue: 'SECRET', description: 'Enter a password')
  }

  //triggers { cron('00 08 01 * *') }.  cron exmample

  stages {

    stage('One') {

     input {
             message "Should we continue?"
             ok "Yes, we should."
             submitter "admin"
           }


      steps {
        sh 'echo One'
        sh ' echo $SAMPLE_URL'
        sh 'echo  $SSH'
        sh 'echo $PERSON'
      }
    }

    stage('Two') {
      steps {
        sh 'echo Two'
      }
    }

  }

  post {
    always {
      echo 'Sending Email'
    }
  }

}