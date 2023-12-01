---
name: Data tidying example template
about: This is a template for submitting examples of 'data tidying' workflows
title: ''
labels: ''
assignees: ''

---

Thank you for submitting a tidying example! 

 - type: input
    id: contact
    attributes:
      label: Dataset Information
      description: Please provide a brief description of the dataset, including links and information needed to reproduce the example. 
      placeholder: dataset info here
    validations:
      required: false
 - type: textarea
    id: issue-description
    attributes:
      label: Main tidying challenges + steps
      description: Please describe 'untidy' characteristics of this dataset. This is also a great place to describe the specific steps you took and share any insight about what worked / didn't work
      placeholder: Tell us what you see!    The next window should have a space to upload a jupyter notebook file with your example *in progress*
