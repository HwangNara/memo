# Memo

### Hexo

###### 배포시 windows10에서 아래와 같은 에러 발생
<pre>
fatal: HttpRequestException encountered.
   �� ��û�� ������ ���� ������ �߻��߽��ϴ�.
bash: /dev/tty: No such device or address
error: failed to execute prompt script (exit code 1)
fatal: could not read Username for 'https://github.com': No error
FATAL Something's wrong. Maybe you can find the solution here: http://hexo.io/docs/troubleshooting.html
Error: fatal: HttpRequestException encountered.
   �� ��û�� ������ ���� ������ �߻��߽��ϴ�.
bash: /dev/tty: No such device or address
error: failed to execute prompt script (exit code 1)
fatal: could not read Username for 'https://github.com': No error

    at ChildProcess.<anonymous> (C:\Users\country\storyof29\node_modules\hexo-util\lib\spawn.js:37:17)
    at emitTwo (events.js:126:13)
    at ChildProcess.emit (events.js:214:7)
    at ChildProcess.cp.emit (C:\Users\country\storyof29\node_modules\cross-spawn\lib\enoent.js:40:29)
    at maybeClose (internal/child_process.js:925:16)
    at Process.ChildProcess._handle.onexit (internal/child_process.js:209:5)
</pre>

아래와 같이 설정해주면 해결
<pre>
  [credential]
    helper = wincred
</pre>
    
<pre> git config --global credential.helper wincred </pre>

출처: https://github.com/tschaub/gh-pages/issues/230#issuecomment-368868268
