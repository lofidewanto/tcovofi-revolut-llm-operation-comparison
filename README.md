# TCO VOFI: Revolut's LLM Operation Comparison

**🔗 Live report: https://lofidewanto.github.io/tcovofi-revolut-llm-operation-comparison/**

> *Is a local LLM really 10× cheaper?* A TCO VOFI review of Revolut's move from metered frontier LLM APIs to self-hosted open-weight models (GLM).

## What this repo is about

Revolut reported that moving about 2,000 engineers from metered frontier APIs (Claude/Codex) to a self-hosted GLM model on 56 Nvidia B200 GPUs cut its AI coding bill by about 90%. That claim compares one price per token with another. It leaves out the time value of money, capital lock-up, financing, taxes, salvage value and opportunity costs.

This repo rebuilds the decision with the **TCO VOFI** method (Total Cost of Ownership based on a *Visualization of Financial Implications*, in German *Vollständiger Finanzplan*). The method comes from Bensberg & Dewanto's paper on TCO VOFI for eLearning platforms, which is included here. The report compares four alternatives over three years:

| | Alternative | Analogy |
|---|---|---|
| **A** | Metered frontier API (status quo) | Taxi |
| **B** | Managed open-weight API (same GLM, hosted by a provider) | Cheaper taxi company |
| **C** | Self-hosted GLM on rented GPUs | Leased car |
| **D** | Self-hosted GLM on owned GPUs (~$4M upfront; what Revolut appears to have done) | Buying the car |

The report is interactive:

- **Assumption lab:** sliders for token volume, prices, GPU costs, staffing, interest and tax rates. Every table and chart updates live.
- **VOFI tables:** a year-by-year financial plan for each alternative.
- **TCO analysis:** final TCO VOFI per alternative (lower is better), with an optional extended view that includes hidden opportunity costs.
- **Validation:** the same JavaScript engine reproduces all four published values from the eLearning example in the paper.
- **Bilingual:** English and German.

## Language (EN / DE)

The language can be set from outside via the URL:

| Link | Result |
|---|---|
| [`?lang=de`](https://lofidewanto.github.io/tcovofi-revolut-llm-operation-comparison/?lang=de) | German |
| [`?lang=en`](https://lofidewanto.github.io/tcovofi-revolut-llm-operation-comparison/?lang=en) | English |
| [`?lang=de#step2`](https://lofidewanto.github.io/tcovofi-revolut-llm-operation-comparison/?lang=de#step2) | German, jumps to a section |
| `#de` / `#en` | Short form (without section anchor) |

Without a parameter, the page uses the last choice made with the EN/DE button, then the browser language. A URL parameter does not overwrite the saved choice.

## Files

| File | Description |
|---|---|
| [`revolut-llm-tco-vofi.html`](revolut-llm-tco-vofi.html) | The self-contained interactive report (published via GitHub Pages) |
| [`index.html`](index.html) | Redirects the Pages root URL to the report |
| [`tco-vofi-elearning-platforms.pdf`](tco-vofi-elearning-platforms.pdf) | The TCO VOFI method paper (Bensberg & Dewanto) |

## Running locally

No build step is needed. Open `revolut-llm-tco-vofi.html` in a browser.

## Disclaimer

Figures not reported by Revolut are estimates from public price lists (GPU rental, DGX pricing, API list prices) and London salary levels. Adjust them in the Assumption lab to fit your own case.

## License

See [LICENSE](LICENSE).
