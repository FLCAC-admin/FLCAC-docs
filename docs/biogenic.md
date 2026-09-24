# Two accounting approaches 
- For simplified modeling, carbon that is sourced from the atmosphere which is re-emitted in the <span title="There is not full agreement between different standards and LCIA methods regarding what represents short-term, though < 100-years is a common benchmark.">short term</span> is assumed to have net zero emissions. That is, biogenic emissions have a characterization factor (CF) of 0, and input resource flows of biogenic carbon have a CF of 0. Long-term sequestration is modeled using `emission / ground` flowables with a CF of -1. This is referred to as the 0/0 approach in this document. 
- Carbon is removed from the atmosphere during photosynthesis (with a CF of -1) and re-emitted during combustion or decomposition (with a CF of +1). This is referred to as the -1/+1 approach in this document. 

By default, all LCIA methods will be made available using the 0/0 approach for the FLCAC. Versions using the -1/+1 approach will be made available in the future. Data providers are encouraged to model their flows to facilitate the use of the -1/+1 approach, and to indicate when that is not feasible. In doing so, the 0/0 approach will also be applicable.  
# Flow characterization
Carbon dioxide and carbon dioxide, biogenic resource flows must always be paired with their corresponding emission flow to arrive at a correct, net characterization. Carbon dioxide resource flows cannot be paired with carbon dioxide, biogenic emission flows (for example).

Characterization factors for carbon dioxide are identical for both accounting methods.

Biotic resource flows such as `carbon / resource / biotic` are not characterized and cannot be used directly for GWP accounting.

Carbon dioxide and `carbon dioxide, biogenic / emission / water` flows are available, but are **not characterized in any GHG method and are generally not recommended for use** under the assumption that any CO{sub}`2` dissolved in water is likely to reach equilibrium and enter the atmosphere.

:::{important}
All emission / ground contexts ASSUME “permanence”. Carbon dioxide that is not permanently sequestered should be modeled as emission / air. The time period associated with permanence is determine by the time period of your GWP indicator. For GWP-100, permanence is carbon stored for >100 years.
:::

:::{table} Carbon dioxide flow characterization 
:label: tbl:areas-html

