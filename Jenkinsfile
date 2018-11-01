node {
	stage 'checkout'
   checkout([$class: 'GitSCM', 
			branches: [[name: '*/mybranch']], 
			doGenerateSubmoduleConfigurations: false, 
			extensions: [], 
			submoduleCfg: [], 
			userRemoteConfigs: [[credentialsId: 'myCredentials', url: 'git@git.servername:https://github.com/timokorny/ucdp-first-repo.git']]])
   echo 'checked out'
}
