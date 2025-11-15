
# LLM Daily Dev Prompts

This repository is a curated collection of prompts designed to enhance the quality, consistency, and reliability of Large Language Models (LLMs) in a daily software development workflow. By standardizing our interactions, we can guide the LLM to produce better, more robust, and more maintainable results.

## Getting Started

The prompts in this repository are not standalone scripts but are meant to be included as part of your interaction with an LLM. You can copy-paste the content of a prompt file directly into your chat or use a tool that automatically includes it in your LLM context for every new session.

## Prompts in this Toolkit

### 📂 `Virtues.md`

This is the foundational prompt of the toolkit. It defines a set of core principles and standards (the "virtues") that the LLM should follow when performing any task, such as clarity, robustness, efficiency, and security.

The goal of using `Virtues.md` is to establish a consistent quality baseline for all LLM-generated output, from code to documentation.

#### Recommended Workflow

To use `Virtues.md` effectively, follow this three-step process:

**1. Initial Task Instruction**

When assigning a new task, instruct the LLM to first read `Virtues.md` and adhere to its principles throughout the task. This sets the stage and defines the success criteria from the beginning.

**Example Prompt:**
```
Please read through @Virtues.md, and make sure your behavior follows the principles in the document.
```

**2. Post-Coding Self-Review**

After the LLM has generated the code or solution, its context window might have truncated the initial instructions. To ensure the standards are met, explicitly ask it to re-read `Virtues.md` and review its own work against the defined virtues. This forces a critical second pass.

**Example Prompt:**
```
Now, please conduct a deep self reflection about your behavior, see if it is following @Virtues.md
```

**3. Work Report and Final Audit**

To verify the quality and document the process, ask the LLM to generate a work report. Then, to ensure an unbiased review, start a **new chat session/context** and ask the LLM to audit the generated report against the standards in `Virtues.md`.

**Step 3a: Report Generation**
```
Please conduct a thorough review of the job associated with commit [COMMIT ID] and provide a report on its compliance with @Virtues.md
```

## Contributing

Contributions are welcome! If you have a prompt that has proven useful in your workflow, feel free to open a Pull Request. Please include a clear description of what the prompt does and a recommended usage workflow.

## License

This project is licensed under the MIT License - see the `LICENSE` file for details.