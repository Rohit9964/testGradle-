pipeline{
	agent any
	tools{
		gradle 'Gradle'
		jdk 'JDK'
	}
	
	stages{
		stage('checkout'){
			steps{
				git branch : 'master', url : 'https://github.com/Rohit9964/testGradle-.git'
			}
		}
		stage('build'){
			steps{
				sh 'gradle build'
			}
		}
		
		stage('test'){
			steps{
				sh 'gradle test'
			}
		}
		stage('Run Application'){
			steps{
				sh 'gradle run'		
			}
		}
		stage('Run task'){
			steps{
				sh 'gradle show'		
			}
		}
	}
	post{
		success{
			echo 'build successful'
		}
		failure{
			echo 'buid fail'
		}
	}
}
