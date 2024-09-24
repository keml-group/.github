# The KEML group

This project contains all relevant modules of the domain-specific language KEML (=Knowledge Elicitation Modeling Language) designed for modelling knowledge elicitation by an LLM as perceived by a human author prompting it.

## Motivation for KEML
We design KEML to document and analyse the interaction with LLMs and potentially more conversation partners. Our main concern is the trust into single pieces of information we receive by the LLM or other sources.

A rough explanation of the language is available on the ReadMe of the [metamodel of KEML](https://github.com/keml-group/keml). An in depth introduction of KEML will be available in our [introductory paper](https://doi.org/10.1145/3652620.3687809) - that will be published in September 2024.

## Structure and Technological Basis

KEML is an [Eclipse EMF project](https://projects.eclipse.org/projects/modeling.emf.emf) meaning it consists of a set of Eclipse Plugins that create several handy editors and analyzers for KEML files.
It follows the standard structure of EMF projects:

1) **Modeling project [keml](https://github.com/keml-group/keml):** The central definition of the .ecore file. The two projects edit and editor can be generated in Eclipse just based on this file. Since edit had some customizations, it is recommended to fork it from this GitLab group.

2) **Edit code project [keml.edit](https://github.com/keml-group/keml.edit):** Originally generated project for general edit functionality (generating and changing KEML elements) heavily used on keml.editor. We did some customizations (own icons, functions defining when to use them) so that we you can install the project from Git if you want to use them. The standard generated version works just as well but is less pretty.

3) **Editor project keml.editor:** Generated project, currently no Git instance exists - just run 'Generate' -> 'Editor code' on the Modeling project's central file. By executing this project as an Eclipse application a text-based editor for KEML files is started.

5) **KEML file generation from extern sources [keml.io](https://github.com/keml-group/keml.io):** This project can run independently of the Eclipse environment. It converts a yEd graphical file into an KEML file. Other IO functionality is used by the analysis project.

6) **Analysis of KEML files [keml.analysis](https://github.com/keml-group/keml.analysis):** This project can run independently of the Eclipse environment. It generates statistical information in various formats about an input KEML file.

7) **KEML (and yEd) samples [keml.sample](https://github.com/keml-group/keml.sample):** Example files including yEd graphical representations and KEML files.

More information about the subprojects is available in their respective ReadMes.

## Support
Support is currently offered by the main developer, Susanne Göbel under goebel@uni-koblenz.de.

## Roadmap
* A graphical web-based editor for KEML files is currently under construction. Since the project is in an early state, it is not shared publically yet.
* We also plan a tool for ad-hoc analysis of an on-going LLM conversation in the near future

## Contributing
We are open to contributors. Maybe you would like to write your bachelor's or master's thesis on KEML? Get in touch with Susanne Göbel goebel@uni-koblenz.de.

## License

The KEML project is subject to (C) 2023-2024, SoftLang Research Team, University of Koblenz, Faculty of CS, contact Susanne Göbel or Ralf Lämmel. It is provided under the [CC BY 4.0 license](https://creativecommons.org/licenses/by/4.0/).
Basically, you are free to share and adapt the material as long as you give proper credit to us and our project. Feel free to include KEML into your research but please cite us, especially our [introductory paper](https://doi.org/10.1145/3652620.3687809).

## Credits

Group icon by <a href="https://www.flaticon.com/free-icons/camel" title="camel icons">Camel icons created by Freepik - Flaticon</a>
