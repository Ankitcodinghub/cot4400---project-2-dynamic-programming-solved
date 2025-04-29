# cot4400---project-2-dynamic-programming-solved
**TO GET THIS SOLUTION VISIT:** [COT4400 – Project 2: Dynamic programming Solved](https://www.ankitcodinghub.com/product/cot4400-project-2-dynamic-programming-solved/)


---

📩 **If you need this solution or have special requests:** **Email:** ankitcoding@gmail.com  
📱 **WhatsApp:** +1 419 877 7882  
📄 **Get a quote instantly using this form:** [Ask Homework Questions](https://www.ankitcodinghub.com/services/ask-homework-questions/)

*We deliver fast, professional, and affordable academic help.*

---

<h2>Description</h2>



<div class="kk-star-ratings kksr-auto kksr-align-center kksr-valign-top" data-payload="{&quot;align&quot;:&quot;center&quot;,&quot;id&quot;:&quot;111062&quot;,&quot;slug&quot;:&quot;default&quot;,&quot;valign&quot;:&quot;top&quot;,&quot;ignore&quot;:&quot;&quot;,&quot;reference&quot;:&quot;auto&quot;,&quot;class&quot;:&quot;&quot;,&quot;count&quot;:&quot;1&quot;,&quot;legendonly&quot;:&quot;&quot;,&quot;readonly&quot;:&quot;&quot;,&quot;score&quot;:&quot;5&quot;,&quot;starsonly&quot;:&quot;&quot;,&quot;best&quot;:&quot;5&quot;,&quot;gap&quot;:&quot;4&quot;,&quot;greet&quot;:&quot;Rate this product&quot;,&quot;legend&quot;:&quot;5\/5 - (1 vote)&quot;,&quot;size&quot;:&quot;24&quot;,&quot;title&quot;:&quot;COT4400 - Project 2: Dynamic programming Solved&quot;,&quot;width&quot;:&quot;138&quot;,&quot;_legend&quot;:&quot;{score}\/{best} - ({count} {votes})&quot;,&quot;font_factor&quot;:&quot;1.25&quot;}">

<div class="kksr-stars">

<div class="kksr-stars-inactive">
            <div class="kksr-star" data-star="1" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" data-star="2" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" data-star="3" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" data-star="4" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" data-star="5" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
    </div>

<div class="kksr-stars-active" style="width: 138px;">
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
    </div>
</div>


<div class="kksr-legend" style="font-size: 19.2px;">
            5/5 - (1 vote)    </div>
    </div>
1 Overview

For this project, you will develop an algorithm to compute the maximum alignment between a target sequence and any possible combination of two given subsequences. Designing and implementing this solution will require you to model the problem using dynamic programming, then understand and implement your model.

In addition to the group submission, you will also evaluate your teammates’ cooperation and contribution. These evaluations will form a major part of your grade on this project, so be sure that you respond to messages promptly, communicate effectively, and contribute substantially to your group’s solution. Details for your team evaluations are in Section 6.2. You will submit the peer evaluations to another assignment on Canvas, labelled “Project 2 (individual).”

2 Problem Description

In this problem, you are given three arrays, seq1, seq2, and target, and the solution to this problem will be the maximum alignment score s of target and a sequence soln, where soln is formed by combining the values in seq1 and seq2 in some order (i.e., seq1 and seq2 are subsequences of soln). Moreover, s will be the maximum alignment score of target with any combination of seq1 and seq2.

For this project, we will calculate alignment scores as the unnormalized cosine similarity. In general, we compute cosine similarity of two normalized vectors or sequences ~a and ~b as a sumproduct (or dot product):

,

3 Worked example

Consider the problem with seq1 = (1, 2, 7), seq2 = (1, 3, 6), and target = (1, 2, 1, 3, 7, 6). Note: after working through this example, we will discuss what a normalized version of this problem would look like.

The solution to this problem will be a score of 100, achieved by the sequence (1, 2, 1, 3, 7, 6) (seq1 and seq2 highlighted in red and blue, respectively). If we compute the dot product of this sequence with target, we see that it has an alignment score of:

If we compare this score to the alignment score for all of the other unique sequences we could produce using seq1 and seq2, shown in the table below, we see that this is the highest possible alignment score with target:

Possible sequence Alignment score

1, 2, 7, 1, 3, 6 72

1, 2, 1, 7, 3, 6 84 1, 2, 1, 3, 7, 6 100 1, 2, 1, 3, 6, 7 99

1, 1, 2, 7, 3, 6 83

1, 1, 2, 3, 7, 6 99

1, 1, 2, 3, 6, 7 98

1, 1, 3, 2, 7, 6 97

1, 1, 3, 2, 6, 7 96

1, 1, 3, 6, 2, 7 80

1, 3, 1, 2, 7, 6 99

1, 3, 1, 2, 6, 7 98

1, 3, 1, 6, 2, 7 82

1, 3, 6, 1, 2, 7 72

Note: there could be more than one sequence that has the maximum alignment score.

As an example of one of the calculations in the table above, the alignment score of the sequence in the first row with target ((1, 2, 7, 1, 3, 6) with (1, 2, 1, 3, 7, 6)) is: h(1,2,7,1,3,6),(1,2,1,3,7,6)i = 1(1) + 2(2) + 7(1) + 1(3) + 3(7) + 6(6)

= 1 + 4 + 7 + 3 + 21 + 36

= 72

Normalization

Cosine similarity should be a value between −1 and 1 indicating how closely aligned two sequences are, but when the sequences are not normalized, this score can be much larger than 1 or smaller than −1. A normalized version of this problem might look like seq1 = (0.1, 0.2, 0.7), seq2 = (0.1, 0.3, 0.6), and target = (0.1, 0.2, 0.1, 0.3, 0.7, 0.6).

Note that the cosine similarity of target with itself is 0.1(0.1) + 0.2(0.2) + 0.1(0.1) + 0.3(0.3) + 0.7(0.7) + 0.6(0.6) = 0.01 + 0.04 + 0.01 + 0.09 + 0.49 + 0.36 = 1, and this is also the cosine similarity of the solution with target. Meanwhile, the cosine similarity of target with the incorrect answer (0.1, 0.2, 0.7, 0.1, 0.3, 0.6) is 0.1(0.1) + 0.2(0.2) + 0.7(0.1) + 0.1(0.3) + 0.3(0.7) + 0.6(0.6) = 0.01 + 0.04 + 0.07 + 0.03 + 0.21 + 0.36 = 0.72.

All of the test problems you will be given for this project will be normalized, and your final answers should be real numbers in the range −1 to 1 (up to round-off errors). That said, the subproblems you evaluate recursively will probably not have this property, and you should not try to normalize the inputs to the problem in your algorithm.

4 Project report

In your project report, you should include brief answers to 7 questions. Note that you must use dynamic programming to solve this problem; other solutions will not receive substantial credit.

1. How would you break down the problem of calculating the maximum alignment score for a combination of two sequences seq1 and seq2 (length n and m, respectively) with the sequence target (length n+m) into one or more smaller instances of this problem? Your answer should include what subproblems you are evaluating, as well as how you are using the answers to these subproblems to solve the original problem.

2. What are the base cases of this recurrence?

3. What data structure would you use to recognize repeated problems? You should describe both the abstract data structure as well as its implementation.

4. Give pseudocode for a memoized dynamic programming algorithm to find the maximum alignment score when combining seq1 and seq2 to align with target.

5. Give pseudocode for an iterative algorithm to find the maximum alignment score when combining seq1 and seq2 to align with target. This algorithm does not need to have a reduced space complexity relative to the memoized solution.

6. Can the space complexity of the iterative algorithm be improved relative to the memoized algorithm? Justify your answer.

5 Coding your solutions

Your code will not need to handle invalid input (e.g., non-normalized sequences or problems where the length of target doesn’t equal the length of seq1 and seq2 combined).

5.1 Input format

Your program should read its input from the file input.txt, in the following format. The first line of the file has two positive integers n and m specifying the lengths of seq1 and seq2, respectively. The second line will list the n real numbers (in the range −1 to 1) that make up seq1, the third line will have the m real numbers that make up seq2, and the fourth line will have the n + m real numbers that make up target. All numbers on a line will be separated by spaces.

5.2 Output

Your program should write its output to the file output.txt. The first line of your output should contain the maximum cosine similarity for seq1, seq2, and target. The second line of your output should list the solution sequence (n + m) that achieves this maximum cosine similarity, with consecutive values separated by spaces. (seq1 and seq2 should be subsequences of this solution sequence.)

6 Submission

Your submission for this project will be in two parts, the group submission and your individual peer evaluations.

6.1 Group submission

The submission for your group should be a zip archive containing 1) your report (described in Section 4) as a PDF document, and 2) your code (described in Section 5). If your code requires more than a simple command to compile and run then you must also provide a Makefile and/or shell script. You should submit this zip archive to the “Project 2 (group)” assignment on Canvas.

6.2 Teamwork evaluation

The second part of your project grade will be determined by a peer evaluation. Your peer evaluation should be a text file that includes 1) the names of all of your teammates (including yourself), 2) the team member responsibilities, 3) whether or not your teammates were cooperative, 4) a numeric rating indicating the proportional amount of effort each of you put into the project, and 5) other issues we should be aware of when evaluating your and your teammates’ relative contribution. The numeric ratings must be integers that sum to 30.

It’s important that you be honest in your evaluation of your peers. In addition to letting your team members whether they do (or do not) need to work on their teamwork and communication skills, we will also evaluate your group submission in light of your team evaluations. For example, a team in which one member refused to contribute would be assessed differently than a team with three functioning members.

You should submit your peer evaluation to the “Project 2 (individual)” assignment on Canvas.

7 Grading

Report 40 points

Question 1, 4, and 5 8 points

Questions 2, 3, 6, and 7 4 each

Code 30 points

Compiles 5

Uses correct input and output format 5

Computes correct alignment score 10

Computes correct sequence 5

Good coding style 5

Teamwork 30 points
