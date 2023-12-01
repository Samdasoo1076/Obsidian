![[Pasted image 20231201112423.png]]

![[Pasted image 20231201112712.png]]

값을 넣기 위해선
(해쉬 이름).put("키 이름", "넣을 값")

HashMap을 조회 하려면 KeySet, EntrySet 방법이 있는데

![[Pasted image 20231201112821.png]]
KeySet을 이용해서 순회할 때, get() 메소드로 다시 해시테이블을 조회하는 오버헤드이다.
만약 전체 HashMap 데이터를 순회해야한다면, KeySet 대신 처음부터 EntrySet을 가져와서 사용 해야함.