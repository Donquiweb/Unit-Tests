# Unit-Tests
# Unit Tests under several languages   
https://fr.wikipedia.org/wiki/Test_unitaire

# C#  
JsUnit  


# C++  
Microsoft dispose de son framework, MSTest. D'autres framework de tests existent, comme le très connu NUnit qui est la version .NET du framework XUnit  
 
 
# Java  
JUnit  


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
