# pacman.ttnt
CÂU HỎI 1 : http://ai.berkeley.edu/search.html#Q1
![image](https://user-images.githubusercontent.com/103712313/163513887-b04ee8c4-a31d-45f4-9916-b9f244b84e21.png)
nodeStack- ngăn được sử dụng để chứa các nút trong DFS quá trình duyệt.    

oldNode- 1 bộ lưu trữ các nút đã được duyệt qua

currentNodeState- trạng thái, trạng thái của nút hiện tại đang duyệt tới

move- bước đi (hành động) từ ban đầu vị trí đến hiện tại nút

👉Duyệt DFS cho đến khi nodeStackkhông có phần tử nào hoặc khi đạt đếngoalState




CÂU HỎI 2 : http://ai.berkeley.edu/search.html#Q2
![image](https://user-images.githubusercontent.com/103712313/163514017-a297d08b-a055-411d-a8ac-f43ea49a37c0.png)
👉Tương tự Question 1nhưng thay vì sử dụng, Stackthì ta sử dụng Queuecho BFS duyệt



CÂU HỎI 3:http://ai.berkeley.edu/search.html#Q3
![image](https://user-images.githubusercontent.com/103712313/163514104-7abec15a-6b04-454a-9cec-4f7d5db1568b.png)
👉Thay vì sử dụng Queue thông thường, ta sử dụng PriorityQueue (hàng đợi ưu tiên) để duyệt UCS. Các nút có mức độ ưu tiên cao hơn (chi phí thấp hơn) sẽ được duyệt trước.

👉 oldNodeuse the type dictbecause setas the question before

👉Trong quá trình duyệt các nút, nếu phát hiện ra chi phí thấp hơn để tiến tới, currentNodeStatethì đánh dấu tiến độ lại chi phí cho currentNodeStatetrongoldNode

👉Duyệt UCSđến khi nodePriorityQueuekhông có phần tử nào hoặc khi đạt tớigoalState



CÂU HỎI 4:http://ai.berkeley.edu/search.html#Q4
![image](https://user-images.githubusercontent.com/103712313/163514212-fe571741-130f-42ea-a758-f3bad69fc1c3.png)
👉Tương Priority Queuetự sử dụng Câu hỏi 3.

👉Change of per node of the priority of public format in Priority Queuethe publicF = G + H



CÂU HỎ 5:http://ai.berkeley.edu/search.html#Q5
![image](https://user-images.githubusercontent.com/103712313/163514297-deb464c4-e28e-4eef-861f-54d67c3f9ae6.png)
👉In init function saveback the start status of Pacman, may be get by function getStartState(...). Kiểm tra Pacman khi bắt đầu ở bất kỳ góc nào hay chưa.

👉 isGoalState(...)kiểm tra Pacman đã tới tất cả các góc hay chưa và trả về True / False

👉 getSuccessors(...)kiểm tra hướng dẫn (xem có tường hay không), cập nhật trạng thái và trả về các successorsthứ có thể đi được.

👉Sử dụng tìm kiếm thuật toán đã làm ở các Câu hỏi trên để giải quyết bài toán


CÂU HỎI 6 http://ai.berkeley.edu/search.html#Q6
![image](https://user-images.githubusercontent.com/103712313/163514368-5d8f58a3-482b-460c-9b91-b2fa60c715b1.png)
👉Tạo thêm 2 mới hàm findClosestPointvà findFarthesetPointtrả về nút gần nhất và xa nhất với nút hiện tại máy chủ tính toán ở Câu hỏi # 6 và # 7

👉Mảng unvisitedCornerchứa các khung không được đi tới

👉 Heuristic= currentToClosest+closestToFarthest



CÂU HỎI 7:http://ai.berkeley.edu/search.html#Q7
![image](https://user-images.githubusercontent.com/103712313/163514406-78f63f72-5560-4857-96d7-d549374ba50f.png)
findClosestPointvà findFarthesetPointviết từ Câu hỏi số 6

👉Thay vì một mảng chứa các góc quay như # 6, ở # 7, ta dùng danh sách foodListđể lưu trữ thức ăn.

👉Tương tự thuật toán với Câu hỏi số 6



CÂU ỎI 8:http://ai.berkeley.edu/search.html#Q8
![image](https://user-images.githubusercontent.com/103712313/163514475-d192ce5c-fe10-43f1-9b75-53af7707c014.png)
👉Use BreathFirstSearch thuật toán để giải quyết bài toán

👉 isGoalStatereturn about the status of the current location must be target or not
