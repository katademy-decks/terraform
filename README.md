#### Questions to refresh your memory of Terraform (WIP)

<hr>

<details>
<summary>Do resources usually have defined relationships with each other?</summary>
Not unless the <b>depends_on</b> meta-argument is set.
<br></details>

<details>
<summary>The _____ meta-argument selects non-default configuration inside a provider block.</summary>
<b>alias</b>
<br></details>

<details>
<summary><div style="font-family: Arial;"><span style="font-family: &quot;Liberation Sans&quot;;">Resources may require a program to be run before Terraform finishes operations on them. The _____ and _____ meta-arguments take&nbsp;</span><span style="font-family: &quot;Liberation Sans&quot;;">extra non-declarative actions after resource creation</span><span style="font-family: &quot;Liberation Sans&quot;;">&nbsp;</span></summary>
<b>provisioner</b>&nbsp;and&nbsp;<b>connection</b>
<br></details>

<details>
<summary>A resource must be associated with one _____ configuration, defined in the same module, or in the parent module (either through _____ or via the _____ argument)</summary>
provider
inheritance
providers
<br></details>

<details>
<summary>Can remote state use GCS?</summary>
Yes
<br></details>

<details>
<summary>Can remote state use Amazon S3?</summary>
Yes
<br></details>

<details>
<summary>The boolean _____ lifecycle meta-argument changes resource update behavior so that the new replacement object is created&nbsp;<em>first,</em>&nbsp;and then the prior object is destroyed only once the replacement is created.&nbsp;
This is an opt-in behavior because many remote object types have unique name requirements or other constraints that must be accommodated for both a new and an old object to exist concurrently. Some resource types offer special options to append a random suffix onto each object name to avoid collisions, for example. Terraform CLI cannot automatically activate such features, so you must understand the constraints for each resource type before using <b>_____&nbsp;</b>with it.</summary>
<b>create_before_destroy</b>&nbsp;
<br></details>

<details>
<summary>The _____ lifecycle meta-argument makes Terraform reject any plan/command that would destroy the object associated with the resource. However, this makes some configuration changes impossible to apply.</summary>
prevent_destroy
<br></details>

<details>
<summary>Settings of a remote object might be modified outside of Terraform, which it would attempt to "fix" on the next run. The <b>_____ </b>lifecycle&nbsp;meta-argument specifies resource attributes that Terraform should ignore when planning updates to the associated remote object.</summary>
<b>ignore_changes</b>&nbsp;
<br></details>

<details>
<summary>What is special about files using the *.auto.tfvars filename structure?</summary>
They get loaded automatically
<br></details>

<details>
<summary>The command <b>terraform _____ </b>selects a workspace.</summary>
terraform workspace select
<br></details>

<details>
<summary>When uploading with the <b>file provisioner</b>, the presence of a trailing slash makes the source dir _____ with destination dir.</summary>
merge
<br></details>

<details>
<summary>A resource spec addresses a specific resource in the config using the fields <b>resource_</b>_____, <b>resource_</b>_____, and an optional <b>.resource_</b>____</summary>
type, name, index
<br></details>

<details>
<summary>When Terraform must make a change to a resource argument that cannot be updated in-place due to remote API limitations, Terraform will replace the existing object with a new one. This can be changed with the _____ lifecycle meta-argument.</summary>
create_before_destroy
<br></details>

<details>
<summary>_____ configure where to store state and where/how to perform operations.</summary>
Backends&nbsp;
<br></details>

<details>
<summary>When an often-changed value is used in many places in the configuration, you can use _____ values.</summary>
local
<br></details>

<details>
<summary>Local state workspaces can be found inside the _____/ directory.</summary>
<b>terraform.tfstate.d/</b>
<br></details>

<details>
<summary>What arguments does the <b>local-exec provisioner</b> take?</summary>
command, [interpreter], [environment], [working_dir]
<br></details>

<details>
<summary>Terraform logs are sent to <b>stderr </b>by default, but only if _____ is set.</summary>
TF_LOG&nbsp;
<br></details>

<details>
<summary>The _____ function convert a list to a set</summary>
<div style="font-family: Arial;"><b>toset</b>
<div style="font-family: Arial;">
<img src="paste-e9fca906b0aea52aad209f068dae18d012496aa8.jpg">
<br></details>

