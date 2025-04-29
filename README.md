# EE2272 Quiz Document

This project contains:
- `EE2272_Quiz.tex`: A sample LaTeX document for a quiz/exam.
- `examstyle.cls`: A custom LaTeX class file defining the styling for quizzes and exams.

## Purpose
The setup allows instructors and students to easily prepare well-formatted quizzes using a consistent styling template.

## Files
- `examstyle.cls`: LaTeX class defining headers, footers, sections, question formatting, and point allocations.
- `EE2272_Quiz.tex`: A LaTeX source file that demonstrates how to use the `examstyle` class to create a formatted quiz.

## How to Compile
1. Ensure that both `EE2272_Quiz.tex` and `examstyle.cls` are in the same directory.
2. Use any standard LaTeX editor (Overleaf, TeXShop, TeXstudio, etc.) to open `EE2272_Quiz.tex`.
3. Compile the file using **PDFLaTeX**.

```bash
pdflatex EE2272_Quiz.tex
```
---

# 📘 USERMANUAL

## Overview
The EE2272 Quiz Template is a simple and flexible system to create professional-looking quizzes using LaTeX. It uses a custom class file `examstyle.cls` which defines custom environments, commands, and styling elements to facilitate quiz/exam creation.

---

## 1. Files Description

### `examstyle.cls`
Defines:
- Page margins
- Title formatting
- Section and subsection formatting
- Custom environments like `question`, `\vopt`, `\hopt`.
- Header and footer details

### `EE2272_Quiz.tex`
A sample LaTeX document showing how to use the custom class.
It includes:
- Title page generation
- Quiz instructions
- Multiple-choice and descriptive questions
- Marks allocation

---

## 2. How to Use

