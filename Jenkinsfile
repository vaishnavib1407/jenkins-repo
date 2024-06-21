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
                    sh 'mvn clean package'
               }    
        }
        stage ('Echo Branch') {

            steps {
                
                    echo "This is master branch"
                }
            
        }
    }
}
