pipeline{
    agent{
        kubernetes {
            yamlFile 'secret_jfrog_jenkins.yaml'
            yamlFile 'docker_jfrog.yaml'
        }
    }
    
    stages{
        stage('run'){
            steps{
                container('nerdctlcont'){
                    sh 'apt update && apt install docker.io -y'
                    sh 'echo "cmVmdGtuOjAxOjE3MTUyNDU2NjI6Nld5em9SaldrcEdDSXNMdk1PdkpDcU1rUndw" >> new.txt'
                    sh 'docker login -uguptamadhur045@gmail.com rahul1705.jfrog.io --password-stdin < new.txt'
                    sh 'docker pull rahul1705.jfrog.io/docker/ubuntuvim:19'
                    sh 'ls -al'
                    sh 'sleep 50'
                }
            }
        }
    }
}
