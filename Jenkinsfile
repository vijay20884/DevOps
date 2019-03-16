node('SLAVE1'){
    stage('Build'){
	    bat 'git clone https://github.com/spring-projects/spring-mvc-showcase'
        bat 'mvn -f C:\\git\\spring-mvc-showcase\\pom.xml install'
    }
    
    stage('Downstream Project'){
        build 'mvc_showcase_deploy'
    }
}