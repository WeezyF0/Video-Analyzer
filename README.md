# Video-Analysis
This model uses a pipeline of LLaVa (Vision Language Model), T5 (for Summarization) and OpenCV (for keyframe extraction). It analyzes and can answer user prompts and generate concise summary of small videos and clips. 

Due to the nature of video processing being resource intensive and colab free tier having memory constraints on t4, it can be improved by quite a bit on availability of better hardware. 

moondream + OpenCV : very very slow.

QwenVL + YOLO : Out of Memory error on colab. (Ideally the best option for the task on hardware availability).

Blip + OpenCV: Fast but extremely brief and generic (1 liners)



Produced Output for sample videos:
#1
![image](https://github.com/user-attachments/assets/2df0b481-832a-4d7a-906a-ee95917f74b0)
the video captures a snowy street scene with a car driving down the road . the street is lined with houses, and there are multiple cars parked or driving along the road. the overall atmosphere of the scene is calm and quiet, with no visible signs of activity .

#2
![image](https://github.com/user-attachments/assets/394ed4db-8390-4126-a65c-aff51ed61028)
A video shows a large fire burning in a city, with smoke billowing into the sky. The fire appears to be near a building, as there is smoke coming from that direction. The video captures the intensity of the fire and the impact it has on the cityscape. In this video, there is a large fire burning in a city, with black smoke billowing from the fire. The fire is located near an apartment building and seems to be spreading rapidly. The scene is quite dramatic, with the fire's intensity making it difficult to focus on the details. Tuation for the city and its residents. tuation for city and their residents. The city is in the midst of a major crisis. It is the first time in its history that the city has been forced to close its doors for more than a year.






