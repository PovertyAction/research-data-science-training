# LLM Introduction Workshop

This comprehensive tutorial series teaches you how to build applications with Large Language Models using the Python chatlas library. These hands-on tutorials follow the Diátaxis framework to provide practical, learner-focused instruction for working with modern AI systems.

> [!NOTE]
> This content uses examples and concepts from the [chatlas library](https://posit-dev.github.io/chatlas/) and is made available under the Creative Commons Attribution license. See [LICENSE.md](./LICENSE.md) for details.

## What are Large Language Models?

Large Language Models (LLMs) are AI systems that can understand and generate human-like text. They power applications like ChatGPT, Claude, and Gemini. This workshop teaches you to build your own applications using these powerful models through the chatlas Python library.

**chatlas** is a Python library developed by Posit that simplifies working with LLMs by providing:

- **Unified Interface**: Work with OpenAI, Anthropic, Google, and other providers using the same API
- **Conversation Management**: Automatic context and history handling
- **Function Calling**: Extend LLMs with custom Python functions
- **Streaming Support**: Real-time response processing
- **Multimodal Capabilities**: Work with text, images, and files

## Workshop Overview

This workshop takes you from basic setup to building production-ready LLM applications. Each tutorial includes hands-on exercises and real-world examples.

### Target Audience

- Python developers interested in AI and LLMs
- Data scientists wanting to integrate LLMs into their workflows
- Researchers looking to automate analysis and writing tasks
- Anyone wanting to build practical AI applications

### Prerequisites

- Basic Python programming knowledge
- Understanding of API concepts
- Access to LLM provider accounts (OpenAI, Anthropic, etc.)
- Familiarity with command-line interfaces

## Tutorial Structure

The workshop consists of four progressive tutorials:

### [0. Setting Up Your LLM Development Environment](0_setup.qmd)

**Type**: Tutorial | **Duration**: 45-60 minutes

Learn to set up a complete Python environment for LLM development, including API key management, virtual environments, and cost controls.

**You will learn to**:

- Set up Python and virtual environments for LLM work
- Install and configure the chatlas library
- Obtain and securely manage API keys from various providers
- Understand API costs and implement cost management
- Verify your setup with working examples

### [1. Basic chatlas Usage and Conversations](1_basic-usage.qmd)

**Type**: Tutorial | **Duration**: 60-75 minutes

Master the fundamentals of chatlas for creating conversations, managing context, and working with different LLM models and providers.

**You will learn to**:

- Create chat instances with different LLM providers
- Conduct single-turn and multi-turn conversations
- Use system prompts to control model behavior
- Handle different response types and formats
- Implement error handling and debugging techniques
- Build practical assistants and tutors

### [2. Advanced LLM Techniques with chatlas](2_advanced-techniques.qmd)

**Type**: Tutorial | **Duration**: 90-120 minutes

Explore advanced features including function calling, multimodal inputs, streaming responses, and sophisticated prompt engineering techniques.

**You will learn to**:

- Implement function calling to extend LLM capabilities
- Create custom tools for data analysis and external system integration
- Work with images, files, and multimodal content
- Use streaming for real-time applications
- Apply advanced prompt engineering patterns
- Build intelligent agents with multiple capabilities
- Monitor performance and handle production concerns

### [3. Building Real-World LLM Applications](3_practical-applications.qmd)

**Type**: Tutorial | **Duration**: 120-150 minutes

Build four complete, production-ready applications that solve real business problems using advanced LLM techniques.

**You will learn to**:

- Build a Document Intelligence System for automated analysis
- Create a Research Assistant for information synthesis
- Develop a Code Review Bot with automated feedback
- Construct a Writing Assistant for content creation
- Implement proper error handling and user interfaces
- Understand deployment and scaling considerations

## Getting Started

### Quick Start

1. **Complete the Setup**: Start with [0_setup.qmd](0_setup.qmd) to configure your environment
2. **Learn the Basics**: Work through [1_basic-usage.qmd](1_basic-usage.qmd)
3. **Explore Advanced Features**: Continue with [2_advanced-techniques.qmd](2_advanced-techniques.qmd)
4. **Build Applications**: Complete [3_practical-applications.qmd](3_practical-applications.qmd)

### Time Commitment

- **Quick Start** (Tutorials 0-1): 2-3 hours
- **Complete Workshop**: 6-8 hours
- **Self-paced**: Can be completed over multiple sessions

### Learning Path Options

**For Beginners**: Complete all tutorials in order
**For Experienced Developers**: Start with tutorial 1, skim setup as needed
**For Specific Applications**: Complete tutorials 0-1, then focus on relevant sections of tutorials 2-3

## System Requirements

- **Python**: 3.10 or newer
- **Operating System**: Windows, macOS, or Linux
- **RAM**: 4GB minimum, 8GB recommended
- **Internet Connection**: Required for API access
- **API Budget**: $10-50 for learning (varies by usage)

## Required API Keys

You'll need at least one of these:

- **OpenAI**: Most popular, good documentation, moderate cost
- **Anthropic (Claude)**: High-quality responses, competitive pricing  
- **Google (Gemini)**: Good free tier, competitive features
- **Local Models**: Free but requires setup (Ollama, etc.)

## Additional Resources

### Official Documentation

- [chatlas Documentation](https://posit-dev.github.io/chatlas/)
- [chatlas GitHub Repository](https://github.com/posit-dev/chatlas)
- [OpenAI API Documentation](https://platform.openai.com/docs)
- [Anthropic API Documentation](https://docs.anthropic.com/)

### Video Resources

- [Getting Started with chatlas](https://youtu.be/owDd1CJ17uQ) - Official introduction video

### Community and Support

- [chatlas GitHub Issues](https://github.com/posit-dev/chatlas/issues)
- [Posit Community](https://forum.posit.co/)
- [OpenAI Community](https://community.openai.com/)

### Related Learning

- [Prompt Engineering Guide](https://www.promptingguide.ai/)
- [LangChain Documentation](https://docs.langchain.com/)
- [Hugging Face Transformers](https://huggingface.co/docs/transformers)

## Workshop Philosophy

This workshop follows the **Diátaxis framework** for technical documentation:

- **Tutorials** (like these): Learning-oriented, hands-on lessons with practical exercises
- **How-to guides**: Problem-oriented instructions for specific tasks
- **Reference material**: Information-oriented technical descriptions
- **Explanation**: Understanding-oriented discussions of concepts

All content is designed as **tutorials** - practical, hands-on lessons that teach through doing real projects.

## Cost Management

### Estimated Costs

- **Tutorial 0-1**: $2-5 (basic testing and learning)
- **Tutorial 2**: $5-10 (function calling and advanced features)
- **Tutorial 3**: $10-20 (building complete applications)
- **Total Workshop**: $20-35 (varies by model choice and usage)

### Cost-Saving Tips

- Start with cheaper models (gpt-3.5-turbo vs gpt-4)
- Use shorter prompts when learning
- Set up billing alerts on provider platforms
- Consider free tiers (Google Gemini, local models)

## Example Applications Built

By completing this workshop, you'll have built:

1. **Document Intelligence System**
   - Analyze and summarize documents
   - Extract key information automatically
   - Generate reports and insights

2. **Research Assistant**
   - Gather information from multiple sources
   - Synthesize findings into coherent reports
   - Manage research sessions and bibliography

3. **Code Review Bot**
   - Analyze code for bugs and improvements
   - Provide specific feedback and suggestions
   - Support multiple programming languages

4. **Writing Assistant**
   - Create content from outlines
   - Improve existing text for clarity and style
   - Generate ideas and brainstorm topics

## Contributing and Feedback

This workshop is part of the IPA Research and Data Science Training. If you find issues or have suggestions:

1. Check existing [GitHub Issues](https://github.com/your-repo/issues)
2. Submit new issues or suggestions
3. Contribute improvements via pull requests

## License and Attribution

This workshop content is licensed under [CC BY 4.0](./LICENSE.md).

**chatlas Library**: Licensed under MIT by Posit PBC  
**Video Content**: [Getting Started with chatlas](https://youtu.be/owDd1CJ17uQ) by Posit  
**Tutorial Content**: Created for IPA Research and Data Science Training  

## Troubleshooting

### Common Issues

**"Cannot install chatlas"**:

- Ensure you're using Python 3.10+
- Try upgrading pip: `pip install --upgrade pip`
- Use virtual environments to avoid conflicts

**API Authentication Errors**:

- Verify your API keys are correct
- Check that billing is set up on provider platforms
- Ensure `.env` file is in the correct location

**High API Costs**:

- Monitor usage on provider dashboards
- Switch to cheaper models for testing
- Use shorter prompts and fewer iterations

**Rate Limiting**:

- Wait before retrying requests
- Consider upgrading your API plan
- Implement exponential backoff in your code

### Getting Help

1. **Check tutorial troubleshooting sections**: Each tutorial includes specific guidance
2. **Consult chatlas documentation**: [posit-dev.github.io/chatlas](https://posit-dev.github.io/chatlas/)
3. **Search GitHub issues**: Often questions have been asked before
4. **Ask on forums**: Use community resources for additional support

## What You'll Achieve

After completing this workshop, you'll be able to:

- Build conversational AI applications with multiple LLM providers
- Create intelligent agents that can use tools and external APIs
- Process multimodal content including text, images, and documents  
- Implement production-ready applications with proper error handling
- Apply prompt engineering techniques for optimal results
- Manage costs and monitor performance in production systems

---

**Workshop Duration**: 6-8 hours total | **Skill Level**: Beginner to Advanced | **Last Updated**: 2024

Ready to start building with LLMs? Begin with [Tutorial 0: Setting Up Your Environment](0_setup.qmd)!
