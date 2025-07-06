# 02 - Requisitos previos para el despliegue de APIs ASP.NET Core

Antes de comenzar con los despliegues en distintas plataformas, es importante asegurarse de tener las herramientas necesarias instaladas y configuradas, así como una estructura de proyecto clara.

---

## ✅ Herramientas necesarias

A continuación, se listan las herramientas requeridas y enlaces para su descarga:

| Herramienta      | Descripción                                     | Enlace oficial                                                                                                                |
| ---------------- | ----------------------------------------------- | ----------------------------------------------------------------------------------------------------------------------------- |
| .NET SDK (6/7/8) | Para compilar y publicar la API                 | [https://dotnet.microsoft.com/download](https://dotnet.microsoft.com/download)                                               |
| Git              | Control de versiones                            | [https://git-scm.com/downloads](https://git-scm.com/downloads)                                                               |
| GitHub           | Plataforma para alojar el repositorio           | [https://github.com](https://github.com)                                                                                     |
| Docker (opcional)| Para contenerizar y desplegar en algunos entornos | [https://www.docker.com/products/docker-desktop](https://www.docker.com/products/docker-desktop)                             |
| Azure CLI (opcional) | Para despliegues en Azure                   | [Instalación Azure CLI](https://learn.microsoft.com/es-es/cli/azure/install-azure-cli)                                       |
| AWS CLI (opcional)   | Para despliegues en AWS                     | [Guía de instalación](https://docs.aws.amazon.com/cli/latest/userguide/install-cliv2.html)                                   |
| EB CLI (opcional)    | CLI específica para AWS Elastic Beanstalk  | [Guía de instalación EB CLI](https://docs.aws.amazon.com/elasticbeanstalk/latest/dg/eb-cli3-install.html)                    |

---

## 🗃️ Repositorio base

El repositorio debe contener una estructura mínima como la siguiente:

```
MiApiDeployDocs/
├── src/
│   └── MiApi/             # Código fuente ASP.NET Core
│       ├── Program.cs
│       ├── Startup.cs (si aplica)
│       └── MiApi.csproj
├── Dockerfile             # Si se usará contenedores
├── .gitignore
├── README.md
└── docs/                  # Documentación del despliegue
```

> 💡 Se recomienda iniciar el proyecto con el comando:
>
> ```bash
> dotnet new webapi -n MiApi
> ```

---

## 📌 Buenas prácticas

- Utilizar `appsettings.Production.json` para configuraciones en entornos de producción.
- Configurar variables de entorno desde la plataforma de hosting (no hardcodear secretos).
- Usar `.gitignore` para excluir `bin/`, `obj/`, `.vs/`, `*.user`, etc.
- Verificar que el proyecto compile y funcione localmente con `dotnet run`.

---

Una vez cubiertos estos requisitos, podemos pasar a explorar las distintas plataformas de despliegue.

➡️ Ir a: [03 - Deploy a Render](03-deploy-render.md)

