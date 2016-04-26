---
published: true
permalink: /dictionary/
layout: hero
filename: data-dictionary.md
title: DATA Act Data Dictionary
---


<h1>The DATA Act Schema Data Dictionary</h1>
<h2>Background</h2>
<p>The purpose of this data dictionary is to provide assistance in understanding the data elements within the DATA Act Schema.</p>

<p>The DATA Act directs the Office of Management and Budget (OMB) and the U.S. Treasury Department (Treasury) to establish government-wide data standards for federal funds and entities receiving such funds. The DATA Act Schema will help to ensure that information is consistent and comparable and ultimately make data more accessible, reusable, and provide the necessary linkages between financial events. By making federal spending data accessible, searchable, reusable and more reliable, the public can understand how government spending impacts their communities. The DATA Act Schema will also reduce the need for massive system changes across federal agencies to collect information and allow agencies to focus on managing data.</p>

<p>The DATA Act data dictionary will be revised periodically and is expected to evolve over time to reflect the content within the DATA Act Schema. As the schema continues to evolve, the latest revision intentionally separates the purpose of defining the elements that comprise the domain of information addressed by the DATA Act, from providing detailed instructions for submission of data corresponding to those element definitions. As a result, the Schema Data Dictionary should become a common reference for the standard description of the overall Information Model covering all available DATA Act data. As such it should provide the same benefits both to data providers and data consumers, regardless of role or familiarity with existing government systems and terminology.</p>

<p>To support this intent, the schema, now referred to as the <strong>DATA Act Information Model Schema (DAIMS)</strong>, has been updated with some new elements and element attributes. Likewise, some prior attributes intended for the purpose of submission instruction, have been removed. (Ultimately, submission instructions will be documented separately as Report Submission Specifications (RSS), specific to the needs of agencies required to provide data.)</p>
<p>The principal changes reflected in the Data Dictionary include:
    <ul>
        <li>The addition of a DAIMS Semantic Standard Label, to provide a description of each element that where appropriate more clearly expresses detailed meaning, purpose and/or relationship context of the data, and when possible doesn’t require system specific domain knowledge. (The original DATA Act field names have been retained on elements where they originally existed.)</li>
        <li>The addition of new elements, which better encompass the breadth or detail required for DATA Act reporting. For example, these include finer breakdowns of reported values for Obligations and Outlays, sometimes to the USSGL account level, or reflect attributes already present in government systems that provide valuable dimension to the data, such as direct versus reimbursable appropriations.</li>
        <li>The removal of Cardinality and Field Width, which focus primarily on constraints that may or may not exist in the ultimate requirements for specific reporting file or data stream formats, of which the DATA Act will eventually support many.</li>
    </ul>
</p>
<p>To provide feedback on the data dictionary, please see our <a href="https://github.com/fedspendingtransparency/fedspendingtransparency.github.io/issues/126" title="provide data dictionary feedback">related issue</a>.</p>

<a href="#" id="back-to-top" title="Back to top"><span class="glyphicon glyphicon-arrow-up"></span></a>

<h2>DATA Act Schema Data Dictionary (v0.7)</h2>

<table id="dictTable" class="tablesorter table-bordered table-striped mb-40" style="word-wrap:break-word; table-layout:fixed;">
    <thead>
        <tr>
            <th style="width:6%">file</th>
            <th> Data Element Label</th>
            <th style="width:40%;">Definition</th>
            <th>Use</th>
            <th style="width:8%">Max Field Length</th>
            <th>Data Category</th>
        </tr>
    </thead>
    {% for element in site.data.elements %}
    <tr>
        <td>{{ element.file }}</td>
        <td>
            {{ element.DataElementLabel }}
        </td>
        <!--<td><a href="#C{{ forloop.index | plus:1 }}">{{ element.DAIMSSemanticLabel }}</a></td>-->
        <td>{{ element.Definition }}</td>
        <td>{{ element.RequiredOptional }}</td>
        <td>{{ element.MaxFieldLength }}</td>
        <td>{{ element.Grouping }}</td>
    </tr>{% endfor %}
</table>



