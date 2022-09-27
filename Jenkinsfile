node {
    
    stage("code")
    {
    git 'https://github.com/learnsoftwares/maven_demo.git'
    }
    stage("build")
    {
    //sh 'mvn verify'
    bat 'mvn verify'
    }
    stage("Deploy")
    {
    deploy adapters: [tomcat9(credentialsId: '752d6505-a033-4979-869c-5ec7d1312eb3', path: '', url: 'http://localhost:8081/')], contextPath: 'scriptedgame', war: '**/*.war'
    }
    
}
