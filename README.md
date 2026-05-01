# Bardo-anal-tico-
Palantir kan 
import streamlit as st

# Configuración visual
st.set_page_config(page_title="Inti Kan Insights", page_icon="☀️")

# Estética de marca: Negro y Dorado
st.markdown("""
    <style>
    .stApp { background-color: #000000; color: #FFD700; }
    h1, h2, h3 { color: #FFD700 !important; }
    .stButton>button { background-color: #FFD700; color: black; border-radius: 10px; }
    </style>
    """, unsafe_allow_html=True)

st.title("☀️ INTI KAN EL BARDO")
st.subheader("Herramienta de Crecimiento Estratégico")

# --- SECCIÓN 1: INTERPRETACIÓN DE MÉTRICAS ---
st.header("📊 Oráculo de Datos")
st.write("Mira tus números en Spotify/YouTube y analicémoslos:")

col1, col2 = st.columns(2)
with col1:
    vistas = st.number_input("Vistas (YouTube)", min_value=0, step=1)
with col2:
    oyentes = st.number_input("Oyentes (Spotify)", min_value=0, step=1)

if st.button("Interpretar mi situación"):
    if vistas > 0 and oyentes > 0:
        ratio = vistas / oyentes
        if ratio > 2:
            st.success("🔥 El bardo es visual: Tienes buena imagen. ¡Mueve a esa gente a Spotify con links directos!")
        else:
            st.warning("🎵 El bardo es auditivo: Tu música gusta, pero falta que vean tu cara. ¡Saca más Shorts!")
    else:
        st.info("Ingresa datos para recibir el consejo del sol.")

# --- SECCIÓN 2: CRECIMIENTO PERSONAL ---
st.header("⚔️ Disciplina del Bardo")
opcion = st.radio("¿En qué enfocamos hoy?", ["Escritura", "Marketing", "Salud Mental"])

if opcion == "Escritura":
    st.write("📝 *Reto:* Escribe 4 barras sobre el frío de Bogotá sin usar la palabra 'frío'.")
elif opcion == "Marketing":
    st.write("📱 *Reto:* Toma un video de 15 seg de una calle de tu barrio y ponle de fondo tu mejor tema.")
else:
    st.write("🧘 *Reto:* 10 min de silencio. Un bardo necesita escuchar el mundo para poder contarlo.")

st.sidebar.write("Hecho para Inti Kan el Bardo")
