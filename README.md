# genai-chatbot-langchain
from langchain_huggingface import HuggingFaceEndpoint, ChatHuggingFace

llm = HuggingFaceEndpoint(
    repo_id="google/flan-t5-base",
    task="text-generation"
)

model = ChatHuggingFace(llm=llm)

response = model.invoke("What is AI?")
print(response.content)
