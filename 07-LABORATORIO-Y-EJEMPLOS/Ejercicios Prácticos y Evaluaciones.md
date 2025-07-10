# Ejercicios Prácticos y Evaluaciones

## Introducción

Esta colección de ejercicios prácticos está diseñada para desarrollar y evaluar competencias reales en ingeniería de prompts. Cada ejercicio incluye múltiples niveles de dificultad, criterios de evaluación específicos, y casos de estudio basados en situaciones empresariales reales.

---

## Nivel Principiante: Fundamentos

### Ejercicio 1: Construcción de Prompts Básicos

**Objetivo:** Dominar la estructura fundamental de un prompt efectivo.

**Escenario:** Eres asistente de marketing en una startup de software B2B que necesita generar copy para redes sociales.

**Tarea:** Diseña prompts para generar contenido de LinkedIn que promocione una nueva feature de tu producto.

**Restricciones:**
- El producto es una herramienta de analytics para equipos de ventas
- La audiencia son sales managers en empresas tech
- Tono profesional pero accesible
- Máximo 280 caracteres por post

**Entregables:**
1. Prompt básico (versión inicial)
2. Prompt mejorado con estructura completa
3. 3 outputs generados
4. Análisis de mejoras aplicadas

**Criterios de Evaluación:**
- **Claridad del rol y contexto (25%):** ¿Define claramente quién es el AI y el contexto?
- **Especificidad de instrucciones (25%):** ¿Las instrucciones son precisas y actionables?
- **Calidad de restricciones (25%):** ¿Las limitaciones están bien definidas?
- **Efectividad del output (25%):** ¿Los resultados cumplen el objetivo?

**Solución de Referencia:**

*Prompt Básico:*
```
Crea posts para LinkedIn promocionando nuestra nueva feature de analytics.
```

*Prompt Mejorado:*
```
# CONTEXTO Y ROL
Eres un growth marketer especializado en B2B SaaS con expertise en LinkedIn organic reach. Tu audiencia son sales managers y heads of sales en empresas tech de 50-500 empleados.

# PRODUCTO
Herramienta de sales analytics que ayuda a equipos de ventas a identificar patrones en su pipeline y optimizar conversion rates. Nueva feature: "Predictive Deal Scoring" que usa ML para predecir probabilidad de cierre.

# TAREA
Genera 3 posts para LinkedIn que generen engagement y awareness sobre la nueva feature.

# ESPECIFICACIONES
- Tono: Profesional pero conversacional, evitar jerga técnica compleja
- Formato: Incluir hook, valor proposition, social proof si es posible
- CTA: Invitar a comentar o hacer preguntas
- Longitud: Máximo 280 caracteres
- Incluir 2-3 hashtags relevantes

# FORMATO DE OUTPUT
Para cada post:
Post [número]:
[Contenido del post]
Hashtags: [lista]
Engagement prediction: [explicación breve]
```

---

### Ejercicio 2: Refinamiento Iterativo

**Objetivo:** Desarrollar habilidades de iteración y optimización de prompts.

**Escenario:** El CEO de tu empresa necesita preparar una presentación para el board sobre performance Q3.

**Tarea Inicial:** Crea un prompt que genere el executive summary de 2 párrafos.

**Datos Disponibles:**
- Revenue Q3: $2.3M (vs $1.8M Q2, target $2.5M)
- New customers: 47 (vs 32 Q2, target 50)
- Churn rate: 3.2% (vs 2.8% Q2, target <3%)
- Burn rate: $400K/month (vs $380K Q2)

**Proceso Requerido:**
1. **Iteración 1:** Prompt básico
2. **Iteración 2:** Incorporar feedback de "muy técnico, necesita más narrativa"
3. **Iteración 3:** Incorporar feedback de "faltan insights accionables"
4. **Iteración 4:** Versión final optimizada

**Criterios de Evaluación:**
- **Evolución del prompt (30%):** ¿Mejora sistemáticamente en cada iteración?
- **Incorporación de feedback (25%):** ¿Integra efectivamente las críticas?
- **Calidad final (25%):** ¿El resultado final es excelente?
- **Reflexión sobre proceso (20%):** ¿Documenta learnings del proceso?

---

### Ejercicio 3: Manejo de Casos Edge

**Objetivo:** Desarrollar robustez en el manejo de situaciones atípicas.

**Escenario:** Sistema de customer support que debe manejar queries diversas y complejas.

**Casos de Prueba:**
1. Query en español sobre producto técnico complejo
2. Queja emocional con múltiples issues mezclados
3. Request de integración técnica con información incompleta
4. Pregunta sobre pricing con contexto específico de nonprofit

