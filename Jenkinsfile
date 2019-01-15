node(label: 'MAVEN') {

  stage('SCM'){
		git 'https://github.com/spring-projects/spring-petclinic.git'
  }

  stage('MAVAN'){
		sh 'mvn clean package'
  }

  stage('Artifacs'){
		archiveArtifacts 'target/*.jar'
  }

    stage('TestResults'){
        junit 'target\\surefire-reports\\*.xml'
  }

}