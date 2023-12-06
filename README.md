# One-API-LLM-Hackathon

Bharat LawLex, Chatbot for the Indian Constitution using Intel OneAPI
Credits : Debojyoti Chakraborty, Komal Rathod, Mangesh Wagh

Bharat LawLex is an ingenious LLM Chatbot dedicated to unraveling the complexities of the Indian Constitution. Our mission is to swiftly and conveniently resolve constitutional queries, revolutionizing the way users access legal information. In this blog post, we embark on a journey to explore the core problem statement that fueled the creation of Bharat LawLex - the quest for a solution that not only ensures quick and accessible legal information but also enriches user understanding and engagement with constitutional matters through the power of an intelligent chatbot platform.

Key Features:
Natural Language Processing (NLP):

User Interaction- Users can engage with Bharat LawLex in natural, conversational language. The chatbot interprets queries and responds intelligently, promoting ease of use.
2. Database Integration:
The chatbot is connected to an extensive database of Indian legal documents, including the Constitution, amendments, and case laws.
3. Case Law Search:
Users can search for specific cases and retrieve relevant information, summaries, and judgments.
4. Notifications and Updates:
The AI Lawyer can send users updates on recent legal developments, amendments, and significant court rulings.
we'll build a full-stack application that uses Retrieval Augmented Generation (RAG) to deliver accurate and contextually relevant responses in a chatbot.

Architecture Diagram

RAG-based chatbot
RAG is a powerful pattern that combines the benefits of retrieval-based models and generative models. Unlike traditional chatbots that can struggle with maintaining up-to-date information or accessing domain-specific knowledge, a RAG-based chatbot uses a knowledge base to provide contextually relevant responses.

Fine-tuning
NeuralChat supports fine-tuning the pretrained large language model (LLM) for text-generation, summarization, code generation tasks, and even TTS model, for user to create the customized chatbot.
# Command line
neuralchat finetune --base_model "meta-llama/Llama-2-7b-chat-hf" --config pipeline/finetuning/config/finetuning.yaml
# Python code
from intel_extension_for_transformers.neural_chat import finetune_model, TextGenerationFinetuningConfig
finetune_cfg = TextGenerationFinetuningConfig() # support other finetuning config
finetune_model(finetune_cfg)

Optimization
NeuralChat provides typical model optimization technologies, like Automatic Mixed Precision (AMP) and Weight Only Quantization, to allow user to define a customized chatbot.
# Command line
neuralchat optimize --base_model "meta-llama/Llama-2-7b-chat-hf" --config pipeline/optimization/config/optimization.yaml
# Python code
from intel_extension_for_transformers.neural_chat import build_chatbot, MixedPrecisionConfig
pipeline_cfg = PipelineConfig(optimization_config=MixedPrecisionConfig())
chatbot = build_chatbot(pipeline_cfg)
Future scope
Expanded Multilingual Support:
Integration of More Regional Languages: Continuously expanding multilingual support to include more regional languages, ensuring that users from diverse linguistic backgrounds can comfortably engage with Bharat LawLex.

Legal Analytics and Trends:
Data Analytics for Legal Trends: Implementing data analytics to identify legal trends, helping legal professionals and policymakers stay ahead of emerging issues.
Predictive Analysis: Developing capabilities for predictive legal analysis, offering insights into potential legal outcomes based on historical data and current legal trends.

Interactive Learning Features:
Virtual Legal Workshops: Introducing virtual workshops and tutorials within the chatbot platform to provide users with interactive learning experiences.
Gamification Elements: Incorporating gamification elements to make learning about the Indian Constitution more engaging, encouraging users to explore legal concepts in a fun and interactive way.

You can follow the project on github to get the complete code.
