# The KEML group

This project contains all relevant modules of the domain-specific language KEML (=Knowledge Elicitation Modeling Language) designed for modelling knowledge elicitation by an LLM as perceived by a human author prompting it.

## Motivation for KEML
We designe KEML to document and analyse the interaction with LLMs and potentially more conversation partners. Our main concern is the trust into single pieces of information we receive by the LLM or other sources.

Some introductory slides also explaining the case study that started this research are available online.

## Structure and Technological Basis

KEML is an [Eclipse EMF project](https://projects.eclipse.org/projects/modeling.emf.emf) meaning it consists of a set of Eclipse Plugins that create several handy editors and analyzers for KEML files.
It follows the standard structure of EMF projects:

1) **Modeling project [keml](https://gitlab.uni-koblenz.de/keml/keml):** The central definition of the .ecore file. The two projects edit and editor can be generated in Eclipse just based on this file. Since edit had some customizations, it is recommended to fork it from this GitLab group.

2) **Edit code project [keml.edit](https://gitlab.uni-koblenz.de/keml/keml.edit):** Originally generated project for general edit functionality (generating and changing KEML elements) heavily used on keml.editor. We did some customizations (own icons, functions defining when to use them) so that we recommend to install the project from Git. The standard generated version works just as well but is less pretty.

3) **Editor project keml.editor:** Generated project, currently no Git instance exists - just run 'Generate' -> 'Editor code' on the Modeling project's central file. By executing this project as an Eclipse application a text-based editor for KEML files is started.

4) **Graphical editor project [keml.design](https://gitlab.uni-koblenz.de/keml/keml.design):** WIP to generate a graphical (SIRIUS) editor for KEML files. Once done, executing this project as an Eclipse application will start a visual editor for KEML files.

5) **KEML file generation from extern sources [keml.io](https://gitlab.uni-koblenz.de/keml/keml.io):** This project can run independently of the Eclipse environment. It converts a yEd graphical file into an KEML file. Other IO functionality is used by the analysis project.

6) **Analysis of KEML files [keml.analysis](https://gitlab.uni-koblenz.de/keml/keml.analysis):** This project can run independently of the Eclipse environment. It generates statistical information in various formats about an input KEML file.

7) **KEML (and yEd) samples [keml.sample](https://gitlab.uni-koblenz.de/keml/keml.sample):** Example files including yEd graphical representations and KEML files.

More information about the subprojects is available in their respective ReadMes.

## Support
Support is currently offered by the main developer, Susanne Göbel under goebel@uni-koblenz.de.

## Roadmap
 * The graphical editor under keml.design is currently under construction
* We also plan a tool for ad-hoc analysis of an on-going LLM conversation in the near future

## Contributing
We are open to contributors. Maybe you would like to write your bachelor's or master's thesis on KEML? Get in touch with Susanne Göbel goebel@uni-koblenz.de.

## License

The KEML project is subject to (C) 2023-2024, SoftLang Research Team, University of Koblenz, Faculty of CS, contact Susanne Göbel or Ralf Lämmel. Restricted access. Do not share. Access is currently only granted by the copyright holders as part of research and teaching activities involving the SoftLang Team at the University of Koblenz. Less restricting sharing and copy righting is deferred for now.

## Credits

Group icon by <a href="https://www.flaticon.com/free-icons/camel" title="camel icons">Camel icons created by Freepik - Flaticon</a>
