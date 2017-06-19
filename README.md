# Unit Tests under several languages   
fr: https://fr.wikipedia.org/wiki/Test_unitaire  
en: https://en.wikipedia.org/wiki/Unit_testing  
  
# C#  
JsUnit  
https://openclassrooms.com/courses/programmez-en-oriente-objet-avec-c/les-tests-unitaires-5  
Code :  
<pre>
public static class Math
{
    public static int Factorielle(int a)
    {
        if (a <= 1)
            return 1;
        return a * Factorielle(a - 1);
    }
}
</pre>
  
Test :  
  
<pre>
[TestClass]
public class MathTests
{
    [TestMethod]
    public void Factorielle_AvecValeur3_Retourne6()
    {
        // test à faire
    }
}
</pre>

# C++  
cppUnit
Tutorials : 
http://matthieu-brucher.developpez.com/tutoriels/cpp/cppUnit/  
https://msdn.microsoft.com/fr-fr/library/hh598953(v=vs.120).aspx  
MSTest : Microsoft framework   
https://docs.microsoft.com/fr-fr/dotnet/core/testing/unit-testing-with-mstest  
NUnit : .NET version of XUnit framework  
https://www.nunit.org/   
 
# Java  
JUnit  
<pre>
import static org.junit.jupiter.api.Assertions.assertEquals;
import org.junit.jupiter.api.Test;

public class MyTests {

    @Test
    public void multiplicationOfZeroIntegersShouldReturnZero() {
        MyClass tester = new MyClass(); // MyClass is tested

        // assert statements
        assertEquals("10 x 0 must be 0", 0, tester.multiply(10, 0));
        assertEquals("0 x 10 must be 0", 0, tester.multiply(0, 10));
        assertEquals("0 x 0 must be 0", 0, tester.multiply(0, 0));
    }
}
</pre>

# Javascript  
JsUnit : http://unitjs.com/
Tape : https://github.com/substack/tape
<pre>
import test from 'tape';
test('A passing test', (assert) => {
  assert.pass('This test will pass.');
  assert.end();
});

test('Assertions with tape.', (assert) => {
  const expected = 'something to test';
  const actual = 'sonething to test';
  assert.equal(actual, expected,
    'Given two mismatched values, .equal() should produce a nice bug report');
  assert.end();
});
</pre>

# jQuery
QUnitJs http://qunitjs.com/  
<pre>
QUnit.test( "hello test", function( assert ) {
  assert.ok( 1 == "1", "Passed!" );
});
</pre>   

# PHP  
PHPUnit : https://phpunit.de/   

<pre>
class StackTest extends PHPUnit_Framework_TestCase
{
    public function testPushAndPop()
    {
        $stack = array();
        $this->assertEquals(0, count($stack));

        array_push($stack, 'foo');
        $this->assertEquals('foo', $stack[count($stack)-1]);
        $this->assertEquals(1, count($stack));

        $this->assertEquals('foo', array_pop($stack));
        $this->assertEquals(0, count($stack));
    }
}
</pre>

# Prolog 
PlUnit : http://www.swi-prolog.org/pldoc/doc_for?object=section(%27packages/plunit.html%27)  
<pre>
:- begin_tests(lists).
:- use_module(library(lists)).

test(reverse) :-
        reverse([a,b], [b,a]).

:- end_tests(lists).
</pre>

# Python
Unittest / PyUnit : https://docs.python.org/2/library/unittest.html  
<pre>  
import unittest

class TestStringMethods(unittest.TestCase):

    def test_upper(self):
        self.assertEqual('foo'.upper(), 'FOO')

    def test_isupper(self):
        self.assertTrue('FOO'.isupper())
        self.assertFalse('Foo'.isupper())

    def test_split(self):
        s = 'hello world'
        self.assertEqual(s.split(), ['hello', 'world'])
        # check that s.split fails when the separator is not a string
        with self.assertRaises(TypeError):
            s.split(2)

if __name__ == '__main__':
    unittest.main()
</pre>  

# PL/SQL
utPLSQL : https://utplsql.github.io/  
utPLSQL v3 Cheat Sheet : https://www.cheatography.com/jgebal/cheat-sheets/utplsql-v3/pdf/  

# R  
RUnit : https://cran.r-project.org/web/packages/RUnit/index.html
documentation https://cran.r-project.org/web/packages/RUnit/vignettes/RUnit.pdf   
Tutorial : http://wiki.inra.fr/wiki/cascisdi/Production/Tests+unitaires+sous+R  
