"""
Smite is a MOBA, where each player gets to select a god from different cultures' mythologies, and fight other gods using a unique set of abilities.
In order to become more powerful, gods need to gain gold and experience, which they can accomplish by killing camps in the jungle.
Experience allows a god to level up, and each time a god levels up, they can level up one of their abilities.
Gold allows a god to by items that will increase stats such as physical or magical power, which will make them deal more damage.
"""

"""
Jungle camps, often referred to as buffs, will respawn a certain amount of time after they are killed. It is important to know when they respawn, as you can increase your efficiency in
gaining gold and experience by being on time for the buffs. You can also steal the enemy team's buffs if you know when they respawn, which is extremely valuable, as you will steal their
gold and experience.
The function bufftimer() will allow the user to input the game time, and any buff camp in the game, and it will return the time that the buff will respawn.
"""
def bufftimer():
    initialmins = int(input("Enter the time in minutes"))
    initialseconds = int(input("Enter the time in seconds"))
    buffs = ["speed","s","yellow","y","p","purple","b","blue","r","red","green","g","firegiant","fire giant","fg","goldfury","gold fury","gf","pyromancer","pyro","scorpion","scorp","mids","midcamps","mid camps"]
    time = 0
    bufftype = input("Enter which buff you would like the timer for")
    bufftype.lower()
    if bufftype not in buffs:
        print(bufftype,"is not a valid buff, please try again")
        bufftimer()
    elif bufftype == "speed" or bufftype == "s" or bufftype == "yellow" or bufftype == "y" or bufftype == "p" or bufftype == "purple" or bufftype == "b" or bufftype == "blue" or bufftype == "r" or bufftype == "red" or bufftype == "green" or bufftype == "g":
        totalmins = initialmins + 2
        totalseconds = initialseconds
    elif bufftype == "firegiant" or bufftype == "fire giant" or bufftype == "fg" or bufftype == "goldfury" or bufftype == "gold fury" or bufftype == "gf" or bufftype == "pyromancer" or bufftype == "pyro":
        totalmins = initialmins + 5
        totalseconds = initialseconds
    elif bufftype == "scorpion" or bufftype == "scorp":
        totalmins = initialmins + 4
        totalseconds = intialseconds
    elif bufftype == "mids" or bufftype == "midcamps" or bufftype == "mid camps":
        totalmins = initialmins + 2
        totalseconds = (initialseconds + 30)
        if totalseconds >= 60:
            totalseconds = totalseconds % 60
            totalmins += 1
            totalseconds = str(totalseconds)
            if len(totalseconds) == 1 and initialseconds == 0:
                totalseconds = totalseconds + "0"
            if len(totalseconds) == 1 and initialseconds != 0:
                totalseconds = "0" + totalseconds
                
    print(bufftype, "will respawn at", totalmins,":",totalseconds)
#bufftimer()

"""
Anubis, the Egyptian God of the Dead, is one of the 100+ gods that can be played.
Anubis has four abilities; Three of his abilities deal damage.
The damage that each of Anubis's abilities deals is based on an equation that has two variables: the level of the ability, and magical power.
Each ability has a maximum level of 5, and deals 'base' damage, which is derived from ability level, along with 'scaling' damage, which is derived from magical power.
The function anubis() will calculate the amount of damage that anubis will theoretically deal if he has perfect accuracy,
given the amount of magical power that he has, along with the level of his abilities.
"""
def anubis():
    magicalpower = int(input("Enter the amount of magical power Anubis has"))

    ability1level = int(input("What level is Anubis's first ability?"))
    if ability1level == 1:
        ability1damage = (35 + round(0.4 * magicalpower)) * 6
    elif ability1level == 2:
        ability1damage = (50 + round(0.4 * magicalpower)) * 6
    elif ability1level == 3:
        ability1damage = (65 + round(0.4 * magicalpower)) * 6
    elif ability1level == 4:
        ability1damage = (80 + round(0.4 * magicalpower)) * 6
    elif ability1level == 5:
        ability1damage = (95 + round(0.4 * magicalpower)) * 6
    print("Anubis's first ability, plague of locusts, will deal",ability1damage, "damage")

    ability3level = int(input("What level is Anubis's third ability?"))
    if ability3level == 1:
        ability3damage = (25 + round(0.35 * magicalpower)) * 4
    elif ability3level == 2:
        ability3damage = (40 + round(0.35 * magicalpower)) * 4
    elif ability3level == 3:
        ability3damage = (55 + round(0.35 * magicalpower)) * 4
    elif ability3level == 4:
        ability3damage = (70 + round(0.35 * magicalpower)) * 4
    elif ability3level == 5:
        ability3damage = (85 + round(0.35 * magicalpower)) * 4
    print("Anubis's third ability, grasping hands, will deal",ability3damage,"damage")

    ability4level = int(input("What level is Anubis's fourth ability?"))
    if ability4level == 1:
        ability4damage = (23 + round(0.15 * magicalpower)) * 30
    elif ability4level == 2:
        ability4damage = (28 + round(0.15 * magicalpower)) * 30
    elif ability4level == 3:
        ability4damage = (33 + round(0.15 * magicalpower)) * 30
    elif ability4level == 4:
        ability4damage = (38 + round(0.15 * magicalpower)) * 30
    elif ability4level == 5:
        ability4damage = (43 + round(0.15 * magicalpower)) * 30
    print("Anubis's fourth ability, death gaze, will deal",ability4damage,"damage")

    totaldamage = ability1damage + ability3damage + ability4damage
    print("Anubis will deal",totaldamage,"damage in total (ignoring protections and mitigations)")
    return totaldamage
