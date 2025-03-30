# A BMI Calculator Using Python
- A mini project BMI calculator which is used to check whether a person is healthy or not according to the weight and height
- BMI calculator is made using python
- Streamlit library is used to develop user interacting module

# Aims
- Provides a good user interface
- Helpful to check whether you are healthy or not
- Can take remdies if you are not healthy

 It is written using jupyter notebook

# Code 

import streamlit as st
name = st.text_input('Enter your name:')
weight_input = st.number_input('Enter Weight(in Kg): ', format = '%.2f')
height_input = st.number_input('Enter Your Height(in Kg): ', format = '%.2f')
if st.button('Calculate BMI'):
    if not weight_input or not height_input:
        st.write('Enter Valid Weight or Height')
    else:
        bmi = (weight_input)/(height_input ** 2)
        if bmi < 18.5:
            st.write(f"{name},Your BMI is {bmi} and You are Under weight")
        elif bmi > 18.5 and bmi <= 24.9:
            st.write(f"{name},Your BMI is {bmi} and You are Healthy")
        elif bmi > 25 and bmi <= 30:
            st.write(f"{name},Your BMI is{bmi} and You are Overweight")
        elif bmi >30 and bmi <= 34.9:
            st.write(f"{name},Your BMI is {bmi} and You are Class 1 Obesity")
        elif bmi > 34.9 and bmi <= 39.9:
            st.write(f"{name},Your BMI is {bmi} and You are Class 2 Obesity")
        elif bmi > 39.9:
            st.write(f"{name},Your BMI is {bmi} and You are Class 3 Obesity(Severe Obesity)")

