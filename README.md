Download Link: https://assignmentchef.com/product/solved-dbms-introduction-to-database-systems-individual-homework-1-sql-tasks-in-mysql
<br>
<h1>1. Introduction</h1>

In this homework you need to practice some basic usages of MySQL, including creating databases, creating tables, loading csv files, loading SQL files, and using MySQL command to find the answer of tasks. After this homework, you will be capable of querying and analyzing your data by MySQL from zero to one.

There will be two datasets for this homework. The first one is COVID-19 data in South Korea, and the second one is European Soccer Dataset, both of these are downloaded from Kaggle Dataset (feel free to google them).

For the first dataset, you need to create a database based on our setting, and load the csv files into your created database. There are 6 easier questions you need to solve by SQL. For the second dataset, you need to load our sql file directly. There are 6 advanced problems you will meet. Read the following content for more details.

<h1>2. Tasks ◈ Part 1 – Data Science for COVID-19 in South Korea</h1>

In this part, you need to create tables based on the provided DB schema, and load csv files into the database.

<h1>            A.   Create Tables</h1>

First, download the COVID-19 data from <a href="https://drive.google.com/file/d/1WUnaQkPtLEaBgDbEz6GtbctTzyXVFqU6/view?usp=sharing">here</a>.

<strong>You can refer to </strong><a href="https://hackmd.io/@7qPkVGGYSTOx_dKfLNSO7g/rkAT268V_"><strong>this page</strong></a><strong> to see the meaning of the columns.</strong>

Then you should create tables based on the following setting. Notice that you <strong>must </strong>make the detail of your tables the same as our description, including

‘table name’, ‘attribute name’, ‘attribute type’, ‘primary key’, ‘foreign key’, ‘null’.

Please <strong>paste the screenshot of your tables by using the `describe` command to your report</strong>, it will take 5% of your grades in this homework.

<table width="597">

 <tbody>

  <tr>

   <td width="112">Table Name</td>

   <td width="160">Attribute Name</td>

   <td width="104">Type</td>

   <td width="73">Primary Key</td>

   <td width="75">Foreign Key</td>

   <td width="73">NULL</td>

  </tr>

  <tr>

   <td rowspan="3" width="112">patient_info</td>

   <td width="160">patient_id</td>

   <td width="104">varchar(10)</td>

   <td width="73">YES</td>

   <td width="75"></td>

   <td width="73">NO</td>

  </tr>

  <tr>

   <td width="160">sex</td>

   <td width="104">varchar(10)</td>

   <td width="73"></td>

   <td width="75"></td>

   <td width="73"></td>

  </tr>

  <tr>

   <td width="160">age</td>

   <td width="104">int</td>

   <td width="73"></td>

   <td width="75"></td>

   <td width="73"></td>

  </tr>

 </tbody>

</table>




