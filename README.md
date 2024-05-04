# crewai_researcher
 
This is a working example of CrewAI working against 2 local LLM's as of May 4th, 2024.  
In many examples that I've come across, they no longer work.  The error I got is that there were no actions matching DuckDuckGoSearch since the 1st LLM is passing 

Action: DuckDuckGoSearch ("2024 generative AI impact on various industries") instead of

Action: DuckDuckGoSearch 
Action Input: { "q": "2024 generative AI impact on various industries" } 

After some reading, I learned that CrewAI works much better with hosted LLM's like OpenAI. After some debugging, it wasn't my simple code that was making the call to that particular action but the first local LLM.  People mentioned that OpenHermes worked better, so I switched Llama2 for OpenHermes and the action called worked.
