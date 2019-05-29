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
                     
    }

    
}
