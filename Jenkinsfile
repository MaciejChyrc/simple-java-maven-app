pipeline {
    agent any
    stages {
        stage('Build') {
            steps {
                bat 'mvn -B -DskipTests clean package'
            }
        }
        stage('Test') {
			steps {
				bat 'mvn test'
			}
		}
		stage('Run') {
			steps {
				bat 'mvn exec:java -Dexec.mainClass="com.mycompany.app.App"'
			}
		}
    }
}
