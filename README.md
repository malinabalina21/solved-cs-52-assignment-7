Download Link: https://assignmentchef.com/product/solved-cs-52-assignment-7
<br>
<strong>Background:</strong>The purpose of this assignment is to practice dealing with arrays and array parameters.  To Computer Scientists, C++ is consider not pure because not everything is actually a class or object.  For example, arrays are neither classes nor objects.  As a result, they have their own way of being passed as a parameter and they also do not support the dot-guy (.), so you cannot determine how full they are.  This results in some pain and suffering when coding with arrays.  It is this awareness that I am trying to get across to you in this homework assignment.

<h3><strong>part_a: grader</strong></h3>

The Grader class is keeping track of a set of exam scores.  Scores can be added one at a time thru calls to addScore( … ) or it can add a set of scores thru calls to addScores( … ).  Once scores have been collected, the Grader class can find the best and worst scores it has seen so far thru calls to findBiggest( ) and findSmallest( ).  Both of these methods are read-only operations, so you won’t be able to change or update anything inside the Grader instance object.  Processing arrays lead to lots of loops and that is what will be necessary in these methods.  As for the MAX_SIZE constant, I would recommend you just set it to a very large number (say 100…) and move on.

You will notice also that the class Grader has an integer counter named valuesSeenSoFar.  This counter is meant to tell you how full the array actually is.  Since an array is not a class, you can’t ask the my_Values array any questions.  This counter needs to be maintained (incremented and decremented) by your Grader class code, as driver code fills and empties the array.

Following the class diagrams shown below, implement the Grader class.  Embed your class in a suitable test program that proves your calculations are correct.  You may choose to create any number of additional methods, but you are required to implement all of the public methods shown below.  You are free to ignore the private parts of the class I suggest below.

<table border="1" cellspacing="0" cellpadding="0">

 <tbody>

  <tr valign="TOP">

   <td width="314"><i><strong>Implementation Details</strong></i></td>

   <td width="314"><i><strong>Sample Driver Code</strong></i></td>

  </tr>

  <tr valign="TOP">

   <td width="314"><strong>Grader</strong></td>

   <td rowspan="3" width="314">Grader g;double d[5]= {99,70,85,93,84};double e[4]= {100,81,80,91};g.addScore( 75 );g.addScore( 82);g.addScores( d, 5 );cout &lt;&lt; “Best Score = ” &lt;&lt; g.findBiggest( ) &lt;&lt; endl;/// should give value 99cout &lt;&lt; “Worst Score = ” &lt;&lt; g.findSmallest( ) &lt;&lt; endl;/// should give value 70g.clear( );g.addScore( 71 );g.addScore( 74 );g.addScores( e, 4 );cout &lt;&lt; “Best Score = ” &lt;&lt; g.findBiggest( ) &lt;&lt; endl;/// should give value 100cout &lt;&lt; “Worst Score = ” &lt;&lt; g.findSmallest( ) &lt;&lt; endl;/// should give value 71</td>

  </tr>

  <tr>

   <td valign="TOP" width="314">Grader( );void addScore( double score );void addScores( double scores[],double size );void clear();double findBiggest( ) const;double findSmallest( ) const;</td>

  </tr>

  <tr>

   <td valign="TOP" width="314">int my_Values[ MAXSIZE ];int my_valuesSeenSoFar;</td>

  </tr>

  <tr valign="TOP">

   <td width="314"> </td>

   <td width="314"><i><strong>Sample Output</strong></i></td>

  </tr>

  <tr valign="TOP">

   <td width="314"> </td>

   <td width="314">Best Score = 99Worst Score = 70Best Score = 100Worst Score = 71</td>

  </tr>

 </tbody>

</table>

<h3><strong>Overall</strong></h3>

<ul>

 <li>Your submission should follow this organization:

  <ul>

   <li>part_a

    <ul>

     <li>main.cpp</li>

     <li>grader.h</li>

     <li>grader.cpp</li>

    </ul></li>

  </ul></li>

</ul>