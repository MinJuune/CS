## 1. Process와 Thread의 차이점에 대해 설명해 보세요.  

**Process**는 실행 중인 독립적인 프로그램 단위이고,  
**Thread**는 Process 내에서 실행되는 여러 흐름 단위입니다.  

<br><br>

## 2. Context Switching에 대해 설명해 보세요.  

**Context Switching**은 CPU가 현재 작업 중인 Process에서 다른 Process로 전환될 때,  
지금까지의 Process 상태를 저장하고, 새로운 상태를 불러와서 실행하는 과정입니다.  

<br><br>

## 3. Race Condition에 대해, 그리고 이를 방지하기 위한 방법에 대해 설명해 보세요.  

**Race Condition**은 여러 Thread가 공유 자원에 동시에 접근하면서 결과가 예측 불가능해지는 현상입니다.  
Race Condition 방지 방법으로는 Mutex, Semaphore 등이 있습니다.  
**Mutex**는 한 번에 하나의 Thread만 공유 자원에 접근하도록 Lock을 거는 방식입니다.  
**Semaphore**는 접근 가능한 Thread의 수를 제한하는 동기화 도구입니다.  

<br><br>

## 4. Deadlock의 발생 조건과 해결 방법에 대해 설명해 보세요.  

**Deadlock**은 둘 이상의 Process가 서로 자원을 기다리며 영원히 대기하는 상태입니다.  
예를 들어 Process A가 자원 1을 점유한 채로 자원 2를 기다리고, Process B가 자원 2를 점유한 채로 자원 1을 기다리는 상황을 말합니다.  

<br><br>

## 5. Virtual Memory와 Page Replacement 알고리즘에 대해 설명해 보세요.  

**Virtual Memory**는 실제 물리 메모리보다 큰 공간을 가상의 주소 공간으로 사용하는 기술입니다.  
**Page Replacement 알고리즘**은 메모리가 가득 찬 상태에서 새로운 Page를 불러와야 할 때, 어떤 Page를 내보낼지 결정하는 알고리즘입니다.  

<br><br>

