# tecnologia
# su codigo esta como bien
# voy a ejecutar una terceros....
SELECT GR001.A_NUMNIT IDENTIFI, 
UPPER( n_apell1 || ' ' || n_apell2 || ' ' || n_nombr1 || ' ' || n_nombr2 || ' ' || n_razons) NOMBRES,
GR001.F_NACIMI FEC_NAC,
GR005.D_TERCER DIRECCION, 
GR005.N_BARRIO BARRIO, 
GR002.N_CIUDAD CIUDAD, 
GR005.T_TERCEL MOVIL, 
GR005.T_TERCER TELEFONO, 
GR003.N_DEPART DEPARTAMENTO, 
GR005.D_EMAIL CORREO_ELE, GR1067.* 
FROM 
GR005MDIRECCIO GR005, 
GR002MCIUDAD GR002, 
GR001MTERCERO GR001, 
GR003MDEPARTAM GR003, 
GR1067MDATTERC GR1067 
WHERE GR005.K_IDTERC = GR001.K_IDTERC 
AND GR001.K_IDTERC = GR1067.K_IDTERC(+) 
AND GR005.K_CIUDAD = GR002.K_CIUDAD 
AND GR005.K_DEPART = GR003.K_DEPART 
AND GR005.I_TIPDIR = 'C' 
ORDER BY 2; 
