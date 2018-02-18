# Louvre Abu Dhabi's Interactive Flute Installation
The project was to come up with an interactive musical installation for Louvre Abu Dhabi. This repo is dedicated to the development of a prototype of the installation. It uses a leap motion input to track hand movement and respond accordingly.

## Getting Started
Download the files in the repo. The flute SFZ file can be found for free here: http://patcharena.com/tag/free-sfz-instruments/ . Wekinator, Sforzando and processing need to be installed for this project to work. The input leap motion processing files and output MIDI files have been taken from the published wekinator examples. 

## Components
1.Wekinator
2.Leap Motion Controller
3.Sforzando
4.Instrument SFZ file


## Documentation
The objective of this project was to create an interactive music installation. The project uses wekinator to implement machine learning. The leap motion controller tracks hand movement which is used as an input to train wekinator. Processing's MIDI output for wekinator is then used to feed the output of the wekinator to Sforzando. A continuous form of learning is used in wekinator where the output is mapped on to individual notes in Sforzando. Processing's MIDI file offers the opportunity to send two outputs, pitch and velocity. I decided on keeping the velocity constant and varying the pitch, which results in a variation of the notes pressed. This allows for simplicity in both implementation and user testing. 

Iteration 1:
The first iteration of the project came after finalising the input and the concept of the implementation. I was struggling to find an output so I used an example drum synth output from wekinator examples to display what the idea could materialise to be. A user testing video can be found [here:](https://www.youtube.com/watch?v=GZNP5Ut9flU). This user testing made me realise that it was hard for users to grasp a control over the musical output thus disabling them from producing a musical tone that they could feel is coming from their movement. 

Iteration 2: 
In the second iteration of the project, I started using Sforzando as an output. In this iteration, I was trying to use finger movement mimicing a piano to move across the flute notes. At this point, the software is accessing all available flute notes in the sfz file. As can be seen [here](https://www.youtube.com/watch?v=ZdJ6LYlyFxw), the leap mtotion controller also seems to be picking up a limited range of motion thus only accessing a limited range of notes. It is struggling to differentiate between different 'key presses'.

Iteration 3:
In the third iteration of the project, I limited the notes that are accessible to Sforzando by changing the limits in the Processing MIDI output file as shown in lines 125-129 of the file. These values will be changed in the latter iterations. The values changed are the upper and lower limits for pitch. This resulted in a demonstration that can be found [here](https://www.youtube.com/watch?v=F8L_mIAdnO4). The problem with this iteration was that the response wasnt as controlled as it should be due to leap motion's inability to track finger presses distinctly. 

Iteration 4:
In the fourth iteration of the project, I tried using both hands as inputs to leap motion so instead of using one finger as a key press I tried using two but this only resulted in more confusion for the leap motion.

Iteration 5: 
In this iteration, I went back to using one hand. In this case, however, I am using a rotating hand motion to go through the range of notes. The video can be found [here](https://www.youtube.com/watch?v=noYlou3NAh4). This showed a much better response to hand movement, which resulted in more user control on the music produced. It also features a shortened range of notes, which allows for a basic control to be established first, leaving room for further development. 

Iteration 6-Final:
In the final iteration, I kept the range of notes from the previous iteration and also kept the hand movement same. I trained wekinator again with additional samples to provide for more optimal output. The final demonstration can be found [here](https://www.youtube.com/watch?v=KWHo-lIT4jg). 

This project gave me an insight into the usefulness of machine learning but also the amount of resources present in the form of outputs. It was also a pleasant experience to work with leap motion, which I transitioned to from the kinect, whose interface was not as user-friendly. 

