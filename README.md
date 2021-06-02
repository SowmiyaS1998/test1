# AUDIO BOOK
# pip install pyttsx3 to convert the text to speech
import pyttsx3
# pip install PyPDF2 to extract text from pdf
import PyPDF2

# open the file within the python directory & #open any pdf/book that you want to read for you by your BOT friend to read
reader = open("Attribute_Info.pdf","rb") 

giversays = PyPDF2.PdfFileReader(reader)

# to find total num of pages
pages=reader.numPages

# initialize
speaker = pyttsx3.init()

# getpage where you wanna start, extract the text from there! ask BOT to read!
for i in range(1,pages):
    page = reader.getPage(1) 
    text = page.extractText()
    speaker.say(text)
    speaker.runAndWait()
