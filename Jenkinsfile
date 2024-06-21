pipeline {
    agent {

            label 'built-in'
        customWorkspace "/mnt/project"
    }

    stages {
        stage (clean){
            steps{
                sh 'rm -rf /mnt/project'
            }
        }
        stage ('git-installation')
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
