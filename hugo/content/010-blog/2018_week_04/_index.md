---
title: Build advanced applications with FaaS
type: Blog
---

<table>
<tr>
<td>
{{% blog_img "logo" "faas.png" %}}
</td>
<td>
{{% md %}}
**[Functions as a Service]({{ relref . "faas/_index.md" }}) offers the function based serverless approach on K8s.** 
If you want to learn  more about the functions/serverless approach the [CNCF white paper](https://goo.gl/udD8Fx) is a 
very good information source.  Functions as a Service is based on the open-source project 
[kubeless](https://github.com/kubeless/kubeless). It can be installed via Helm charts. Afterwards you will be able 
to write, deploy and test functions.
{{% /md %}}

</td>
</tr>
</table>



Functions as a Service currently supports:
 - NodeJS as programming language(s). 

Supported trigger types for functions are currently:
 - HTTP trigger
 
More trigger types will be available soon:
 - RabbitMQ trigger
 - timer trigger

Please note, kubeless itself already supports additional programming languages and triggers.