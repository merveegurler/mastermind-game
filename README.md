# mastermind-game

It can be compiled:

    g++ -std=c++11 mastermind_game.cpp -o mastermind
   
Then program can be called like the following:

    ./mastermind -r 6
    
With this call, user is expected to enter a 6 digit number. If user enters a number which has more or less than 6
digits, program will print the following error message and exit.

    E1

If the user enters something but not an integer, program will print the following error:

    E2

If the user enters a valid number program will return the hints in the following format:

    mastermind -r 6 ------> Assume that your program generates secret 130456

    123456 ------> User enters 123456

    4 1 ------> First count is 4, Second count is 1 (separated by a space)

    132456 ------> User enters 132456

    5 0 ------> First count is 5, Second count is 0 (separated by a space)

    130456 ------> User enters 130456

    FOUND 3 ------> User found the number in 3 iterations, program exits. (separated by a space)
  
  
If the user cannot find in 100 iterations, print the following message and exit the program:

    FAILED

Program can also be called like the following:

    mastermind -u 12345

If this happens, program will use 12345 (the given argument) as the secret number. The rest of your code will
not change.

# Error Checking

If there is any error, prints the following and exits:

    E0

Errors in program call include the following:

    • Missing parameters.

    • Wrong parameters.

    • Undefined parameters.

    • Negative value or 0 value following the -r option.

    • Digits of the number followed by -u are not unique.

    
    
