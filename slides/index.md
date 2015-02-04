- title : Where No Type Has Gone Before
- description : Pushing F# types into new places
- author : Ross McKinlay
- theme : night
- transition : zoom

***

## TO BOLDLY GO

![](images/warp.jpg)

## WHERE NO TYPE
## HAS GONE BEFORE

<small>Ross McKinlay 2015</small>

***
### TB-303, 1982
![](images/303.jpg)
###Produced for just 2 years.
###A sad failure :(

###Perhaps the world just wasn't ready...

---

###1984
![](images/newcleus.jpg)
###What happens if we press..
## THESE buttons?

---

###1987
![](images/acidtrax.jpg)
###What happens if we fiddle with ...
##ALL THE CONTROLS AT THE SAME TIME !?!

---

###1998
![](images/fatoftheland.jpg)
##Want a 303? Prepare to pay £2000, if you can find one!

***


### ME
<br/>
<br/>
###@pezi_pink
<br/>
<br/>
###www.pinksquirrellabs.com

---

####TYPE PROVIDERS: PROVIDING YER TYPES SINCE F# 3.0
<br/>
<div class="fragment">
<small>Do you have a schema for your information source? If so, what’s the mapping into the F# and .NET type system?</small>
</div>
<div class="fragment">
<small>Can you use an existing (dynamically typed) API as a starting point for your implementation?</small>
</div>
<div class="fragment">
<small>Will you and your organization have enough uses of the type provider to make writing it worthwhile? Would a normal .NET library meet your needs?</small>
</div>
<div class="fragment">
<small>How much will your schema change?</small>
</div>
<div class="fragment">
<small>Will it change during coding?</small>
</div>
<div class="fragment">
<small>Will it change between coding sessions?</small>
</div>
<div class="fragment">
<small>Will it change during program execution?</small>
</div>
<div class="fragment">
<small>Type providers are best suited to situations where the schema is stable at runtime and during the lifetime of compiled code.</small>
</div>   
<br/>
<div class="fragment">
####<span style="color:red">You should use this mechanism only where necessary and where the development of a type provider yields very high value.</span>
</div>

---

##dun.Dun.DUUUN!

