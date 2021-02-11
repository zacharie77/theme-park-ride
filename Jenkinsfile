node('master'){
    env.PATH = "/opt/maven3/bin/:$PATH"
    
    stage('Git Clone/Pull'){
        git branch: 'master', 
        url: 'https://github.com/benjamaa-soufiene/theme-park-ride.git'
    }
    stage('Build'){
         sh "mvn clean compile"
    }
    stage('Test'){
          sh "mvn clean test"
    }
    stage('Package'){
          sh "mvn clean package"
   }
   stage('Install'){
          sh "mvn clean install"
   }
}