<table>
    <tr>
      <th rowspan="2" style="vertical-align: middle;">Flow direction</th>
      <th rowspan="2" style="vertical-align: middle;">Compartment</th>
      <th colspan="3" style="text-align: center;">Flow</th>
    </tr>
    <tr>
      <th>Carbon dioxide<br><em>synonym: "carbon dioxide, fossil"</em></th>
      <th>Carbon dioxide, biogenic<br><em>synonym: "carbon dioxide, non-fossil"</em></th>
      <th>Carbon dioxide, land use change<br><em>synonym: "carbon dioxide, from soil or biomass stock"</em></th>
    </tr>
    <tr>
      <td rowspan="6" style="vertical-align: middle;"><strong>Input</strong></td>
      <td rowspan="3" style="vertical-align: middle;">Resource/ground</td>
      <td><b>GWP: 0</b></td>
      <td><b>GWP 0/0: +1 <a href="#note-1"><sup>[1]</sup></a><br>GWP -1/+1: 0</b></td>
      <td rowspan="3">n.a.</td>
    </tr>
    <tr>
      <td><b>Use:</b> Track carbon content in fossil fuels, peat or underground CO<sub>2</sub> reservoirs.</td>
      <td><b>Use:</b> Track biogenic C extracted from soil. Uncommon.</td>
    </tr>
    <tr>
      <td><b>Subcompartment(s):</b><br> only use resource/ground/subterranean</td>
    </tr>
    <tr>
      <td rowspan="3" style="vertical-align: middle;">Resource/air</td>
      <td><b>GWP: -1</b></td>
      <td><b>GWP 0/0: 0<br>GWP -1/+1: -1</b></td>
      <td rowspan="3">n.a.</td>
    </tr>
    <tr>
      <td><b>Use:</b> Anthropogenic sequestration (e.g., direct air capture)</td>
      <td><b>Use:</b> Track carbon incorporated in living things (e.g., photosynthesis).</td>
    </tr>
    <tr>
      <td><b>Subcompartment(s):</b><br> resource/air/troposphere (preferred)</td>
      <td><b>Subcompartment(s):</b><br> resource/air/troposphere (preferred)</td>
    </tr>
    <tr>
      <td rowspan="8" style="vertical-align: middle;"><strong>Output</strong></td>
      <td rowspan="3" style="vertical-align: middle;">Emission/air</td>
      <td><b>GWP: +1</b></td>
      <td><b>GWP 0/0: 0<br>GWP -1/+1: +1</b></td>
      <td><b>GWP: +1</b></td>
    </tr>
    <tr>
      <td rowspan="2"><b>Use:</b> Fossil combustion emissions</td>
      <td rowspan="2"><b>Use:</b> Track biogenic emissions (e.g. combustion or decomposition).</td>
    </tr>
    <tr>
      <td><b>Use:</b> Track emissions from direct and indirect land use change. </td>
    </tr>
    <tr>
      <td rowspan="2" style="vertical-align: middle;">Emission/water</td>
      <td><b>GWP: not characterized</b></td>
      <td><b>GWP: not characterized</b></td>
      <td rowspan="2">n.a.</td>
    </tr>
    <tr>
      <td><b>Use:</b> Track the quantity of CO<sub>2</sub> emitted to air.</td>
      <td><b>Use:</b> Track the quantity of CO<sub>2</sub> emitted to air.</td>
    </tr>
    <tr>
      <td rowspan="3" style="vertical-align: middle;">Emission/ground</td>
      <td><b>GWP: 0</b></td>
      <td><b>GWP 0/0: -1<br>GWP -1/+1: 0</b></td>
      <td rowspan="3">n.a.</td>
    </tr>
    <tr>
      <td><b>Use:</b> Underground sequestration. Assume permanence, else report emissions to air.</td>
      <td><b>Use:</b> Model underground sequestration or storage in long-term soil carbon. Assume permanence, else report emissions to air.</td>
    </tr>
    <tr>
      <td><b>Subcompartment(s):</b><br> emission / ground / subterranean</td>
      <td><b>Subcompartment(s):</b><br>Underground storage - emission / ground / subterranean<br>Soil storage - emission / ground / {terrestrial or human-dominated}</td>
    </tr>
    <tfoot>
    <tr>
      <td colspan="5" style="padding-top: 10px; font-size: 0.9em;">
        <p id="note-1"><sup>[1]</sup> Why is `carbon dioxide, biogenic / resource / ground` a +1 (in 0/0 method)? In this simplified modeling approach (biogenic emissions = 0), carbon removed from the ground must be offset by the credit earned when it is returned to the ground via `carbon dioxide, biogenic / emission / ground`. Inventory will need adjusted if carbon is stored in a product for a given study scope. </p>
      </td>
    </tr>
  </tfoot>
</table>
:::