<details>
<summary>the command <b>terraform _____</b> views the specified version constraints for all providers in the configuration.</summary>
<b>terraform providers</b>
<br></details>

<details>
<summary>What is the default local state filename?</summary>
terraform.tfstate
<br></details>

<details>
<summary>Is terraform.tfvars always automatically loaded?</summary>
Yes
<br></details>

<details>
<summary>When using remote state, you access root module outputs using the<b>&nbsp;_____&nbsp;</b>data source.</summary>
terraform_remote_state
<br></details>

<details>
<summary>What arguments does the file provisioner take?</summary>
source, destination, content
<br></details>

<details>
<summary>After a resource is created, a binary must be executed on your local host. The _____ provisioner does this.</summary>
local-exec
<br></details>

<details>
<summary>Terraform log levels (TRACE, DEBUG, INFO, WARN, ERROR) are set via the _____ environment variable.</summary>
TF_LOG&nbsp;
<br></details>

<details>
<summary>Input Variables are accessible ONLY from the same module via the ____.&lt;NAME&gt; keyword.</summary>
<b>var.</b>
<br></details>

<details>
<summary>The _____ tracks real world instances of your configuration and their metadata.</summary>
state
<br></details>

<details>
<summary>Are workspaces equivalent to renaming your state file?</summary>
Yes - with added support for remote state
<br></details>

<details>
<summary>A <b>provider</b>&nbsp;block can appear in any module down the line, but should ideally be kept inside the _____ module for reusability.</summary>
root
<br></details>

<details>
<summary>The syntax of a resource is:&nbsp;<i>
</i><i>resource&nbsp;"_____"&nbsp;"_____"&nbsp;&nbsp;</i><i>{_____}</i><b>
</b></summary>
<i>&lt;type&gt;&nbsp;</i><i>&lt;local_name&gt;&nbsp;</i><i>configuration arguments</i>
<i>
</i><img src="paste-591e121ba7a98d2d60657269d68abe2c5c3a048f.jpg">
<br></details>

<details>
<summary>Are&nbsp;<b>count</b> and <b>for_each </b>meta-arguments mutually exclusive?</summary>
Yes
<br></details>

<details>
<summary>Customize a resource's CRUD behaviour using meta-arguments inside the _____ block.</summary>
<b>lifecycle</b>

<img src="paste-25ade283404adef3cae7cdd8b4ca1ab28a938c95.jpg" style="font-family: Arial;">
<br></details>

<details>
<summary>Variables can be passed to <b>terraform plan</b> or <b>terraform apply </b>via the _____ flag.</summary>
-var
<br></details>

<details>
<summary>The _____&nbsp;<b>provisioner&nbsp;</b>copies files from localhost to the resource via ssh or winrm.</summary>
file
<br></details>

<details>
<summary>Where do resource types come from?</summary>
Providers
<br></details>

<details>
<summary>How to use the same <b>provider</b> with different configurations for different resources?</summary>
<b>alias</b>
<br></details>

<details>
<summary>Variable files (.tfvars) are loaded in the CLI via the _____ flag.</summary>
<b>-var-file</b>
<br></details>

<details>
<summary>The names of Terraform-specific environment variables have the prefix _____</summary>
<b>TF_VAR_</b>
<br></details>

<details>
<summary>Terraform configurations consist of a _____ module where evaluation begins and _____ modules, created when modules call each other.</summary>
<b>root</b><b>
</b><b>child</b>
<br></details>

<details>
<summary>A resource can have an inner _____ block defined, to customize how long different CRUD operations are allowed to take before they fail.</summary>
Timeouts
<img src="paste-c0fd60b9eda21d33822f385b1279127368c1f369.jpg" style="font-family: Arial;">
<br></details>

<details>
<summary>Is .tfvars syntax just some&nbsp;&nbsp;variable name assignments?</summary>
Yes
<img src="paste-8750c20b8e8c202754910b7c64f3f5e58b441643.jpg">
<br></details>

<details>
<summary>Can remote state use HashiCorp Cloud / HashiCorp Consul?</summary>
Yes
<br></details>

<details>
<summary><div style="font-family: Arial;">The _____ meta-argument replicates a resources into indexed, identical clones.</summary>
count
<br></details>

