import streamlit as st

print("Salut, c'est Faoussane,🤓")
nom_esperé = "nina"
date_naissance_esperee = "2004"

st.title("Message d'anniversaire")

nom = st.text_input("Entrez votre nom :").strip().lower()
if nom == nom_esperé:
    date_naissance = st.text_input("Entrez votre date de naissance (Année seulement) :").strip()
    if date_naissance == date_naissance_esperee:
        st.success("Joyeux anniversaire, Nina ! 🎉")
        st.markdown("""
        ### Message personnalisé :
        Salut Nina😁,

        Je voulais profiter de ce jour spécial pour te souhaiter un très joyeux anniversaire. 🎂🎈  
        Ton soutien et ta gentillesse m'ont énormément aidé l'année passée lorsque nous étions en faculté de médecine.  
        Tu as toujours été là pour moi, disponible à chaque fois que j'avais besoin de toi, et pour cela, je te suis infiniment reconnaissant. 💖  

        C'est un vrai privilège de te connaître et de voir à quel point tu t'épanouis en licence 2. Continue d'être la personne exceptionnelle et généreuse que tu es. 🏥✨  

        Je te souhaite une année remplie de bonheur, de réussite, et de moments inoubliables. Que tous tes rêves se réalisent.  

        Avec toute mon affection,  
        *Faoussane*  
        """)

        # Affichage de l'image
        image_path = "/mnt/data/file-Fiyf1sMuZri8RhWEKwSm6B"
        st.image(image_path, caption="Joyeux anniversaire, Nina !", use_column_width=True)
    else:
        st.error("Ce message n'est pas destiné à vous, programme terminé.")
else:
    st.error("Ce message n'est pas destiné à vous, programme terminé.")
