# MugUp Local
Custom mug mockup generator with mathematical text deflection and Amazon marketplace automation.

## Why It Exists
Creating realistic product mockups for print-on-demand requires expensive design software and manual work. This automates the entire pipeline from text input to Amazon-ready product listings with mathematically accurate text curvature that mimics real mug surfaces.

## What Makes It Interesting
- **Custom deflection library**: Built from scratch using quadratic curve fitting and pixel-level transformations to create realistic text curvature on mug surfaces
- **Mathematical precision**: Uses numpy polynomial fitting to solve 3-point equations for natural-looking text deflection
- **Production e-commerce pipeline**: Generates complete Amazon marketplace CSV files with 400+ product fields
- **Batch processing**: Validates input, renders hundreds of mockups, uploads to S3, and creates marketplace listings automatically

## Tech Stack
- **Image Processing**: PIL/Pillow for graphics manipulation
- **Mathematics**: NumPy for quadratic curve fitting and transformations
- **Cloud Storage**: AWS S3 with boto3
- **E-commerce**: Amazon Marketplace API integration
- **Validation**: Custom font/text validation with detailed error reporting

## How to Run
```bash
git clone https://github.com/lancejohnson/mugup-local.git
cd mugup-local
pip install -r requirements.txt

# Set AWS credentials
export AWS_ACCESS_KEY_ID=your_key
export AWS_SECRET_ACCESS_KEY=your_secret

# Run with input CSV
python src/render_mugs.py -F input.csv
```

## Demo
See example mug renders and Amazon CSV output in the repo.

## Status
Production-ready - Successfully used for actual Amazon marketplace listings.

## Notes
The mathematical deflection algorithm was developed through experimentation with quadratic curves to achieve realistic text curvature. Cross-platform font handling ensures consistent results on Windows and macOS.
