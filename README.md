# Workflow-Debugger

```php
Wfr:Ex($exception);
Wfr:Ex($exception, 'Method does not exist for class'.$method);
Wfr:Ex(exception: $exception, exit: true);

class Wfr
{
  public function Ex(Exception $exception, string $msg = '', bool $exit = true)
  {
    if (empty($msg)) {
          dump($exception->getMsg());
    }

    if (!empty($msg)) {
          dump($exception->getMsg().'with additional info: '.$msg);
    }

    if ($exit) exit;
  }
}
```

Checking if an element exit for an array
```php
Wfr::exist($context, 'next');  // Element  $context['next'] does not exist on line 234 of FILE
Wfr::exist($context, 'next', 'custom message here');  // this will override the above message
```

Output for returns
```php
Wfr::return($value); // Outputs: $value is float:123 on FILE() on line LINE
```
