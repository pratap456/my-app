node{
   stage('SCM Checkout'){
     git 'https://github.com/javahometech/my-app'
   }
   stage('Compile-Package'){
      // Get maven home path
      def mvnHome =  tool name: 'maven-3', type: 'maven'   
      sh "${mvnHome}/bin/mvn package"
   }
   mail bcc: '', body: '''hi welcome to jenkins pipeline
this file
email text from pipeline''', cc: '', from: '', replyTo: '', subject: 'jenkins_jobs', to: 'prataptangirala1991@gmail.com'

   stage('Email Notification'){
      mail bcc: '', body: '''hi welcome to jenkins pipeline
this file
email text from pipeline''', cc: '', from: '', replyTo: '', subject: 'jenkins_jobs', to: 'prataptangirala1991@gmail.com'

      mail bcc: '', body: '''Hi Welcome to jenkins email alerts
      Thanks
      Hari''', cc: '', from: '', replyTo: '', subject: 'Jenkins Job', to: 'hari.kammana@gmail.com'
   }
   stage('Slack Notification'){
       slackSend baseUrl: 'https://hooks.slack.com/services/',
       channel: '#jenkins-pipeline-demo',
       color: 'good', 
       message: 'Welcome to Jenkins, Slack!', 
       teamDomain: 'javahomecloud',
       tokenCredentialId: 'slack-demo'
   }
}
