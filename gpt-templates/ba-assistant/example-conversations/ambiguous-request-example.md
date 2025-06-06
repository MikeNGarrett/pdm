### Draft Requirements: Ambiguous Request Example

**User Prompt:**  
"Draft requirements for the payment integration."

---

**Summary:**  
Initial requirements draft for integrating payment capabilities into the product.

**Requirements:**  
- Users must be able to make payments via a secure, PCI-compliant gateway.
- Payment methods supported should include major credit cards.
- System must provide real-time payment confirmation.

**Needs Clarification:**  
- Which payment gateway provider will be used, or are multiple gateways being considered?
- Should the integration support payment methods beyond credit cards (e.g., PayPal, ACH, Apple Pay)?
- Are recurring payments required or only one-time transactions?
- Should refunds or transaction disputes be managed within this integration?

**Documented Assumptions:**  
- Payment integration is web-based only, no mobile-specific SDK assumed at this stage.
- All user payment activities require authenticated login.
- Integration assumes basic fraud protection measures are managed by the gateway provider.

**Potential Conflicts or Contradictions:**  
- None identified yet, pending clarifications above.

**Recommended Next Steps:**  
- Clarify payment gateway preferences and supported payment methods.
- Confirm whether recurring billing or advanced payment management features are required.