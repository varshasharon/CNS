## EX. NO: 1(A) : IMPLEMENTATION OF CAESAR CIPHER
 

## AIM:

To implement the simple substitution technique named Caesar cipher using C language.

## DESCRIPTION:

To encrypt a message with a Caesar cipher, each letter in the message is changed using a simple rule: shift by three. Each letter is replaced by the letter three letters ahead in the alphabet. A becomes D, B becomes E, and so on. For the last letters, we can think of the
alphabet as a circle and "wrap around". W becomes Z, X becomes A, Y bec mes B, and Z
becomes C. To change a message back, each letter is replaced by the one three before it.

## EXAMPLE:



![image](https://github.com/Hemamanigandan/CNS/assets/149653568/eb9c6c43-8c80-4cdd-b9d4-91705a311c79)


## ALGORITHM:

### STEP-1: Read the plain text from the user.
### STEP-2: Read the key value from the user.
### STEP-3: If the key is positive then encrypt the text by adding the key with each character in the plain text.
### STEP-4: Else subtract the key from the plain text.
### STEP-5: Display the cipher text obtained above.


PROGRAM :-
```
        function encrypt()
        {
            let message = document.getElementById("pt").value;
            let key = parseInt(document.getElementById("key").value);
            let result = "";
            for(let i=0;i<message.length;i++)
            {
                let char = message[i];
                if(char.match(/[a-zA-Z]/))
                {
                    let code = char.charCodeAt(0);
                    let base = (code >= 65 && code <= 90)?65 : 97;
                    let newCode = ((code-base+key)%26) +base;
                    result += String.fromCharCode(newCode); 
                }
                else{
                    result += char;
                }
            }
            document.getElementById("ct").innerText =  result ;
        
        
        }
  ```  


OUTPUT :-
