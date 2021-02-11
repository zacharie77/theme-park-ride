node('master'){
    env.PATH = "/opt/maven3/bin/:$PATH"
    docker {
            image "maven:3.6.0-jdk-13"
            label "docker"
            args "-v /tmp/maven:/var/maven/.m2 -e MAVEN_CONFIG=/var/maven/.m2"
        }
    stage('Git Clone/Pull'){
        git branch: 'master', 
        url: 'https://github.com/benjamaa-soufiene/theme-park-ride.git'
    }
    stages {
        stage("Build") {
            steps {
                sh "mvn -version"
                sh "mvn clean install"
            }
        }
    }
    post {
        always {
            cleanWs()
        }
    }
