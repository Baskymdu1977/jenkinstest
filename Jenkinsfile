#!groovy
import jenkins.model.Jenkins;

pipeline {
    agent any 
    stages {
        stage('Stage 1') {
            steps {
                echo 'Hello world!' 
                Jenkins.instance.getItemByFullName(multibranchPipelineProjectName).getItems().each { repository->
		  repository.getItems().each { branch->
		    branch.builds.each { build->
			echo " build " + build
			}
		  }
}
            }
        }
    }
}