7. Try to answer the following questions, and write the answer in the and new file readme.md in 
you repository.  
- What is amqp?
AMQP adalah singkatan dari Advanced Message Queuing Protocol. AMQP memungkinkan terjadinya komunikasi secara asinkronus. AMQP dirancang untuk memfasilitasi pertukaran pesan antara aplikasi dengan menyediakan berbagai fitur, seperti antrean pesan, pengalihan, keandalan, dan keamanan. AMQP memungkinkan aplikasi client untuk bisa berkomunikasi dengan aplikasi sumber


- What it means? guest:guest@localhost:5672 , what is the first guest, and what is 
the second guest, and what is localhost:5672 is for?
Guest pertama merupakan nama pengguna yang akan mengakses broker AMQP. Guest kedua merupakan kata sandi dari pengguna. "localhost:5672" terdiri dari dua bagian, yaitu "localhost" dan "5672". "5672" menunjukkan nomor port tempat broker AMQP berjalan. "localhost" menunjukkan bahwa hostnya terdapat pada local machine.

Picture of Running RabbitMQ while sending and processing event with sleep:
![rabbit](img/rabbitmq-slow-screenshot.png)
Gambar diatas menunjukkan adanya banyaknya message yang dikirim oleh publisher. Kita juga dapat melihat bahwa Consumer Ack bernilai 1, yaitu consumer menerima satu message per detik yang disebabkan oleh sleep selama satu detik. Kenaikan message yang dikirim oleh publisher secara masif mengakibatkan penumpukan pada queue karena subscriber hanya bisa menerima satu message per detik.