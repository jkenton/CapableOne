---
title: "Suspicious Minds and NeuralHASH"
date: 2021-09-01 06:00:00
layout: post
comments: true
---


<iframe width="560" height="315" src="https://www.youtube.com/embed/RxOBOhRECoo" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>


**THEN**

A few years ago, Apple and the FBI got into a set-to about forcibly unlocking the iOS device of a terrorist and his wife (both deceased by that time).[[FBI–Apple encryption dispute](https://en.m.wikipedia.org/wiki/FBI%E2%80%93Apple_encryption_dispute)] The FBI wanted Apple to use its internal wizardry to unlock the iOS  device (a phone that ran software written by Apple). Apple said that it was not able to do so. Apple claimed that its encryption was not "breakable" by exploiting a "back door", so they said, "nothing doing."

```
NAYSAYERY
Are you trying to protect terrorists? Why would you want to make it easier for terrorists to get away with their crimes?
```

**Apple's Side**

At the time, I said Apple had done the "Right Thing" by rejecting the request from the FBI, especially since they claimed they were powerless to break their own encryption.

There are some who might say that Apple was protecting its user base from the sometimes spurious requests the [executive branch] makes to get evidence "out of" suspects, easing their investigatory process. 

**The FBI's Side**

The FBI wanted to know if the phone contained information about other planned attacks, associates, etc. As far as the FBI goes, and their desire to identify other active terrorists, this request seems utterly reasonable. 

My understanding is that people are not *obligated to cooperate* with ongoing investigations. Yes, the [executive branch] can threaten them, cajole them, and even attempt to deceive them into cooperation ("Them" is a pronoun to represent "persons of interest" or even "suspects"). If they can *prove* that someone has useful information, and is withholding it, the [executive branch] can detain those people. It seems to me that the [executive branch] has most of the tools on their side in this equation.  And I suppose that's fair, given - in my understanding - that folks are not obligated to cooperate.

OK, so Apple told the FBI to figure it out on their own (and they did, by the way [[The FBI wanted to unlock the San Bernardino shooter’s iPhone. It turned to a little-known Australian firm.](https://www.washingtonpost.com/technology/2021/04/14/azimuth-san-bernardino-apple-iphone-fbi/)]). I thought that was the right and proper thing to do in the situation. Why would a company claim that even they cannot see your stuff, but then turn tail instantly and say under their breath "unless there's a warrant"? 

Anyway, Apple was on the "Right Thing" list for that action. They had no obligation to assist, especially since their contention was that there was no way for them to assist.

**Now**

Now, Apple is no longer on the "Right Thing" list. They announced about a month ago (August 18)[[Expanded Protections for Children - Apple](https://www.apple.com/child-safety)] that they have created a tool that they can use on YOUR PHONE to scan for stuff like child pornography. It's called NeuralHASH. And I think it is a BAD THING. (In Maryland, possession of Child Pornography is a misdemeanor, punishable with a maximum five year prison sentence for a first offense, and ten years imprisonment for subsequent offenses.)

**Limits of [executive branch] rights**

I used to have really long arguments with my mom about the potential of a police agency to surveil a person, looking for evidence of wrong-doing. Her opinion was "if you don't have anything to hide, you shouldn't have any reason to worry." And I want to believe further that her opinion was that the police SHOULD be able to watch people if they are suspicious. BUT I don't want to attribute that to her, because I do not have a clear memory of her saying those words.

My opinion was (and is) that if the [executive branch] goes through the existing channels (getting a warrant after convincing a judge that  surveillance is necessary), at least someone is aware of their actions, and maybe can monitor the surveillance, limit the surveillance to a narrow focus, or make sure the surveillance is done in a reasonable way (or properly, or in a legal way).

This (reasonable, proper, or legal approaches) is where I think the NeuralHASH app [[CSAM Detection Technical Summary](https://www.apple.com/child-safety/pdf/CSAM_Detection_Technical_Summary.pdf)] is over the line. 

**What is a Hash, how does it work**

Hash algorithms work by analyzing the bits in a file and creating a unique ID number for that file. Unique, because the hash is exceedingly unlikely to randomly generate the same ID for two files that are not identical. I guess, you can call it a fingerprint if that is easier to understand.

If two files are analyzed by the same hash algorithm, and their ID numbers are identical, that means one of the files is an exact copy of the other. That is the nature of digital copying. Each copy is essentially identical to its "parent". 

Then, a group can create a database of every file in a collection, and can then test each file against the reference database to know that the copying process was successful. For example, if someone is sending their music collection to another device, the hash ID of the source and the copy can be compared to know if any kind of corruption took place during the transmission.

**NeuralHASH**

The NeuralHASH algorithm is focused on finding child pornography. And there is a database of file IDs that represent files that are, or contain, child pornography.

Apple claims that the chance of a new file (e.g. a picture of your Aunt Harriet at her 100th birthday) being mistakenly identified as child porn (because their hash numbers just happened to be identical) is 1-in-a-trillion. I'd be tempted to agree with their assertion. If the hash algorithm is sufficiently complex, it would be nearly impossible to MAKE a file have the same ID, let alone have it occur at random.

As with other hashes, the NeuralHASH algorithm converts each photo file it finds into a unique ID number. Once that file's number is created, it is compared against the database of IDs that correspond with files that are known to contain child pornography. In this way, the hash can determine whether there is known child porn on a person's phone or in their iCloud account. 

**Outcomes for Apple**

What happens when neuralHASH finds child porn (in excess of 30 images)? The user's AppleID gets locked (which will stop them using any iOS devices or iCloud services, etc.), and someone can then appeal to Apple to overturn the results.

Yes, Apple has the right to limit who it accepts as its customers. They seem to have decided that folks with child porn are no longer worthy to be customers. That's their right.


**Stipulations**

This technology is certainly good news for people who want to try to do something about trafficking child porn. On its face, that is a worthy endeavor. 

Yet, let's include some due process. Let's wait until someone actually commits a crime, or is plausibly accused of possessing or distributing child porn before wielding the tool. It would certainly seem to make a case a slam-dunk if a person's device and/or iCloud account has child porn images on it, so why get pre-emptive? 


```
NAYSAYERY
Wait just a minute, buddy! These are kids, man... How can you defend people having child porn? I am not defending people having child porn. I am suggesting that the company is overstepping its bounds when it puts software onto your phone that would scan the files on your computer or phone without your approval.
Further, if giving this approval requires me to approve the unrestricted scanning of my files, I will take my business elsewhere. I don't have tolerance for that level of intrusion. UNLESS you GAVE me something in return (e.g. free devices or access to certain services). But that is a different story altogether.
```


**Suspicions**

Apparently, Apple is collecting this information about its users' files for their own purposes? What could those be? If they have this evidence, what is being done with it? Are they handing it over to the [executive branch]? If they are not, is it just to prevent folks from using iOS and iCloud to distribute child pornography? Are there not less intrusive ways to get at the same goal? Such as, a request to share info would trigger such a scan?

My suspicious mind says that if the database of child porn images can be created, it can be augmented to include other types of evidence. Like, let's say a shared spreadsheet that has the locations of future attacks (and the [executive branch] wants to know who has it, or has seen it), or the names of the other folks in a roving band of thugs. Or ANY kind of file that the [executive branch] wants to track.

**Conclusion**

The [executive branch] has tremendous power already to do its job. It's not necessary or needed to provide them additional assistance. Let the [executive branch] get the necessary warrant, and obtain the evidence in a way that satisfies the 4th Amendment, and let's get on with our lives. 

And if your company wants to collect information that would tend to indicate evidence of criminality, acknowledge that you are acting on behalf of the [executive branch]. 

**Epilogue**

It looks like others have published concerns [[Opinion: We built a system like Apple’s to flag child sexual abuse material — and concluded the tech was dangerous](https://www.washingtonpost.com/opinions/2021/08/19/apple-csam-abuse-encryption-security-privacy-dangerous/)]. 

Apple is pulling it back now [[Apple delays plans to roll out CSAM detection in iOS 15](https://techcrunch.com/2021/09/03/apple-csam-detection-delayed/0)]

---
