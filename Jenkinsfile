pipeline {
    agent any
	
	
	stages {
		stage('WorkspaceCleanup'){
			steps {
				script {
					try {
						//cleanWs()
																		
				}catch (err) {                                        
					unstable(message: "unstable")
				}
			}
		  }
		}
	
		
		stage("Env Variables") {
			steps {
				script {
					try {
								
								
				}catch (err) {                                        
					unstable(message: "unstable")
				}
			}
		  }
		}
		
		stage('SCM Checkout') {			
					steps{
						script {
							
							checkout([$class: 'GitSCM', branches: [[name: '*/master']], doGenerateSubmoduleConfigurations: false, extensions: [], submoduleCfg: [], userRemoteConfigs: [[credentialsId: 'smondut', url: 'https://github.com/shireeshamonduti/SeleniumWebTesting.git']]])
							
						}
					}
				}	
				
		stage('Selenium_TestRun') {			
					steps{
						script {
						
							bat 'mvn -f /pom.xml clean test'
							
						}
					}
				}
			}
		}

