<<<<<<< HEAD
# morze abc-s fordíto

MORSE_CODE_DICT = { 'A':'.-', 'a':'.-','B':'-...','b':'-...', 
                    'C':'-.-.','c':'-.-.', 'D':'-..', 'd':'-..','E':'.','e':'.', 
                    'F':'..-.','f':'..-.', 'G':'--.','g':'--.', 'H':'....','h':'....', 
                    'I':'..','i':'..', 'J':'.---','j':'.---', 'K':'-.-','k':'-.-', 
                    'L':'.-..','l':'.-..', 'M':'--','m':'--', 'N':'-.','n':'-.', 
                    'O':'---','o':'---', 'P':'.--.', 'p':'.--.','Q':'--.-','q':'--.-', 
                    'R':'.-.','r':'.-.', 'S':'...','s':'...', 'T':'-', 't':'-',
                    'U':'..-','u':'..-', 'V':'...-','v':'...-', 'W':'.--','w':'.--', 
                    'X':'-..-','x':'-..-', 'Y':'-.--','y':'-.--', 'Z':'--..','z':'--..', 
                    '1':'.----', '2':'..---', '3':'...--', 
                    '4':'....-', '5':'.....', '6':'-....', 
                    '7':'--...', '8':'---..', '9':'----.', 
                    '0':'-----', ', ':'--..--', '.':'.-.-.-', 
                    '?':'..--..', '/':'-..-.', '-':'-....-', 
                    '(':'-.--.', ')':'-.--.-'}

def encrypt(message): 
    cipher = '' 
    for letter in message: 
        if letter != ' ': 
            cipher += MORSE_CODE_DICT[letter] + ' '
        else: 
            cipher += ' '
    return cipher 

def decrypt(message): 
    message += ' '
    decipher = '' 
    citext = '' 
    for letter in message: 
        if (letter != ' '): 
            i = 0
            citext += letter 
        else: 
            i += 1
            if i == 2 : 
                decipher += ' '
            else: 
                decipher += list(MORSE_CODE_DICT.keys())[list(MORSE_CODE_DICT 
                .values()).index(citext)] 
                citext = '' 
    return decipher 
	
	encrypt('Szeretem a csokit')
=======
# Többvált Projekt

### Anyagok git használatához:

A következő linken találtok anyagot git használatához. Javaslom mindenkinek, hogy olvassátok el ha lesz rá kis időtök, mert hasznos.
Ez alapvetően nem konkrétan a githubról szól, hanem magáról a git verziókezelésről amit a github is használ. A git parancsokat nem kell ismerni ha github desktopot használunk de a működés és egyes kulcsszavak megértése hasznos lenne.

https://desoft.hu/downloads/git/git_v1.0.pdf
>>>>>>> d6e34b23ef0625ab27d9b004f402c5c782c039a3
