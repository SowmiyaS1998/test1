# AUDIO BOOK
# pip install pyttsx3 to convert the text to speech
import pyttsx3
# pip install PyPDF2 to extract text from pdf
import PyPDF2
#open the file within the python directory
reader = open("Attribute_Info.pdf","rb") #open any pdf/book that you want to read for you by your BOT friend
#to read
giversays = PyPDF2.PdfFileReader(reader)
pages=book.numPages # to find total num of pages
speaker = pyttsx3.init() #initialize
for i in range(1,pages):
    page = reader.getPage(1) #getpage here you wanna start
    text = page.extractText() #extract the text from there
    speaker.say(text) #ask BOT to read
    speaker.runAndWait()
