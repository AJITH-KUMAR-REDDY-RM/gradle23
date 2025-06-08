pipeline{
	agents any
	tools{
		gradle 'Gradle'
		jdk 'JDK'
	}
	stages{
		stage('checkout'){
			steps{
				git branch:'master',url='https://github.com/AJITH-KUMAR-REDDY-RM/gradle23.git'
				}
			}
		stage('Build'){
			steps{
				sh 'gradle build'
			}
		}
		stage('run'){
			steps{
				sh 'gradle run'
			}
		}
	}
	POST{
		success{
			echo 'build and deploy gradle'
			}
		failure{
			echo 'gradle failed'
			}
	}
}
		
