# Prompts for papers
*Note: This might need refinement to get the output similar to the one present in the files presented in this repository. A few manipulations had to be made. But they do provide a starting point*

## Prompt - Sections, Terminology, Chunks and Summaries

```
## **Step 1: Identify Sections**

1. Identify sections using **explicit headings** or **natural thematic breaks**.
2. Assign **descriptive titles** summarizing each section.
3. Provide **location data** for each section in `(Paragraph X–Y)` format.

### **Output Format**

	```markdown
	# English Output
	```

	```markdown
	### Step 1: Identify Sections (English)  
	- **Section 1: Introduction to Cooperation** (Paragraph 1–5)  
	- **Section 2: Evolutionary Model** (Paragraph 6–12)  
	```

	```markdown
	# Icelandic Output
	```

	```markdown
	### Skref 1: Greining á Kaflaskiptingu (Íslenska)  
	- **Kafli 1: Inngangur að Samvinnu** (Málsgrein 1–5)  
	- **Kafli 2: Þróunarlíkan** (Málsgrein 6–12)  
	```

→ **Confirm before moving to Step 2.**

---

## **Step 2: Extract Keywords**

1. Extract **key terms** for each section with **short definitions**, in order of appearance.

### **Output Format**

	```markdown
	# English Output
	```

	```markdown
	### Step 2: Extract Keywords (English)  
	- **Keyword 1:** Definition.  
	- **Keyword 2:** Definition.  
	```

	```markdown
	# Icelandic Output
	```

	```markdown
	### Skref 2: Útdráttur á Lykilhugtökum (Íslenska)  
	- **Lykilhugtak 1:** Skilgreining.  
	- **Lykilhugtak 2:** Skilgreining.  
	```

→ **Confirm before moving to Step 3.**

---

## **Step 3: Group Keywords into Thematic Clusters**

1. **Group related keywords** into **thematic clusters**.
2. Each cluster should have:
    - A **title** summarizing its focus.
    - A **short description** explaining the theme.
    - A **comma-separated list** of keywords in order.

### **Output Format**

	```markdown
	# English Output
	```

	```markdown
	### Step 3: Thematic Clusters (English)  
	**Cluster Name:** [Title]  
	**Description:** [Short explanation]  
	**Keywords:** [Comma-separated list]  
	```

	```markdown
	# Icelandic Output
	```

	```markdown
	### Skref 3: Þematískir Klasar (Íslenska)  
	**Heiti Klasans:** [Titill]  
	**Lýsing:** [Stutt útskýring]  
	**Lykilhugtök:** [Kommu-aðskilinn listi]  
	```

→ **Confirm before moving to Step 4.**

---

## **Step 4: Generate a Summary for Each Section**

For **each section**, create:

1. A **title** (1-4 words, max 6).
2. A **short description** (max 2 sentences).
3. A **2-4 paragraph abstract/overview** explaining the **core ideas and findings**.

### **Output Format**

	```markdown
	# English Output
	```

	```markdown
	### Step 4: Section Summaries (English)  
	**Title:** [Section Title]  
	**Short description:** [One or two sentences]  
	**Abstract:**  
	[Paragraph 1]  
	[Paragraph 2]  
	[Paragraph 3 (if needed)]  
	```

	```markdown
	# Icelandic Output
	```

	```markdown
	### Skref 4: Samantektir Kafla (Íslenska)  
	**Titill:** [Titill Kafla]  
	**Stutt lýsing:** [Ein eða tvær setningar]  
	**Samantekt:**  
	[Málsgrein 1]  
	[Málsgrein 2]  
	[Málsgrein 3 (ef nauðsynlegt)]  
	```

→ **After confirming, the process is complete!**
```

## Prompt to generate structured notes files for sections

```
Generate structured notes for the sections of the processed papers in **both English and Icelandic**. Each section from the papers should be included, and its title should be used as the header in markdown format.

Format the output as follows:

English output: 
	```markdown

	# Section 1: <Section 1 Title>  
	(Paragraphs X-Y)  
	<br><br><br><br><br>  
	
	# Section 2: <Section 2 Title>  
	(Paragraphs A-B)
	<br><br><br><br><br>  

	# Section 3: <Section 3 Title>  
	(Paragraphs C-D) 
	<br><br><br><br><br>  
	```

Icelandic output: 

	```markdown
	# Kafli 1: <Icelandic Section 1 Title>  
	(Málsgrein X-Y)  
	<br><br><br><br><br>  
	
	# Kafli 2: <Icelandic Section 2 Title>  
	(Málsgrein A-B)  
	<br><br><br><br><br>  
	
	# Kafli 3: <Icelandic Section 3 Title>  
	(Málsgrein C-D)  
	<br><br><br><br><br>  
	```

After every fifth section, starting at section five (special case: if the total number of sections is divisible by 5, do not do this after the last section):

- Add a new line, `<div style="page-break-after: always;"></div> `, and another new line before continuing.

Ensure that **English and Icelandic outputs are in separate code blocks**, maintaining an equal amount of empty space for formatting consistency. Place the entire output for each paper in its own respective code block.
```
