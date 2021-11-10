pipeline {
  agent any
  stages {
    stage('Example') {
      steps {
        echo "Hello ${params.PERSON}"
        echo "Biography: ${params.BIOGRAPHY}"
        echo "Toggle: ${params.TOGGLE}"
        echo "Choice: ${params.CHOICE}"
        echo "Password: ${params.PASSWORD}"
        sh 'echo $version'
      }
    }

    stage('Build') {
      steps {
        echo 'Building'
      }
    }

    stage('Test') {
      steps {
        echo 'Testing'
      }
    }

    stage('Deploy') {
      steps {
        echo 'Deploying'
      }
    }

  }
  environment {
    version = 'VersionNumber([ projectStartDate: \'2018-12-31\', versionNumberString: \'aodb-$PREFIX-${BUILD_DATE_FORMATTED, "yyyy-MM-dd"}-${BUILDS_TODAY}\', versionPrefix: \'\', worstResultForIncrement: \'SUCCESS\' ])'
  }
  parameters {
    string(name: 'PERSON', defaultValue: 'Mr Jenkins', description: 'Who should I say hello to?')
    text(name: 'BIOGRAPHY', defaultValue: '', description: 'Enter some information about the person')
    booleanParam(name: 'TOGGLE', defaultValue: true, description: 'Toggle this value')
    choice(name: 'CHOICE', choices: ['One', 'Two', 'Three'], description: 'Pick something')
    password(name: 'PASSWORD', defaultValue: 'SECRET', description: 'Enter a password')
  }
}