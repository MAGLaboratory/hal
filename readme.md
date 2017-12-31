**Readme**

This repository is meant to document the current state and history of the **HAL** computer installed at *MAG Laboratory*. If you are a current member of MAG Laboratory and find an error in this repository you are highly encouraged to fork it, fix it and push.  Don’t be afraid to take ownership and clobber what has come before, we can always revert if you screw up.

**Hardware**

The HAL system consists of the following hardware:
* Raspberry PI V?
* Open Access 4.0
  * [schematics](http://www.accxproducts.com/wiki/index.php?title=File:Open_Access_Control_v4_std_136.zip)
  * [code](https://github.com/MAGLaboratory/halley)
* Custom Hardware
* Sensors

**Roadmap**

HAL is foolproof and incapable of error, therefor there is no need for changes.

**History**

This repository is the fallout of a [discussion on the MAG Lab google group]( https://groups.google.com/forum/#!topic/maglaboratory/54QvicI6HVY). In the event that the original thread is purged the gist of it is captured here:

“It seems we are having some issues with HAL and our reading of HAL in order to report an accurate "open" or "closed" on the website.  Hal monitors its different input (motion and reed switches for doors, as well as temperature), hal also writes to the access controll board (custom shield that reads the rfid scanner, and opens/locks the door automatically) lists of rfid numbers that can open the door and allows remote opening of the space for certain situations.
We have been having issues with false positives and negatives for the space status.  We need some help getting hal and the website to read status of the sensors and report a true status of the space as open or closed.  This involves correct collection and reporting of the sensors from hal to the website and writing code on the website to interpret the data and report based off of some logic.”
can anyone help with this?”

--Trent

“It could be possible that a human did not turn the Open Switch to the off position and the broken Pod Bay Door which consistently read open generated a condition where the space was falsely open.
The current logic which determines the open status of the space is as follows:
Set Open Status to open if Open Switch is on and (Pod Bay Door is open or Front Door is open) otherwise set to closed.
Based on discussions that we've had about the space and the broken open status, I am strongly leaning towards writing a disclaimer on the "Are we open?" page and changing the logic so that Open Status is determined solely on the status of the Open Switch.  This logic change is based on the fact that Winter is cold, and open doors make the space colder.  Additionally, this change would coincide with the history and intent of naming our monitoring system HAL.”
In the movie 2001: A Space Odyssey, a computerized AI controls the Discovery One's systems on its trip to Jupiter.  The AI is named HAL 9000 and insists that it is "foolproof and incapable of error."  During the course of the movie, Hal reports the status of an antenna control on the ship as faulty.  The astronauts perform extra-vehicular activity (EVA) to retrieve the supposedly faulty antenna control, but find nothing wrong with it.  Hal insists that this is due to human error and that the antenna control should be reinstalled to observe its behavior until it fails.  Ground control's twin HAL 9000 disagrees with Hal's observations.  The astronauts have a discussion about Hal's behavior in supposed secret in an EVA pod where they assume that Hal cannot understand their conversation.  Hal is able to read their lips and determine their conversation.  The astronauts agree to disconnect Hal if he is proven wrong.  On the EVA performed to replace the antenna control, Hal overrides the astronaut's control over his EVA pod and severs the umbilical line which kills the astronaut and sends him adrift.  Another astronaut goes to retrieve the now dead astronaut.  Hal shuts off life support systems, killing all remaining astronauts aboard the ship.  The astronaut who went to retrieve the dead astronaut comes back and finds that Hal refuses to open the Pod Bay Doors under the observation that the astronauts would disable (kill) Hal if it did open the Pod Bay Doors.
I should mention that our HAL cannot open the Pod Bay Door.  In short, our HAL is a satirical impression of HAL 9000.  It is purposely non-sentient, unimportant, and human-reliant.  And it would be reasonable to change the Open Status of the space to be controlled solely by humans.
Did somebody leave the cat in?  The Shop Motion sensor is still picking up something...”

--Brandon Lu

