    import random 
     
    def dice_game(): 
        collected_parts = [] 
       # body_parts = { 
       #     1: "Body", 
       #     2: "Head", 
       #     3: "Antenna", 
       #     4: "Eye", 
       #     5: "Mouth", 
       #     6: "Leg" 
       #} 
        body_count=0 
        eye_count = 0 
        antenna_count = 0  
        leg_count = 0 
        head_count = 0 
        mouth_count = 0 
        print("Starting the game") 
        print("\n")
        print("Rolling Dice.....") 
        print("\n") 
        while len(collected_parts) < 13: 
                roll = random.randint(1, 6) 
                if roll == 1: 
                    print("\n Roll=",1) 
                    if 1 not in collected_parts: 
                        print("\n You got the Body") 
                        collected_parts.append(1) 
                        body_count+=1 
                    else: 
                        print("\n You already got the Body") 
                     
            elif roll == 2 and 1 in collected_parts: 
                print("\n Roll=",2) 
                if 2 not in collected_parts: 
                    print("\n You got the Head") 
                    collected_parts.append(2) 
                    head_count+=1 
                else: 
                    print("\n You already got the Head") 
            elif roll == 3 and 1 in collected_parts and 2 in collected_parts: 
                print("\n Roll=",3) 
                if antenna_count < 2: 
                    print("\n You got an Antenna") 
                    collected_parts.append(3) 
                    antenna_count += 1 
                else: 
                    print("\n You already got enough Antennas") 
 
            elif roll == 4 and 1 in collected_parts and 2 in collected_parts: 
                print("\n Roll=",4) 
                if eye_count < 2: 
                    print("\n You got an Eye") 
                    collected_parts.append(4) 
                    eye_count += 1 
                else: 
                    print("\n You already got enough Eyes") 
 
            elif roll == 5 and 1 in collected_parts and 2 in collected_parts: 
                print("\n Roll=",5) 
                if 5 not in collected_parts: 
                    print("\n You got the Mouth") 
                    collected_parts.append(5) 
                    mouth_count+=1 
                else: 
                    print("\n You already got the Mouth") 
                     
            elif roll == 6 and 1 in collected_parts and 2 in collected_parts: 
                print("\n Roll=",6) 
                if leg_count < 6: 
                    print("\n You got a Leg") 
                    collected_parts.append(6) 
                    leg_count += 1 
                else: 
                    print("\n You already got enough Legs")
    print("\n<-------------------------------->") 
    print("Body:",body_count) 
    print("Head:",head_count) 
    print("Antenna:",antenna_count) 
    print("Eyes:",eye_count) 
    print("Mouth:",mouth_count) 
    print("legs:",leg_count) 
    print("<----------------------------------->") 
    print("You Won") 
    print("Collected_parts= ",len(collected_parts)) 
 
    dice_game()'