### Step 1: Setup Variables
Place both `EE2272_Quiz.tex` and `examstyle.cls` in the same working directory.
```Latex
%%  Global Commands (User-defined fields) %%
%% Define your variables here %%
\newcommand{\TheInstitute}{National Institute of Technology, Rourkela}
\newcommand{\TheLogo}{path_to_logo} % Preferabel resolution (640 X 640) px 
\newcommand{\TotalQuestions}{10} % Total No of Questions
\newcommand{\Fullmarks}{10} % Total assigned mark for the test
\newcommand{\MarksPerQuestion}{1} % Marks assigned per question (Evenly Distributed) (Each question carries 1 or 2 marks.)
\newcommand{\SubjectCode}{EE2272} % Subject code
\newcommand{\SubjectName}{Power Electronics Lab} % Subject Name
\newcommand{\ExamDuration}{30 Min} % Test duration 
```
### Step 2: Setup Evaluation Tables
#### 2.1: 10 Marks Evaluation Table [Short Table]
```Latex
\begin{minipage}{\textwidth}
\section*{Evaluation:}
\vspace{-1cm}
\renewcommand{\arraystretch}{2}
\resizebox{\columnwidth}{!}{%
\begin{tabular}{llllllllllll}
 &  &  &  &  &  &  &  &  &  &  &  \\ \cline{1-10} \cline{12-12} 
\multicolumn{1}{|c|}{Q1} &
  \multicolumn{1}{c|}{Q2} &
  \multicolumn{1}{c|}{Q3} &
  \multicolumn{1}{c|}{Q4} &
  \multicolumn{1}{c|}{Q5} &
  \multicolumn{1}{c|}{Q6} &
  \multicolumn{1}{c|}{Q7} &
  \multicolumn{1}{c|}{Q8} &
  \multicolumn{1}{c|}{Q9} &
  \multicolumn{1}{c|}{Q10} &
  \multicolumn{1}{l|}{\multirow{2}{*}{}} &
  \multicolumn{1}{l|}{\multirow{2}{*}{\begin{tabular}[c]{@{}l@{}}Obtained Marks\\   \noindent\hfill\Huge \textbf{/\Fullmarks}\end{tabular}}} \\ \cline{1-10}
\multicolumn{1}{|c|}{} &
  \multicolumn{1}{c|}{} &
  \multicolumn{1}{c|}{} &
  \multicolumn{1}{c|}{} &
  \multicolumn{1}{c|}{} &
  \multicolumn{1}{c|}{} &
  \multicolumn{1}{c|}{} &
  \multicolumn{1}{c|}{} &
  \multicolumn{1}{c|}{} &
  \multicolumn{1}{c|}{} &
  \multicolumn{1}{l|}{} &
  \multicolumn{1}{l|}{} \\ \cline{1-10} \cline{12-12} 
 &  &  &  &  &  &  &  &  &  &  &  \\
 &  &  &  &  &  &  &  &  &  &  &  \\
 &  &  &  &  &  &  &  &  &  &  &  \\
 &  &  &  &  &  &  &  &  &  &  & 
\end{tabular}%
}
\hfill
\end{minipage}
```
##### Already defined in the class file, use shortcut
```latex
\shortevaluationtable{10}
\vspace*{-6cm} % If \shortevaluationtable{10} is active
```
#### 2.2: 20 Marks Evaluation Table [Long Table]
```Latex
\begin{minipage}{\textwidth}
\section*{Evaluation:}
\vspace{-1cm}
\renewcommand{\arraystretch}{2}
\begin{longtable}{ccccccccccl|c|}
\\
\cline{1-10} \cline{12-12}
\multicolumn{1}{|c|}{\textbf{Q1}} &
  \multicolumn{1}{c|}{\textbf{Q2}} &
  \multicolumn{1}{c|}{\textbf{Q3}} &
  \multicolumn{1}{c|}{\textbf{Q4}} &
  \multicolumn{1}{c|}{\textbf{Q5}} &
  \multicolumn{1}{c|}{\textbf{Q6}} &
  \multicolumn{1}{c|}{\textbf{Q7}} &
  \multicolumn{1}{c|}{\textbf{Q8}} &
  \multicolumn{1}{c|}{\textbf{Q9}} &
  \multicolumn{1}{c|}{\textbf{Q10}} &
  \multirow{5}{*}{} &
  \multirow{5}{*}{\textbf{\begin{tabular}[c]{@{}c@{}}Obtained Marks\\ \vspace{0.1cm}\\ \hline\\ \vspace{-0.2cm}\Huge 20\end{tabular}}} \\ \cline{1-10}
\multicolumn{1}{|c|}{} &
  \multicolumn{1}{c|}{} &
  \multicolumn{1}{c|}{} &
  \multicolumn{1}{c|}{} &
  \multicolumn{1}{c|}{} &
  \multicolumn{1}{c|}{} &
  \multicolumn{1}{c|}{} &
  \multicolumn{1}{c|}{} &
  \multicolumn{1}{c|}{} &
  \multicolumn{1}{c|}{} &
   &
   \\ \cline{1-10}
\multicolumn{10}{l}{} &
   &
   \\ \cline{1-10}
\endhead
%
\multicolumn{1}{|c|}{\textbf{Q11}} &
  \multicolumn{1}{c|}{\textbf{Q12}} &
  \multicolumn{1}{c|}{\textbf{Q13}} &
  \multicolumn{1}{c|}{\textbf{Q14}} &
  \multicolumn{1}{c|}{\textbf{Q15}} &
  \multicolumn{1}{c|}{\textbf{Q16}} &
  \multicolumn{1}{c|}{\textbf{Q17}} &
  \multicolumn{1}{c|}{\textbf{Q18}} &
  \multicolumn{1}{c|}{\textbf{Q19}} &
  \multicolumn{1}{c|}{\textbf{Q20}} &
   &
   \\ \cline{1-10}
\multicolumn{1}{|c|}{} &
  \multicolumn{1}{c|}{} &
  \multicolumn{1}{c|}{} &
  \multicolumn{1}{c|}{} &
  \multicolumn{1}{c|}{} &
  \multicolumn{1}{c|}{} &
  \multicolumn{1}{c|}{} &
  \multicolumn{1}{c|}{} &
  \multicolumn{1}{c|}{} &
  \multicolumn{1}{c|}{} &
   &
   \\ \cline{1-10} \cline{12-12} 
\end{longtable}
}
\hfill
\end{minipage}
```
##### Already defined in the class file, use shortcut
```latex
\longevaluationtable{}{20}
```
### Step 3: Insert Questions
#### MCQ Type
```Latex
\begin{Question}[mcq]
    \qitem{A single-phase half-controlled bridge rectifier is connected to a 230 V, 50 Hz AC supply. The load is purely resistive with a resistance of $R = 10 \Omega$. The firing angle of the SCRs is $\alpha = 60^o$. The average output voltage across the load will be:}
    \hopt{325.27 V}
    \hopt{160 V}
    \hopt{\correctoption{155.3 V}}
    \hopt{170 V}
    \label{CO2} % Labling question will helpful while displaying Explanations
\end{Question}
```
#### Theory/Descriptive Question
```Latex
\begin{Question}[theory]
  \qitem{Question statement here./?}
  \correctoption{Optional/Not requried}
  \vspace{Give some empty space to write answers.}
  \label{CO1} % Optional but helpful to provide expalation
\end{Questions}
```
##### #Example usage
```Latex
\begin{Question}[theory]
    \qitem{Draw the I-V characteristics of SCR and transfer characteristic of N-channel MOSFET. Identify all regions and parameters clearly.}
    \label{CO1}
    \correctoption*{Diagram need to be drawn.} % Optional
    \vspace{4cm} % Empty space for answer
\end{Question}
```