**Tarea:** Diseña un prompt que maneje consistentemente todos los casos.

**Requisitos:**
- Respuestas empáticas y profesionales
- Escalación apropiada cuando sea necesario
- Información precisa sin over-promising
- Consistency en tono y approach

---

## Nivel Intermedio: Aplicación Práctica

### Ejercicio 4: Análisis de Datos Complejos

**Objetivo:** Integrar análisis de datos con generación de insights accionables.

**Escenario:** Eres head of data en una e-commerce fashion startup. Necesitas analizar performance de campañas y generar recomendaciones.

**Dataset Proporcionado:**
```
Campaign Performance Q3 2024:
- Instagram Ads: $50K spend, 2.3M impressions, 23K clicks, 890 conversions
- Google Ads: $75K spend, 1.8M impressions, 67K clicks, 1,240 conversions  
- Facebook Ads: $40K spend, 3.1M impressions, 19K clicks, 720 conversions
- Email Marketing: $5K spend, 150K opens, 12K clicks, 450 conversions
- Influencer Partnerships: $30K spend, 800K reach, 15K clicks, 380 conversions

Product Category Performance:
- Dresses: 35% of revenue, 2.8% return rate
- Shoes: 28% of revenue, 4.1% return rate  
- Accessories: 22% of revenue, 1.9% return rate
- Outerwear: 15% of revenue, 3.2% return rate

Customer Segments:
- New customers: 60% of orders, $85 AOV
- Returning customers: 40% of orders, $125 AOV
```

**Tarea:** Crea un prompt que genere un análisis completo con:
1. Performance summary por canal
2. ROI analysis y recommendations
3. Product strategy insights
4. Customer acquisition vs retention strategy
5. Action plan para Q4

**Entregables:**
- Prompt completo
- Output generado
- Validation de datos y cálculos
- Executive summary (1 página)

**Criterios de Evaluación:**
- **Precisión analítica (35%):** ¿Los cálculos y análisis son correctos?
- **Insight quality (30%):** ¿Los insights son valiosos y accionables?
- **Estructura y claridad (20%):** ¿La presentación es clara y lógica?
- **Strategic thinking (15%):** ¿Las recomendaciones son estratégicamente sólidas?

---

### Ejercicio 5: Integración Multi-Modal

**Objetivo:** Trabajar con inputs de diferentes tipos (texto, imágenes, datos estructurados).

**Escenario:** Consultora de retail ayuda a un cliente a optimizar su store layout.

**Inputs Disponibles:**
- Floor plan image del store actual
- Sales data por zona (CSV)
- Customer flow heatmap
- Inventory turnover por categoría
- Competitor analysis report (PDF)

**Tarea:** Diseña un sistema de prompts que:
1. Analice cada input tipo
2. Integre insights cross-functional
3. Genere recomendaciones específicas
4. Priorice implementación por impacto/esfuerzo

**Desafío Adicional:** El cliente tiene budget limitado ($50K) y timeline de 60 días.

---

### Ejercicio 6: Prompt Chains Complejos

**Objetivo:** Diseñar workflows de prompts interconectados.

**Escenario:** Investment fund necesita proceso de due diligence automatizado para startup investments.

**Workflow Requerido:**
1. **Screening inicial:** Review de pitch deck y basic metrics
2. **Market analysis:** TAM/SAM analysis y competitive landscape
3. **Team assessment:** Founder background y team composition
4. **Financial modeling:** Revenue projections y unit economics
5. **Risk assessment:** Key risks y mitigation strategies
6. **Investment thesis:** Final recommendation con terms sheet

**Requisitos:**
- Cada paso debe informar al siguiente
- Decision gates para continuar o stop
- Confidence scoring en cada etapa
- Audit trail completo

**Entregables:**
- Sistema completo de 6 prompts
- Logic flow diagram
- Test con 2 casos reales
- Performance metrics del sistema

---

## Nivel Avanzado: Maestría Profesional

### Ejercicio 7: AI Safety en Aplicaciones Críticas

**Objetivo:** Implementar safeguards en sistemas de alto riesgo.

**Escenario:** Hospital implementa AI assistant para triaje en emergency room.

**Restricciones Críticas:**
- No puede dar diagnósticos médicos
- Debe escalar situaciones life-threatening
- Compliance con HIPAA
- Precisión en priorización >95%
- Explicabilidad completa de decisiones

**Casos de Prueba:**
1. Paciente con chest pain y shortness of breath
2. Niño con fever y rash
3. Adulto mayor con confusion y weakness
4. Accidente con multiple injuries
5. Mental health crisis

**Tarea:** Diseña sistema de prompts con safeguards robusts que maneje todos los casos apropiadamente.

