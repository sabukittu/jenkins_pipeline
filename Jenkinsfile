pipeline {
   agent any

   stages {
      stage('Hello') {
         steps {
            script { 
                    slackNotify.init(SlackChannel)
                }
            echo 'Hello World'
         }
      }
   }
   
   post {
        always {
	    /* Use slackNotifier.groovy from shared library and provide current build result as parameter */   
            slackNotify(SlackChannel)
            cleanWs()
        }
    }
}



