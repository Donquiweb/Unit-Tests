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
Tutorial : http://matthieu-brucher.developpez.com/tutoriels/cpp/cppUnit/  
MSTest : Microsoft dispose de son framework. 
NUnit : la version .NET du framework XUnit.
 
 
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


# R  
RUnit : https://cran.r-project.org/web/packages/RUnit/index.html
documentation https://cran.r-project.org/web/packages/RUnit/vignettes/RUnit.pdf   


# PL/SQL
utPLSQL : https://utplsql.github.io/  
utPLSQL v3 Cheat Sheet : https://www.cheatography.com/jgebal/cheat-sheets/utplsql-v3/pdf/  

