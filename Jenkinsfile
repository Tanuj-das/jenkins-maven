pipeline {
    agent any
    stages {
        
       stage('Compile Stage') {
                         steps{
  							withMaven(maven : 'Apache Maven 3.3.9')
                          {
    						bat 'mvn clean compile'   
    					  }

                        
}
                      }
	stage('Testing Stage') {
                         steps{
  							withMaven(maven : 'Apache Maven 3.3.9')
                         {
    						bat 'mvn test'
                             

                         }
 
                        
}
                      }
             stage('Slack Notification')    
	    {
		    slackSend baseUrl: 'https://hooks.slack.com/services/', channel: '#frie', message: 'Hey welcome to slack', teamDomain: 'friends', tokenCredentialId: 'slack-demo'
	    }           
    }

    
}
