# Python_Proyecto

#Analisis
##.1 ¿Cuáles son las habilidades más demandadas para los 3 roles de datos más populares?

Para identificar las habilidades más solicitadas en los 3 puestos de datos más populares, primero filtré los cargos según su popularidad y luego extraje las 5 habilidades principales para cada uno. Este análisis destaca los títulos de trabajo más populares y sus habilidades clave, indicando qué competencias debería priorizar según el rol que me interese.

Mira mi notebook con los pasos detallados aqui:
[SkillsCount.ipynb](PythonProyecto/SkillsCount.ipynb)

### Visualizar Datos

´´´ python
fig, ax = plt.subplots(len(job_titles), 1)

for i, job_title in enumerate(job_titles):
  df_plot = df_skills_perc[df_skills_perc['job_title_short'] == job_title].head(5)
  sns.barplot(data=df_plot, x='skill_percent', y='job_skills', ax=ax[i], hue='skill_count',palette='dark:b_r')

plt.show()
´´´

### Resultados

