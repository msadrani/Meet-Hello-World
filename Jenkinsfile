def mvnHome
pipeline{
    agent any
    tools{
        maven 'M2_HOME'
    }
    stages{
        stage("Initialize"){
            steps{
                sh '''
                   echo "mvnHome= ${M2_HOME}"
                   '''
            }
        }
        stage("Build"){
            steps{
                echo 'This is minimal'
                sh 'mvn -Dmaven.test.failure.ignore=true install'
/*                 script{
                 withEnv(["MVN_HOME=${mvnHome}"])
                 {
                    if (isUnix()){
                        sh '"$MVN_HOME/bin/mvn" -Dmaven.test.failure.ignore clean package'
                    }
                    else{
                        bat(/"%MVN_HOME%\bin\mvn" -Dmaven.test.failure.ignore clean package/)
                    }
                 }
                } */
            }
        }

    }
}