### Step 4: Placing Options

#### Vertcal Options
- It will place option in vertical manner and automatically label it as *(A), (B), ..., (D)*
- ```\corretoption{}``` can be placed inside ```\vopt{\correctoption{Option_statement}}```.
##### Example usage
```Latex
\vopt{Mango}
\vopt{\correctoption{Orange}}
\vopt{Apple}
\vopt{Banana}
```
- This will give:
- ![image](https://github.com/user-attachments/assets/05a45f52-d147-47ff-85a4-19984767d39e)


#### Horizontal Options
- It will place option in horizontal manner and automatically label it as *(A), (B), ..., (D)*
- ```\corretoption{}``` can be placed inside ```\hopt{\correctoption{Option_statement}}```.
##### Example usage
```Latex
\hopt{Mango}
\hopt{\correctoption{Orange}}
\hopt{Apple}
\hopt{Banana}
```
- This will give:
- ![image](https://github.com/user-attachments/assets/d9415a3b-9a9e-4a77-b4d8-131957c24722)

#### Answerkey (Example)
- ![image](https://github.com/user-attachments/assets/e52dcbe3-24a6-4ef4-a156-89c4b8c0dd1c)

### Step 4: Showing Explanations

```Latex
\showexplanation{Question_Label}{
  ... provide expalnations here ...
}
```
#### (Expample Usage)

```Latex
\showexplanation{CO2}{
$\bullet$ The input AC voltage is sinusoidal, and its peak value is:

\[
V_m = \sqrt{2} \cdot V_{\text{rms}} = \sqrt{2} \cdot 230 \approx 325.27 \, \text{V}
\]
$\bullet$ For a half-controlled bridge rectifier, the average output voltage is:

\[
V_{\text{avg}} = \frac{V_m}{\pi}(1 + \cos \alpha)
\]

$\bullet$ Substitute \( V_m = 325.27 \) V and \( \alpha = 60^\circ \):

\[
V_{\text{avg}} = \frac{325.27}{\pi}(1 + \cos 60^\circ) = \frac{325.27}{\pi}(1 + 0.5)
= \frac{325.27 \times 1.5}{\pi}
\approx \frac{487.9}{\pi} \approx 155.3 \, \text{V}
\]

% $\bullet$ Since the load is purely resistive:

% \[
% I_{\text{avg}} = \frac{V_{\text{avg}}}{R} = \frac{155.3}{10} = 15.53 \, \text{A}
% \]
}
```
![image](https://github.com/user-attachments/assets/bc3ffa57-9b60-414e-9ffb-33bc0389b227)

### Step 4: Toggle between Teacher mode and Student Mode (Hide/Show Answers, Answer Key and Explanations)

```Latex
\setboolean{showanswers}{true} % Correct Option, Answer key and Explantion is visible
```

```Latex
\setboolean{showanswers}{false} % Correct Option, Answer key and Explantion is hidden
```