<table width="597">

 <tbody>

  <tr>

   <td rowspan="3" width="112"></td>

   <td width="160">province</td>

   <td width="104">varchar(20)</td>

   <td width="73"></td>

   <td width="75"></td>

   <td width="73"></td>

  </tr>

  <tr>

   <td width="160">city</td>

   <td width="104">varchar(20)</td>

   <td width="73"></td>

   <td width="75"></td>

   <td width="73"></td>

  </tr>

  <tr>

   <td width="160">infection_case</td>

   <td width="104">varchar(100)</td>

   <td width="73"></td>

   <td width="75"></td>

   <td width="73"></td>

  </tr>

  <tr>

   <td rowspan="5" width="112">search_trend</td>

   <td width="160">date</td>

   <td width="104">date</td>

   <td width="73">YES</td>

   <td width="75"></td>

   <td width="73">NO</td>

  </tr>

  <tr>

   <td width="160">cold</td>

   <td width="104">float</td>

   <td width="73"></td>

   <td width="75"></td>

   <td width="73"></td>

  </tr>

  <tr>

   <td width="160">flu</td>

   <td width="104">float</td>

   <td width="73"></td>

   <td width="75"></td>

   <td width="73"></td>

  </tr>

  <tr>

   <td width="160">pneumonia</td>

   <td width="104">float</td>

   <td width="73"></td>

   <td width="75"></td>

   <td width="73"></td>

  </tr>

  <tr>

   <td width="160">coronavirus</td>

   <td width="104">float</td>

   <td width="73"></td>

   <td width="75"></td>

   <td width="73"></td>

  </tr>

  <tr>

   <td rowspan="6" width="112">time</td>

   <td width="160">date</td>

   <td width="104">date</td>

   <td width="73">YES</td>

   <td width="75"></td>

   <td width="73">NO</td>

  </tr>

  <tr>

   <td width="160">test</td>

   <td width="104">int</td>

   <td width="73"></td>

   <td width="75"></td>

   <td width="73"></td>

  </tr>

  <tr>

   <td width="160">negative</td>

   <td width="104">int</td>

   <td width="73"></td>

   <td width="75"></td>

   <td width="73"></td>

  </tr>

  <tr>

   <td width="160">confirmed</td>

   <td width="104">int</td>

   <td width="73"></td>

   <td width="75"></td>

   <td width="73"></td>

  </tr>

  <tr>

   <td width="160">released</td>

   <td width="104">int</td>

   <td width="73"></td>

   <td width="75"></td>

   <td width="73"></td>

  </tr>

  <tr>

   <td width="160">deceased</td>

   <td width="104">int</td>

   <td width="73"></td>

   <td width="75"></td>

   <td width="73"></td>

  </tr>

  <tr>

   <td rowspan="4" width="112">time_age</td>

   <td width="160">date</td>

   <td width="104">date</td>

   <td width="73">YES</td>

   <td width="75"></td>

   <td width="73">NO</td>

  </tr>

  <tr>

   <td width="160">age</td>

   <td width="104">int</td>

   <td width="73">YES</td>

   <td width="75"></td>

   <td width="73">NO</td>

  </tr>

  <tr>

   <td width="160">confirmed</td>

   <td width="104">int</td>

   <td width="73"></td>

   <td width="75"></td>

   <td width="73"></td>

  </tr>

  <tr>

   <td width="160">deceased</td>

   <td width="104">int</td>

   <td width="73"></td>

   <td width="75"></td>

   <td width="73"></td>

  </tr>

  <tr>

   <td rowspan="4" width="112">time_gender</td>

   <td width="160">date</td>

   <td width="104">date</td>

   <td width="73">YES</td>

   <td width="75"></td>

   <td width="73">NO</td>

  </tr>

  <tr>

   <td width="160">sex</td>

   <td width="104">varchar(10)</td>

   <td width="73">YES</td>

   <td width="75"></td>

   <td width="73">NO</td>

  </tr>

  <tr>

   <td width="160">confirmed</td>

   <td width="104">int</td>

   <td width="73"></td>

   <td width="75"></td>

   <td width="73"></td>

  </tr>

  <tr>

   <td width="160">deceased</td>

   <td width="104">int</td>

   <td width="73"></td>

   <td width="75"></td>

   <td width="73"></td>

  </tr>

  <tr>

   <td rowspan="5" width="112">time_province</td>

   <td width="160">date</td>

   <td width="104">date</td>

   <td width="73">YES</td>

   <td width="75"></td>

   <td width="73">NO</td>

  </tr>

  <tr>

   <td width="160">province</td>

   <td width="104">varchar(20)</td>

   <td width="73">YES</td>

   <td width="75"></td>

   <td width="73">NO</td>

  </tr>

  <tr>

   <td width="160">confirmed</td>

   <td width="104">int</td>

   <td width="73"></td>

   <td width="75"></td>

   <td width="73"></td>

  </tr>

  <tr>

   <td width="160">released</td>

   <td width="104">int</td>

   <td width="73"></td>

   <td width="75"></td>

   <td width="73"></td>

  </tr>

  <tr>

   <td width="160">deceased</td>

   <td width="104">int</td>

   <td width="73"></td>

   <td width="75"></td>

   <td width="73"></td>

  </tr>

  <tr>

   <td rowspan="9" width="112">region</td>

   <td width="160">code</td>

   <td width="104">int</td>

   <td width="73">YES</td>

   <td width="75"></td>

   <td width="73">NO</td>

  </tr>

  <tr>

   <td width="160">province</td>

   <td width="104">varchar(20)</td>

   <td width="73"></td>

   <td width="75"></td>

   <td width="73"></td>

  </tr>

  <tr>

   <td width="160">city</td>

   <td width="104">varchar(20)</td>

   <td width="73"></td>

   <td width="75"></td>

   <td width="73"></td>

  </tr>

  <tr>

   <td width="160">elementary_school_co unt</td>

   <td width="104">int</td>

   <td width="73"></td>

   <td width="75"></td>

   <td width="73"></td>

  </tr>

  <tr>

   <td width="160">kindergarten_count</td>

   <td width="104">int</td>

   <td width="73"></td>

   <td width="75"></td>

   <td width="73"></td>

  </tr>

  <tr>

   <td width="160">university_count</td>

   <td width="104">int</td>

   <td width="73"></td>

   <td width="75"></td>

   <td width="73"></td>

  </tr>

  <tr>

   <td width="160">elderly_population_rat io</td>

   <td width="104">float</td>

   <td width="73"></td>

   <td width="75"></td>

   <td width="73"></td>

  </tr>

  <tr>

   <td width="160">elderly_alone_ratio</td>

   <td width="104">float</td>

   <td width="73"></td>

   <td width="75"></td>

   <td width="73"></td>

  </tr>

  <tr>

   <td width="160">nursing_home_count</td>

   <td width="104">int</td>

   <td width="73"></td>

   <td width="75"></td>

   <td width="73"></td>

  </tr>

  <tr>

   <td rowspan="5" width="112">weather</td>

   <td width="160">code</td>

   <td width="104">int</td>

   <td width="73">YES</td>

   <td width="75">region (code)</td>

   <td width="73">NO</td>

  </tr>

  <tr>

   <td width="160">date</td>

   <td width="104">date</td>

   <td width="73">YES</td>

   <td width="75"></td>

   <td width="73">NO</td>

  </tr>

  <tr>

   <td width="160">avg_temp</td>

   <td width="104">float</td>

   <td width="73"></td>

   <td width="75"></td>

   <td width="73"></td>

  </tr>

  <tr>

   <td width="160">most_wind_direction</td>

   <td width="104">int</td>

   <td width="73"></td>

   <td width="75"></td>

   <td width="73"></td>

  </tr>

  <tr>

   <td width="160">avg_relative_humidity</td>

   <td width="104">float</td>

   <td width="73"></td>

   <td width="75"></td>

   <td width="73"></td>

  </tr>

 </tbody>

