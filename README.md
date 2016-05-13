# List-Sequences-Assignment-Final

#A-1

def unluckyOne(numlist):
    
    """
    determine if 1 followed by a 3 (unluckyOne) is in the first 2 positions of the list or last 2 positions
    :param numlist: int - list with numbers
    :return: boolean - return True or False if there is an unluckyOne
    """
    # to determine the position of 1 in the given areas of the list and if 3 follows immediately after
    if numlist[0] == 1 and numlist[1] == 3:
        return True
    elif numlist[1] == 1 and numlist[2] == 3:
        return True
    elif numlist[-2] == 1 and numlist[-1] == 3:
        return True
    else:
        return False

#B-3

def after4(numlist):
   
    """
    find the last occurring 4 in a list and print out all numbers after it
    :param numlist: int - list of numbers
    :return: int - returns list of numbers after the last occurring 4
    """
    # to find the location of the last occurring 4 in a list
    for i in range(len(numlist)):
        if numlist[i] == 4:
            location = i
    # prints out the numbers in the list after the last occurring 4
    print numlist[location+1:]

#C-2

def acromatch(wordlist1, wordlist2):

    """
    determine if the acronym of the words in wordlist1 equals to the acronym of wordlist2
    :param wordlist1: str - list of words
    :param wordlist2: str - list of words
    :return: boolean - return True or False if the acronyms are equal
    """
    # set 2 empty strings
    acro1 = ""
    acro2 = ""
    # iterate through the lists and add the first letter of each word to the corresponding empty string
    for i in range(len(wordlist1)):
        acro1 += wordlist1[i][0]
    for i in range(len(wordlist2)):
        acro2 += wordlist2[i][0]
    # comparing the two strings
    if acro1 == acro2:
        print True
    else:
        print False

#D-2

def canVote(birthdate):
    
    """
    determine if a person is eligible to vote in the presidential election on Nov 8,2016,
    they must be at least 18 years of age.
    :param birthdate: str - birthdate (mm/dd/year)
    :return: boolean - returns True or False if person is eligible to vote or not
    """
    # splits the "/" in the string
    date = birthdate.split("/")
    # access the individual strings to compare and convert the strings to integers
    if int(date[2]) < 1998:
        print True
    elif int(date[2]) == 1998:
        if int(date[0]) < 11:
            print True
        elif int(date[0]) == 11:
            if int(date[1]) <= 8:
                print True
            elif int(date[1]) > 8:
                print False
        else:
            print False
