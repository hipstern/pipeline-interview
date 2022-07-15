pipeline {
  options {
    timeout(time: 5, unit: 'MINUTES')
  }
  parameters {
    choice(name: 'targetCloud', choices: ['', 'AWS', 'Azure'], description: 'The cloud provider')
    choice(name: 'targetEnvironment', choices: ['', 'dev', 'QA', 'prod'], description: 'The environment')
    string(name: 'additionalConfigs', defaultValue: '', description: 'Additional configs to apply')
  }
  stages {
    stage('Prep') {
      steps {
        echo 'Starting pipeline'
        echo "the target cloud is: ${params.targetCloud}"
        echo "the target environment is: ${params.targetEnvironment}"
        echo "additional configs: ${params.additionalConfigs}"
      }
    }
    stage('Build') {
      steps {
        echo 'Starting build'
        sleep(time: 10, unit: 'SECONDS')
        echo 'Finished build'
      }
    }
    stage('Deploy') {
      steps {
        sh """
        # Generate the configuration
        """
        echo 'Starting deploy using CLI'
        echo 'Finished deploy'
      }
    }
    stage('Test') {
      steps {
        echo 'Starting test'
        sleep(time: 10, unit: 'SECONDS')
        echo 'Finished test'
      }
    }
  }
}
