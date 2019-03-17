node('SLAVE1')
{
    stage('Copy from Github')
	{
	    bat 'git clone https://github.com/spring-projects/spring-mvc-showcase'
	}
	
	stage('Move from local jenkins to git')
	{
		bat 'xcopy C:\\jenkins\\workspace\\Jenkins_Pipeline_Projects\\mvc_showcase_build\\spring-mvc-showcase C:\\git\\spring-mvc-showcase'
    }    
	
	stage('Build')
	{
		bat 'mvn -f C:\\git\\spring-mvc-showcase\\pom.xml install'
    }
    
    stage('Downstream Project')
	{
        build 'mvc_showcase_deploy'
    }
}