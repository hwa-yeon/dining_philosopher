# dining_philosopher
1. hold and wait 방지
 왼쪽 포크와 오른쪽 포크를 한 번에 들도록 한다. 이를 위해 왼쪽 포크와 오른쪽 포크를 요청하는 코드를 원자적으로 처리해주었다. lock과 unlock을 걸어주어 왼쪽 포크를 들면 오른쪽 포크까지 한 번에 요청하도록 처리하였다. 이를 통해 한 포크를 점유하면서 다른 포크를 기다리는 상황을 없앴다. 그러므로 hold and wait이 방지되어 데드락이 일어나지 않는다.

2. circular wait 방지
 포크에 번호를 메기고 이 포크를 작은 번호에서 큰 번호로만 요청하도록 한다. 이를 위해 만약 철학자4라면 오른쪽 포크를 먼저 요청하도록 하였다. 철학자4는 왼쪽 포크인 포크4와 오른쪽 포크인 포크0을 요청하게 된다. 다른 철학자들과 달리 오른쪽 포크의 번호가 더 작다. 그러므로 이러한 처리를 해준 것이다. 이를 통해 circular wait이 방지되어 데드락이 일어나지 않는다.
