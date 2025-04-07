## 🔍 Insights
### Efficiency and Cost Analysis:
<p align="justify">
This experiment, evaluate the computational efficiency and cost of implementation and use of LLMs for RE tasks. The analysis focuses on comparing the models over terms such as their token consumption, processing speed, financial cost, and overall effectiveness. The goal of this analysis is to determine which model offers the best trade-off between cost, efficiency, and accuracy when generating requirements documentation, including user stories, Epic FDS, and FDS.

Computational efficiency of the models assessed based on speed of generation, understanding how quick each model produces documents, verbosity and redundancy by understanding the model tendency to generate excessive or repetitive information, handling of complex requirements on the model ability to capture detailed technical specification accurately, and token limitations which is the model restriction of the input context windows.
</p>

- <p align="justify"> <b>Speed and Processing Time:</b> In this context, each model showed a unique characteristic in speed and output generation. GPT4, generated the most structured, contextually relevant documentation, making it the best choice for technical accuracy. In counter part, since the model tended to produce extensive descriptions, this behavior led to increasing token usage and response time therefore its processing speed was slower due to its ability to generate detailed and complex outputs. The examination also showed GPT3 was significantly faster but highly redundant. It frequently rephrased similar content multiple times, leading to unnecessary token consumption. While it could generate user stories quickly, the manual effort required to filter out redundant text made it less efficient in practical scenarios. Llama also revealed that it is the most computationally lightweight model and generated concise and efficient outputs. However, it struggled to maintain technical depth and specificity, often requiring manual expansion by human analysts. This trade-off made it more useful for high-level documentation but less suitable for detailed functional specifications.</p>
- <p align="justify"><b>Handling of Token Limits:</b> A major challenge during experimentation was the limitation of token context windows, particularly for GPT3 and Llama-3, which have smaller input capacities compared to GPT4. To answer this limitation for models, raw input data (e.g., requirement lists, meeting notes, regulatory documents) had to be summarized manually before feeding it into the models. This summarization not only added an extra processing step to process, but also increased the risk of critical information loss, leading to less efficiency for the models. In this case, GPT4’s extended token capacity made it well-suited for handling long technical documents, reducing the need for excessive summarization.</p>
- <p align="justify"><b>Cost Analysis:</b> The result has been reported for cost per 1,000 tokens, total token usage for each model and overall expenditure on cloud computing resources. The result revealed that GPT4 was the most expensive model primarily due to its high output cost and extensive token generation. In counter part, GPT3 was the cheapest model but its redundancy meant that token efficiency was lower, requiring additional human revision. Llama fell in the middle, offering a cheaper alternative than GPT4 while still providing structured outputs.</p>
</p>

Presented below are the input/output and total costs associated with each model in this experiment.


<table style="width:100%;">
  <tr>
    <td style="width:50%; vertical-align: top; padding-right: 20px;">
      <table style="width:100%; text-align: center;">
        <thead>
          <tr>
            <th colspan="4" style="text-align: center;">Costs of Each Model for 1000 Tokens</th>
          </tr>
          <tr>
            <th>Model</th>
            <th>Input Cost</th>
            <th>Output Cost</th>
            <th>Total Cost</th>
          </tr>
        </thead>
        <tbody>
          <tr>
            <td>GPT3</td>
            <td>0.0010</td>
            <td>0.0019</td>
            <td>3,60</td>
          </tr>
          <tr>
            <td>Llama</td>
            <td>0.0034</td>
            <td>0.0099</td>
            <td>11,80</td>
          </tr>
          <tr>
            <td>GPT4</td>
            <td>0.0047</td>
            <td>0.0141</td>
            <td>24,80</td>
          </tr>
        </tbody>
      </table>
    </td>
  </tr>
</table>


<p align="justify">
To conclude, GPT4 offers the highest accuracy and structured documentation but at a significantly higher cost, making it suitable for projects requiring minimal manual refinement. GPT3, although it’s cost-effective, suffers from redundancy, requiring substantial human intervention to refine outputs, which can offset its financial advantage. Llama, while more efficient in token usage, lacks technical depth, making it a viable choice for high-level summarization rather than detailed requirement specifications.
</p>

👉 For a detailed evaluation based on expert feedback and TAM analysis, see [Expert Feedback and TAM Evaluation](../Interview%20with%20Analyst/Expert-Feedback-And-TAM-Evaluation.md).
