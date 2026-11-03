# ExamGuard

ExamGuard is a CNN-based real-time online examination behaviour monitoring system using OpenCV and PyTorch.

## Project objective
Build a real-time webcam monitoring system that recognises predefined examination behaviours and raises alerts only when behaviours persist or repeat over time. The system must assist invigilators and must not automatically conclude that a student is cheating.

## Core rules
1. Explain the concept before writing code.
2. Explain why each feature is being implemented.
3. Work in small, manageable steps.
4. Never generate the entire project at once.
5. Explain unfamiliar Python, OpenCV, and PyTorch concepts.
6. Ask for approval before creating or modifying files.
7. Do not install dependencies without explaining why and getting approval.
8. Help debug errors step by step.
9. Explain Git commands and suggest commits after milestones.
10. Never commit or push without explicit user permission.
11. Use only a public, existing dataset and do not collect training data from a webcam.
12. Train a CNN from scratch with random initialization; do not use pretrained weights for the main model.
13. Keep the laptop webcam for real-time inference only, not for dataset collection.

## Project requirements
- Python 3.10
- OpenCV
- PyTorch
- NumPy
- Matplotlib
- Scikit-learn
- Streamlit
- Git and GitHub
- VS Code

## Dataset rules
- Use an existing public dataset only.
- Inspect the dataset structure before using it.
- Understand the annotations and class labels.
- Identify which labels match the required behaviour classes.
- Check licence and usage conditions.
- Do not assume the dataset contains all required classes.
- If absence is not available in the dataset, implement absence detection separately with OpenCV-based face-presence detection.
- Do not label unrelated images as absent.

## Required behaviour classes
Initial supported classes:
1. Normal examination behaviour
2. Looking sideways
3. Looking down
4. Student absent from the camera

## ML requirements
- Use PyTorch
- Train a custom CNN from scratch
- Randomly initialised weights only
- No pretrained weights for the main CNN
- Input image size: 128 x 128 RGB
- Include convolution, ReLU, max pooling, and fully connected layers
- Use proper training, validation, and test splits
- Avoid data leakage by keeping related recordings or participant data in the same split whenever possible
- Report training and validation accuracy/loss curves
- Report confusion matrix
- Report precision, recall, and F1-score

## Real-time system expectations
- Capture webcam video
- Classify behaviours
- Show predicted class and confidence
- Smooth predictions across consecutive frames
- Track behaviour duration
- Generate alerts for persistent or repeated behaviour
- Maintain timestamped logs
- Show a Streamlit dashboard for monitoring

## Development approach
- Start with environment setup and project structure
- Inspect the dataset before coding
- Prepare and validate preprocessing pipelines
- Build the CNN in small steps
- Evaluate model performance before moving to real-time integration
- Add OpenCV inference only after model performance is acceptable
- Add temporal smoothing and alert logic after classification works
- Add the Streamlit dashboard last

## Git and GitHub workflow
- Keep commits small and milestone-based
- Explain each Git command before running it
- Suggest commits after meaningful progress
- Never commit or push without user approval
- Keep the repository clean and production-focused

## Repository conventions
- Use a virtual environment for all Python work
- Keep project dependencies explicit
- Prefer small, readable code files
- Document setup steps in a README when appropriate
- Avoid committing generated datasets, model artifacts, or environment files

## Important constraints
- Do not create or modify files without approval.
- Do not install dependencies without explaining why and receiving approval.
- Do not download the dataset before inspection and approval.
- Do not start with a large code generation step.
- Prefer guided, incremental development and learning.
