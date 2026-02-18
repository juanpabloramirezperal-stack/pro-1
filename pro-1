
# Título y Descripción
st.title("🛍️ La Calculadora de Rebajas")
st.markdown("Bienvenido. Introduce tus datos para calcular las rebajas de tu producto.")
st.write("---") # Línea separadora

# 2. Entrada de Datos (Barra Lateral)
st.sidebar.header("Tus Datos")
preciooriginal = st.sidebar.number_input("precio original (€)", min_value=0, max_value=200, value=60)
rebaja = st.sidebar.slider("Tu rebaja (%)", 00, 100, 15)

# 3. Botón de Cálculo y Lógica
if st.button("Calcular ahora"):
    
    # Fórmula Matemática: Peso entre altura al cuadrado
    precio = preciooriginal * (rebaja / 100)
    ahorro = preciooriginal - precio
    
    # 4. Mostrar Resultado con Diseño
    col1, col2 = st.columns(2)
    
    with col1:
        # Usamos metric para que el número se vea grande
        st.metric(label="precio final:", value=f"{ahorro:.2f}")
        st.success(f"Te ahorras {precio}")
        
    with col2:
        # Usamos condicionales (if/elif/else) para el diagnóstico
        if rebaja > 50:
            st.error("buena compra")
            st.balloons()
        elif rebaja < 25:
            st.error("algo es algo")
            st.balloons() # ¡Premio!
