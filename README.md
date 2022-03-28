# trimLabResults
Nucleus EHR software by Monad Yazılım, has ability to copy/paste laboratory results to patient's history.
As an oncologist, I have lots of visits for a patient, so lots of text to write to patients history. 
I need to shorten the laboratory result texts, I need to shorten the laboratory result texts, following:
```
"Kalsiyum - 10,6 mg/dL"  
"Sodyum - 135,0 mg/dL"
```
to:
```
"Ca:10,6" "Na:135,0" 
```


So I wrote a html web page, with minimal JavaScript coding. Just paste laboratory results text to form on the top, click "Kısalt" button, see trimmed text in the form on the bottom. Now you can select the trimmed text, and copy it to clipboard, then paste it to patients history.

JavaScript split and join () methods instead of replace method.

		shortText=shortText.split(myDict[i]).join(myDict[i+1]);
