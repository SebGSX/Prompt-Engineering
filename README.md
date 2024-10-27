# Prompt Engineering

## Overview

This project is a production-ready implementation of two prompts that are used to configure ChatGPT to serve as a 
principal developer for pull request review support 
([Tom](https://github.com/SebGSX/Utilities/blob/main/prompt-engineering/pull-request-review.md)) and a product manager
([Tim](https://www.promptingguide.ai/)). The prompts have been exhaustively developed and tested over a period of about a year. 

While creating Tim was relatively straightforward, creating Tom was a highly complex proposition that required a 
suitably complex codebase upon which to "train" Tom. By train, I mean activate the prompt, provide Tom with code, 
then carefully review the output. The author thus created a multi-threaded listener using lock primitives to help 
ensure that Tom had a sufficiently complex problem to solve. As the code evolved, so too did the prompt. The result 
is a prompt that renders the latest model of ChatGPT as a highly capable principal developer adept at analysing 
codded solutions irrespective of the language, frameworks, or packages used.

### AI Custom Instructions (Standing Instructions)

ChatGPT has a useful feature called Custom Instructions. This feature allows the user to provide the AI with a set 
of standing instructions that are used to guide the AI in its all of its responses. Given that large language models 
(LLMs) are probabilistic systems trained on vast amounts of data, it behoves the user to limit the AI's domain so 
that more accurate and in-depth responses are generated.

The author has experimented with a variety of custom instructions over the past year to 18 months and has found that the
set provided within the [AI Custom Instructions](https://github.com/SebGSX/AI-Custom-Instructions) repository is the
most effective.

> **Note:** The custom instructions do evolve and are thus subject to change. Given the experimental nature of the work 
> the custom instructions are sometimes suboptimal and may contain errors or out-of-the-box thinking.

## Getting Started

To use the prompts, you will need to have access to OpenAI's ChatGPT service or the API. Other AIs will likely work; 
however, the author has only tested OpenAI's variant.

In its simplest form, simply copy the prompt's text into the chat window, then provide the code that should be
reviewed. The same works for Tim, the product manager. A somewhat more sophisticated approach is to use the Custom 
GPT feature of ChatGPT to create a customised chat using the prompts as the main system instructions. In that form, 
style guides, policies, and other documentation can be included to help guide the AI in its reviews. Such an 
approach is known as retrieval-augmented generation (RAG) and is a powerful tool for creating highly specialised AIs 
without needing to train a model from scratch or fine-tune an existing one.

> **Note:** You MUST ensure that your organisation's policies and procedures are followed when using the prompts and 
> any AI service in general. There are legitimate risks associated with using AI in a professional context, 
> including but not limited to: copyright infringement, data leakage, intellectual property theft, and more. Make 
> sure that any AI service you use is approved, compliant with your organisation's policies, and that you have the 
> necessary authorisations to use it. The author cannot and will not be held responsible for any misuse of the 
> prompts or any AI service.

### Getting Started with Tom (Principal Developer)

For a quick five-minute introduction to Tom, the principal developer, see the video:
[AI Pull Request Reviewer](https://rumble.com/v5j1zrx-ai-pull-request-reviewer.html?e9s=src_v1_ucp).

The author has found that the AI is more likely to provide a useful response if the code is: 
- Well-formatted;
- Clearly documented and annotated using domain-appropriate and precise, professional language in formal register;
- Applicable coding standards and conventions are followed; and
- Naming of namespaces, classes, methods, fields, properties, constants, and variables are meaningful and descriptive.

> **Note:** The guidance above can be generalised to any technical prompt for best results.

### Getting Started with Tim (Product Manager)

The author has found that the AI is more likely to provide a useful response if the request for work item definition is:
- Well-formatted;
- Specific and detailed;
- Uses domain-appropriate and precise, professional language in formal register; and
- Is clear and concise.

> **Note:** The guidance above can be generalised to any non-technical prompt for best results.

## Contributing

Contributions are welcome as are corrections. The author follows Crocker's Rules. Direct, honest, and constructive
feedback is appreciated. Please submit a pull request with your changes or an issue with your feedback.

## License

The project is licensed under the MIT License. Please see the `LICENSE` file for more information.

## Further Development

The author actively uses both prompts for all product and software engineering activities. As such, the prompts are 
constantly in use and will evolve. Additional prompts are planned, including a prompt for a technical writer to 
support documentation efforts.
