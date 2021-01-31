node('master'){
    env.PATH = "/opt/maven3/bin/:$PATH"
    
    stage('Git Clone/Pull'){
        git branch: 'master', 
        url: 'https://github.com/COMPTE_GITHUB/theme-park-ride'
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
}

