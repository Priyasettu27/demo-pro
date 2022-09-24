pipeline {
    agent any

    stages {
        stage('SCM') {
            steps {
                git branch: 'war', url: 'https://github.com/Priyasettu27/demo-pro.git'
            }
}
	stage('build') {
            steps {
               sh 'mvn clean'
               sh 'mvn install'

        }
}
stage('deploy') {
            steps {
              deploy adapters: [tomcat9(credentialsId: 'bad18ccf-0f62-4752-b319-accf1454cd47', path: '', url: 'http://3.111.53.135:9090/')], contextPath: 'demopipe', war: '**/*.war'

        }
    }
}
}

