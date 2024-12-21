pipeline {
    agent any

    stages {
       
        stage('deploy yaml') {
            steps {
               sh 'kubectl apply -f nginx.yaml'
            }
        }
        
        
          }


    post{
        always{
            emailext body: '''Hi,

     The jenkins has been failed . please check it.

     Thanks
     Devops Team''', subject: 'testing jenkins pipeline: $JOB_URL', to: 'malleshdevops2021@outlook.com'
    }
    }

}
