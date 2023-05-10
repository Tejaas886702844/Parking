# Automated Parking System
Automated Parking System CPSC 531 Advanced Database Management 

#Team Members:
Tejaas Mukunda Reddy: CWID 886702844
Sai Chand Meda: CWID 885237370

Google Colab Link: https://colab.research.google.com/drive/1iIcM2LV_eXZ6o9PMCn7pTxKCbEbW3QFF?usp=sharing

Steps to Run the Application:
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
 
o	Modify the save path variable with the value on 20th cell. Note: keep the .mp4 same as your sources .mp4 name
 
o	Same goes while running the cell 22nd and 24th cell.
o	Note: If you get an error while downloading any files from drive please use the file given on github
o	predict.py file is uploaded
o	cars.mp4 file is uploaded
o	demo.mp4 file is uploaded

7.	For Hadoop Part:
Install Hadoop HDFS on your local machine:
a.	Delete the files in datanode folder
b.	Delete the files in namenode folder 
c.	Run the following commands
i.	#hadoop namenode -format
ii.	#star-all.cmd
iii.	#jps

8.	For Apache Kafka Part:

Install Apache Kafka & Zookeeper
a.	Run the following commands 
i.	C:\kafka>.\bin\windows\zookeeper-server-start.bat .\config\zookeeper.properties
ii.	C:\kafka>.\bin\windows\kafka-server-start.bat .\config\server.properties
iii.	C:\kafka\bin\windows>kafka-topics.bat --create --bootstrap-server localhost:9092 --topic test
iv.	C:\kafka\bin\windows>kafka-console-producer.bat --broker-list localhost:9092 --topic test
v.	C:\kafka\bin\windows>kafka-console-consumer.bat --topic test --bootstrap-server localhost:9092 --from-beginning
b.	Download the CroppedImages.zip and unzip it from github and store it locally
c.	Download the producer.ipynb and consumer.ipynb file from github
i.	Modify the path of the folder_path = 'C:/Users/tejas/OneDrive/Desktop/Latest/DB/CroppedImages/CroppedImages' based on where you have downloaded and unzipped CroppedImages folder
ii.	Run consumer.ipynb first and then run producer.ipynb
iii.	You will see the data being loaded to HDFS
iv.	Run producer code again and you will see the amount being displayed in consumer.ipynb



