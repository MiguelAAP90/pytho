# pytho
#obtain data from stock market with python.

#import the libraries

	import time  #Time structure 
	import datetime  #Date structure
	import pandas  as pd  #ata analysis and manipulation


	tiker = (input("Insert Tiker:")).upper()

#periods needed from the tiker given 

	period1 = int(time.mktime(datetime.datetime(2021, 1, 1, 23, 53).timetuple()))
	period2 = int(time.mktime(datetime.datetime(2021, 9, 30, 23, 53).timetuple()))
	interval1 = '1wk'
	
#extracting data from yahoo finance
		
		data_tiket = f'https://query1.finance.yahoo.com/v7/finance/download/{tiker}?period1=
		{period1}&period2={period2}&interval={interval1}&events=history&includeAdjustedClose=true'
		
		df = pd.read_csv(data_tiket)
		print(df)	
