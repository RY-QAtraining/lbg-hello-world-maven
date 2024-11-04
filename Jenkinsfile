pipeline{
    agent any
    tools{
        maven "M3"
    }
    stages{
        stage("checkout"){
            steps{
                git branch:"main",url:"https://github.com/RY-QAtraining/lbg-hello-world-maven.git"
            }
        }
        stage("compile"){
            steps{
                sh "mvn clean compile"
            }
        }
        stage("test"){
            steps{
                sh "mvn test"
            }
        }
        stage("Package"){
            steps{
                sh "mvn -Dmaven.test.skip -Dmaven.compile.skip package"
            }
        }
    }
}