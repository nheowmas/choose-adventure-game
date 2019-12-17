# choose-adventure-game
A high school project that allows the user to create their own story based on inputs. Each input prints out a given message.

/*Giang_Felix.ch
my choose your own adventure game*/
//declare
string_t choosename;
string_t randname2[]={"Mason","Jabon","Jacko","Sky","Lay","Kyle","Matt","Jake","Edward","Elijah","Ibrahim","Keisun","Sowon","Ahri"};
string_t randname1[]={"Mason","Jabon","Jacko","Sky","Lay","Kyle","Matt","Jake","Edward","Elijah","Ibrahim","Keisun","Sowon","Ahri"};
int a=randint(0,11);
int b=randint(0,11);
string_t ab;
string_t bc;
string_t s;
string_t op;
int y;
int n, d;
string_t cop;
string_t cheatr;

//functions
//cheat
void cheat(){
    printf("Would you like to see a roadmap of the game? (Yes, No)\n");
    scanf("%s", &cheatr);
    if(cheatr=="Yes"){
        printf("                                    Introduction                        \n");
        printf("Option 1(Help others)           Option 2(Don't help)                    Option 3(Maybe help)\n");
        printf("End 1 | End 2 | End 3           End 4 | End 5 | End 6                   End 7 | End 8 | End 9\n");
    }else{
        printf("Alrighty. We'll continue.\n");
    }
}
//name
void name1(){
    if(choosename=="1"){
        sleep(3);
        printf("Your main characters are %s and %s.\n", randname1[a], randname2[b]);
    }
}
void name2(){
    if(choosename=="0"){
        printf("Please enter two of your own names.\n");
        scanf("%s%s", &ab, &bc);
        sleep(3);
        printf("Your main characters are %s and %s.\n", ab, bc);
    }
}
void guesscheck(){
    while(choosename!="0" && choosename!="1") {
        printf("Error 404: Page Not Found | Please choose 1 to generate names or 0 to choose them.\n");
        scanf("%s", &choosename);
    }
    if(choosename=="1"){
        name1();
        }
    if(choosename=="0"){
        name2();
    }
}
//intro
void introq(){
    printf("You are on a train from Seoul to Busan.\n");
    printf("The view is nice as you eat your lunch.\n");
    printf("You broke a chopstick, but it's okay. %s has an extra pair for your pleasure.\n", randname1[a]);
    sleep(3);
    printf("***CRASH***\n");
    sleep(1);
    printf("Wha-What was that!? The line of cars have come off the track and flipped over, killing %s and %s.\n", randname1[a], randname2[b]);
    sleep(5);
    printf("Do you try to help the others? (Yes, No, Maybe)\n");    
    scanf("%s", &s);
    while(s!="Yes" && s!="No" && s!="Maybe"){
        printf("You failed the game. Please choose Yes, No, or Maybe.\n");
        printf("You are on a train from Seoul to Busan.\n");
        printf("The view is nice as you eat your lunch.\n");
        printf("You broke a chopstick, but it's okay. %s has an extra pair for your pleasure.\n", randname1[a]);
        sleep(3);
        printf("***CRASH***\n");
        sleep(1);
        printf("Wha-What was that!? The line of cars have come off the track and flipped over, killing %s and %s.\n", randname1[a], randname2[b]);
        sleep(5);
        printf("Do you try to help the others? (Yes, No, Maybe)\n");
        scanf("%s", &s);
    }
}
//option 1
void yes(){
    if(s=="Yes"){
        sleep(3);
        printf("Way to not be selfish and save yourself.\n");
        printf("Unfortunately, everyone made it out safe.\n");
        printf("Fortunately, you were not able to make it out.\n");
        printf("Your family gets fame by the government for your heroics.\n");
        printf("Your body gets placed in a viewing area for the public.\n");
    }
}
//option 2
void no(){
    if(s=="No"){
        sleep(3);
        printf("You have no heart and decided to keep yourself alive and survive with a few other people.\n");
        printf("You're running low on food so you need to care for each other.\n");
        printf("You need to work quickly.\n");
        printf("Your group is sitting with very little supplies and need time before the next train or air transport pass the area.\n");
        sleep(3);
        printf("Do you equally split rations with everyone? (Yes, No, Maybe)\n");
        scanf("%s", &op);
    
    //end 1
        if(op=="Yes"){
            sleep(3);
            printf("You have died of hunger as others will continue their life in being saved.\n");
            printf("The government pays deeds to your family and lets them receive a big house that you have been saving money for.\n");
            printf("You are buried in respect.\n");
            printf("Turns out you were buried alive as you survived the famine.\n");
            printf("Now you and your family live happily after ever.\n");
        }
        //end 2
        if(op=="No"){
            y=randint(1,30);
            sleep(3);
            printf("Half of your group survive and will make it all the way back to Seoul.\n");
            printf("Your family has been brutally blugeoned to death by James Charles.\n");
            printf("He is the person that unhinged the tracks to throw off the train and is continuing to go on a murder spree.\n");
            sleep(5);
            printf("%d years later...\n", y); //random number
            sleep(3);
            printf("The police never caught him and he is in hiding somewhere in the country of Wakanda.\n");
        }
        //end 3
        if(op=="Maybe"){
            sleep(3);
            n=randint(1,20);
            d=randint(1,20);
            printf("Some people died from what was left. It is not given whether or not you will survive afterwards. It is certain that you will go down as a legend.\n");
            printf("About %d/%d of your pack died because you gave food to people who needed it and the others kept wasting food.\n", n, d); //random number
            printf("You are rescued and receive 1000000 Won in return for your good deeds.\n");
        }
        while(op!="Yes" && op!="No" && op!="Maybe"){
            printf("You failed the game. Please choose Yes, No, or Maybe.\n");
            //scan
            scanf("%s", &op);
            if(s=="No"){
                sleep(3);
                printf("You have no heart and decided to keep yourself alive and survive with a few other people.\n");
                printf("You're running low on food so you need to care for each other.\n");
                printf("You need to work quickly.\n");
                printf("Your group is sitting with very little supplies and need time before the next train or air transport pass the area.\n");
                sleep(3);
                printf("Do you equally split rations with everyone? (Yes, No, Maybe)\n");
                scanf("%s", &op);
            }
    //end 1
            if(op=="Yes"){
                sleep(3);
                printf("You have died of hunger as others will continue their life in being saved.\n");
                printf("The government pays deeds to your family and lets them receive a big house that you have been saving money for.\n");
                printf("You are buried in respect.\n");
                printf("Turns out you were buried alive as you survived the famine.\n");
                printf("Now you and your family live happily after ever.\n");
            }
            //end 2
            if(op=="No"){
                y=randint(1,30);
                sleep(3);
                printf("Half of your group survive and will make it all the way back to Seoul.\n");
                printf("Your family has been brutally blugeoned to death by James Charles.\n");
                printf("He is the person that unhinged the tracks to throw off the train and is continuing to go on a murder spree.\n");
                sleep(5);
                printf("%d years later...\n", y); //random number
                sleep(3);
                printf("The police never caught him and he is in hiding somewhere in the country of Wakanda.\n");
            }
            //end 3
            if(op=="Maybe"){
                sleep(3);
                n=randint(1,20);
                d=randint(1,20);
                printf("Some people died from what was left. It is not given whether or not you will survive afterwards. It is certain that you will go down as a legend.\n");
                printf("About %d/%d of your pack died because you gave food to people who needed it and the others kept wasting food.\n", n, d); //random number
                printf("You are rescued and receive 1000000 Won in return for your good deeds.\n");
            }
        }
    }
}
//option 3
void maybe(){
    if(s=="Maybe"){
        sleep(3);
        printf("Everyone that rode the train has died due to your indecision and you only survive.\n");
        printf("You have to do anything to avoid legal trouble.\n");
        printf("There are plenty of trees around.\n");
        printf("Your briefly study your surroundings.\n");
        printf("Your only choice now is to hide. Are you going to do so? (Yes, No, Maybe)\n");
        sleep(3);
        scanf("%s", &cop);
    
    //end 1
        if (cop=="Yes"){
            sleep(3);
            printf("You escape back to the city.\n");
            printf("The police never found you and your family is delighted to see you.\n");
            printf("You now take on the new moniker of Joe Smith.\n");
            printf("You get your old job as an accountant and they ask you why you look like a fugitive.\n");
            printf("Your financial problems are solved.\n");
        }
        //end 2
        if(cop=="No"){
            sleep(3);
            printf("The police arrest you for the murder of thousands of Koreans.\n");
            printf("You get thrown in the cell for life and will no longer see your family.\n");
            printf("You don't know what to say. You believe you are wrongfully arrested.\n");
            printf("That's how mafia works!\n");
        }
        //end 3
        if(cop=="Maybe"){
            sleep(3);
            printf("You decide that it wasn't your fault for all the deaths and leave the scene.\n");
            printf("A forensics scientist traced back the DNA to you and you were arrested.\n");
            printf("You head to court and are tried. The judge is biased against you.\n");
            printf("You plead innocent and are released since you did nothing wrong as James James had tried to set you up in the beginning.\n");
        }
        while(cop!="Yes" && cop!="No" && cop!="Maybe"){
            printf("You failed the game. Please choose Yes, No, or Maybe.\n");
            scanf("%s", &cop);
            if(s=="Maybe"){
            sleep(3);
            printf("Everyone that rode the train has died due to your indecision and you only survive.\n");
            printf("You have to do anything to avoid legal trouble.\n");
            printf("There are plenty of trees around.\n");
            printf("Your briefly study your surroundings.\n");
            printf("Your only choice now is to hide. Are you going to do so? (Yes, No, Maybe)\n");
            sleep(3);
            scanf("%s", &cop);
        }
        //end 1
            if (cop=="Yes"){
                sleep(3);
                printf("You escape back to the city.\n");
                printf("The police never found you and your family is delighted to see you.\n");
                printf("You now take on the new moniker of Joe Smith.\n");
                printf("You get your old job as an accountant and they ask you why you look like a fugitive.\n");
                printf("Your financial problems are solved.\n");
            }
            //end 2
            if(cop=="No"){
                sleep(3);
                printf("The police arrest you for the murder of thousands of Koreans.\n");
                printf("You get thrown in the cell for life and will no longer see your family.\n");
                printf("You don't know what to say. You believe you are wrongfully arrested.\n");
                printf("That's how mafia works!\n");
            }
            //end 3
            if(cop=="Maybe"){
                sleep(3);
                printf("You decide that it wasn't your fault for all the deaths and leave the scene.\n");
                printf("A forensics scientist traced back the DNA to you and you were arrested.\n");
                printf("You head to court and are tried. The judge is biased against you.\n");
                printf("You plead innocent and are released since you did nothing wrong as James James had tried to set you up in the beginning.\n");
            }
        }
    }
}
//end
void endgame(){
    sleep(1); printf("G "); sleep(1); printf("A ");sleep(1); printf("M "); sleep(1); printf("E "); sleep(1); printf("O "); sleep(1); printf("V "); sleep(1); printf("E "); sleep(1); printf("R\n"); 
}



int main(){
//optional cheat
    cheat();
//intro
    printf("Hello! Welcome to Partnership of POP/STARS.\nPress 1 to randomly generate two names or type 0 for your own names.\n");
    scanf("%s", &choosename);
//names
    guesscheck();
//starting question
    introq();
//option 1
    yes();
//option 2
    no();
//option 3
    maybe();
//very end
    sleep(3);
    printf("I just wasted so much time in your life that %s and %s will never forgive you.\n", randname1[a], randname2[b]);
    endgame();
//you
    printf("This is you.\n");
    printf(" /\\_/\\n");
    printf("(>'.'<)\n");
    printf("(U   U)\n");
    printf("('')__('')\n");
}
