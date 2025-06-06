# class MyAGVPro()

### 1. ϵͳ & ��Ʒ��Ϣ

#### def get_system_version(self) -> None:
- **����:** ��ȡ���̼��汾��
- **����ֵ:**
  - **float: version**

#### def get_modify_version(self) -> None:
- **����:** ��ȡ�ι̼��汾��
- **����ֵ:**
  - **int: version**

#### def power_on(self) -> None:
- **����:** ����������
- **����ֵ:**
  - **int: �������, 1: �ɹ�, 0: ʧ��**

#### def power_on_only(self) -> None:
- **����:** ���������ˣ������������Ƴ���
- **����ֵ:**
  - **int: ���������, 1: �ɹ�, 0: ʧ��**

#### def power_off(self) -> None:
- **����:** �رջ�����
- **����ֵ:**
  - **int: ���رս��, 1: �ɹ�, 0: ʧ��**

#### def is_power_on(self) -> None:
- **����:** ���������Ƿ��ѿ���
- **����ֵ:**
  - **int: ��Դ״̬, 1: ����, 0: �ر�**

### 2. �˶�����

#### def move_backward(self, speed) -> None:
- **����:** ƽ�ƻ��������
- **����:**
  - **speed(float): 0 ~ 1.5 m/s**
- **����ֵ:**
  - **int: 1: �ɹ�, 0: ʧ��**

#### def move_forward(self, speed) -> None:
- **����:** ƽ�ƻ�������ǰ
- **����:**
  - **speed(float): 0 ~ 1.5 m/s**
- **����ֵ:**
  - **int: 1: �ɹ�, 0: ʧ��**

#### def move_left_lateral(self, speed) -> None:
- **����:** ƽ�ƻ���������
- **����:**
  - **speed(float): 0 ~ 1 m/s**
- **����ֵ:**
  - **int: 1: �ɹ�, 0: ʧ��**

#### def move_right_lateral(self, speed) -> None:
- **����:** ƽ�ƻ���������
- **����:**
  - **speed(float): 0 ~ 1 m/s**
- **����ֵ:**
  - **int: 1: �ɹ�, 0: ʧ��**

#### def turn_left(self, speed) -> None:
- **����:** ������ת
- **����:**
  - **speed:**
- **����ֵ:**
  - **int: 1: �ɹ�, 0: ʧ��**

#### def turn_right(self, speed) -> None:
- **����:** ������ת
- **����:**
  - **speed:**
- **����ֵ:**
  - **int: 1: �ɹ�, 0: ʧ��**

#### def stop(self) -> None:
- **����:** ֹͣ�ƶ�
- **����ֵ:**
  - **int: 1: �ɹ�, 0: ʧ��**

#### def set_auto_report_state(self, state) -> None:
- **����:** �����Զ�����״̬
- **����:**
  - **state(int): 0: �ر�, 1: ����**
- **����ֵ:**
  - **int: 1: �ɹ�, 0: ʧ��**

#### def get_auto_report_state(self) -> None:
- **����:** ��ȡ�Զ�����״̬
- **����ֵ:**
  - **int: 0: �ر�, 1: ����**

#### def get_auto_report_message(self) -> None:
- **����:** ��ȡ�Զ�������Ϣ
- **����ֵ:**
  - **list[int | list[int] | float]:**
  - **0 - (float)rx**
  - **1 - (float)ry**
  - **2 - (float)rw**
  - **3 - (list[int])����״̬**
  - **4 - (list[int])�����Ϣ**
  - **5 - (float)��ص�ѹ**
  - **6 - (int)���ʹ��״̬ 0: ����, 1: ����**

### 3. �������

#### def get_motor_enable_status(self) -> None:
- **����:** ��ȡ���ʹ��״̬
- **����ֵ:**
  - **list[int]: ���ʹ��״̬**
  - **0: ����**
  - **1: ����**

#### def get_motor_status(self) -> None:
- **����:** ��ȡ���״̬
- **����ֵ:**
  - **list[int]: ���״̬**
  - **0: ����**
  - **any: �������**

#### def get_motor_temps(self) -> None:
- **����:** ��ȡ����¶�
- **����ֵ:**
  - **list[float]: ����¶�**

#### def get_motor_speeds(self) -> None:
- **����:** ��ȡ����ٶ�
- **����ֵ:**
  - **list[float]: ����ٶ�**

#### def get_motor_torques(self) -> None:
- **����:** ��ȡ���Ť��
- **����ֵ:**
  - **list[float]: ���Ť��**

#### def set_communication_state(self, state) -> None:
- **����:** ����ͨѶ״̬
- **����:**
  - **state(int):**
  - **0: ����ͨѶ (Ĭ��)**
  - **1: Socket ͨѶ**
  - **2: ����ͨѶ (�� MAC ��ַд���ļ��Ͷ˵㣬Ȼ�󷵻ص���״̬)**
- **����ֵ:**
  - **int: 1: �ɹ�, 0: ʧ��**

#### def get_communication_state(self) -> None:
- **����:** ��ȡͨѶ״̬
- **����ֵ:**
  - **int: ͨѶ״̬**
  - **0: ����ͨѶ,**
  - **1: Socket ͨѶ,**
  - **2: ����ͨѶ**

#### def set_led_color(self, position, brightness, color) -> None:
- **����:** ���� LED ��ɫ
- **����:**
  - **position(int):**
  - **0: ��� LED**
  - **1: �Ҳ� LED**
  - **brightness(int): 0 - 255**
  - **color(tuple(int, int, int)): RGB ��ɫ**
- **����ֵ:**
  - **int: 1: �ɹ�, 0: ʧ��**

#### def get_motor_loss_count(self) -> None:
- **����:** ��ȡ�����������
- **����ֵ:**
  - **list[int]: �����������**

### 4. IO ����

#### def get_pin_input(self, pin) -> None:
- **����:** ��ȡ���� IO
- **����:**
  - **pin(int): 1, 2, 3, 4, 5, 6, 7, 8, 254**
- **����ֵ:**
  - **int: 0: �͵�ƽ, 1: �ߵ�ƽ, -1: û���������**

#### def set_pin_output(self, pin, state) -> None:
- **����:** ������� IO
- **����:**
  - **pin(int): 1 - 6**
  - **state(int): 0: �͵�ƽ, 1: �ߵ�ƽ**
- **����ֵ:**
  - **int: 1: �ɹ�, 0: ʧ��**

### 5. WiFi & ����

#### def get_wifi_ip_port(self) -> None:
- **����:** ��ȡ wi-fi ip �Ͷ˿�
- **����ֵ:**
  - **tuple(str, int): wi-fi ip, wi-fi �˿�**

#### def get_wifi_account(self) -> None:
- **����:** ��ȡ wi-fi �˺�
- **����ֵ:**
  - **tuple(str, str): wi-fi �˺�, wi-fi ����**

#### def get_bluetooth_address(self) -> None:
- **����:** ��ȡ���� MAC ��ַ
- **����ֵ:**
  - **str: ���� MAC ��ַ**

#### def get_bluetooth_uuid(self) -> None:
- **����:** ��ȡ���� uuid
- **����ֵ:**
  - **tuple(str, str, str): ��������, ���� uuid, ���� uuid**