#anubis()

"""
Medusa, a prominent figure in Greek mythology, is another god in SMITE.
Medusa has some unique interactions with her abilities that make her damage calculations different from Anubis.
Additionally, Medusa has another unique mechanic with her fourth ability, petrify. Medusa is known to turn people to stone if they look into her eyes.
Medusa's fourth ability will deal full damage and turn the enemy into stone if they are facing her, and it will deal 75% of the damage if they are not facing her.
The function medusa() will calculate the amount of damage that Medusa will theoretically deal if she has perfect accuracy, given her physical power, the level of her abilities,
as well as a unique condition (whether the enemy is looking at her).
"""
def medusa():
    physicalpower = int(input("Enter the amount of physical power Medusa has"))
        
    ability1level = int(input("What level is Medusa's first ability?"))
    if ability1level == 1:
        ability1damage = round(4 * (30 + (0.3 * physicalpower)))
    elif ability1level == 2:
        ability1damage = round(4 * (45 + (0.3 * physicalpower)))
    elif ability1level == 3:
        ability1damage = round(4 * (60 + (0.3 * physicalpower)))
    elif ability1level == 4:
        ability1damage = round(4 * (75 + (0.3 * physicalpower)))
    elif ability1level == 5:
        ability1damage = round(4 * (90 + (0.3 * physicalpower)))
    print("Medusa's first ability, viper shot, will deal",ability1damage, "damage")

    ability2level = int(input("What level is Medusa's second ability?"))
    if ability2level == 1:
        ability2damage = 90 + round(0.8 * physicalpower)
    elif ability2level == 2:
        ability2damage = 140 + round(0.8 * physicalpower)
    elif ability2level == 3:
        ability2damage = 190 + round(0.8 * physicalpower)
    elif ability2level == 4:
        ability2damage = 240 + round(0.8 * physicalpower)
    elif ability2level == 5:
        ability2damage = 290 + round(0.8 * physicalpower)
    print("Medusa's second ability, acid spray, will deal",ability2damage, "damage")

    ability3level = int(input("What level is Medusa's third ability?"))
    if ability3level == 1:
        ability3damage = 80 + round(0.7 * physicalpower)
    elif ability3level == 2:
        ability3damage = 130 + round(0.7 * physicalpower)
    elif ability3level == 3:
        ability3damage = 180 + round(0.7 * physicalpower)
    elif ability3level == 4:
        ability3damage = 230 + round(0.7 * physicalpower)
    elif ability3level == 5:
        ability3damage = 280 + round(0.7 * physicalpower)
    print("Medusa's third ability, lacerate, will deal",ability3damage,"damage")

    ability4level = int(input("What level is Medusa's fourth ability?"))
    direction = input("Is the target facing Medusa?")
    if direction == "Y" or direction == "YES" or direction == "y" or direction == "yes":
        if ability4level == 1:
            ability4damage = 300 + physicalpower
        elif ability4level == 2:
            ability4damage = 400 + physicalpower
        elif ability4level == 3:
            ability4damage = 500 + physicalpower
        elif ability4level == 4:
            ability4damage = 600 + physicalpower
        elif ability4level == 5:
            ability4damage = 700 + physicalpower
        ability4damage = int(ability4damage)
    else:
        if ability4level == 1:
            ability4damage = (300 + physicalpower) * .75
        elif ability4level == 2:
            ability4damage = (400 + physicalpower) * .75
        elif ability4level == 3:
            ability4damage = (500 + physicalpower) * .75
        elif ability4level == 4:
            ability4damage = (600 + physicalpower) * .75
        elif ability4level == 5:
            ability4damage = (700 + physicalpower) * .75
        ability4damage = int(ability4damage)
    print("Medusa's fourth ability, petrify, will deal",ability4damage,"damage")

    totaldamage = ability1damage + ability2damage + ability3damage + ability4damage
    print("Medusa will deal",totaldamage,"damage in total (ignoring protections and mitigations)")
    return totaldamage
#medusa()

"""
In SMITE, damage calculations are not only limited to physical and magical power. There are many variables at play, including percent penetration, flat penetration, protections, and mitigations.
The amount of damage that an enemy takes is dependent on algebraic equations that consider each of these variables when they are appropriate.
Therefore, the theoretical damage that an ability will do based purely on power is not necessarily equivalent to how much damage it will do in practice.
"""
def damageTaken():
    totaldamage = anubis()

    magicalpercentpen = float(input("How much percent penetration does Anubis have?"))
    magicalflatpen = float(input("How much flat penetration does Anubis have?"))
    magicalprotections = float(input("How much magical protection does the target have?"))
    initialmitigation = float(input("How much percent mitigation does the target have?"))
    magicalpercentpen = magicalpercentpen / 100
    mitigation = initialmitigation / 100

    penmagicalprotections = (magicalprotections * (1 - magicalpercentpen)) - magicalflatpen
    
    damagetaken = (1 - mitigation) * (totaldamage * 100) // (100 + penmagicalprotections)
    damagetaken = int(damagetaken)
    magicalprotections = int(magicalprotections)
    mitigation = int(mitigation)
    print("Anubis will deal",damagetaken,"damage to a target with",magicalprotections,"magical protections and",(initialmitigation),"% mitigation")
    return damagetaken
#damageTaken()


    
        