</table>

Please <strong>answer the following question in your report</strong>, it will take 10% of this homework.

<ol>

 <li>(3%) What is the difference between type “char” and type “varchar”? ？</li>

 <li>(3%) How many bytes it should take for “tinyint”, “smallint”, “mediumint”,</li>

</ol>

“int”? (e.g. 8 bytes for “bigint”)

And what’s the range they can express? (e.g. from -1000 to 1000) ：“tinyint”, “smallint”, “mediumint”, “int”？

(e.g. 8 bytes for “bigint”)

？(e.g. from -1000 to 1000)

<ol start="3">

 <li>(4%) What do you think about this DB schema? If you can change this table architecture, how would you modify it and why?</li>

</ol>

？

<h1>            B.    Load CSV Data</h1>

After creating the database, you need to load the downloaded csv files into your database.

Here we don’t restrict the method you use, but you have to check the data is loaded successfully by yourself. The following number is the data records for each table.

<table width="513">

 <tbody>

  <tr>

   <td width="229">Table Name</td>

   <td width="284"># of Data Records</td>

  </tr>

  <tr>

   <td width="229">patient_info</td>

   <td width="284">5164</td>

  </tr>

  <tr>

   <td width="229">search_trend</td>

   <td width="284">1642</td>

  </tr>

  <tr>

   <td width="229">time</td>

   <td width="284">163</td>

  </tr>

  <tr>

   <td width="229">time_age</td>

   <td width="284">1089</td>

  </tr>

  <tr>

   <td width="229">time_gender</td>

   <td width="284">242</td>

  </tr>

  <tr>

   <td width="229">time_province</td>

   <td width="284">2771</td>

  </tr>

  <tr>

   <td width="229">region</td>

   <td width="284">243</td>

  </tr>

  <tr>

   <td width="229">weather</td>

   <td width="284">26271</td>

  </tr>

 </tbody>

