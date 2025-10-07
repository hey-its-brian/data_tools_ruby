# Data Tools (Ruby)

A collection of small, focused Ruby utilities for working with data: cleaning, reporting, automation, and light API integration.

This repo demonstrates practical Ruby scripting outside of Rails — modular, tested, and ready to extend.

---

## 🧩 Overview

These scripts are designed to show how plain Ruby can handle real-world data tasks:
- Parsing CSVs and generating formatted reports  
- Fetching and transforming JSON from APIs  
- Writing reusable helpers and loggers  
- Automating everyday data cleanup jobs  

Each tool is independent but shares a common structure for clarity and reuse.

---

## ⚙️ Tech Stack

- **Ruby** 3.2.5  
- **RSpec** for testing  
- **Bundler** for dependency management  

---

## 📂 Project Structure

```
data_tools_ruby/
├── lib/
│   ├── csv_reporter.rb           # Generates CSV summaries and filters
│   ├── api_fetcher.rb            # Fetches and transforms remote JSON data
│   ├── color_logger.rb           # Pretty terminal output helper
│   └── helpers/
│       └── time_utils.rb         # Time and date formatting helpers
├── scripts/
│   ├── generate_report.rb        # CLI entry point for CSV reporting
│   ├── fetch_and_clean_data.rb   # Pulls API data and saves cleaned output
│   └── notify_summary.rb         # Example of scheduling or email notification
├── spec/
│   └── csv_reporter_spec.rb
├── Gemfile
└── README.md
```

---

## 🚀 Getting Started

### Prerequisites

Install Ruby 3.2.5 and Bundler:
```bash
gem install bundler
```

Install dependencies:
```bash
bundle install
```

---

### Running a Script

Each script in `/scripts` can be executed directly with Ruby.

Example:
```bash
ruby scripts/generate_report.rb data/sample.csv
```

Output will be saved to `/output` (created automatically if missing) and printed to the terminal with colorized summaries.

---

### Example: CSV Reporter

**Input:**
```
applicant_name,household_size,total_income
Jane Doe,2,42000
John Smith,4,90000
```

**Output (terminal):**
```
✅ 1 record eligible for aid
⚠️ 1 record above threshold
```

**Output (file):**  
`output/filtered_report_2025-10-07.csv`

---

### Example: API Fetcher

Fetches and cleans JSON from a public API:
```bash
ruby scripts/fetch_and_clean_data.rb
```

Internally uses:
```ruby
require 'net/http'
require 'json'
```

and writes clean structured data to `output/api_results.json`.

---

## 🧪 Testing

Run all specs:
```bash
bundle exec rspec
```

---

## 🛠 Future Plans

- Add YAML configuration for script parameters  
- Include CLI option parsing (`OptionParser`)  
- Dockerfile for isolated execution  
- Publish gems for `ColorLogger` and `CsvReporter`

---

## 📄 License

MIT License — free to use, adapt, and destroy data responsibly.

---

## 👨‍💻 Author

**Brian Meyer**  
Ruby Developer & Automation Engineer  
[GitHub Profile](https://github.com/<your-username>)
