# Sandalwood-Conservation-QA-Sys

---

## Introduction

This project presents a comprehensive speech-enabled question-answering system designed specifically for Kannada language users, with English translation capabilities. The system addresses the linguistic barriers often encountered in traditional QA systems by creating a bidirectional bridge between Kannada and English languages. By integrating speech recognition, natural language processing, and machine translation technologies, the system enables users to interact using their native language while still benefiting from the wealth of information available in English.

The primary objectives of this system are:
1. To enable seamless voice-based querying in Kannada
2. To provide accurate and contextually relevant answers in both Kannada and English
3. To overcome language barriers through automated translation
4. To create an accessible interface for users with varying degrees of language proficiency

This system has particular relevance in multilingual regions where Kannada is spoken, potentially serving educational purposes, customer service applications, and information access for those who are more comfortable communicating in Kannada than in English.

<img width="2752" height="1536" alt="unnamed (1)" src="https://github.com/user-attachments/assets/336ab3ad-6724-4e45-b866-05ece0728ca4" />


---

## Methodology

The methodology of the Kannada-English QA system involves several key technical components working in an integrated pipeline:

### 1. Audio Input and Transcription
- **Audio Capture**: The system accepts Kannada audio input, either from pre-recorded files or through direct microphone recording.
- **Audio Processing**: The input audio is divided into manageable chunks (10 seconds each) to improve recognition accuracy.
- **Speech Recognition**: Using Google's Speech Recognition API with the Kannada language model ('kn-IN'), the system transcribes the audio chunks into Kannada text.

### 2. Translation Processing
- **Language Translation**: The Google Translate API is used to convert Kannada text to English, facilitating further processing and enabling bilingual output.
- **Text Storage**: Both the original Kannada text and its English translation are stored in separate Word documents with timestamps for reference.

### 3. Semantic Question Matching
- **Embedding Generation**: The system utilizes the SentenceTransformer model ('paraphrase-MiniLM-L6-v2') to encode the English translation of the user's question.
- **Similarity Calculation**: Cosine similarity is calculated between the encoded question and a pre-existing database of question-answer pairs.
- **Best Match Identification**: The system identifies the most semantically similar question in the database, applying a configurable similarity threshold (default: 0.5) to ensure relevance.

### 4. Answer Retrieval and Presentation
- **Answer Extraction**: Upon finding a match, the system retrieves the corresponding answer in English.
- **Answer Translation**: The English answer is translated back to Kannada using the Google Translate API.
- **Audio Response Generation**: For the retrieved answer, the system either:
  - Plays the original audio recording if available in the dataset, or
  - Synthesizes Kannada speech from the translated answer text using Google's Text-to-Speech (gTTS) service

### 5. Integration and User Interface
- **Multimodal Output**: The system presents answers in multiple formats—audio playback for auditory learning and text display in both languages for visual confirmation.
- **Interactive Controls**: The user interface includes intuitive recording controls for starting and stopping audio input.

---

## Conclusion

The Kannada-English Question-Answering System successfully demonstrates the integration of speech recognition, natural language processing, and machine translation technologies to create a functional cross-lingual information retrieval system. By enabling users to interact in Kannada while accessing information that might primarily exist in English, the system addresses a significant accessibility gap in multilingual computing.

Key achievements of this system include:
1. Successfully processing Kannada speech input and converting it to text with reasonable accuracy
2. Performing effective semantic matching to find relevant information regardless of the exact phrasing
3. Generating natural-sounding Kannada speech output when original audio recordings are unavailable
4. Creating a bidirectional bridge between languages that maintains context and meaning

Several opportunities for future enhancement exist:
1. Expanding the QA dataset to cover a broader range of topics and questions
2. Improving the speech recognition accuracy for Kannada through model fine-tuning
3. Implementing more sophisticated natural language understanding techniques to better handle complex queries
4. Adding support for additional Indian languages to increase the system's reach and utility
5. Optimizing the system for deployment on resource-constrained devices to enhance accessibility

This system represents a significant step toward breaking down language barriers in information access and demonstrates the potential of multilingual AI systems to serve diverse linguistic communities. By continuing to refine and expand such systems, we can work toward a more inclusive digital experience that honors linguistic diversity while providing equal access to information.

---

![WhatsApp Image 2025-04-28 at 23 49 44_a9afa3dd](https://github.com/user-attachments/assets/cfb385d2-3094-4e4c-bd7f-2af071d3005b)

---

- Working: https://www.youtube.com/watch?v=mNLS1jSLXuo

- Detail Documentaion: https://code2tutorial.com/tutorial/91dc2c0f-fc51-4ca9-a1f1-7c8e30c2eacb/index.md
