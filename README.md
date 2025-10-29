# Desafío DIO: Implementando mi Primera Stack con AWS CloudFormation
# Anna Elizabeth Parra Rausseo
# https://github.com/annaeparrar/

> **Status:** Concluído

## Descripción del Desafío

Este repositorio documenta mi experiencia en la implementación de mi primera **Stack con AWS CloudFormation**, un componente central del desafío de proyecto propuesto por la [DIO (Digital Innovation One)](https://www.dio.me/).

El objetivo principal es practicar la **automatización de infraestructura en la nube** utilizando AWS CloudFormation, a través de la creación y ejecución de *templates* en formato **YAML** o **JSON**. Durante el proceso, simulé desafíos reales como la creación de recursos AWS (por ejemplo, instancias EC2, servidores web y reglas de seguridad), aplicando el concepto de **Infraestructura como Código (IaC)**, y documentando mi camino de aprendizaje.

---

## Objetivos de Aprendizaje Demostrados

Al completar y documentar este desafío, demuestro mi capacidad para:

* **Aplicar Conceptos Prácticos:** Utilizar los conocimientos adquiridos en las aulas de la DIO sobre AWS CloudFormation en un entorno real.
* **Documentación Técnica:** Crear y mantener una documentación técnica clara y estructurada, incluyendo *insights* y anotaciones personales.
* **Infraestructura como Código (IaC):** Entender y aplicar los principios de IaC, incluyendo versionamiento, reutilización de *templates* y buenas prácticas de aprovisionamiento de recursos en AWS.
* **Uso de GitHub:** Utilizar GitHub como herramienta central para el versionamiento, organización y compartición de la documentación técnica.

---

## Contenido del Repositorio

Este repositorio está organizado para servir como material de apoyo y registro de mi proceso de aprendizaje:

* **`README.md` (Este Archivo):** Visión general del desafío, objetivos, contenido y *insights* clave.

---

## Insights y Anotaciones Clave

A continuación, se listan los puntos clave de mi experiencia con AWS CloudFormation:

### 1. Estructura de un Template CloudFormation

* **`AWSTemplateFormatVersion`:** Esencial para definir la versión del formato del *template*.
* **`Description`:** Buenas prácticas para dar un contexto claro a la *Stack*.
* **`Parameters`:** Crucial para hacer el *template* reutilizable, permitiendo que el usuario ingrese valores (como el tipo de instancia o el nombre de un *key pair*) en el momento de la creación.
* **`Resources`:** La sección principal donde se definen los recursos AWS a crear (e.g., `AWS::EC2::Instance`, `AWS::S3::Bucket`, etc.).
* **`Outputs`:** Importante para exportar valores clave (e.g., la URL pública de un servidor o el ID de un recurso) que pueden ser utilizados por otras *Stacks*.

### 2. Infraestructura como Código (IaC)

* **Versionamiento:** La capacidad de guardar el *template* en GitHub permite el versionamiento del diseño de la infraestructura, facilitando la auditoría y la reversión a estados anteriores.
* **Automatización:** CloudFormation elimina la necesidad de aprovisionamiento manual a través de la consola, garantizando que el entorno se construya de forma consistente y repetible.
* **Reutilización:** Mediante el uso de `Parameters`, el mismo *template* puede ser usado para desplegar entornos de desarrollo, *staging* y producción con mínimas modificaciones.

### 3. Desafíos Encontrados y Soluciones

> *\[Aquí puedes añadir un punto de dolor que tuviste, como un error de sintaxis YAML, un problema de dependencias entre recursos, o un error de IAM, y cómo lo resolviste. Ejemplo: ]*
>
> * **Desafío:** Inicialmente, mi instancia EC2 fallaba al iniciarse.
> * **Solución:** Descubrí que el *Security Group* no estaba referenciado correctamente en la propiedad `SecurityGroupIds` de la instancia. Corregí la referencia utilizando `!Ref [LogicalResourceName]`.

---

## 📚 Recursos Útiles y Material de Apoyo

Para la realización y documentación de este desafío, utilicé los siguientes recursos:

* **[AWS CloudFormation - Documentación Oficial](https://aws.amazon.com/cloudformation/):** La fuente definitiva para la sintaxis y tipos de recursos.
* **[Material Complementar: Implementando sua Primeira Stack com AWS CloudFormation.zip](link-al-archivo-si-es-relevante):** Material de apoyo proporcionado por el curso.
* **[GitHub Markdown Guide](https://guides.github.com/features/mastering-markdown/):** Para estructurar este `README.md`.

---
