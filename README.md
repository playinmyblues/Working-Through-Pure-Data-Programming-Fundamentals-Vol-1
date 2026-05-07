# Working-Through-Pure-Data-Programming-Fundamentals-Vol-1

EDIT:
During the working through of this material, I was trying to create several constructs for which I later realized Pd already has objects. A good example of this the use of what is usually the [t b f] object. I created my own little construct, of which I was quite pleased at the time, to get around the problem of the order of operations used with hot and cold inlets on the [+] object. You can see how I got around the cold inlet addition problem by sending a bang to the hot inlet every time a number connected to the cold inlet was changed. This is seen in the patch named p73_volume_control_8_oscs_2_inits.pd and other similarly named patches. As I worked through more of the book, I realized my time was spent doing something already addressed in Pd. Hopefully, I do not make that mistake too often.
This is a collection of Pure Data patches that have been created to help learn the material presented in the book "Pure Data Programming Fundamentals: Patching, effects, sound synthesis," by Maurizio Di Berardino. Comments should be found throughout the patches to help with understanding.

The general format for patch names is to include an abbreviation for the word "page," "p," followed by the page number at the beginning of the patch name. The rest is often a description of the patch.

For the first patch posted here, the material I was reading at the time was around page 36 and it was regarding the use of externals in Pure Data. It also talked about how to add objects to reference individual parts of external libraries. I provided a lot of comments in the patch to describe what I have done.

As of this moment, the associated folder for p36_adding_small_number_of_patches.pd is <Example_external>.

The latest batch of patches I have worked through are p38... to p63...

P63_message_boxes.pd also has a 2nd and 3rd version. I create them and name them this way to group them together for the purpose of keeping a concept in mind and exploring it. The 2nd and 3rd versions should be obvious but I do not number the first version with 1.

There are also some ideas and concepts I have explored and been exposed to in other explorations of Pd and I often include those in my patchs as I explore the book. Most of that type of material is explained in the comments.

Patches p67... to p68... are fairly vanilla patches. p73_volume_control.pd gets a little interesting but is kind of plain. P73... is where I could see something more interesting happening with finer control made available with the two horizontal sliders. I figured out for the second time how to get the [+] object to add two numbers and make the cold inlet add the two numbers. It does not really do that. It is still the hot inlet of the [+] object triggering the adding of two numbers but have a look and see what is going on. It should be apparent from the explanations in the comments. p73_volume_control_8oscs_2.pd is the more interesting with better control and adding works when either horizontal slider is moved.

The newest batch of patches includes: p73_volume_control_8_oscs_2_inits.pd and those starting with p74 to p83. Patch p73_volume_control_8_oscs_2_inits.pd is an update of the previously made patch named in a similar manner because I wanted to add the ability to have the patch load and make noise as soon as the DSP turns on. Fortunately, when the sliders are used, you can select an option in the Properties where there is an initial value or not when the patch opens. That makes is easy to make that version of the patch its own preset, in a sense.

The rest of the patches cover topics in the books and they are mainly related to what is in the name of the file. Makes sense to me. When I get to p83 in the book, it recommends using logic operators to build something like a sequencer and I go about that. But I was trying to rememeber how to build a counter without actually referring to some other patch I had previously built. I remembered seeing one somewhere in my previous explorations of learning Pd. In the process, I succeeded in building a counter but could not figure out the reset feature myself although got kind of close. I could have gotten a sequencer built but my counter would eventually run out of variable space as it would not reset. I had thought of the [mod] operator from other programming. If you are not familiar with it, check out the patches. So, eventually, I looked up a couple of examples and found something simple. In the process, I took the time to learn more about the [trigger float float] object and how it works in the resettable counter.

In the end, while I find I am not getting through this book very quickly, I feel I am learning a lot about Pd.

I have added in some work on the canvas object in the process of learning about visuals in Pd. I have been using the loadbang book found online. I would like to be able to add oscilloscopes to my patches so I can see waveforms.