<details>
<summary>The state locks down for every state-_____ operation.</summary>
state-writing
<br></details>

<details>
<summary>What do credential helpers do?</summary>
Program custom ways to fetch credentials
<br></details>

<details>
<summary>_____-arguments aren't specific to any one resource type.</summary>
meta-arguments
<br></details>

<details>
<summary>Using the <b>file provisioner</b> via ssh, the remote directory must already _____</summary>
exist
<br></details>

<details>
<summary>You can download the remote state with the terraform _____ command.</summary>
<b>terraform state pull</b>
<br></details>

<details>
<summary>What's the root module?</summary>
The files in the working directory
<br></details>

<details>
<summary>The _____ meta-argument is used to replicate infrastructure where some arguments need specific values.</summary>
<b>for_each</b>
<br></details>

<details>
<summary>Every&nbsp;<b>each</b>&nbsp;Object has a _____ and a ____ corresponding to its particular instance.</summary>
<b>.key
</b>
<b>.value</b>
<br></details>

<details>
<summary>_____ resources exist only within the local Terraform state and glue together other resources by&nbsp;<a href="https://www.terraform.io/docs/providers/random/r/id.html">generating random ids</a>,&nbsp;<a href="https://www.terraform.io/docs/providers/tls/r/private_key.html">generating private keys</a>,&nbsp;<a href="https://www.terraform.io/docs/providers/tls/r/self_signed_cert.html">issuing self-signed TLS certificates</a>.</summary>
local-only
<br></details>

<details>
<summary>A module's output values are defined via named _____ resources.</summary>
output<b>
</b><img src="paste-9e619bdcbf06ae0d3d5789aeaa399e23e7543964.jpg">
<br></details>

<details>
<summary>Does Terraform local state automatically back up?</summary>
Yes
<br></details>

<details>
<summary>Resource _____ settings have consequences - they modify the dependency graph and its traversal. Only literal values can be used because the processing happens too early.</summary>
<div style="font-family: &quot;Liberation Sans&quot;;">lifecycle
<br></details>

<details>
<summary>Local values are defined in the _____ block.</summary>
<b>locals</b>

<img src="paste-cbecdc61ad409bd1e95ba0b5800f44a7f2fd1685.jpg">
<br></details>

<details>
<summary>The command <b>terraform _____</b> creates a new workspace.</summary>
<b>terraform workspace new</b>
<br></details>

<details>
<summary>Terraform logs can be sent to a desired file if its path is defined in the _____ environment variable.</summary>
TF_LOG_PATH
<br></details>

<details>
<summary>What's a module?</summary>
A container of related resources
<br></details>

<details>
<summary>An output value with the _____ argument set won't be shown after&nbsp;<b>terraform apply </b>(but is still visible in the state)</summary>
sensitive
<br></details>

<details>
<summary>How to define multiple configurations for the same provider?</summary>
<b>alias</b><b>
</b><img src="paste-cfd2d73e7b9fabd2709b924abfd85509dd95b916.jpg"><b>
</b>
<br></details>

<details>
<summary>Do you work in a Workspace by default?</summary>
Yes, called <b>default</b>
<br></details>

<details>
<summary>How to have multiple states?</summary>
Use Workspaces
<br></details>

<details>
<summary>Can local values be expressions?</summary>
Yes
<br></details>

<details>
<summary>The current workspace be inferred and used inside Terraform code logic via the _____ variable.</summary>
terraform.workspace
<br></details>

<details>
<summary>To prevent conflicts from multiple users applying different plans on the same resources, you should _____.</summary>
lock the state
<br></details>

<details>
<summary>What uniquely identifies a resource?</summary>
Its type + name
<br></details>

<details>
<summary>Can empty <b>provider </b>blocks be omitted?</summary>
Yes
<br></details>

<details>
<summary>You should constrain a <b>provider'</b>s allowed versions in production via the _____ block.</summary>
<b>required_providers</b><b>
</b><img src="paste-90d5c2a3f7c8c735f99d3e434f012bc2480b976e.jpg">
<br></details>

<details>
<summary>Which file should you store your CLI variables in?</summary>
.tfvars
<br></details>

<details>
<summary>Referencing a local value is done via the ____.&lt;VALUE_NAME&gt; keyword.</summary>
local
<br></details>

