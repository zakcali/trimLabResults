# trimLabResults
Nucleus EHR software by Monad Yazılım, has ability to copy/paste laboratory results to patient's history.
As an oncologist, I have lots of visits for a patient, so lots of text to write to patients history. 
I need to shorten the laboratory result texts, as follows:

	"Kalsiyum - 10,6 mg/dL"  
	"Sodyum - 135,0 mg/dL" -> 
	
	"Ca:10,6" "Na:135,0" 

So I wrote a html web page, with minimal JavaScript coding. Just paste laboratory results text to form on the top, click "Kısalt" button, see trimmed text in the form on the bottom. Now you can select the trimmed text, and copy it to clipboard, then paste it to patients history.

JavaScript String replace() Method

	shortText = shortText.replace ("Kalsiyum - ", "Ca:");
	shortText = shortText.replace ("mg/dL", "");

Look at the source code. If a string to be replaced only once, the code below is enough:

	shortText = shortText.replace (longArray[index], shortArray[index]);

The term "Kalsiyum" expected to be seen only once, but "mg/dL" could be seen multipl times, so the code above only removes first occurence of "mg/dL"

this code removes all occurences (globally) of "mg/dl"

  	shortText = shortText.replace (/mg/dL/g, "");

We must supply /mg/dL/g as a variable to Method by reading from an array. This code doesn't work:

  	rText="/" + longArray[index] + "/g";
  	shortText = shortText.replace (rText, shortArray[index]);

but this code works:

	rText= longArray[index];
	shortText = shortText.replace (new RegExp(rText,"g"), shortArray[index]);
	
    
