# Extented Chinese date-time recognition for Python

This project is based on Miscrosoft Recognizers Text. We add some extension to meet our internal usage and are glad to share it with the community.

## Building and installation

### Clone this repo

    git clone https://github.com/xuanhua/Recognizers-Text.git 
    cd Recognizers-Text

### Uninstall official version of `recognizers-text` if you have installed it

If you have installed `recognizers-text` via `pip` you could use following command to do uninstallation:

```bash
pip uninstall recognizers-text
```
If some sub-package of `recognizers-text` remains, you might meet weird errors later.


### Build and do installatioon

Launch `build.sh` file to install requirements, generate resources, install local packages and run all tests.

```bash
  cd Recognizers-Text/Python
  ./build.sh
```

## New features besides official `recognizers-text` supported

* Support for `next week of next monday` only for Chinese, e.g "下下周一"


Below is the original README content
---

# Microsoft Recognizers Text Overview

![Build Status](https://msrasia.visualstudio.com/_apis/public/build/definitions/310c848f-b260-4305-9255-b97bfb69974b/116/badge)
![Build Status](https://ci.appveyor.com/api/projects/status/github/Microsoft/Recognizers-Text?branch=master&svg=true&passingText=all%20plats%20-%20OK)

Microsoft.Recognizers.Text provides robust recognition and resolution of entities like numbers, units, and date/time; expressed in multiple languages. Full support for Chinese, English, French, Spanish, Portuguese, German, Italian, Turkish, Hindi, and Dutch. Partial support for Japanese, Korean, Arabic, and Swedish. More on the way.

# Utilizing the Project

Microsoft.Recognizers.Text powers pre-built entities in [**LUIS: Language Understanding Intelligent Service**](https://www.luis.ai/home), [**Power Virtual Agents**](https://powervirtualagents.microsoft.com/en-us/), and [**Microsoft Bot Framework**](https://dev.botframework.com/); base entity types in [**Text Analytics Cognitive Service**](https://docs.microsoft.com/en-us/azure/cognitive-services/text-analytics/how-tos/text-analytics-how-to-entity-linking); and it is also available as standalone packages (for the base classes and the different entity recognizers).

The Microsoft.Recognizers.Text packages currently target four platforms:
* [C#/.NET](https://github.com/Microsoft/Recognizers-Text/tree/master/.NET) - **NuGet packages** available at: https://www.nuget.org/profiles/Recognizers.Text
* [JavaScript/TypeScript](https://github.com/Microsoft/Recognizers-Text/tree/master/JavaScript/packages/recognizers-text-suite) - **NPM packages** available at: https://www.npmjs.com/~recognizers.text
* [Python](https://github.com/Microsoft/Recognizers-Text/tree/master/Python) - **PyPI packages** available at: https://pypi.org/user/recognizers-text/ (alpha)
* [Java](https://github.com/Microsoft/Recognizers-Text/tree/master/Java) (in progress)

Contributions are greatly welcome! Both for fixes and extensions in the currently supported languages and for expansion to new ones.
Especially for Japanese, Korean, Arabic, Swedish, and others! More info below.

.NET is the primary package version and contributions propagate to the other platforms with time.

## Citing the Recognizers-Text project

If you utilize the recognizers in academic works, please cite it as below (you can omit the version number or update it to a specific version if relevant):

```tex
@software{soft:recognizers-text,
  author    = {Wenhao Huang and Zijia Lin and Chris McConnell and B{\"{o}}rje F. Karlsson},
  title     = {{Recognizers-Text}: {R}ecognition and resolution of numbers, units, and date/time entities expressed across multiple languages},
  month     = jul,
  year      = 2017,
  publisher = {Zenodo},
  version   = {1.0.0},
  doi       = {10.5281/zenodo.6860598},
  url       = {https://doi.org/10.5281/zenodo.6860598}
}
```

Feel free to change "@software" to "@misc" if it better fits your templates.

# Help

If you have any questions, please go ahead and [open an issue](https://github.com/Microsoft/Recognizers-Text/issues/new/choose), even if it's not an actual bug. Issues are an acceptable discussion forum as well.

# Contributing

This project has adopted the [Microsoft Open Source Code of Conduct](https://opensource.microsoft.com/codeofconduct/). For more information see the [Code of Conduct FAQ](https://opensource.microsoft.com/codeofconduct/faq/) or contact [opencode@microsoft.com](mailto:opencode@microsoft.com) with any additional questions or comments.

Good starting points for contribution are:
* the list of [open issues](https://github.com/Microsoft/Recognizers-Text/issues) (especially those marked as ```help wanted```); 
* the json spec cases temporarily marked as ```NotSupported``` ([Specs](./Specs)); and
* translating json test spec cases that work in English, but don't yet exist in a target language.

The links below describe the project structure and provide both an overview and tips on how to contribute (although some steps may have become a little out-of-date). Thank you!

* [Overview and language resources](https://blog.botframework.com/2018/01/24/contributing-luis-microsoft-recognizers-text-part-1/)
* [Implementing language specific behaviour](https://blog.botframework.com/2018/02/01/contributing-luis-microsoft-recognizers-text-part-2/)
* [Test specs and testing in general](https://blog.botframework.com/2018/02/12/contributing-luis-microsoft-recognizers-text-part-3/)

# Supported Entities across Cultures

The table below summarizes the currently supported entities. Support for English is usually more complete than others. The primary platform is .NET (shown in table) and support should propagate to the others.

| Entity Type       | EN      | ZH-CN   | NL    | FR     | DE    | IT      | JA     | KO     | PT     | ES      |
|:-----------------:|:-------:|:-------:|:-----:|:------:|:-----:|:-------:|:------:|:------:|:------:|:-------:| 
| Number (cardinal)    | ✓    | ✓       | ✓    | ✓     | ✓     | ✓       | ✓      | ✓     | ✓      | ✓       |
| Ordinal              | ✓    | ✓       | ✓    | ✓     | ✓     | ✓       | ✓      | ✓     | ✓      | ✓       |
| Percentage           | ✓    | ✓       | ✓    | ✓     | ✓     | ✓       | ✓      | ✓     | ✓      | ✓       |
| Number Range         | ✓    | ✓       | ✓    | ✓     | ✓     | ✓       | PA/EO  | ✓      | ✓     | ✓       |
| Unit - Age           | ✓    | ✓       | ✓    | ✓     | ✓     | ✓       | ✓      | PA/EO  | ✓     | ✓       |
| Unit - Currency      | ✓    | ✓       | ✓    | ✓     | ✓     | ✓       | ✓      | PA/EO  | ✓     | ✓       |
| Unit - Dimensions    | ✓    | ✓       | ✓    | ✓     | ✓     | ✓       | ✓      | PA/EO  | ✓      | ✓      | 
| Unit - Temperature   | ✓    | ✓       | ✓    | ✓     | ✓     | ✓       | ✓      | ✓     | ✓      | ✓      | 
| Choice - Boolean     | ✓    | ✓       | ✓    | ✓     | ✓     | ✓       | ✓      | **SO** | ✓     | ✓       | 
| Seq. - E-mail        | G    | G*       | G    | G      | G     | G       | G*     | G*     | G      | G       |
| Seq. - GUID          | G    | G        | G    | G      | G     | G       | G      | G      | G      | G       |
| Seq. - Social        | G    | G        | G    | G      | G     | G       | G      | G      | G      | G       |
| Seq. - IP Address    | G    | G        | G    | G      | G     | G       | G      | G      | G      | G       |
| Seq. - Phone Number  | G    | G        | G    | G      | G     | G       | G      | G      | G      | G       |
| Seq. - URL           | G    | G*       | G    | G      | G     | G       | G*     | G*     | G      | G       |
| DateTime (+subtypes) | ✓    | ✓       | ✓    | ✓     | ✓     | ✓       | ✓      | **SO** | ✓     | ✓       | 

| Entity Type       | SV      | BG      | TR    | HI     | AR     |         |        |        |        |         |
|:-----------------:|:-------:|:-------:|:-----:|:------:|:------:|:-------:|:------:|:------:|:------:|:-------:| 
| Number (cardinal)    | ✓    | :x:     | ✓    | ✓      | PA/EO  |         |        |        |        |         |
| Ordinal              | ✓    | :x:     | ✓    | ✓      | PA/EO  |         |        |        |        |         |
| Percentage           | ✓    | :x:     | ✓    | ✓      | PA/EO  |         |        |        |        |         |
| Number Range         | :x:  | :x:     | ✓     | ✓     | PA/EO  |         |        |        |        |         |
| Unit - Age           | ✓    | :x:     | ✓     | ✓     | :x:    |         |        |        |        |         |
| Unit - Currency      | ✓    | :x:     | ✓     | ✓     | :x:    |         |        |        |        |         |
| Unit - Dimensions    | ✓    | :x:     | ✓     | ✓     | :x:    |         |        |        |        |         | 
| Unit - Temperature   | ✓    | :x:     | ✓     | ✓     | :x:    |         |        |        |        |         | 
| Choice - Boolean     | ✓    | ✓      | ✓     | ✓      | ✓     |         |        |        |        |         |
| Seq. - E-mail        | G    | G       | G     | G      | G      |         |        |        |        |         |
| Seq. - GUID          | G    | G       | G     | G      | G      |         |        |        |        |         |
| Seq. - Social        | G    | G       | G     | G      | G      |         |        |        |        |         |
| Seq. - IP Address    | G    | G       | G     | G      | G      |         |        |        |        |         |
| Seq. - Phone Number  | :x:  | :x:     | :x:   | :x:    | :x:    |         |        |        |        |         |
| Seq. - URL           | G    | G       | G     | G*     | G*     |         |        |        |        |         |
| DateTime (+subtypes) | **SP** | :x:     | ✓     | ✓     | **SO** |         |        |        |        |         |

* G: Generic entity, not language-specific (* unicode TLDs not-supported);
* EO: Extraction-only (parsing/resolution/normalization pending);
* PA: Partial support (type not fully supported);
* SO: Specs-only (test specs coverage OK, but support pending);
* SP: Partial specs;
* SI: Very initial specs (typically language support start for a new language).
