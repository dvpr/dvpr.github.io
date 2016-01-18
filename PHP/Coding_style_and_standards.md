##Coding style and standards

###文件格式

************************************************************************

文件统一使用UTF-8编码

###缩进和每行代码的长度

************************************************************************

使用制表符完成缩进，制表符的长度为4。

每行代码的长度没有硬性标准，可根据该行的性质和代码的可读性自行把握。

###赋值语句

************************************************************************

赋值语句的等号前后都至少要有一个空格

示例:

    $var = 0;

在多个相关的赋值语句中，使用制表符将等号对齐以增加代码的可读性

示例:

    $short          = 0;
    $long_variable  = $short;

###流程控制语句

************************************************************************

在流程控制语句中，关键词、参数、花括号之间应该有一个空格以便与函数调用格式区分

在任何时候都必须使用花括号，以增加代码的可读性，避免添加新行时造成的逻辑错误

if语句

示例:

    if ((condition1) || (condition2)) {
        action1();
    } elseif ((condition3) && (condition4)) {
        action2();
    } else {
        defaultAction();
        anotherAction();
    }

在页面布局中使用流程控制的替代语法，条件语句逻辑运算符也应该使用大写的单词（AND，OR，等），而不是使用符号（$，|，等）

示例:

    if ((condition1) OR (condition2)) :
        action1();
    elseif ((condition3) AND (condition4)) :
        action2();
    else :
        defaultAction();
        anotherAction();
    endif;

    foreach ($array as $element) :
        echo $element;
    endforeach;

switch语句

示例:

    switch (condition) {
        case 1:
            doAction1();
            break;

        case 2:
            doAction2();
            break;

        default:
            doDefaultAction();
            break;
    }

使用缩进代替case语句的花括号来增加代码的可读性

case语句中条件和冒号之间不能有空格

###函数调用

************************************************************************

函数名和圆括号之间不能有空格

圆括号和第一个参数以及最后一个参数之间不能有空格

参数和逗号之间不能有空格（多个参数的情况下）

每个参数的逗号后要有一个空格（多个参数的情况下）

示例:

    $var = foo($bar, $baz, $quux);

###函数声明

************************************************************************

函数或类的声明遵循“one true brace”原则（开始的花括号单独占一行，而不是跟在其他语句后面）

示例:

    function fooFunction($arg1, $arg2 = '')
    {
        if (condition) {
            statement;
        }
        return $val;
    }

    class fooClass
    {
        function fooMethod($arg1)
        {
            if ($arg) {
                $result = true;
            } else {
                $result = false;
            }
            return $result;
        }
    }

有默认值的参数要放在参数列表的最后

当函数有返回值时，必须保证函数返回一个有意义的值

示例:

    function connect(&$dsn, $persistent = false)
    {
        if (is_array($dsn)) {
            $dsninfo = &$dsn;
        } else {
            $dsninfo = DB::parseDSN($dsn);
        }

        if (!$dsninfo OR !$dsninfo['phptype']) {
            return $this->raiseError();
        }

        return true;
    }

###注释

************************************************************************

类，属性和方法，函数，常量都应该提供适当的DocBlocks。

所有的包名使用小写字母表示用"."连接

类

示例:

    /**
     * 类的简短描述
     *
     * 类的详细描述(可选)
     *
     * @package         packagename
     * @subpackage      subpackagename
     * @author          <作者>
     * @since           <起始版本>
     * @deprecated      --不被推荐的过期的(可选)
     */

属性

示例:

    /**
     * 简短描述
     *
     * @var 类型
     */

函数和方法

示例:

    /**
     * 简短描述
     *
     * @since   <起始版本>
     * @param   <类型>  <变量名> <描述>  --参数
     * @return  <类型>  <描述>  --返回值
     */

保证适当的非文档注释量（原则:当你看到一段代码，然后想:“Wow, I don't want to try and describe that”，那么你就应该在你忘记程序的工作流程之前为这段代码添加非文档注释） 内联的类文件的注释应遵循PHPDoc惯例，详见http://www.phpdoc.org/

###PHP标签

************************************************************************

使用<?php ?>不要使用<? ?>

当文件中只包含php代码时不要使用结束标记?>

###SQL语句

************************************************************************

关键词必须大写，其他字符必须小写

SQL语句中不能包含回车符

使用缩进来提高SQL语句可读性

使用单引号提高执行效率

所有整型和浮点型变量都要进行强制类型转换

所有字符变量使用Quote()方法

所有表明使用#_前缀

示例:

    $state = 1;
    $name  = 'bill';
    $query = 'SELECT COUNT( c.id ) AS num_articles, u.id, u.username'.
        ' FROM #__content AS c'.
        ' LEFT JOIN #__users AS u ON u.id = c.created_by'.
        ' WHERE c.state = '.(int) $state
        '  AND u.id IS NOT NULL'.
        '  AND u.username <> '.$db->Quote( $name ).
        ' GROUP BY u.id'.
        '  HAVING COUNT( c.id ) > 0';

###命名约定

************************************************************************

类

类要以描述性的名称命名

类名使用完整单词不要使用缩写

类名首字母大写

类名使用CamelCase拼写法

类名可以使用全部大写的特殊名词（eg HTML,XML）

框架类，都是以大写的H开头（eg HApplication，HModel）

函数和方法

函数和方法使用 "studly caps" 样式命名

名字的首字母应该是小写，每一个新单词应该以大写字母开头

示例:

    connect();
    getData();
    buildSomeWidget();

类的私有成员以_开头，单词间以_连接，全部小写

示例:

    class HFooBar
    {
        private $_status = null;

        protected $field_name = null;

        protected function _sort()
        {
        }
    }

常量

全部大写，单词间以_连接，使用所在的类或包做为前缀 例如HError类中的常量都以"HERROR_"做为前缀

全局变量 以下划线开头，连接类名或包名，再连接下划线和变量名（eg $_HERROR_LEVELS）
