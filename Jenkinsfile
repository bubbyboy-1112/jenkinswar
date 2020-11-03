pipeline
{
    agent {label 'label1'} 
    
    stages
    {
     
     stage ('compile code')
     {
         steps
         {
             sh 'mvn clean install'
         }
     }
     stage ('test')
     {
         steps
         {
             sh 'mvn test'
         }
     }
     
     stage ('deploy')
     {
         steps
         {
             sh 'cp -R /opt/jenkins/workspace/node_maven_slave/target/* /opt/apache-tomcat-8.5.3/webapps'
         }
     }
        
    }
}
