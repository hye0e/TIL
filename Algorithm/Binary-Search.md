### 이분 탐색 알고리즘

- " 정렬되어 있는" (이분 탐색의 주요 조건) 배열에서 데이터를 찾으러 시도할 때, 순차 탐색처럼 처음 부터 모든 데이터를 체크 하여 값을 찾는 것이 아닌, 탐색 범위를 절반씩 줄여 가며 찾아가는 Search 방법이다.
- 자료들의 집합에서 특정 자료를 찾고자 할 때,  많이 사용 되며 매우 빠른 탐색의 알고리즘이다.
- '분할 후 정복(divide and conquer)'의 전략을 사용하기 때문에 실행 시간은 log의 설정을 갖는다.


> 이분 탐색 알고리즘 구현 JAVA

    public class BinarySearch {
    	public static void main (String[] args) {
    		int[] arr = {1, 2, 3, 4, 5, 6, 7, 8, 9};
    		binarySearch(2, arr); // 
    	}
    
    	public static void binarySearch(int iKey, int[] arr) {
    		int mid;
    		int left = 0;
    		int right = arr.length - 1;
    
    		mid = (right + left) / 2;
    		while (right >= left) {
    			if (iKey == arr[mid]) {
    				System.out.println("Find iKey ! Array index value: " + mid);
    				break;
    			}
    
    			if (iKey < arr[mid]) {
    				right = mid - 1;
    			} else {
    				left = mid + 1;
    			}
    		}
    	}
    }
    
출처: [https://blog.opid.kr/489](https://blog.opid.kr/489) [opid's document]