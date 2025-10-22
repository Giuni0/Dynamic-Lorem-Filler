
**Dynamic Lorem padding for incomplete LaTeX text blocks**

`filltext.sty` is a lightweight LaTeX package for **automatically padding user-supplied text with Lorem Ipsum** up to a desired character or word count. It helps maintain consistent document layouts while drafting, simulating a “live typing” or “autofill” effect in LaTeX documents.

---

## Features

- Fills a defined text length using your input plus Lorem Ipsum text  
- Supports both **character** and **word** length modes  
- Respects user text and smoothly appends filler text  
- Works seamlessly with `lipsum` for consistent placeholder text  
- Built with **LuaLaTeX** for speed and flexibility  

---

## Requirements

- **LuaLaTeX** (this package relies on Lua scripting)  
- LaTeX packages:  
  - `luacode`  
  - `lipsum`

---

## Installation

1. Download `filltext.sty` from this repository.  
2. Place it in your LaTeX project directory or in a system-wide path (e.g., `~/texmf/tex/latex/filltext/`).  
3. Include it in your document preamble:

    
   \usepackage{filltext}
    

4. Compile your document with **LuaLaTeX**.

---

## Usage

### Basic Command

 
\filltext[<mode>]{<target_length>}{<user_text>}
 

**Arguments:**

- `<mode>` (optional): Filling mode — `char` (default) or `word`  
- `<target_length>`: Desired total number of characters or words  
- `<user_text>`: Your partial text that will be filled up with Lorem Ipsum  

### Example

 
\documentclass{article}
\usepackage{filltext}

\begin{document}

% Character mode
\filltext{200}{This section is partially written. }

\vspace{1em}

% Word mode
\filltext[word]{50}{This abstract will eventually be extended}

\end{document}
 

Output:
- The first block will be padded to 200 total **characters**.  
- The second block will be padded to 50 total **words**.  

---

## Example Output

> This section is partially written. Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore...

---

## Roadmap

- [ ] Optional truncation of text that exceeds the target length  
- [ ] Multiple Lorem sources (e.g., random paragraph cycling)  
- [ ] Visual width–based alignment for typesetting experiments  

---

## License

MIT License © 2025  
Created by Giunio Osman-Mansour

---

## Contributing

Pull requests are welcome. If you’d like to propose new features or bug fixes:

1. Fork the repo  
2. Create a feature branch  
3. Submit a pull request with a clear description of your update  
 
