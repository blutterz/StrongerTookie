PHP�Ķ������࣬����PHP��PCNTL��POSIX��չ��ʵ�ֲ������ж������ܣ�

Ӧ�ó����磬Ⱥ��������Ϣ���������ݴ���ȣ�

ʹ��˵����

��1������ classes/MooMPC.class.php �ļ�
��2��ʹ�� MooMPC::getInstance() ��ʼ��
��3������ init() �Ļ��Ǽ���Ƿ������� pcntl �� posix ��չ�����ȷ�����ػ����Ѿ����ã����Ժ���
��4������ task() ����������ִ�к���
��5������ exec() ��ʼִ�д�����ִ�ж��������

ʵ�����̣�
    
    ����ο� examples/main.php �ļ���
    ��Ҫ�������£����Զ�ε���task()���ö��ֲ�ͬ������
    ----------------------------------
    MooMPC::getInstance()
        ->init()
        ->task('procFunc1')
        ->task('procFunc2', 2, 'a', $idx)
        ->task(array($pro, 'func1'), 1, 'ok')
        ->task(array($pro, 'func2'), 1, 'hello', 'world')
        ->exec();
    ------------------------------------
