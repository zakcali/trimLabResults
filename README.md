# trimLabResults
Nucleus EHR software by Monad Yazılım, has ability to copy/paste laboratory results to patient's history.
As an oncologist, I have lots of visits for a patient, so lots of text to write to patients history text. 
I need to shorten the laboratory result texts, as below:
"Kalsiyum - 10,6 mg/dL" -> "Ca:10,6"
Sodyum - 135,0 mg/dL" -> "Na:135,0" 
Morover, I need whole text in one line, instead of one result per line.

So I wrote a html web page, with minimal JavaScript coding.
Paste laboratory results text to form on the top, click "Kısalt" button, see trimmed text in the form on the bottom.
Now you can select the trimmed text, and copy it to clipboard, then paste it to patients history text.
