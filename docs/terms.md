# Terms and Definitions

term:application under test
:   The application which is tested by a <term:test project>.

term:test project
:   A repository containing <term:feature|features>, <term:step|steps> in order to
    test a specific <term:application under test>. Usually, one test project tests
    a single applciation.

term:system under test
:   See <term:application under test>

term:test run
:   A test run is a single run over a defined set of tests using the <cmd:run|acre run>
    command. A test run is identified by a unique <term:testrun id>.

term:feature
:   A feature file contains a number of <term:scenario|scenarios>.

term:scenario
:   A <term:feature> can consist of multiple scenarios testing different
    aspects of a feature.

term:step
:   A single human-readable sentence in the Gherkin syntax to either:

    -   Establish a prerequisite for a <term:feature> or <term:scenario> (**Given**)
    -   Do an action on the <term:application under test> (**When**)
    -   Evaluate the result of an action (**Then**)

term:testrun id
:   A UUID4 string value uniquely identifying a single <term:test run>.

term:tid
:   A unique **test case id** identifying either a specific <term:feature> or <term:scenario>.
