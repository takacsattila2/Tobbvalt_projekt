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
