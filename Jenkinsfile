node('BDP'){
    stage('Build'){
        bat 'mvn -f C:\\git\\spring-mvc-showcase\\pom.xml install'
    }
    
    stage('Downstream Project'){
        build 'mvc_showcase_deploy'
    }
}