</table>

<h1>            C.   Query Tasks</h1>

In this part, here are 6 query tasks you need to write. <strong>Please read the following rules carefully</strong>.

You are only allowed to use <strong>one </strong>query (<strong>one delimiter</strong>) to find the answer, and you <strong>don’t </strong>have to explain your SQL. Noted that the <strong>column names </strong>of your query answers should be <strong>the same as our examples</strong>.

For homework submission, please write every query task into a single `sql` file, named as “1.sql”, “2.sql”, etc.

<ol>

 <li>(5%) How many days have the word “cold” been searched over 2000 times in one day? “cold”。</li>

</ol>

<table width="76">

 <tbody>

  <tr>

   <td width="76">cnt</td>

  </tr>

  <tr>

   <td width="76">5566</td>

  </tr>

 </tbody>

</table>

<ol start="2">

 <li>(5%) How many ways are there for those men under 30, living in Seoul Gangnam-gu being infected? List out in the alphabetical order as the following example.</li>

</ol>




<table width="110">

 <tbody>

  <tr>

   <td width="110">infection_case</td>

  </tr>

  <tr>

   <td width="110">eating</td>

  </tr>

  <tr>

   <td width="110">talking</td>

  </tr>

  <tr>

   <td width="110">sleeping</td>

  </tr>

 </tbody>

</table>

<ol start="3">

 <li>(5%) Find out the province, city, and the elementary school count in which the elementary school count is the top three most <strong>and the name of the province is different from the city</strong>. List out in decreasing order of the count.</li>

</ol>




<table width="330">

 <tbody>

  <tr>

   <td width="110">province</td>

   <td width="111">city</td>

   <td width="109">cnt</td>

  </tr>

  <tr>

   <td width="110">Apple</td>

   <td width="111">Taipei</td>

   <td width="109">5566</td>

  </tr>

  <tr>

   <td width="110">Banana</td>

   <td width="111">Hsinchu</td>

   <td width="109">3344</td>

  </tr>

  <tr>

   <td width="110">Cherry</td>

   <td width="111">Taichung</td>

   <td width="109">1122</td>

  </tr>

 </tbody>

</table>

<ol start="4">

 <li>(5%) Find out the provinces whose days count of the average relative humidity larger than 70 are the top three most in May of 2016, and list their days count in decreasing order.</li>

</ol>

<ol start="5">

 <li>(5%) Find out the province where the elderly population ratio is larger than the average and the date with maximum confirmed in one day. List out in the order of date increasingly. <strong>Notice that the average of the elderly population ratio is the average of those provinces which have the same name as the city.</strong></li>

</ol>




<table width="220">

 <tbody>

  <tr>

   <td width="110">province</td>

   <td width="111">date</td>

  </tr>

  <tr>

   <td width="110">Apple</td>

   <td width="111">2020-01-01</td>

  </tr>

  <tr>

   <td width="110">Banana</td>

   <td width="111">2020-02-02</td>

  </tr>

 </tbody>

</table>

<ol start="6">

 <li>(5%) How many “accumulated-confirmed”, “added-confirmed”,</li>

</ol>

“accumulated-dead”, “added-dead” are there while the search number of the word “coronavirus” is larger than two standard deviations? List your answer in ascending order by date and round coronavirus to second decimal place. The standard deviation should be calculated by the period from 2019-12-15 to 2020-06-29.

The added-confirmed and the added-dead should be calculated by “the accumulated count of that day minus the accumulated count of the previous day“. ：coronavirus

