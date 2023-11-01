---
description: A design system equals system design
---

# Frontend Development

Developing software is a detailed and time-consuming task where design and development should work together for the best results. Large teams may become less effective, leading to misunderstandings, undocumented user interface patterns, and the creation of numerous disposable components over time.

### **Creating Reusable Components**

In a design system, the focus should be on developing reusable components that exclusively handle the presentation layer, respond to inputs, and remain free of application-specific business logic. Application-specific components with business logic should be avoided to ensure flexibility across different applications using the system. This approach helps maintain a clean and sustainable component library.

### **Using External Component Libraries**

External component libraries are suitable for quick prototyping, ideation, and Minimum Viable Products (MVPs). However, they may pose challenges when customizing or adapting components to specific needs over time.

For the purpose of this GovStack Sandbox, we used an external component library called [Chakra UI](https://chakra-ui.com/). For the selection of this library, we [evaluated some candidates](https://govstack-global.atlassian.net/wiki/spaces/DEMO/pages/96043009/Component+Library+Evaluation) based on criteria like performance, maintenance activity, accessibility features, licence.

### **Building Your Component Library**

Building a component library from scratch offers complete control over visuals and functionality, making it easier to involve developers of different levels. However, it requires significant effort and may not be suitable for all developers.

Building a component library may be more suitable for experienced specialists who can design and structure the library effectively. Their experience will translate into a more useful and efficient tool for development teams.

### **Sustainability**

To maintain a sustainable component library, create an inventory of frequently used components, treat the library as a separate product with its own team, and maintain the scope to prevent components from becoming too complex.

Break down all components into their smallest reusable parts early in the design phase. This facilitates the composition of larger and more complex components from simpler ones and ensures that these components can be effectively utilized by third-party developers when necessary.

Developers using a well-structured component library, especially junior developers, can focus on solving business problems and integrating components without the need to reinvent the wheel for each project. This streamlined approach eases the onboarding of new team members and promotes consistency across applications.

### **Versioning and Testing**

Components should be broken down into their smallest reusable parts from the design phase, and a single source of truth should be established. Versioning, testing, and adequate documentation are essential.

Versioning and testing are essential components of building and maintaining a robust and reliable component library. These practices promote consistency, reliability, and collaboration within your development team, ultimately contributing to the success of your projects and applications.

### **Tools**

When building and managing a component library, you'll need suitable tools to streamline the development, testing, documentation, and integration of components into your projects. Two popular tools for this purpose are [Storybook](https://storybook.js.org/) and [Bit](https://bit.dev/).

***

Building and maintaining a design system and component library is an ongoing challenge. Proper management and development of these resources are essential to avoid chaos and software rot in software development.
