import jenkins.model.Jenkins;

pipeline {
    agent any 
    stages {
        stage('Stage 1') {
            steps {
                echo 'Hello world!' 


                script {
                            def buildName = Jenkins.instance.getItemByFullName('repotest/feature%2FPR3')
                            echo "Last success: ${buildName.getLastSuccessfulBuild()}"
                            echo "All builds: ${buildName.getBuilds().collect{ it.getNumber()}}"
                            echo "Last build: ${buildName.getLastBuild()}"
                            echo "Is building: ${buildName.isBuilding()}"                      
                    
                }

              }
        }
    }
}