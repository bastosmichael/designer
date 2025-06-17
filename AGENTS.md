# Overview of Agents in This Repository

This document provides detailed information about the LLM-based and autonomous agents used in this project. It serves as a reference for contributors and AI tooling, detailing the roles, triggers, behavior, and outputs of each agent.

## Table of Agents

| Name               | Description                                                        | Trigger                                           |
|--------------------|--------------------------------------------------------------------|--------------------------------------------------|
| Image Generator     | Generates images based on user prompts using AI technology         | User input in the AI sidebar                     |
| Background Remover  | Removes the background from selected images                        | User selection in the Remove Background sidebar   |

### Image Generator

**Description:**  
The Image Generator agent uses AI to create images based on user-provided prompts. It leverages the Replicate API to generate images with specified parameters.

**Trigger:**  
The agent is triggered when a user submits a prompt in the AI sidebar.

**Inputs:**  
- User prompt (string)
- Configuration parameters (e.g., aspect ratio, output format)

**Outputs:**  
- Generated image (URL)

**Logic Location:**  
The logic for this agent is located in `src/features/ai/api/use-generate-image.ts`.

**Review/Audit Process:**  
The generated images are reviewed by the user before being added to the canvas. No automated audit process is currently implemented.

### Background Remover

**Description:**  
The Background Remover agent uses AI to remove the background from selected images. It utilizes the Replicate API to process the image and return a new image without the background.

**Trigger:**  
The agent is triggered when a user selects an image and clicks the "Remove Background" button in the Remove Background sidebar.

**Inputs:**  
- Selected image (URL)

**Outputs:**  
- Image with background removed (URL)

**Logic Location:**  
The logic for this agent is located in `src/features/ai/api/use-remove-bg.ts`.

**Review/Audit Process:**  
The processed image is reviewed by the user before being added to the canvas. No automated audit process is currently implemented.

## How to Invoke Each Agent

### Image Generator
- **CLI:** Not applicable
- **CI:** Not applicable
- **Prompts:** Enter a prompt in the AI sidebar and click "Generate".

### Background Remover
- **CLI:** Not applicable
- **CI:** Not applicable
- **Prompts:** Select an image and click "Remove background" in the Remove Background sidebar.

## Future Agent Proposals

- **Text-to-Speech Agent:** An agent that converts text on the canvas to speech for accessibility purposes.

## Contribution Instructions for New Agents

To add a new agent to this document, follow these steps:
1. Identify the agent's role and functionality.
2. Document the agent's name, description, trigger, inputs, outputs, and logic location.
3. Add the agent to the Table of Agents and create a detailed section below.
4. Update the "How to Invoke Each Agent" section if applicable.
5. Submit a pull request with your changes.
