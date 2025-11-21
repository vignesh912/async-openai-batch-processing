# async-openai-batch-processing
Implements asynchronous Azure OpenAI client requests to support sending ~100 messages concurrently, improving throughput and reducing total response time.

Async Azure OpenAI Client – Parallel Message Processing

This feature introduces an asynchronous implementation of the Azure OpenAI client, enabling the application to send and process multiple (100+) requests in parallel. By leveraging Python’s asyncio capabilities, this solution significantly improves throughput and reduces total response time compared to sequential execution.

✨ Why This Feature Exists

The existing implementation sends requests one-by-one, which becomes slow and inefficient when processing large batches of messages.
This update adds:

Async Azure OpenAI client

Parallel request execution (e.g., 100 concurrent calls)

Improved throughput & reduced latency

More scalable structure for future AI workloads

🚀 What This Code Does

Wraps Azure OpenAI operations in an async function

Uses asyncio.gather() to fire off multiple prompts at once

Handles request throttling, retries, and error logging

Returns results in a structured, ordered format

Supports scaling to high request volumes safely

📁 Project Structure (example)
/async-openai/
│── async_client.py          # Async Azure OpenAI wrapper
│── batch_processor.py       # Handles parallel message execution
│── examples/
│     └── run_demo.py        # Demo sending 100 parallel requests
│── README.md

🔧 Tech Used

Python 3.10+

asyncio

Azure OpenAI SDK

Optional: aiohttp (if used)

Logging & retry logic
