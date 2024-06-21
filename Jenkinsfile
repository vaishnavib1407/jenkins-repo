pipeline{
    agent{
        label{
        label 'built-in'
        customWorkspace "/mnt/project"
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
