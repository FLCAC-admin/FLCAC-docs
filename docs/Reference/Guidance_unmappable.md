# Guidance on Avoiding Ambiguous Elementary Flows

As the USLCI Database converted to the [Federal Elementary Flow List (FEDEFL)](https://cfpub.epa.gov/si/si_public_record_report.cfm?dirEntryId=347251&Lab=NRMRL) in 2020, several "un-mappble" flows were identified as non-compliant and are being phased out.
The FEDEFL approach discourages using groups of flowables that lead to uncharacterizable impact assessment results.
Accordingly, NREL recommends avoiding the following as elementary flow names in datasets submitted to the USLCI Database, where possible.
More information on choosing FEDEFL-preferred elementary flows is available in the USLCI Data Submission Handbook Appendix [FEDEFL Nomenclature Highlights](https://github.com/uslci-admin/uslci-content/blob/dev/docs/submission_handbook/05-FEDEFL%20Guidelines%20-%20Appendix%20Fork.md).

<br>
<br>


|🚩 _**&quot;Aldehydes, unspecified&quot;**_| 🚩 **From incomplete combustion organic compounds (fuels &amp; vehicle exhaust) but also various specific industries; often formaldehyde or acrolein but can be specific aldehydes with dissimilar impact factors so formaldehyde or acrolein may or may not be appropriate proxies; formaldehyde is responsible for ~ 90 % of US air emissions contributing to carcinogens totals in the US and Canada; if ambiguous aldehyde emissions to air in USLCI were converted to formaldehyde (as a proxy), this adds an average of 8.3e-6 kg formaldehyde/kg materials to inventories; using TRACIv2.1 2008 normalization factors, this average per kilogram emission level amounts to ~ 40% and 200% of human health non-cancer and cancer effects, respectively, from non-metals per US person per year. Leaving this ambiguous could significantly underestimate toxicity and smog impact categories. Speciate where possible.**</div> |
| --- | --- |
| _**&quot;Alkylated benzenes&quot;**_ | Examples are toluene, xylene, and ethylbenzene. Alkylated benzenes can occur naturally in crude oil and natural gas or from volcanoes and forest fires but also from many industries such as petroleum refining, paints, adhesives, inks, cosmetics, and pharmaceuticals. This flow is used by many data providers but affects no methods. Many speciated benzene emissions affect toxicity and smog impacts; thus, leaving this ambiguous could underestimate toxicity and smog results. Speciate where possible |
| _**&quot;Clean gas&quot;**_ | This flow may be air/waste heated air used for mass balance but affects no methods |
| _**&quot;Energy, from heat&quot; or &quot;Heat, waste&quot;**_ | When reported in mass units is impossible to convert to more meaningful energy units |
| _**&quot;Detergents&quot;**_ | This flow affects no methods; only the EDIP 2003 Method captures _**&quot;Detergent, anionic&quot;**_ for Ecotoxicity with a water acute toxicity factor 1,300 m3/kg |
| _**&quot;Different pollutants&quot;**_ | This flow may be used for mass balance but affects no methods |
| _**&quot;Exhaust&quot;**_ | This flow may be air/waste heated air used for mass balance but affects no methods |
| _**&quot;HAPs (Hazardous Air Pollutants)&quot;**_ | This flow may be used for mass balance but affects no methods even though carcinogenity is implied |
| _**&quot;Salts and acids, unspecified&quot;**_ | This flow may be used for mass balance but affects no methods |
| _**&quot;Oil and grease, unspecified&quot;**_&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;| Can include in inventory totals but affects no impact methods |
| _**&quot;Process effluent or solvents&quot;**_ | This flow may be used for mass balance but affects no methods |
| _**&quot;Raw material, unspecified&quot;**_ | This flow may be used for mass balance but affects no methods |
