node {
  stage ('Check'){
    script { 
      slackNotify.init(SlackChannel)
    }
    sh 'terraform -v'
  }
}