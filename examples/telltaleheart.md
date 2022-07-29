# Example: *Tell-tale Heart*

```ink
This project is designed to explore possible variations on Edgar Allan Poe's short story, "The Tell-Tale Heart." The player will be allowed to follow the original story, or can instead create their own alternate version.

+[Go to the game]
    -> Start

== Start
"True! --nervous --very, very dreadfully nervous I had been and am; but why will you say that I am mad? The disease had sharpened my senses --not destroyed --not dulled them. Above all was the sense of hearing acute. I heard all things in the heaven and in the earth. I heard many things in hell. How, then, am I mad? Hearken! and observe how healthily --how calmly I can tell you the whole story..." (Poe)

While I will be happy to relate my tale to you, you might have questions, my dear friend! Many have wondered, for example, about who I am, and what relationship I have to the old man in the story I am about to tell you...
-> Relationship

== Relationship
*[Were you employed by the old man?]
    -> Relationship.Employee
*[Was he your father?]
    -> Relationship.Father
*[Did you have a relationship with him?]
    -> Relationship.Lover
*[Actually, I'd rather it be a mystery!]
    -> Relationship.Mystery

= Employee
Why yes! He was my employer! I lived with him and working with him for many years.
-> Motive

= Father
Why yes! He was my father! I was living with him to care for him in his old age.
-> Motive

= Lover
Yes! We were lovers! We had been together for many years.
-> Motive

= Mystery
Yes, such details are not really interesting, are they?
-> Motive

== Motive
Perhaps you are interested in knowing why I committed such a deed?

*[Did you kill him for his gold?]
    -> Motive.Gold
*[Maybe you were seeking revenge...]
    -> Motive.Revenge
*[Was it a crime of passion?]
    -> Motive.Passion
*[I have heard it was because of his eye!]
    -> Motive.Eye

= Gold
Yes, that was it! The old man’s gold always called to me, until one day my greed became overwhelming.
-> Weapon

= Revenge
Why yes! I could no longer bear his insults and injuries, and my enmity grew toward the old man until one day I determined to take my vengeance.
-> Weapon

= Passion
Passion, yes! I both loved and hated the old man. On some days he was a wonderful person, but on others his actions were terrible, and my emotions were confused until one day I was drove to murder.
-> Weapon

= Eye
Yes! That is it! It was because of the old man's evil, blue, vexing eye! How it endlessly haunted me!
-> Weapon

I heard you killed him quickly... what did you use to do it?
-> Weapon

== Weapon
And the murder itself? I am sure you have heard details about the crime...
*[I heard you used a knife.]
    -> Weapon.Knife
*[They say you poisoned him.]
    ->Weapon.Poison
*[You strangled him, didn't you?]
    -> Weapon.Strangled
*[Some say you suffocated him under the bed!]
    -> Weapon.Suffocated

= Knife
A knife, yes! I used the blade to carve out his eye, then, slashed him through the throat!
-> Finale

= Poison
Yes, poison in his cup... My employer always helped himself to a nightcap before bed...
-> Finale

= Strangled
With my bare hands, yes... Doing the deed with my bare hands satisfied my emotions...
-> Finale

= Suffocated
Yes! A most cunning method, I should think. No weapon to find, no poison on his lips, and no signs of choking upon his neck. Only the truly mad would choose such awful means!
-> Finale

== Finale
Then I disposed of the body, of course; I dismembered the old man, then concealed his remains beneath the floorboards of my house.
*[Is that when you made your escape?]
    -> Escape
*[Is that when the police arrived?]
    -> Police

==Escape
{~Escape, yes... And of course, because there was no sign of the deed, and it took them hours to find the body... giving me enough time for you, my good friend, to come to my aid and ensure that I will never be found!->Escape.Success|Escape... yes, I attempted to escape, and with the aid of you, my good friend, I made it far... but they caught me just as I was boarding a ship at the port.->Escape.Failed}
= Success
    *[Go to the ending.]
        -> Ending
= Failed
    *[Go to the ending.]
        ->Ending

== Police
Why yes... two police officers knocked at the door a few hours later, claiming that a neighbor had heard a scream in the night...
*[Is that when you attacked them?]
    -> Attack
*[And you lead them to the room where the corpse was hidden?]
    -> Ending

== Attack
Yes! I let them in, and then I fell upon them! I assaulted one viciously, knocking him to the floor! 

{Weapon.Knife: I then pulled my blade, turning toward the other...->Attack.Knife|However, the other clubbed me about the head, knocking me unconscious.->Attack.Failed}->END

= Knife
I set upon him viciously with my knife, stabbing him over and over until he fell. Realizing that my murder of the two officers would arouse further suspicions, I made plans for my escape... and luckily you, my good friend, were there to help me get away!
*[Go to the ending.]
    -> Ending

= Failed
My assault aroused further suspicious, and a search of the house was effected, soon revealing the corpse of the old man. I was arrested for his murder, but at least they are allowing me to see you, my good friend, one last time before I am executed for my crimes!
    *[Go to the ending.]
        -> Ending.Final

== Ending
Yes... in my arrogance, I believed that no sign of my deed could be detected... But I did not account for the heart! That horrible, pulsing, beating heart, sounding in my ears even though the man was long dead! I could take it no longer, and I tore up the floorboards myself, revealing his corpse. I was arrested, of course... but at least they are allowing me to see you, my good friend, one last time before I am executed for my crimes!

*[Go to the ending.]
    -> Ending.Final

= Final
You decided that the narrator{Relationship.Employee: was the old man's employee.}{Relationship.Father: was the old man's child.}{Relationship.Lover: was the old man's lover.}{Relationship.Mystery:'s relationship to the old man was ambiguous.} 

You decided that the motive for the murder was {Motive.Gold:gold}{Motive.Revenge:revenge}{Motive.Passion:passion.}{Motive.Eye:the eye}.

You decided that the murder method was {Weapon.Knife:a knife}{Weapon.Poison:poison}{Weapon.Strangled:strangulation}{Weapon.Suffocated:suffocation}.

You decided that the story ended with {Escape.Success:the narrator's successful escape attempt.}{Escape.Failed:the narrator's failed escape attempt.}{Attack.Knife:the narrator murdering the police and escaping.}{Attack.Failed:the narrator attacking the police unsuccessfully.}
-> END
```
