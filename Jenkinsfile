pipeline 
{
    agent any
    stages
    {
        stage('scm checkout')
        {
            steps
            {git branch: 'master', url: 'https://github.com/Devanshbirthare/old-maven-project.git'}
        }
        stage('code compile')
        {
            steps
            {
               withMaven(globalMavenSettingsConfig: '', jdk: 'JAVA_HOME', maven: 'MAVEN_HOME', mavenSettingsConfig: '', traceability: true) 
               {sh 'mvn compile'} 
            }

        }
    }
}