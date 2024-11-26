java c
Problem   Set   3
ECO3121   -   Fall   2024
Due   3   PM,   November   28,   2024
No   late   submission   is   allowed
Please   combine   your   answer,   Stata   code   and   requested   output   in   one pdf   ﬁle   and   upload   it   to   Blackboard
Question   1Download   aghousehold.dta   and   village   rainfall.dta   datasets   from   the   blackboard   site   and   load   into   Stata.   The   main   data   we   use   is   the   National   Fixed   Point   Survey   (NPFS),   which   is   a   nationally   representative   panel   dataset (unbalanced)   of   roughly   5000   households   in 88 villages between   1995 and 2002.   It   is   collected   by   the   Ministry   of Agriculture   and Rural Afairs of China.On the blackboard, we also uploaded a second dataset regarding precipitation records   in each village in 2001.   See the variable list below.   Write up the answers to 1) - 6) below.   In addition, also attach the do ﬁle that you used   to   answer   the   following   questions.
variable name
type
format
label
vl   id
int
%8.0g
village   ID, consistent   with   household   data
lat   o
float
%8.0g
latitude of each village
lon   o
float
%8.0g
longitude of each village
provname
str24
%24s
province name in   Chinese
cityname
str33
%33s
city   name   in   Chinese
countyname
str33
%33s
county name in   Chinese
av   rain
float
%9.0g
average precipitation in 2001, measured   by   mm
sd   rain
float
%9.0g
standard deviation of precipitation across months in 2001
z   rain
float
%9.0g
zero score of precipitation in   2001
First,   limit   the   sample   to   households   in      the      year      2001    by   running   code      “keep if   year==2001”   in   Stata.      You   can   generate   variable   yield      (output   per   unit   of   land)
via      ,   and   variable   fertilizer      (fertilizer   application   per   unit   of   land)   through
nh6   3    hx95   nh112 .
1.   The variable   h95      nh269    indicates   how   many   days   for   household   members   in   each
household had been working as temporal migrants   (measured by days)   in   2001.
Generate   a   binary   variable   regarding   household   migration   decision.      It   takes   the   value of 1 if h95      nh269      is greater   than   zero,   otherwise   it   is   0.    Generate the   natu-   ral   log   of   yield   and   fertilizer   application   intensity   (using   log(fertilizer      +    1)   and log(yield   +   1)   to   smooth   zero   values.).   (2 points)
2.   Run a linear probability model   of household   migration   decision   in   question   (1)   on   the   natural   log   of   yield.
Interpret   the   result   and   comment   on   its   statistical   signiﬁcance.   (2 points)
3.   List   three   plausible   arguments   why   the   point   estimate   in   question   (2)   could   be   biased, and   the   corresponding   bias   directions   (upwards   or   downwards) relative   to the true causal efect of   household’s agricultural production on household migration  代 写ECO3121 - Fall 2024 Problem Set 3Prolog
代做程序编程语言 decision.   (3 points)
4.   Now   your   professor   suggests   that   the   rainfall   (precipitation)   could   be   a   valid   in-   strumental   variable   (IV) for   your   measure   of   household’s   yield.    Try   to   merge   the household’s   production   dataset   and   precipitation   dataset   via   vl      id, the   speciﬁc   vil-   lage identiﬁer, using stata command merge    (Many-to-one merge, type   “help   merge”   in   Stata   for   assistance).You   decide to   use the   natural   log   of average   rainfall   in   2001   (log(av      rain))   as the   IV   for   the   natural   log   of   yield.    Verify   if   the   assumption   of   instrument   relevance is   satisﬁed   using   the   ﬁrst   stage   regression,   and   obtain   the   results   in   Stata.    Write down   the   ﬁrst   stage   regression   model   and interpret the result and statistical   signiﬁcance   of   your   result.   (2 points)
5.   Now use Stata to estimate the 2nd stage IV point estimate (using linear probability   model) as   suggested   by   the   professor,   and   export   your   result.          Write      down   the second   stage   regression   model   and   interpret the   result   and   statistical   signiﬁ-   cance   of   your   result.   (2 points)
6.   Now your   professor tells you   that   you   can   use   ivregress      2sls      command   directly   to   replicate   the   results   in   question   (5).
(a)   Do   you   ﬁnd   any   diference   in   the   IV   estimations   (βIV   )   using   ivregress      2sls command regarding   the   coe       cients   and   standard   errors   relative to (5).   (2 points)
(b)   In reference to your answer to questions   (2) and   (3), is the diference between   the   linear   probability   model   and   IV   point   estimates   as   you   expected   or   rather   not?   (2 points)
Question   2
Consider the two-way relationship between crop yield and fertilizer usage   Crop   = α0   +   β0   Fertilizer   +   u
Fertilizer   = α   1   +   β1   Crop   +   vThe   ﬁrst   equation   models   the   determinant   of crop   yield   given   the   amount   of fertilizer   usage.   The second equation models the amount of fertilizer   the   farmer   chooses   to   apply   given the crop yield in   the   area.
1.   What   do   you   expect   the   signs   of   β0      and   β1      are?   Explain.   (2 points)
2.   Explain   why   the   OLS   estimator   for   β0       and   β1       are   biased.      If   we   use   the   OLS estimator   to   estimate   β0       and   β1   ,   what   directions   are   the   biases?      Explain.       (4   points)
3.   Suppose   the   only   variables   available   are   Crop, Fertilizer   , Sunshine   (the   sunshine of   the   area),   and   Budget      (the   budget   constraint   of   the   farmer).    To   estimate   β0   and   β1      by   the   two-stage   least   squares   estimator,   which   variables   among   the   data   you   have   should   be   used   as   instruments?   Be   speciﬁc, what   IV   is   for   Fertilizer   and which IV is for Crop.   Explain.   (4 points)

         
加QQ：99515681  WX：codinghelp  Email: 99515681@qq.com