<table width="689">

 <tbody>

  <tr>

   <td width="91">date</td>

   <td width="99">coronavirus</td>

   <td width="164">confirmed_accumulate</td>

   <td width="117">confirmed_add</td>

   <td width="131">dead_accumulate</td>

   <td width="88">dead_add</td>

  </tr>

  <tr>

   <td width="91">2020-01-01</td>

   <td width="99">66.00</td>

   <td width="164">3</td>

   <td width="117">0</td>

   <td width="131">12</td>

   <td width="88">0</td>

  </tr>

  <tr>

   <td width="91">2020-01-02</td>

   <td width="99">55.12</td>

   <td width="164">23</td>

   <td width="117">20</td>

   <td width="131">34</td>

   <td width="88">22</td>

  </tr>

 </tbody>

</table>

<h1>◈ Part 2 – European Soccer Database</h1>

In this Part, instead of creating tables and loading csv files, you need to load the provided DB file directly. Please download the file from <a href="https://drive.google.com/file/d/1bqHvBfj-VXmrpcYaOTax2tQtxcR-nKpX/view?usp=sharing">here</a>.

<h1>            D.   Load SQL File</h1>

Here we provide simple steps for the Linux environment. You can also load the SQL file by other methods, like execute the sql file using the “source” command.

<ol>

 <li>Firstly, create a database</li>

 <li>Then, back to your shell and enter command mysql -u {user_name} -p {DB Name} &lt; hw1_part2.sql</li>

</ol>

(You can google “IO Redirection” for more detail of the above mechanism)

<h1>            E.    Query Tasks</h1>

In this part, you are also only allowed to use <strong>one </strong>query (<strong>one delimiter</strong>) to find the answer, and you <strong>don’t </strong>have to explain your SQL, <strong>except task 11 and task 12</strong>. Noted that the <strong>column names </strong>of your query answers should be <strong>the same as our examples</strong>.

For <strong>task 11 and 12</strong>, take <strong>screenshots </strong>of your queries, and <strong>write your analysis </strong>into the report. Try to explain what’re your queries doing, why you write these queries, what’s the meaning of the result, what’s your conclusion, etc.

For submission, also write every query task into a single `.sql` file, named as “7.sql”,

“8.sql” …, “11.sql”, “12.sql”

<strong>For the meaning of each table and column in part2, please refer to </strong><a href="https://hackmd.io/@7qPkVGGYSTOx_dKfLNSO7g/rkAT268V_"><strong>this page</strong></a><strong>.</strong>

<ol start="7">

 <li>(10%) List the average long_shots score(<strong>round to the second decimal place</strong>) of the players who had participated in the Italy Serie A league during 2015/2016 season with respect to the preferred foot. You should calculate the long_shots score by the newest data of each player.</li>

</ol>




<table width="231">

 <tbody>

  <tr>

   <td width="110">preferred_foot</td>

   <td width="121">avg_long_shots</td>

  </tr>

  <tr>

   <td width="110">left</td>

   <td width="121">30.87</td>

  </tr>

  <tr>

   <td width="110">right</td>

   <td width="121">20.87</td>

  </tr>

 </tbody>

</table>

<ol start="8">

 <li>(10%) During the 2015/2016 season, for each of the leagues, if we have known that the average height of members in one team is over 180, what is the probability that the team can win?</li>

</ol>

The numerator is the winning count of those over-180-teams, and the denominator is the count of those over-180-teams. Round the probability to fourth decimal place. List out in the alphabetical order.

(e.g. In two matches, A and B, one team of A is over-180-teams and wins the game. Both team of B are over-180-teams and one of the team win the game, then the win probability is ⅔)

(e.g. In two matches, A and B, one team of A is over-180-teams and ties the game. Both team of B are not over-180-teams, then the win probability is 0) (You need to calculate the record of the same team in different matches. For example, team a1 and team a2 take match A, and team a1 and team b1 take match

B, then you need to consider a1 multiple times)




<table width="231">

 <tbody>

  <tr>

   <td width="110">name</td>

   <td width="121">prob</td>

  </tr>

  <tr>

   <td width="110">AppleLeague</td>

   <td width="121">0.5566</td>

  </tr>

  <tr>

   <td width="110">BananaLeague</td>

   <td width="121">0.3344</td>

  </tr>

 </tbody>

