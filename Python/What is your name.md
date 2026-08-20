##ask user for first and last name then remove whitespace from str and capitalize first letter of each word

fname = input ("What's your full name? ").strip().title()
  
##split user's name into first and last

first, last = fname.split(" ")

##check for numbers if its a name then print name if numbers are present print "Hmm what an interesting name.."

if fname.replace(" ", "").isalpha():

    ##say hello to user

    print (f"Hello, {fname}.")

else:

    ##say interesting name

    print (f"{fname}? Hmmmm what an interesting name.")

  

##bid user fairwell using first name only

print (f"{first}, it has been a pleasure meeting you! I have to go tata for now!")


Updating program
--------------------------------

So this program runs into the problem of what if the person only has 1 name or more than 2. What I'm going to do is add the input to a list and then call the name back is (o) and (-1)

What's your name v2
------------------------------------

##ask user for first and last name then remove whitespace from str and capitalize first letter of each word

fname = input ("What's your full name? ").strip().title()

##check for numbers if its a name then print name if numbers are present print "Hmm what an interesting name.."

if fname.replace(" ", "").isalpha():

    ##split names into list

    names = fname.split()

    ##separate names into first and last

    first = names[0]

    last = names[-1]

  

    print(f"Hello, {fname}! That's a sick name")

  

else:

    print(f"{fname}? What an interesting name.")

  

print(f"Well, {first} {last} I've got to head out. It's been a pleasure")

[[scripts]]