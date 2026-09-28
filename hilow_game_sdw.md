START

OUTPUT "Welcome to the higher/lower game!"
OUTPUT "Enter the lower bound:"
INPUT lowerBound
OUTPUT "Enter the upper bound:"
INPUT upperBound
WHILE lowerBound >= upperBound
    OUTPUT "The lower bound must be less than the upper bound."
    OUTPUT "Enter the lower bound:"
    INPUT lowerBound
    OUTPUT "Enter the upper bound:"
    INPUT upperBound
END WHILE
LET randomNumber = RANDOM NUMBER BETWEEN lowerBound AND upperBound
OUTPUT "Great, now guess a number between lowerBound and upperBound:"
INPUT guess
WHILE guess != randomNumber
    IF guess < lowerBound OR guess > upperBound THEN
        OUTPUT "Your guess must be between the lower bound and upper bound."
    ELSE IF guess < randomNumber THEN
        OUTPUT "Nope, too low."
    ELSE
        OUTPUT "Nope, too high."
    END IF
    OUTPUT "Guess another number:"
    INPUT guess
END WHILE
OUTPUT "You got it!"


