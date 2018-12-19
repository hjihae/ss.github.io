---
title: "code"
layout: post
date: 2018-12-19 22:10
tag: jekyll
image: http://hjihae.github.io/hanyang.jpg
headerImage: false
projects: true
hidden: true # don't count this post in blog pagination
description: "This is a simple and minimalist template for Jekyll for those who likes to eat noodles."
category: project
# author: johndoe
externalLink: false
---

#pragma config(Sensor, S1,     c1,             sensorEV3_Color)
#pragma config(Motor,  motorB,          rm,            tmotorEV3_Large, PIDControl, encoder)
#pragma config(Motor,  motorC,          rm,            tmotorEV3_Medium, PIDControl, encoder)

#define Blue 2
#define Green 3
#define Red 5


int color,cs;




task main()
{

   while(1)
   {
      setMotorSpeed(motorB, 8);
      color = getColorName(cs);


      if(color == Blue){
         setMotorSpeed(motorB, 0);
         sleep(1000);
         setMotorSpeed(motorB, 8);
         sleep(1000);
         setMotorSpeed(motorC, 30);
         sleep(1200);
         setMotorSpeed(motorC,0);
         sleep(500);
         setMotorSpeed(motorB, 0);
         sleep(500);
      }

      else if(color == Red){
         setMotorSpeed(motorB, 0);
         sleep(1000);
         setMotorSpeed(motorB,8);
         sleep(1000);
         setMotorSpeed(motorC, -30);
         sleep(1200);
         setMotorSpeed(motorC,0);
         sleep(500);
         setMotorSpeed(motorB, 0);
         sleep(500);
      }
   }
}


