node {
	stage 'checkout'
   checkout([$class: 'GitSCM', 
			branches: [[name: '*/master']], 
			doGenerateSubmoduleConfigurations: false, 
			extensions: [], 
			submoduleCfg: [], 
			userRemoteConfigs: [[credentialsId: 'myCredentials', url: 'https://github.com/timokorny/ucdp-first-repo.git']]])
   echo 'checked out'
}