</table>

<ol start="9">

 <li>(10%) The “win point” can be calculated by the following rule: “For each match, the winning team will get two points. The loser will get zero point. If the match is a draw, both of the teams will get one point. The win points of each team is the point divided by the match count the team participating in during the whole season.” The top five teams with the highest win points are called “the greats of the season”. Find out the average winning score (<strong>round to the second decimal place</strong>) and the team’s long name of the greats of the season during the 2015/2016 season. List out in the decreasing order of their win points.</li>

</ol>




<table width="248">

 <tbody>

  <tr>

   <td width="128">team_long_name</td>

   <td width="120">avg_win_score</td>

  </tr>

  <tr>

   <td width="128">AppleTeam</td>

   <td width="120">5.55</td>

  </tr>

  <tr>

   <td width="128">BananaTeam</td>

   <td width="120">4.44</td>

  </tr>

  <tr>

   <td width="128">CherryTeam</td>

   <td width="120">3.33</td>

  </tr>

  <tr>

   <td width="128">JellyTeam</td>

   <td width="120">2.22</td>

  </tr>

  <tr>

   <td width="128">OreoTeam</td>

   <td width="120">1.11</td>

  </tr>

 </tbody>

</table>

<ol start="10">

 <li>(15%) We call it a landslide victory if there is a “larger than or equal to five” score gap between two teams in a match. And we call it an upset if any one of the sports betting companies has a higher betting odds on a team with landslide victory. Find out that for an upset, what is the average age of the player at that time and the average rating of the players of each team from the previous six months? Round the score to second decimal place and list out in the order of</li>

</ol>

match id increasingly.

(If a player has scores multiple times, please average all of them)

(Here we want to see the average data of players on the home side and away side in the upset matches. You don’t need to consider which team the team belongs to)

<table width="714">

 <tbody>

  <tr>

   <td width="39">id</td>

   <td width="159">home_player_avg_age</td>

   <td width="159">away_player_avg_age</td>

   <td width="181">home_player_avg_rating</td>

   <td width="176">away_player_avg_rating</td>

  </tr>

  <tr>

   <td width="39">1</td>

   <td width="159">22.22</td>

   <td width="159">23.23</td>

   <td width="181">60.60</td>

   <td width="176">58.58</td>

  </tr>

  <tr>

   <td width="39">2</td>

   <td width="159">23.23</td>

   <td width="159">24.24</td>

   <td width="181">62.62</td>

   <td width="176">75.75</td>

  </tr>

  <tr>

   <td width="39">3</td>

   <td width="159">24.24</td>

   <td width="159">21.21</td>

   <td width="181">55.55</td>

   <td width="176">99.99</td>

  </tr>

 </tbody>

</table>

<ol start="11">

 <li>(10%) Do the home team with home advantage has much more opportunity to win the game, or the team with a higher average score(which can be one of the overall_rating, dribbling, strength, interceptions, or the average of the four scores, calculated by the latest attribute before the player participating in the match) of the whole team players? <strong>Answer by your own view with one SQL query.</strong></li>

</ol>

<ol start="12">

 <li>(10%) You are a gambler of sport lottery. Analyzing this dataset with SQL and finding out the better way to place a bet. <strong>You can answer by your own view with multiple SQL queries. Focus on observation to the dataset and explain your analysis.</strong></li>

</ol>

<h1>4. Discussion</h1>

TAs had opened a channel HW1 on New E3 forum of the course, you can post questions about the homework on the forum. TAs will answer questions as soon as possible.

Discussion rules:

<ol>

 <li>Do not ask for the answer to the homework.</li>

 <li>Check if someone has asked the same question before asking.</li>

 <li>We encourage you to answer other students’ questions, but again, do not give the answer of the homework. Reply the messages to answer questions.</li>

 <li>Since we have this discussion forum, do not send email to ask questions about the homework unless the questions are personal and you do not want to ask publicly.</li>

</ol>