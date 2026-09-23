# Two accounting approaches 
- For simplified modeling, carbon that is sourced from the atmosphere which is re-emitted in the short term is assumed to have net zero emissions. That is, biogenic emissions have a characterization factor (CF) of 0, and input resource flows of biogenic carbon have a CF of 0. Long-term sequestration is modeled using emission / ground flowables with a CF of -1. This is referred to as the 0/0 approach in this document. 
- Carbon is removed from the atmosphere during photosynthesis (with a CF of -1) and re-emitted during combustion or decomposition (with a CF of +1). This is referred to as the -1/+1 approach in this document. 

By default, all LCIA methods will be made available using the 0/0 approach for the FLCAC. Versions using the -1/+1 approach will be made available in the future. Data providers are encouraged to model their flows to facilitate the use of the -1/+1 approach, and to indicate when that is not feasible. In doing so, the 0/0 approach will also be applicable.  
# Flow characterization
Carbon dioxide and carbon dioxide, biogenic resource flows must always be paired with their corresponding emission flow to arrive at a correct, net characterization. Carbon dioxide resource flows cannot be paired with carbon dioxide, biogenic emission flows (for example).

Characterization factors for carbon dioxide are identical for both accounting methods.

Biotic resource flows such as carbon / resource / biotic are not characterized and cannot be used directly for GWP accounting.

Carbon dioxide and carbon dioxide, biogenic / emission / water are available as flows, but are **not characterized in any GHG method and are generally not recommended for use** under the assumption that any CO{sub}`2` dissolved in water is likely to reach equilibrium and enter the atmosphere.

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
      <td><b>GWP 0/0: +1<br>GWP -1/+1: 0</b></td>
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
      <td><b>Use:</b> Track direct and indirect land use change. </td>
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
</table>
:::

# Examples of modeling approach
- **Combustion of bio-energy or bio-materials.** Carbon dioxide is removed from the atmosphere via photosynthesis during crop growth, assigned to carbon dioxide, biogenic / resource / air. When it is combusted, it is assigned as carbon dioxide, biogenic / emission / air. These are either both assigned a CF of 0 or a +1 / -1 depending on the approach used. 
- **Carbon capture and sequestration of a fossil-based fuel.** The portion of sequestered carbon dioxide should be assigned to carbon dioxide / emission / ground / subterranean (net 0 CF for that portion). 
- **Carbon capture and synthetic e-fuel production.** During the carbon capture stage, carbon dioxide emissions to air are reduced as they are instead captured as an intermediate flow. In subsequent processing stages that carbon dioxide remains as an intermediate flow until the e-fuel is combusted as carbon dioxide / emission / air. Specific modeling decisions regarding allocation of any carbon dioxide emissions to specific unit processes may require adjustments to this approach by the practitioner. 
- **Cement**
  - The calcination process that occurs during pyroprocessing in the cement kiln decomposes the calcium carbonate (limestone, CaCO3) into calcium oxide (CaCO) and carbon dioxide (CO2). Additionally, the pyroprocessing step requires fuels that typically release about the same amount of CO2 as the calcination process. 
  - Carbonation is the passive uptake of atmospheric CO2 reacting with calcium hydroxide (Ca(OH)2 a byproduct of hydration resulting from imperfect reaction) within the cement paste (typically within a concrete structure). The process of carbonation can last many years and the calcium hydroxide is a small amount of the Portland cement, and not the calcium hydroxide will capture CO2 from the air due to surface area and airflow restrictions within the concrete, thus the captured CO2 is a small fraction of what was released in order to fuel the kiln process and the calcination that occurred during production (maybe 10-15% of the CO2). 
- **Marine sequestration**
- **Bio-energy carbon capture and sequestration (BECCS).** The portion of the sequestered carbon dioxide should be assigned to carbon dioxide, biogenic / emission/ ground/ subterranean. The resource flow has a CF of 0 and the emission / ground flow has a CF of -1. Alternatively, in the -1 / + 1 approach, the portion that is stored has a CF of 0, the portion that is emitted to air has a CF of 1, while an offsetting carbon dioxide, biogenic / resource / air flow has a CF of -1. 
- **Direct air capture.** Carbon that is removed from the atmosphere can be tracked as carbon dioxide / resource / air (CF of -1). When it is sequestered use carbon dioxide / emission  / ground / subterranean (CF of 0)for a CF of …. 
- **Long-term soil carbon amendments** can be assigned via carbon dioxide, biogenic / emission / ground / terrestrial or human-dominated. 
- **Emissions from land use change.** Changes in land use practices can result in pulses of carbon emissions from above- or below-ground biomass. While a pure modeling approach would suggest tracking this carbon dioxide as a flow of carbon dioxide, biogenic / resource / ground and an offsetting flow of carbon dioxide, biogenic / resource / air, this approach risks muddling this source of emissions with out bio-based combustion emissions which also use carbon dioxide, biogenic / resource / air. As such, a specific flowable “carbon dioxide, land use change / emission / air” is recommended for tracking these emissions separately (the net GHG characterization is the same as the above pure modeling approach). 

:::{note}
- Where possible, account for the carbon removed from the soil for biomass growth using carbon dioxide, biogenic / resource / ground. 
- All emission / ground contexts ASSUMES “permanence”. Carbon dioxide this is not permanently sequestered should be modeled as emission / air. 
- Carbon dioxide {biogenic} / emission / water are available as flows, but are not characterized in any GHG method and are generally not recommended for use under the assumption that any CO2 dissolved in water is likely to reach equilibrium and enter the atmosphere. 
- Note about “carbon dioxide, fossil” not always being accurate in all cases? 
:::
 
