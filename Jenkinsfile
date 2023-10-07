properties([
  parameters([
    string(name: 'PLANET', defaultValue: 'Earth', description: 'Which planet are we on?'),
    string(name: 'GREETING', defaultValue: 'Hello', description: 'How shall we greet?')
  ]),
  pipelineTriggers([
    Main('''
        */2 * * * * %GREETING=Hola;PLANET=Pluto
        */3 * * * * %PLANET=Mars
    ''')
  ])
])
