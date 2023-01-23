Author: Mario Saraiva

Date: April, 2018

# Brazilian-Politicians
Exploratory data analysis about Brazilian politicians, in particular, congresspeople, their performance in office and election results.

Important Processing steps:

Before opening the files convert each file to encoding UTF-8.:
Open the file with notepad click “save as” and choose encoding UTF-8. This will take care of Portuguese accents and special characters.
Then create a master list to compare the observations of each file.
First extract key variables. Before extracting, use the PivotTable to summarise results per id. I started this process with the Ano-2015 file. Extract the keys to a new sheet (I will call it keys_sheet).
Repeat the same step for Ano-2016 file.
Extract the key from the deputado.xls file and paste it into the keys_sheet).
Use VLOOKUP to compare the keys between the common keys, i.e. see all the names that appear in both ano-2015 and deputado columns. Repeat this step for ano-2016 and deputados columns.
In a similar fashion, extract and compare the key from proposicoes_unicode.xls. Keep track of the values that are common between all keys.
Before extracting the keys from Resultado_da_Eleicao, you need to remove the white spaces from the sheet, (optional: I also calculated the ratio of votes received or the state total number of votes). 
Then extract and compare as in the previous steps.
Note that there will be several congresspeople that will not appear in the Resultado_da_Eleicao.csv (in my case I only downloaded candidates that were elected). 69 “suplentes” came into office during legislature 55. In order to get their names to match, you must download the election results data for “suplentes” from TSE. For some strange reason, I had to use a VBA (google the code) to remove the accents from the keys_sheet name in order to be able to match the keys through VLOOKUP.
The result was saved in the Keys_sheet.xlsx (in the interim folder)


Interim Data:

I used excel’s PivotTable to summarise the data for all sheets (besides eleicoes_2014).
I had to use additional VLookup to insert the keys on the deputado.xls file.
