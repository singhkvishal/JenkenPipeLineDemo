pipeline {
    agent any
    parameters {
      string(name: 'PLANET', defaultValue: 'Earth', description: 'Which planet are we on?')
      string(name: 'GREETING', defaultValue: 'Hello', description: 'How shall we greet?')
    }
    triggers {
        parameterizedCron('''
            # leave spaces where you want them around the parameters. They'll be trimmed.
            # we let the build run with the default name
            */2 * * * * %GREETING=Hola;PLANET=Pluto
            */3 * * * * %PLANET=Mars
        ''')
    stages {
        stage('Example') {
            when {
                triggeredBy 'ParameterizedTimerTriggerCause'
            }
            steps {
                echo 'This build was triggered by a `parameterizedCron` trigger'
            }
        }
    }
   }
}
