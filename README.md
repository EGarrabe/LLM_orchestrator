# LLM orchestrator for robotic systems
This repo contains prototype code for an LLM orchestrator and planner in the context of robotics. The idea is to solve tasks by relying on the LLM's "common sense". The planner outputs a plan, which is then carried out step by step by the orchestrator.

# How to use
First, motion primitives (such as grasps, moves, etc) should be defined by the user, and made available as an API with clear and intuitive naming conventions. A quick description of available objects and locations should be written, and all this information, along with the API documentation should be added in the initial prompt in the appropriate file.

Then, once a task is published on the appropriate topic (/task), the planner and orchestrator are started and the task is carried out.

#Design guidelines
Ideally, the primitives should return some feedback (such as a syntax check) if they are misused to allow the orchestrator LLM to fix its mistakes. We are currently investigating mechanisms to systematically design such feedback mechanisms, along with other ways of increasing the robustness of the pipeline.

Author: Émiland Garrabé (garrabe@isir.upmc.fr). Prototype module designed as part of ongoing works, will be updated as work advances.
