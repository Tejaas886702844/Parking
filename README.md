# Automated Parking System
Automated Parking System CPSC 531 Advanced Database Management 

Team Members:
Tejaas Mukunda Reddy: CWID 886702844
Sai Chand Meda: CWID 885237370

Google Colab Link: https://colab.research.google.com/drive/1iIcM2LV_eXZ6o9PMCn7pTxKCbEbW3QFF?usp=sharing

#Steps to Run the Application:
For Machine Learning Part

1.	The Github links contains the below file 
a.	Automatic_Number_Plate_Detection_Recognition_YOLOv8_new.zip
b.	Colab Code.ipynb
c.	Colab Code To Test.ipynb
d.	CroppedImages.zip
e.	cars.mp4
f.	consumer.ipynb
g.	demo.mp4
h.	predict.py
i.	producer.ipynb

2.	Open Colab Code.ipynb on google colab (Runtime as GPU)
3.	Unzip and load Automatic_Number_Plate_Detection_Recognition_YOLOv8_new.zip folder onto the google colab (Runtime as GPU)
4.	Run all the cells of Colab Code (Runtime as GPU)
5.	For running cell 6 if you face any issues, please create a roboflow account for accessing their dataset. An api will be assigned which you can use in the code.
6.	While running 18th cell note where the results are saved  
7.	Modify the save path variable with the value on 20th cell. Note: keep the .mp4 same as your sources .mp4 name
8.	Same goes while running the cell 22nd and 24th cell.

o	Note: If you get an error while downloading any files from drive please use the file given on github
o	predict.py file is uploaded
o	cars.mp4 file is uploaded
o	demo.mp4 file is uploaded

9. For Hadoop Part:
Install Hadoop HDFS on your local machine:
1. Delete the files in datanode folder
2. Delete the files in namenode folder 
3. Run the following commands
4. #hadoop namenode -format
5. #star-all.cmd
6. #jps

10.	For Apache Kafka Part:

Install Apache Kafka & Zookeeper
1. Run the following commands 
2. C:\kafka>.\bin\windows\zookeeper-server-start.bat .\config\zookeeper.properties
3. C:\kafka>.\bin\windows\kafka-server-start.bat .\config\server.properties
4. C:\kafka\bin\windows>kafka-topics.bat --create --bootstrap-server localhost:9092 --topic test
5. C:\kafka\bin\windows>kafka-console-producer.bat --broker-list localhost:9092 --topic test
6. C:\kafka\bin\windows>kafka-console-consumer.bat --topic test --bootstrap-server localhost:9092 --from-beginning
7. Download the CroppedImages.zip and unzip it from github and store it locally
8. Download the producer.ipynb and consumer.ipynb file from github
9. Modify the path of the folder_path = 'C:/Users/tejas/OneDrive/Desktop/Latest/DB/CroppedImages/CroppedImages' based on where you have downloaded and unzipped CroppedImages folder
10. Run consumer.ipynb first and then run producer.ipynb
11. You will see the data being loaded to HDFS
12. Run producer code again and you will see the amount being displayed in consumer.ipynb