![DRAMATIC CHIPMUNK IS DRAMATIC!"](http://www.gifbin.com/bin/1232550297_Dramatic chipmunk.gif)

##FORGET THE GUIDELINES ..

---

###But first, a little terminology.

#### Erased Types
<br/>

- Consist of two parts
- A compile-time type
- A runtime type

<br/>
<br/>
The compile-time type is said to </i>"erase down"</i> to the runtime type.
The compile-time types <i>disappear</i> at runtime.

***

##PART 1
#### CHOOSE YOUR OWN ADVENTURE

![](images/cyoa.jpg)

---

###STUFF LEARNT
<br>
<br>
<div class="fragment">
####YOU CAN MAKE SILLY TYPE PROVIDERS
</div>

***

##PART 2
#### SQUIRRELIFY

![](images/squirrel.png)

---

###STUFF LEARNT
<br>
<br>
<div class="fragment">
####INFINITE (UNBOUNDED) TYPE SYSTEMS ARE POSSIBLE!
</div>
<div class="fragment">
####INTELLISENSE WAS REALLY NOT DESIGNED FOR THIS..
</div>
<div class="fragment">
####PARA AND ALT+255 ARE YOUR FRIENDS!
</div>

---

###POSSIBLE EXTENSIONS
<div class="fragment">
####KEYWORD IMAGE SEARCH. ASCIIFIY. SHOW.
</div>

***

##PART 3
#### MINESWEEPER

![](images/minesweeper.png)

---

###STUFF LEARNT
<br>
<br>
<div class="fragment">
####YOU CAN WRITE FULL ON PROPER GAMES!
<small>*with some limitations</small>
</div>
<div class="fragment">
####INTELLISENSE IS STILL NOT DESIGNED FOR THIS..
</div>
<div class="fragment">
####A FIXED-WIDTH FONT IN YOUR TOOLTIPS HELPS
</div>
<div class="fragment">
####PROPERTIES ARE EVALUATED UP FRONT WHICH AN BE A MENACE!
</div>


***

![](images/intermission.jpg)

---

##RDF TYPE PROVIDER

<div class="fragment">
####ERASE TYPES TO <I>OTHER</I> ERASED TYPES ?
</div>

![](images/Erasure.jpg)


---

###STUFF LEARNT
<br>
<br>
<div class="fragment">
####PSEUDO-INHERITANCE IS POSSIBLE WITH ERASED TYPES
</div>
<div class="fragment">
####AN ODD KIND OF MULTIPLIE INHERITANCE IS POSSIBLE
</div>
<div class="fragment">
####YOU CAN PROVIDE "LENSES" TO CONVERT BETWEEN COMPATIBLE ERASED TYPES
</div>
<div class="fragment">
####YOU CAN CREATE MULTIPLE LAYERED COMPLEX TYPE SYSTEMS WITH NEGLIGIBLE RUNTIME COST
</div>

***

##PART 4
#### INTERACTIVE PROVIDER

![](images/ip.png)

---

    type IInteractiveState=
        abstract member DisplayText : string
        abstract member DisplayOptions : (string * obj) list

    type IInteractiveServer = 
        abstract member NewState : IInteractiveState
        abstract member ProcessResponse : IInteractiveState * obj -> IInteractiveState

---

###STUFF LEARNT
<br>
<br>
<div class="fragment">
####IT IS POSSIBLE AND USEFUL TO CREATE TYPE PROVIDER ABSTRACTION LAYERS
</div>
<div class="fragment">
####THE PROCESS OF CREATING COMPLEX TYPE SYSTEMS IS VASTLY SIMPLIFIED
</div>


***

##PART 5
#### 2048

![](images/2048.png)

---

###STUFF LEARNT
<br>
<br>
<div class="fragment">
####USING ABSTRACTIONS ALLOWS YOU TO FOCUS READILY ON THE PROBLEM RATHER THAN THE TYPE SYSTEM
</div>
<div class="fragment">
####INTELLISENSE IS STILL NOT DESIGNED FOR THIS
</div>

***

##PART 6
#### FIGHTING FANTASY

![](images/cityofthieves.jpg)

---

###STUFF LEARNT
<br>
<br>
<div class="fragment">
####USING TYPE PROVIDERS INSIDE OTHER TYPE PROVIDERS IS POWERFUL AND EFFECTIVE
</div>
<div class="fragment">
####INTELLISENSE IS REALLY, REALLY NOT DESIGNED FOR THIS
</div>

***


![](images/intermission.jpg)


---

###STUFF LEARNT
<br>
<br>
<div class="fragment">
####CRAZY STUFF HAPPENS IN TYPE PROVIDERS
</div>


***

##PART 7
#### MULTIPLAYER BATTLESHIPS

![](images/battleships.png)

---

##COMMUNICATIONS
![](images/comms.png)

---

##THREADS
![](images/threads.jpg)

---

##AGENTS
![](images/agent.jpg)

---

###STUFF LEARNT
<br>
<br>
<div class="fragment">
####TYPE SYSTEMS CAN BE MADE TO COMMUNICATE WITH EACH OTHER!
</div>
<div class="fragment">
####YOU CAN PLAY MULTIPLAYER GAMES IN YOUR IDE INSTEAD OF WORKING!
</div>
<div class="fragment">
####THREADS ARE A MENACE BUT CAN BE DEALT WITH!
</div>
<div class="fragment">
####AGENTS WORK JUST FINE IN TYPE PROVIDERS..
</div>
<div class="fragment">
####INTELLISENSE IS* SO* NOT DESIGNED FOR THIS
</div>

***


##PART 8
#### SANTA'S GROTTO

![](images/santa.png)

---

###STUFF LEARNT
<br>
<br>
<div class="fragment">
####YOU CAN WRITE *REALLY* COMPLEX TYPE PROVIDER GAMES
</div>
<div class="fragment">
####EVEN WITH THE ABSTRACTION, THE IP GETS UNWIELDY WITH LARGE SYSTEMS
</div>


***


##PART 9
#### ENIGMA 

![](images/enigma.jpg)

---


    type IInteractiveServer = 
        abstract member NewState : IInteractiveState
        abstract member ProcessResponse : IInteractiveState * obj -> IInteractiveState

    type InteractiveState<'a> =
        { displayOptions : 'a -> (string * obj) list 
          displayText : 'a -> string 
          processResponse : 'a * obj -> IInteractiveState
          state : 'a }
        member x.ProcessResponse o = x.processResponse (x.state, o)
        interface IInteractiveState with
            member x.DisplayOptions =  x.displayOptions x.state
            member x.DisplayText = x.displayText x.state

    type Enigma() =
        interface IInteractiveServer with
            member x.NewState: IInteractiveState = start() :> IInteractiveState        
            member x.ProcessResponse(state: IInteractiveState, response: obj): IInteractiveState =      
                let state = (state:?>InteractiveState<EnigmaTypes>)
                state.ProcessResponse(response) 
                                        

---        

###STUFF LEARNT
<br>
<br>
<div class="fragment">
####ABSTRACTION LAYERS ARE COOLER WHEN ABSTRACTED MORE!
</div>


***

##PART 10
#### INCEPTION PROVIDER

![](images/inception1.png)

---
###THINGS I HAVE TRIED

<br>
<br>
<div class="fragment">
####ALL THE 'OBVIOUS' THINGS
</div>
<div class="fragment">
####HOSTING AN FSI SESSION IN A TP
</div>
<div class="fragment">
####ERASING TO EXISING TYPE PROVIDERS
</div>
<div class="fragment">
####EMITTING IL IN TP QUOTATIONS
</div>
<div class="fragment">
####HOSTING THE F# COMPILER, BUILDING AN ASSEMBLY AND LOADING IT
</div>

---

###STUFF LEARNT
<br>
<br>
<div class="fragment">
####INHERITANCE WITH TYPE PROVIDERS WORKS JUST FINE
</div>
<div class="fragment">
####THE PROVIDED TYPES API DOESN'T LET YOU DO A WHOLE BUNCH OF STUFF
</div>
<div class="fragment">
####ALL KINDS OF THINGS!  EXCEPT HOW TO GET THIS TO WORK...
</div>

---

###THINK OF THE POSSIBILTIES...
<br>
<br>
<div class="fragment">
####A 'PACKAGE' TYPE PROVIDER. ONE TYPE PROVIDER THAT GETS OTHER TYPE PROVIDERS
</div>
<div class="fragment">
####TYPE PROVIDERS THAT SEND SERIALIZED QUOTATIONS TO OTHER TYPE PROVIDERS
</div>
<div class="fragment">
####TYPE PROVIDERS THAT SEND / GET SERIALIZED .NET ASSEMBLIES
</div>


***

##IN CONCLUSION

<br/>
<div class="fragment">
####There is certainly big scope for creating type provider toolkits and abstraction layers
</div>
<div class="fragment">
####I have tried many crazy things that may be genuinely useful!
</div>
<div class="fragment">
####I have tried many crazy things are probably completely useless
</div>
<div class="fragment">
####Maybe YOU can dream up some idea that will become the next big thing for type providers!
</div>

***

#QUESTIONS
<br/>
<br/>
##¿


