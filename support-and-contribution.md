# Support and contribution

### Contributions

Feel free to propose PR and suggest the improvements. I'll highly appreciate help with packaging for various distributions. If you wish to contribute with translation into your language, please see the `translations.py` file.\
\
If you'd like to contribute to the documentation, please make pull requests to [this repository](https://github.com/anufrievroman/waypaper-docs).

#### Contribution Instructions

1. Fork the `wayapaper` repository on Github.
2. Clone your fork of `waypaper`

```bash
git clone https://github.com/YOUR_GITHUB_USERNAME/waypaper.git
```

3. Enter the repository directory.

```bash
cd waypaper
```

4. Create the folder for the virtual environment.

```bash
mkdir venv
```

5. Create the Python virtual environment.

```bash
python3 -m venv venv
```

6. Source the Python virtual environment.

```bash
source venv/bin/activate
```

**Note**: If you are using the `fish` shell use `activate.fish` instead.

7. Install `waypaper` to the virtual environment.

```bash
pip install -e .
```

**Note**: If the compilation of dependencies fail, try downloading `gobject-introspection` and `cairo` from your distributions package manager.

8. Run the `waypaper` executable

```bash
waypaper
```

**Note**: If you are using a debugger while developing, it will use the `waypaper` from the virtual environment and you can make changes to the source code and they will be reflected when you call `waypaper` from the virtual environment.

9. Once you are ready to commit, please enter a message that describes your additions and (if applicable) cite the Github issue you are addressing with the #NUMBER syntax.
10. Create a pull request with your changes `waypaper` main. Please describe what you addressed or added and (if applicable) cite the Github issue. If necessary, please describe technical details of your implementation.

### Support

I am not a professional developer and work on this project in my free time. If you'd like to support the development, consider donations via:

* Card or PayPal [https://buymeacoffee.com/angryprofessor](https://buymeacoffee.com/angryprofessor)
* BTC `bc1qpkzmutdqfxkce34skt09vll97s5smpa0r2tyzj`
* ETH `0x6f1Ce9cA181458Fc153a5f7cBF88044736C3b00C`
* BNB `0x40f22c372758E35C905458cAF8BB17f51ac133d1`
* LTC `ltc1qtu33qyv2xlzxda5mmrmk943zpksq8q75tuh85p`&#x20;
* XMR `4AHRhpNYUZcPVN78rbUWAzBuvMKQdpwStS5L3kjunnBMWWW2pjYBko1RUF6nQVpgQPdfAkM3jrEWrWKDHz1h4Ucd4gFCZ9j`
