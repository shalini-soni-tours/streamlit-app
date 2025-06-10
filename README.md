import streamlit as st
import pandas as pd
import numpy as np
import matplotlib.pyplot as plt

# Title
st.title("Tour Website by Shalini")

# Introduction
st.write("Welcome to my interactive tour website built with Streamlit!")

# Example: Displaying data
df = pd.DataFrame({
    'Location': ['Delhi', 'Agra', 'Jaipur', 'Mumbai'],
    'Visitors': [12000, 8500, 9400, 11000]
})

st.write("### Tour Statistics")
st.dataframe(df)

# Example: Simple Plot
st.write("### Visitor Trends")
fig, ax = plt.subplots()
ax.bar(df['Location'], df['Visitors'], color='skyblue')
st.pyplot(fig)

# User Input Example
name = st.text_input("Enter your name:")
if name:
    st.write(f"Hello, {name}! Hope you enjoy exploring the tours.")

# Footer
st.write("---")
st.write("Powered by Streamlit | Created by Shalini")
