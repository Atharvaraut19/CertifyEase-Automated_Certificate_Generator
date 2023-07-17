**CertifyEase: Automated Certificate Generator**

The Certificate Generator is a Python script that automates the process of creating personalized certificates. It uses the Python Imaging Library (PIL) to manipulate images and add custom text, logos, and signatures to a certificate template. This script is particularly useful for events or programs where you need to generate multiple certificates with unique names and other details.

**Requirements**

- Python 3.x
- Python Imaging Library (PIL) - You can install it using `pip`:
  ```
  pip install pillow
  ```

**Usage**

1. Clone or download the repository to your local machine.
2. Place the certificate template image (`quarktemplate.png`) in the root directory of the project.
3. Create a `font` directory within the root directory and place the required font files (`GreatVibes-Regular.ttf`, `RobotoSlab-Regular.ttf`, and `OpenSans-Regular.ttf`) in it. These fonts are used for different text styles on the certificate.
4. Prepare the following inputs for each certificate you want to generate:
   - `name`: The name to be displayed on the certificate.
   - `text`: A paragraph of text to be displayed on the certificate. This text will be split into three lines for better layout.
   - `logo`: The image file (e.g., `quark.png`) to be placed on the certificate. This could be an organization logo or an event logo.
   - `sig_1`: The signature image file (e.g., `Signature_1.jpeg`) of the first signer.
   - `head_1`: The name of the first signer.
   - `designation_1`: The designation of the first signer.
   - `sig_2`: The signature image file (e.g., `Signature_2.jpeg`) of the second signer.
   - `head_2`: The name of the second signer.
   - `designation_2`: The designation of the second signer.
5. Modify the `names` list in the script to include the names for which you want to generate certificates.
6. Run the script:
   ```
   python certificate_generator.py
   ```

**Example**

Suppose you have the following inputs:

```python
names = ['Siddhesh', 'Ritu']
paragraph = "Congratulations for participating in the XYZ event organized in Month - Year by our awesome community."
logo = "quark.png"

sig_1 = "Signature_1.jpeg"
head_1 = "Raj"
designation_1 = "Club Head"

sig_2 = "Signature_2.jpeg"
head_2 = "Atharva"
designation_2 = "Co Head"

for name in names:
    make_certificates(name, split_sentence(paragraph), logo, sig_1, head_1, designation_1, sig_2, head_2, designation_2)

print(len(names), "certificates generated.")
```

**Output**

The generated certificates will be saved in the `out` directory with filenames based on the corresponding names.


Note: The images shown above are just examples. The actual certificates will vary based on the provided input and template.

Feel free to customize the inputs and the template to suit your needs. Enjoy creating personalized certificates for your events!
