properties([
  parameters([
    string(name: 'PLANET', defaultValue: 'Earth', description: 'Which planet are we on?'),
    string(name: 'GREETING', defaultValue: 'Hello', description: 'How shall we greet?'),
    choice(name: 'Test_Envirement',choices:['QA','UAT'])
  ]),
  pipelineTriggers([
    parameterizedCron('''
        */2 * * * * %GREETING=Hola;PLANET=Pluto
        */3 * * * * %PLANET=Mars
    ''')
  ])
])
