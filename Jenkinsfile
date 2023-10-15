pipeline {
  agent {
    node { label 'workstation' }
  }
  environment {
    SAMPLE_URL ="https://cricbuzz.com"
  }
  stages {

    stage('one') {

      steps{
       sh 'echo one'

       }
    }

       stage('two') {
        steps{
        sh 'echo two'
        sh 'echo ${SAMPLE_URL}'
       }

    }
   }

   post {
    always {
    echo  'sending email'

}
}
}