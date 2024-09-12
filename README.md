from PIL import Image
import requests
import streamlit as st
from streamlit_lottie import st_lottie

st.set_page_config(page_title="<3", page_icon=":face_with_raised_eyebrow", layout="wide")


def load_lottieurl(url):
    r = requests.get(url)
    if r.status_code != 200:
        return None
    return r.json()

lottie_coding = load_lottieurl("https://lottie.host/fa8fa4bd-26d6-40aa-9293-aa808e45b314/55FAjNijyC.json")


with st.container():
    st.title("For Hriizini Hazel Sapriina")
    st.subheader("Hello my love :bouquet:")
    st.write("Here's a website dedicated to you")



with st.container():
    st.write("---")
    left_column, right_column = st.columns(2)
    with left_column:
        st.header("Reasons why you're the best girl")
        st.write("##")
        st.write(
            """
            1. You treat me super good
            2. You're very patient with me
            3. You make me laugh
            4. You make me the happiest person alive!!!
            """
        )
    with right_column:
        st_lottie(lottie_coding, height=300, key="dog")
        
with st.container():
    st.write("---")
    st.header("Songs I want to dedicate to you")
    st.write("##")
    image_column, text_column = st.columns((1,  2))
    with text_column:
        st.subheader("As the world caves in")
        st.write(
            """
          I really like the idea of being together, doing absolutely ordinary things(something as simple as watching TV)
          while the world around us falls apart.
          It would be such a pleasure to die beside you.
          """
        )
        st.markdown("[Click](https://open.spotify.com/track/4JE6agBLHGA5TaF6FlqfBD?si=cde70c02eb3c47f1)")

with st.container():
    with text_column:
        st.subheader("La Vie En Rose")
        st.write(
            """
            I'm honestly such a lovesick fool. I love being in love with you.
            """
        )
        st.markdown("[Click](https://open.spotify.com/track/3lAun9V0YdTlCSIEXPvfsY?si=100e18e3f71a4702)")

with st.container():
    with text_column:
        st.subheader("Misty")
        st.write(
            """
            Loving you and being loved by you feels like what this song sounds like.
            """
        )
        st.markdown("[Click](https://open.spotify.com/track/75KRlncgTKRWd9CjqPZgcx?si=de1ad322d3e04758)")
