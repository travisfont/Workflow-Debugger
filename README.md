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
