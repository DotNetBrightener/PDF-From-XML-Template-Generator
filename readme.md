PDF From XML Template Generator
===============================

A library that allows you to generate PDF files from pre-defined XML templates, using **[PDFSharp](https://github.com/empira/PDFsharp)** and **[MigraDoc](https://github.com/empira/MigraDoc)** library.

[![GitHub release](https://img.shields.io/github/v/release/dotnetbrightener/PDF-From-XML-Template-Generator.svg)](https://GitHub.com/dotnetbrightener/PDF-From-XML-Template-Generator/releases/)


Inspiration
===========

I have been looking for a solution for my projects at work that helps generating the PDF files from friendly syntax like HTML/XML, and I found a good example at [https://github.com/cedricmartel/PdfTemplate](https://github.com/cedricmartel/PdfTemplate).

However this project has been using iTextSharp library, which was in LGPL license back in version 4.5.3.3 and earlier. Anything newer are licensed under commercial licenses and I found myself cannot use this library.

So I started to build up the project that hopefully might fit my need and hope it will be useful for everyone who needs something similar.

.NET versions supported
=======================

At the moment the library supports .Net Core 3.1. I will add support to lower LTS versions of .Net Core soon.

Development
===========

Installation
============

Install using Package Reference
---

1. Create a `nuget.config` in your project / solution folder with the following content:

```xml
<?xml version="1.0" encoding="utf-8"?>
<configuration>
    <packageSources>        
        <add key="githubDotnetBrightener" value="https://nuget.pkg.github.com/dotnetbrightener/index.json" />
    </packageSources>
    <packageSourceCredentials>
        <githubDotnetBrightener>
            <add key="Username" value="[your_github_username]" />
            <add key="ClearTextPassword" value="[github_access_token]" />
        </githubDotnetBrightener>
    </packageSourceCredentials>
</configuration>
```

2. Replace `[your_github_username]` with your Github account, and `[github_access_token]` with your developer personal access token.

To generate your token if you do not have one, visit [Personal Access Tokens](https://github.com/settings/tokens), then click the [Generate new token] button. Make sure you select `read:packages` scope to be able to download packages from Github Packages. Once done, copy the generated token as it will no longer be shown to you once you leave this page.

3. Use the following command to install the package to your project
   
```
dotnet add [YOUR_PROJECT_NAME] package PdfFromXmlTemplate
```

You can optionally specified version by using `--version [version]` parameter

4. Follow the steps in *[Install PDFSharp and MigraDoc for your project](#install-pdfsharp-and-migradoc-for-your-project)* to set up PDFSharp and MigraDoc library in order to get the library work.

Install manually
---

If you do not want to go through the Nuget configuration process, you can visit the [Releases](https://GitHub.com/dotnetbrightener/PDF-From-XML-Template-Generator/releases) page and download the binary from there, then add reference directly to your project.

Then follow the steps in *[Install PDFSharp and MigraDoc for your project](#install-pdfsharp-and-migradoc-for-your-project)* to set up PDFSharp and MigraDoc library in order to get the library work.


Install PDFSharp and MigraDoc for your project
---

Usage
=====


More Tutorials
=========


Reference
=========

[https://github.com/cedricmartel/PdfTemplate](https://github.com/cedricmartel/PdfTemplate)