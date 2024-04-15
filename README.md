# Workflow Debugger

```php
Wfd:Ex($exception);
Wfd:Ex($exception, 'Method does not exist for class'.$method);
Wfd:Ex(exception: $exception, exit: true);

class Wfd
{
  public function Ex(Exception $exception, string $msg = '', bool $exit = true)
  {
    if ($msg === '') {
          dump($exception->getMsg());
    }

    if ($msg !== '') {
          dump($exception->getMsg().'with additional info: '.$msg);
    }

    if ($exit) exit;
  }
}
```

Checking if an element exit for an array
```php
Wfd::exist($context, 'next');  // Element  $context['next'] does not exist on line 234 of FILE
Wfd::exist($context, 'next', 'custom message here');  // this will override the above message
```

Output for returns
```php
Wfd::return($value); // Outputs: $value is float:123 on FILE() on line LINE
```
