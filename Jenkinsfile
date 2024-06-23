pipeline {
    agent {
        label {
            label 'Slave-1'
            customWorkspace "/mnt/test"
    }
    }
    stages {
        stage ('Maven') {
            steps {
                //sh 'sudo chmod -R 777 /root/server'
                dir ("/mnt/test/") {   
                sh 'sudo yum install maven -y'
                sh 'sudo rm -rf /root/.m2/' 
                }
            }
        }
        stage ('Compile Stage') {

            steps { 
                    sh 'sudo mvn clean package'
            }
        }
        stage ('Echo Branch') {
            steps {
                    echo "This is qa branch"
                }
        }
        stage ("Tomcat") {
            steps {
                dir ("/mnt/server") {
                sh 'sudo wget https://dlcdn.apache.org/tomcat/tomcat-9/v9.0.90/bin/apache-tomcat-9.0.90.zip'
                sh 'sudo unzip apache-tomcat-9.0.90.zip'
                sh 'sudo rm -rf apache-tomcat-9.0.90.zip'
                sh 'sudo chmod -R 777 *'    
        
    }
}
            
        }
    }
}