**Evaluación Incluye:**
- Safety testing con red team scenarios
- Compliance review con healthcare expert
- Performance bajo stress conditions
- Fail-safe mechanism effectiveness

---

### Ejercicio 8: Optimización Multi-Objetivo

**Objetivo:** Balancear objetivos conflictivos en sistemas complejos.

**Escenario:** Global supply chain optimization durante crisis (pandemic, war, natural disasters).

**Objetivos Conflictivos:**
- Minimizar costos operativos
- Maximizar resilience y backup options
- Reducir environmental impact
- Mantener service levels
- Cumplir regulatory requirements

**Variables:**
- 50+ supplier locations
- 12 product categories
- 8 destination markets
- Seasonal demand patterns
- Geopolitical risk factors

**Tarea:** Crea sistema de prompts que optimize decisions considerando todos los objetivos con weights dinámicos.

**Complejidad Adicional:** Weights de objetivos cambian based on external conditions (crisis level, regulatory changes, etc.).

---

### Ejercicio 9: Self-Improving Systems

**Objetivo:** Diseñar prompts que evolucionan basado en performance feedback.

**Escenario:** Customer service chatbot que debe mejorar continuously basado en satisfaction scores y resolution rates.

**Requisitos:**
- Auto-detection de performance degradation
- Automatic prompt adjustment based on patterns
- A/B testing integration para nuevas versions
- Learning desde successful human interventions
- Rollback capability si performance drops

**Métricas de Éxito:**
- Customer satisfaction score >85%
- First contact resolution >70%
- Escalation rate <15%
- Response time <30 seconds
- Continuous improvement trend

**Entregables:**
- Core prompt system
- Self-optimization mechanism
- Performance monitoring dashboard
- Case studies de mejoras automáticas

---

## Evaluaciones Integrales

### Proyecto Final: Sistema Empresarial Completo

**Duración:** 2 semanas

**Escenario:** Consulting firm especializada en digital transformation necesita sistema integral de AI para:
- Lead qualification automática
- Proposal generation customizada
- Project scoping y resource allocation
- Progress tracking y client reporting
- Knowledge management y lessons learned

**Requisitos del Sistema:**
1. **Multi-tenant:** Diferentes clients con needs específicos
2. **Scalable:** Handle 1000+ projects simultaneously
3. **Secure:** Client confidentiality y data protection
4. **Auditable:** Complete trail de decisions y changes
5. **User-friendly:** Non-technical staff can operate

**Entregables Finales:**
1. **System Architecture:** Complete design document
2. **Prompt Library:** 20+ production-ready prompts
3. **Integration Specs:** APIs y data flow diagrams
4. **Testing Results:** Performance metrics y user acceptance
5. **Deployment Plan:** Rollout strategy y change management
6. **Maintenance Guide:** Monitoring y update procedures

**Criterios de Evaluación:**
- **Technical Excellence (30%):** Quality y robustness del system design
- **Business Value (25%):** Potential ROI y strategic impact
- **Implementation Feasibility (20%):** Realistic approach y timeline
- **Innovation (15%):** Creative solutions y cutting-edge approaches
- **Documentation Quality (10%):** Clarity y completeness de deliverables

---

## Metodología de Evaluación

### Scoring Framework

**Nivel Principiante (Ejercicios 1-3):**
- **Novice (0-59%):** Basic understanding, requires significant support
- **Competent (60-74%):** Solid foundation, ready for guided practice
- **Proficient (75-89%):** Independent work capability
- **Advanced (90-100%):** Teaching capability, innovation potential

**Nivel Intermedio (Ejercicios 4-6):**
- **Developing (0-69%):** Needs additional practice y support
- **Competent (70-84%):** Ready for professional responsibilities
- **Advanced (85-94%):** Senior practitioner level
- **Expert (95-100%):** Thought leadership capability

**Nivel Avanzado (Ejercicios 7-9):**
- **Competent (0-79%):** Functional in complex environments
- **Advanced (80-89%):** Leadership in technical projects
- **Expert (90-95%):** Industry recognition level
- **Master (96-100%):** Research y innovation contributions

### Feedback Framework

**Immediate Feedback (Durante ejercicios):**
- Hint system para guidance
- Progress indicators
- Real-time validation

**Comprehensive Feedback (Post-ejercicio):**
- Detailed rubric scores
- Specific improvement areas
- Best practice examples
- Next learning steps

**Peer Learning Integration:**
- Collaborative exercises
- Peer review assignments
- Knowledge sharing sessions
- Mentorship programs

---

*Esta suite de ejercicios debe completarse en secuencia, building competencias incrementalmente hacia maestría profesional.*
