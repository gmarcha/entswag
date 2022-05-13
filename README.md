# entswag

An entgo extension to generate ent schemas from data definitions in a swagger specification 2.0.

# Usage

...

# Misc

I worked on a project using entgo to generate data models and goswagger to generate restapi code.
Problem is both of these frameworks generate their own data model.

I needed to avoid coexistence of two data models in my applicaton. I used a specific workflow:
- writing route paths in a swagger specification 2.0;
- writing ent schemas;
- generate an openapi specification 3.0 from ent schemas and make it swagger 2.0 compliant;
- merging route paths swagger specification with data definitions to obtain final swagger specification.

This workflow is really annoying: hard to explain to newcomers on the project, error prone because of generation dependencies.

I should develop an extension to directly generate schemas from specification, avoiding complexity and errors.
