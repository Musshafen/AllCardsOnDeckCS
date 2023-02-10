# AllCardsOnDeckCS

PEDAC

Problem

Create a new deck of cards which will be a list of 52 strings where the strings are similiar to "Ace of Clubs", "2 of Clubs", ... , "Ace of Diamonds", ... -- Then when we have a list of cards we will shuffle them with the Fisher Yates. Then we will show the 0th index of the list and the 1st index of the list to show the first two cards.

Example

Ace of Clubs
2 of Clubs
3 of Clubs
...
ALL 52 CARDS

Data

'string'
'List'
looping?

Algorithm

-Make a new list of strings named 'deck'
-Initialize the list of strings with 52 explicity stated cards from our Example section
-Shuffle them with Fisher Yates
numberOfCards = length of our deck

for rightIndex from numberOfCards - 1 down to 1 do:
leftIndex = random integer that is greater than or equal to 0 and LESS than rightIndex. See the
section "How do we get a random integer"

    Now swap the values at rightIndex and leftIndex by doing this:
      leftCard = the value from deck [leftIndex]
      rightCard = the value from deck [rightIndex]
      deck[rightIndex] = leftCard
      deck[leftIndex] = rightCard

-first card = [0]
-second card = [1]
-print first and second card

Algorithm

-Make a list of the 4 suits and call this list 'suits'
-Make a list of the 13 ranks and call this list 'ranks'
-Make a new list of strings named 'deck'
-Make a loop that goes through the list 'suits'
-Make a loop that goes through the list 'ranks'
-for each rank, make a new string of the form $"{rank} of ${suit}"
-add the newly formed string to the end of the deck list
-Same as Algo 1

                     // foreach (var suit in suits)
            {

                //foreach (var rank in ranks)
                {
                   // var card = $"{rank} of {suit}";

                  //  deck.Add(card);

                }
            }


            var numberOfCards = deck.Count;


            for (var rightIndex = numberOfCards - 1; rightIndex >= 1; rightIndex--)
            {

                var randomNumberGenerator = new Random();
                var leftIndex = randomNumberGenerator.Next(rightIndex);



                var leftCard = deck[leftIndex];

                var rightCard = deck[rightIndex];

                deck[rightIndex] = leftCard;

                deck[leftIndex] = rightCard;

            }

            Console.WriteLine("Done shuffling");


            var firstCard = deck[0];

            var secondCard = deck[1];

            Console.WriteLine($"The first card is {firstCard} and the second card is {secondCard}");
