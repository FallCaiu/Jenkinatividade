pipeline {
    agent nome

    stages  ('Build'){
        agent{
            docker { image 'maven' }
        }
           steps {
                echo "mvn package -Dmave.test.skip=true"
            }
        }
    stage('Test'){
        agent{
            docker {image 'maven'}
        }
        steps{
            echo "mvn clean install"
        }
    }
}
