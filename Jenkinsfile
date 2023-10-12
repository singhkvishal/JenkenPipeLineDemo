properties([
	parameters([
				string(name: 'USERNAME', defaultValue: 'Vishal Singh', description:'Enter the Name os the test pack'),
				choice(name: 'Test_Envirement',choices:['QA','UAT'])
				]), pipelineTriggers([
					parameterizedCron('''
						*/2 * * * * %Test_Envirement=QA;USERNAME='Vishal'
						*/3 * * * * %Test_Envirement=UAT;USERNAME='Singh'
					''')
				  ])
				])
