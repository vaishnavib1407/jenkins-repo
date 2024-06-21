pipeline{
    agent{
        label{
        label 'built-in'
        customWorkspace "/mnt/project"
        }
        tools {
        maven 'apache-maven-3.9.8' 
    }
    }
    stages{
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
