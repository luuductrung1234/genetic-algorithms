# Giới thiệu và khái quát về ý tưởng
 - là thuật toán bắt nguồn từ nghiên cứu của John Holland từ đại học Michigan vào năm 1960 nhưng đến những năm 90 thì mới bắt đầu phổ biến. Mục đính chỉnh của nó là giúp giải quyết các vấn đề mà nếu ta sử dụng những thuật toán xác định bình thường sẽ rất tốt kém

**Ví dụ**:   ta muốn tạo ra một chương trình liên tục sinh ra một chuỗi kí tự cho đến khi nào nó khớp với chuỗi kí tự cho trước. Chẳng hạn chuỗi kí tự trong thành ngữ "To be or not to be that is the question" với 39 kí tự. Và ta có một tập hợp các kí tự latin cho trước gồm 27 chữ cái từ a-z. Để có thể sinh một chuỗi kí tự gồm 39 chữ cái một cách ngẫu nhiên từ 27 kí tự cho trước sao cho khớp với thành ngữ, tỉ lệ có thể xảy ra là 1/27 ^ 39 ~ 6.655593703386783+55E. Nếu máy tính cần 1s để sinh tạo ra một chuỗi thì cần thời gian gấp tỉ tỉ lần tuổi của vũ trụ để duyệt hết tất cả trường hợp => Quá lớn

Theo thuật ngữ khoa học máy tính, độ phức tạp của thuật toán này O(27^n). Dẫn đến sự không khả thi khi thực hiện các thuật toán xác định thông thường. Từ đó ta cần một thuật toán khác tốt hơn, hiệu quả hơn  => Genetic Algorithm ra đời, lấy cảm hứng từ học thuyết tiến hoá của Darwin
    + Đứng trên góc nhìn của thuật toán xác định thông thường, cách thức nó sinh ra một giải pháp (trong ví dụ trên là sinh ra một chuỗi kí tự) là tiến hành tuần tự tuyến tính, và hầu như không hề rút kinh nghiệm từ lần này  qua lần khác, cứ thể chạy một cách máy móc
    + Đứng trên góc nhìn của thuật toán Genetic, cách thức nó sinh  ra một giải pháp dự trên học thuyết Darwin, khi mà các giải pháp liên tục được sinh ra, quá trình chọn lọc xuất hiện và tìm ra những giải pháp tốt nhất, sau đó những giải pháp tiếp theo sẽ dựa trên (hay nói cách khác là kế thừa) những thành quả đã đạt được trong những lần thực thi trước đó, tiếp tục biến đổi không ngừng cho đến khi tìm ra giải pháp thoả đáng nhất

 - So về độ phức tạp cài đặt, Generic Algorithm đòi hỏi nhiều tính toán, kiến thức nền tảng về học thuyết di truyền trong sinh học,.... Nhưng so về độ phức tạp thuật toán, ta thấy nó hoạt động hiệu quả hơn các thuật toán xác định thông thường gấp tỉ tỉ lần

 - Ta có thể xem Genetic Algorithms là một ví dụ điển hình trong ngành Khoa học máy tính nói chung và nhánh Trí tuệ nhân tạo nói riêng. Các vận hành của Genetic Algorithms được hiểu như là một hình thức máy học, khi mà ta áp đặt khái niệm tiến hoá vào quá trình cài đặt, giúp chúng biết rút kinh nghiệm, biết học hỏi từ cái sai và cái đúng cũng như ngày càng hoàn thiện dần


 - Tóm gọn lại: Genetic algorithm tập trung vào sự tiến hoá của một nhóm các cá thể cho trước. Trong từng thế hệ,  các cá thể có biểu hiện tốt trước quá trình chọn lọc tự nhiên, sẽ hợp lại cùng nhau để tái sản sinh và chia sẻ các tính trạng di truyền của chúng (gọi là tái tổ hợp). Các thể hệ sau sẽ nhận các tổ hợp tính trạng di truyền khác nhau từ thế hệ trước và ngẫu nhiên xuất hiện các đặc tính dị biến (đột biến)

# Hình thức vận hành
ta có một vấn đề cần giải quyết, và ta sẽ áp dụng Genetic Algorithms với các bước sau:
        + Tạo ra một nhóm cá thế cho trước
        + Đánh giá từng cá thể (liệu chúng có thích hợp với sự chọn lọc, cụ thể là có thích hợp để giải quyết vấn đề không?)
        + Tiến hành chọn lọc cá thể (càng thích hợp thì càng có cơ hội tồn tại)
        + Tiến hành bắt chéo(crossover) và tái sản sinh(reproduction)   (bắt chéo 2 cá thể để sản sinh ra cá thể con mới chứa tính trạng kế thừa từ cả hai cha mẹ)
        + Phát sinh đột biến (một số cá thể con mới dù đã kế thừa nhưng ngẫu nhiên xuất hiện các tính trạng lạ dị biệt)

# Tham khảo
 -  Tài liệu
        ![tech.io](https://tech.io/playgrounds/334/genetic-algorithms/history), 
        ![www.obitko.com](http://www.obitko.com/tutorials/genetic-algorithms/), 
        ![www.schatten.info](http://www.schatten.info/resources_ga.html), 
        ![rednuht.org](http://rednuht.org/genetic_cars_2/)
 -  Video
        ![youtube-the coding train](https://www.youtube.com/watch?v=9zfeTw-uFCw&list=PLRqwX-V7Uu6bJM3VgzjNV5YxVxUwzALHV)
 - Thực hành
        ![stackexchange-lab rat race an exercise](https://codegolf.stackexchange.com/questions/44707/lab-rat-race-an-exercise-in-genetic-algorithms), 
        ![codinggame-coder strike back](https://www.codingame.com/multiplayer/bot-programming/coders-strike-back), 
        ![codinggame-mars lander](https://www.codingame.com/training/easy/mars-lander-episode-1), 
        ![codinggame-fantastic bits](https://www.codingame.com/multiplayer/bot-programming/fantastic-bits), 
        ![codinggame-game of drones](https://www.codingame.com/multiplayer/bot-programming/game-of-drones)


# Mã nguồn mẫu
 - sẽ được cập nhật sớm nhất
