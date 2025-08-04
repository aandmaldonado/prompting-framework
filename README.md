# Prompting Framework

A comprehensive framework for creating structured prompts for Large Language Models (LLMs) in both JSON and Markdown formats.

> **📝 Attribution & Credits**: This framework is inspired by and builds upon the original JSON prompting concept shared by [How to Prompt](https://www.linkedin.com/company/how-to-prompt/posts/?feedView=all) on LinkedIn. The foundational idea of using structured JSON for prompt engineering was introduced in their post "[Your prompts are too vague. Try this JSON framework to get better results](https://www.linkedin.com/posts/how-to-prompt_your-prompts-are-too-vague-try-this-json-activity-7357047524890714113-SvdV?utm_source=share&utm_medium=member_desktop&rcm=ACoAAAcZFHUBIX-FVqWDsFlFbjodw2NA6Sv87hc)". This project expands upon that concept with additional parameters, examples, and comprehensive documentation.

## Overview

This framework provides a systematic approach to prompt engineering, ensuring consistent, high-quality outputs from AI models. It includes all necessary parameters for controlling generation, quality, compliance, and iteration.

## Files Structure

```
📁 prompting-framework/
├── 📄 README.md                        # Project documentation and guide
├── 📄 LICENSE                          # Creative Commons Attribution-ShareAlike 4.0 License
├── 📄 .gitignore                       # Git ignore rules for documentation projects
├── 📁 templates/                       # Framework templates
│   ├── 📄 json-prompting-framework.json    # JSON template
│   └── 📄 json-prompting-framework.md      # Markdown template
├── 📁 examples/                        # Example implementations
│   ├── 📄 data-analysis-report.md     # Technical analysis example
│   ├── 📄 creative-content.md         # Creative writing example
│   └── 📄 legal-document.md           # Legal document example
└── 📁 framework-results/               # Generated outputs from examples
    ├── 📄 data-analysis-report-result.md     # Analysis report output
    ├── 📄 creative-content-result.md         # Creative blog post output
    ├── 📄 legal-document-result.md           # Privacy policy output
    └── 📄 execution-summary.md               # Framework validation summary
```

## How to Use

### 1. Choose Your Format

- **JSON Format**: Use for programmatic integration, APIs, or when you need structured data
- **Markdown Format**: Use for human readability, documentation, or when working in text editors

### 2. Fill in the Template

1. Copy the template file of your choice
2. Replace all placeholder text (ALL_CAPS) with your specific requirements
3. Delete any sections you don't need
4. Add more examples if helpful
5. Adjust parameters based on your use case

**Note**: The `context` field can include both background information and specific data to process, eliminating the need for a separate `input` field. The framework has been simplified by consolidating redundant parameters and removing overly technical generation parameters. Related fields are now grouped logically and ordered by importance: `task` (action, type, objective, requirements), `scope` (audience, domain, context), `role` (primary, secondary, specialization), and `output` (style, format, constraints, generation) for better organization. The `examples` field is now a simple list of strings for maximum flexibility. The `notes` and `quality` fields have been removed to encourage more specific use of other fields.

### 3. Submit to LLM

Send the completed framework to your preferred LLM (ChatGPT, Claude, GPT-4, etc.)

## Parameter Guidelines

### Generation Parameters

#### Output Configuration

**Style Options:**
- **Formal**: Professional, business-like communication
- **Casual**: Relaxed, conversational tone
- **Fun**: Engaging, entertaining approach
- **Professional**: Industry-standard, polished content
- **Creative**: Innovative, imaginative content
- **Analytical**: Data-driven, logical approach

**Creativity Level:**
- **Conservative**: Use for factual, technical, or sensitive content
- **Balanced**: Good for most general use cases
- **Creative**: Use for marketing, storytelling, or innovative content
- **Experimental**: Use for brainstorming or when you want unexpected results

#### Sampling
- **Top-k**: Number of tokens to consider (lower = more focused)
- **Top-p**: Probability threshold (lower = more deterministic)
- **Frequency/Presence Penalty**: Control repetition (-2.0 to 2.0)
- **Repetition Penalty**: Avoid word repetition (1.0 = no penalty)

### Content Types

#### Technical/Analytical Content
- Temperature: 0.1-0.3
- Creativity Level: conservative
- Originality: FACTUAL or ANALYTICAL
- Citations: REQUIRED

#### Creative Content
- Temperature: 0.7-1.0
- Creativity Level: creative
- Originality: CREATIVE
- Citations: OPTIONAL

#### Legal/Medical Content
- Temperature: 0.1-0.2
- Creativity Level: conservative
- Originality: FACTUAL
- Citations: REQUIRED
- Compliance: Strict adherence to regulations

#### Marketing/Entertainment
- Temperature: 0.8-1.2
- Creativity Level: creative or experimental
- Originality: CREATIVE
- Citations: OPTIONAL

## Best Practices

### 1. Be Specific
- Use precise values for all fields
- Provide clear, detailed task descriptions
- Specify exact requirements

### 2. Provide Context
- Always include relevant background information
- Explain the purpose and audience
- Specify any constraints or limitations

### 3. Set Clear Constraints
- Define time limits and urgency
- Specify technical level and language
- Include compliance requirements

### 4. Include Examples
- Provide sample inputs and outputs
- Show the expected format and style
- Demonstrate the desired quality level

### 5. Consider Compliance
- Always specify regulatory requirements
- Include industry-specific standards
- Consider data sensitivity levels

### 6. Enable Iteration
- Allow for follow-up questions
- Set reasonable revision limits
- Enable feedback loops

## Use Cases

### Content Creation
- Blog posts, articles, reports
- Marketing copy, social media content
- Documentation, manuals, guides

### Data Analysis
- Insights, recommendations, summaries
- Market research, trend analysis
- Performance reports, dashboards

### Code Generation
- Scripts, functions, applications
- API documentation, code comments
- Testing scenarios, debugging

### Research
- Literature reviews, market analysis
- Competitive intelligence, surveys
- Academic papers, white papers

### Communication
- Emails, presentations, proposals
- Customer support, FAQs
- Training materials, tutorials

## Examples

The `examples/` folder contains three complete examples:

1. **Data Analysis Report**: Technical analysis with conservative settings
2. **Creative Content**: Blog post with creative settings
3. **Legal Document**: Privacy policy with strict compliance requirements

Use these as templates for your specific use cases.

## Tips for Success

1. **Start with the template**: Use the framework as a starting point
2. **Customize for your domain**: Adjust parameters for your specific field
3. **Test and iterate**: Refine your prompts based on results
4. **Keep it consistent**: Use the same framework across similar tasks
5. **Document your changes**: Track what works for future reference

## Support

For questions or improvements to the framework, please refer to the example files or create your own variations based on your specific needs.

## Credits & Attribution

### Original Inspiration
This prompting framework is based on the innovative JSON structure concept originally shared by **How to Prompt** on LinkedIn. The foundational approach of using structured JSON for prompt engineering was introduced in their viral post that demonstrated how to create more precise and effective prompts.

### Key References
- **[How to Prompt LinkedIn Post](https://www.linkedin.com/posts/how-to-prompt_your-prompts-are-too-vague-try-this-json-activity-7357047524890714113-SvdV?utm_source=share&utm_medium=member_desktop&rcm=ACoAAAcZFHUBIX-FVqWDsFlFbjodw2NA6Sv87hc)**: The original post that introduced the JSON prompting framework concept
- **[How to Prompt Company Page](https://www.linkedin.com/company/how-to-prompt/posts/?feedView=all)**: Official company page with additional prompt engineering resources
- **[Ruben Hassid LinkedIn Profile](https://www.linkedin.com/in/ruben-hassid/)**: Individual contributor to the prompt engineering community

### What This Project Adds
While inspired by the original concept, this project expands the framework with:
- Additional parameters for quality control and compliance
- Comprehensive documentation and best practices
- Multiple example implementations
- Extended generation parameters
- Iteration and feedback mechanisms
- Domain-specific guidelines

### License & Usage
This project is licensed under the [Creative Commons Attribution-ShareAlike 4.0 International License](LICENSE). This means you are free to share and adapt the material, but you must provide appropriate attribution and share any derivatives under the same license.

Please respect the original creators by maintaining proper attribution when sharing or building upon this work, as detailed in the [Credits & Attribution](#credits--attribution) section above.

---

**Note**: This framework is designed to be flexible and adaptable. Feel free to modify it to suit your specific requirements while maintaining the structured approach to prompt engineering. 