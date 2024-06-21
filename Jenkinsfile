pipeline {
    agent {

            label 'built-in'
        customWorkspace "/mnt/project"
    }

    stages {
        stage ('git')
        {
            steps{
                sh 'yum install git -y'
    
            }
        }
          
        stage ('Compile Stage') {

            steps {
                
                    sh 'mvn clean install'
                }
            
        }

        
        stage ('Echo Branch') {

            steps {
                
                    echo "This is master branch"
                }
            
        }
    }
}