# Examples of modeling approach
- **Combustion of bio-energy or bio-materials.** Carbon dioxide is removed from the atmosphere via photosynthesis during crop growth, assigned to `carbon dioxide, biogenic / resource / air`. When it is combusted, it is assigned as `carbon dioxide, biogenic / emission / air`. These are either both assigned a CF of 0 or a -1 / +1, respectively, depending on the approach used. 
- **Carbon capture and sequestration of a fossil-based fuel.** The portion of sequestered carbon dioxide should be assigned to `carbon dioxide / emission / ground / subterranean` (CF of 0). 
- **Carbon capture and synthetic e-fuel production.** During the carbon capture stage, carbon dioxide emissions to air are reduced as they are instead captured as an intermediate flow. In subsequent processing stages that carbon dioxide remains as an intermediate flow until the e-fuel is combusted as `carbon dioxide / emission / air`. Specific modeling decisions regarding allocation of any carbon dioxide emissions to specific unit processes may require adjustments to this approach by the practitioner. 
- **Cement production.** The calcination process that occurs during pyroprocessing in the cement kiln decomposes the calcium carbonate (limestone, CaCO{sub}`3`) into calcium oxide (CaCO) and carbon dioxide (CO{sub}`2`). Additionally, the pyroprocessing step requires fuels that typically release about the same amount of CO{sub}`2` as the calcination process. In both cases, `carbon dioxide / resource / ground` flows can be used to track carbon content in calcium carbonates and kiln fuels. `Carbon dioxide / emission / air` flows should be used to track all emissions. 
- **Cement carbonation** is the passive uptake of atmospheric CO{sub}`2` reacting with calcium hydroxide (Ca(OH){sub}`2` a byproduct of hydration resulting from imperfect reaction) within the cement paste (typically within a concrete structure). The `carbon dioxide / resource / air / troposphere` flow can be used to model sequestration of atmospheric carbon in cement. The process of carbonation can last many years and calcium hydroxide is a minor component of Portland cement. Additionally, not all calcium hydroxide in cement will capture CO{sub}`2` from the air due to surface area and airflow restrictions within the concrete, thus the captured CO{sub}`2` is a moderate fraction of CO{sub}`2` released in production. 
- **Marine sequestration.** Numerous strategies are being explored for sequestration of carbon within the ocean such as deep-ocean injection, alkalinity enhancement or ocean fertilization. For simplicity and due to the limited availability of oceanic subcompartments within the FEDEFL, we recommend using `emission / ground` flows to model marine sequestration. Include exchange descriptions to describe the mode of carbon capture that is reflected. 
- **Bio-energy carbon capture and sequestration (BECCS).** The portion of carbon dioxide sequestered should be assigned to `carbon dioxide, biogenic / emission/ ground/ subterranean`. In the 0/0 accounting method, the resource flow has a CF of 0 and the emission / ground flow has a CF of -1. Alternatively, in the -1/+1 approach, the portion that is stored has a CF of 0, the portion that is emitted to air has a CF of +1, while an offsetting `carbon dioxide, biogenic / resource / air` flow has a CF of -1. 
- **Direct air capture.** Carbon that is removed from the atmosphere can be tracked as `carbon dioxide / resource / air` (CF of -1). When it is sequestered use `carbon dioxide / emission  / ground / subterranean` (CF of 0). 
- **Long-term soil carbon amendments** can be modeled using the `carbon dioxide, biogenic / emission / ground / terrestrial` or `human-dominated` flows. In the 0/0 accounting method, A CF of 0 will be assigned to `carbon dioxide, biogenic / resource / air` flows used to model incorporation in plants via photosynthesis. The `carbon dioxide, biogenic / emission / ground` flows can be used to model the fraction of carbon retained in soil for greater than 100-years (in the case of GWP-100), and will be assigned a CF of -1. The portion of carbon in soil amendments that decomposes in less than 100 years should be modeled as `carbon dioxide, biogenic / resource / air` which is assigned a CF of 0, resulting in net zero impact for the re-emitted fraction of fixed carbon. Using the -1/+1 approach, sequestration is logged when using the `carbon dioxide, biogenic / resource / air` flow (CF of -1). The portion of re-emitted carbon (`emission / air`) is a assigned a CF of +1, resulting in net zero impact. Long term storage is modeled using the `carbon dioxide, biogenic / emission / ground` flows and is assigned a CF of 0.  
- **Emissions from land use change.** Changes in land use practices can result in pulses of carbon emissions from above- or below-ground biomass. The `carbon dioxide, land use change / emission / air` flow is available for separate tracking of these emissions as prescribed in ISO 21930 and to avoid confusion with other emissions of biogenic carbon to air.  

 
