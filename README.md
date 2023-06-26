# Text-To-Speech-Converter

#This is Project languages used in Html,Css and JavaScript.

The JavaScript File
In the JavaScript file, we are mainly going to use three interfaces: SpeechSynthesis , window.speechSynthesis and SpeechSynthesisUtterance. So, let’s understand them briefly.

#JavaScript SpeechSynthesis Interface
This is the principal interface for the speech synthesis service, which controls the synthesis or production of speech based on the text input. This interface is used to start, stop, pause, and restart speech, as well as to access the device’s supported voices.
The methods provided in this Interface are as follows:

speak(): To add the utterance(object of SpeechSynthesisUtterance) in the queue, which will be spoken when there is no pending utterance before it, this is the function, we will be using to
getVoices(): To get the list of all supported voices which the device supports

JavaScript window.speechSynthesis Property
The speak() method is called on the voice synthesis controller interface, which is referenced by this property of the JavaScript window object.

We will understand this more when we jump into the code.

#JavaScript SpeechSynthesisUtterance Interface
This is the interface where we really produce the speech or utterance from the text provided, including language type, volume, voice pitch, rate of speech, and so on. After creating an object for this interface, we provide it to the speak() method of the SpeechSynthesis object to play the speech.


#Voice:

The voice property retrieves and modifies the voice that will be used to deliver the speech. One of the SpeechSynthesisVoice objects should be used. If it isn’t configured, the most appropriate default voice for the language setting of the utterance will be utilized.

We need to retrieve the list of available voices in the window object to set the voice of the utterance. The voices will not be available right away when the window object loads. It’s an async operation. When the voices are loaded, an event will be triggered. We can set a function that should be executed when the voices are loaded.

window.speechSynthesis.onvoiceschanged = () => {
  // On Voices Loaded
};
Using window.speechSynthesis.getVoices(), we can retrieve a list of voices. It will return an array of accessible SpeechSynthesisVoice objects. Let’s save the list in a global array and use it to update the web page’s select menu with the available voices.

#Screenshot
![Screenshot (183)](https://github.com/123peeush/Text-To-Speech-Converter/assets/79499675/469126c3-716b-4e04-8449-2c9f1e669d9d)
