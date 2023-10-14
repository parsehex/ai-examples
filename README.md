# ai-examples

collection of ai-related code examples across multiple languages (python, js/ts)

## plans

- basic examples using openai and langchain
- langchain
  - js app: nextjs single-thread chat with conversational agent with access to search and browsing
  - python app: streamlit chat, prototype of the above
- apps
  - end-to-end voice chat
    - as a user, you can speak into the microphone and hear back the AI's response in a natural voice, able to repeat from there
    - the app would record the user with the browser media API, transcribe the recording with either openai's whisper service or whisper.cpp-wasm to keep costs down, get response from llm (chatgpt, llama), generate tts from response and play
    - challange will be to orchestrate an actual conversation
    - ideas:
      - the user should be able to interrupt the ai while it's speaking, easily enough. if the ai's response is being played and the user starts talking, calculate the index in the message that the user interrupted at, edit ai's message to "cut it off" at that point, and begin a new user message
