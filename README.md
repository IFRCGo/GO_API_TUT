# IFRC GO API Tutorial

[![Binder](https://mybinder.org/badge_logo.svg)](https://mybinder.org/v2/gh/IFRCGo/GO_API_TUT/master)

Interactive Python notebooks demonstrating how to use the IFRC GO API.

## 🚀 Quick Start with Binder

Click the badge above to launch the notebooks in your browser - no installation required!

> **Note:** You'll need an IFRC GO API token. [Learn how to generate one](https://go-wiki.ifrc.org/en/go-api/Connecting_to_GO_API#generating_an_api_token)

## 📓 Notebooks

| Notebook             | Description                         |
| -------------------- | ----------------------------------- |
| `notebook_1.ipynb` | Projects analysis by sector (Nepal) |
| `notebook_2.ipynb` | Events analysis by country          |
| `notebook_3.ipynb` | Appeal documents fetcher            |
| `notebook_4.ipynb` | Project status distribution         |
| `notebook_5.ipynb` | Surge alerts analysis               |
| `notebook_6.ipynb` | Deaths by event type and country    |

### 🏠 Local Units Management

Specialized notebooks for managing Red Cross / Red Crescent local units.

Note: You can only do a Bulk upload of local units, add information on new local unit type for a country or update exiting local unit information via the API only after you have been granted appropriate permissions.

For National Society Users contact <im@ifrc.org> for necessary permissions.

| Notebook                                 | Description                                                 |
| ---------------------------------------- | ----------------------------------------------------------- |
| `01_list_local_units_by_country.ipynb` | List local units for a specific country with status filters |
| `02_patch_local_unit.ipynb`            | Update specific fields of an existing local unit (Staging)  |
| `03_put_local_unit.ipynb`              | Create or fully replace a local unit type (Staging)         |
| `04_bulk_upload_local_units.ipynb`     | Download templates and perform bulk uploads via Excel       |

## 🔧 Local Setup

1. Clone the repository:

   ```bash
   git clone https://github.com/IFRCGo/GO_API_TUT.git
   cd GO_API_TUT
   ```

2. Create a virtual environment and install dependencies:

   ```bash
   python -m venv .venv
   source .venv/bin/activate  # On Windows: .venv\Scripts\activate
   pip install -r requirements.txt
   ```

3. Create a `.env` file with your API token:

   ```bash
   cp .env.example .env
   # Edit .env and add your token
   ```

4. Launch Jupyter:

   ```bash
   jupyter notebook notebooks/
   ```

## 🔑 API Token Setup

To use these notebooks, you need an IFRC GO API token.

**Follow the official guide to generate your token:**
👉 [Generating an API Token - GO Wiki](https://go-wiki.ifrc.org/en/go-api/Connecting_to_GO_API#generating_an_api_token)

Once you have your token, add it to your `.env` file:

```
IFRC_API_TOKEN=your_token_here
```

## 📁 Project Structure

```
GO_API_TUT/
├── notebooks/           # Jupyter notebooks
│   ├── local_units/     # Local unit management notebooks
│   │   ├── 01_list_local_units_by_country.ipynb
│   │   └── ...
│   ├── notebook_1.ipynb
│   ├── notebook_2.ipynb
│   └── ...
├── .env.example         # Template for environment variables
├── requirements.txt     # Python dependencies
├── runtime.txt          # Python version for Binder
└── postBuild            # Binder setup script
```

## License

MIT License
