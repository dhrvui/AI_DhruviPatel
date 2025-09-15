# AI_DhruviPatel
AI-Powered Knowledge Graph to Manim Animation Automation
Overview

This project automates the creation of animated educational videos using AI and Manim. It generates slides and teaching scripts from a knowledge graph of books and converts them into animated videos.

Features:

Extracts concepts and passages from a Neo4j knowledge graph.

Generates teaching scripts using MPT-7B-Instruct (MosaicML) or other LLMs.

Converts scripts into PowerPoint slides.

Automatically generates animated videos using Manim.

Fully CPU/GPU compatible with optimized memory usage.

Dependencies

Install the required packages:

pip install transformers torch accelerate sentencepiece python-pptx neo4j spacy yake pdfplumber tqdm manim
python -m spacy download en_core_web_sm

Usage
1. Generate PowerPoint Slides

Make sure your Neo4j knowledge graph is running and populated.

python mpt_slide_generator_fixed.py


Output: Artificial Intelligence_slides.pptx


Convert PPT to Animated Video
python ppt_to_manim_video.py


Output: AI_Lecture.mp4

Configuration

Neo4j connection:

NEO4J_URI = "bolt://127.0.0.1:7687"
NEO4J_USER = "neo4j"
NEO4J_PASSWORD = "your_password"


MPT model:

MODEL_NAME = "mosaicml/mpt-7b-instruct"


Chunk size (for long passages):

CHUNK_SIZE = 1000  # words per chunk

Tips

For large models, GPU is recommended for faster inference.

On CPU, use bfloat16 to save memory.

Add a .gitignore to avoid pushing large model files, PPTX, and MP4 outputs.

Future Improvements

Add voice narration using TTS for a full AI lecture experience.

Add background music and slide transitions.

Support multiple concepts at once and batch video generation.

License

This project is open-source and free to use under the MIT License.

