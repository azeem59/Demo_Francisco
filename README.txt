
The demo is using XML files as input. Currently those XML files only work if they were exported from a test suite in TestLink. Here are the steps to Run:

======== SELECTION DEMO =======

1- Install and get TestLink Running (I recommend Bitnami for a quick installation)
2- Go to a TestLink project (if none exist, then create one).
3- Go the the “Test Specification” view.
4- Create a test suite, or import one.
4.1. - Click on a “cog” icon when selecting a TEST SUITE to operate with test suites.
4.2. - If you click the cog icon while selecting a test case, you will import one test case, instead of a test suite.

5 - Export your TEST SUITE as an XML file
6 - For the similarity based selection run the script: selection_demo.sh
6.1. - The first input argument is a removal percentage (e.g. 0.2 = Remove 20% of test cases)
6.2. - The second input argument is the Path to the folder with the exported XML file.
6.3. - After runniing a new XML file is created with the resulting Subset.

7 - To view the results import the test suite back to TestLink.

java -cp arrest_demo.jar:jdom-2.0.6.jar:commons-lang3-3.4.jar:jsoup-1.9.2.jar demo.DemoSelection /Users/gomesf/Documents/code_projects/demo_arrestt/testsuites/selection/

======== REGRESSION DEMO =======

1. Same steps as the Selection Demo, but this time the selection focuses on finding new, obsolete and unchanged test cases. The resulting subset from the technique is actually a mix of those (except for obsolete).

2. Follow the same steps 1 - 5
3. Run the Script: demo_regression.sh
3.1. The only input is the folder wher eyou have both test suites.
4. Import the generated test suites back.

IMPORTANT: The XML file needs to be named: Chat_App_v1 and Chat_App_v2 for the new version!

java -cp arrest_demo.jar:jdom-2.0.6.jar:commons-lang3-3.4.jar:jsoup-1.9.2.jar demo.DemoRegression /Users/gomesf/Documents/projetos_codigo/demo_arrestt/testsuites/regression/




java -cp "./target/classes/" br.edu.ufcg.splab.synergia.CmdMain sut_objects.SUTCalculator 30