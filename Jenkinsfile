pipeline {
  agent {
    node{ label 'workstation'}
  }
  environment {
    SAMPLE_URL ="https://cricbuzz.com"
  }
  stages {

    stage('one') {

      steps{
       sh 'echo one'
       # mail bcc: 'sainagarjuna184@gmail.com', body: 'hello', cc: 'sainagarjuna184@gmail.com', from: '', replyTo: '', subject: 'reports', to: 'sainagarjuna184@gmail.com'
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