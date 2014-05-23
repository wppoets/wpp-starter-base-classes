foundation-namespace-base
==========

By following the below instructions you will be able to download the newest code without affecting you selected namespace

Add the submodule to your project

Add filter to the .gitattributes 
	For example we will use namespace, we run "echo '*.php filter=namespace' >> .gitattributes" from inside the submodule directory

Add the filters to the git global config
	For example are desired namespace will be WPP\New_Project_Name\Base
		git config filter.namespace.smudge "sed -e 's/WPP\\\\Foundation_Namespace_Base/WPP\\\\New_Project_Name\\\\Base/'"
		git config filter.namespace.clean "sed -e 's/WPP\\\\New_Project_Name\\\\Base/WPP\\\\Foundation_Namespace_Base/'"

=Versions

===1.0.0
* Initial Release

===0.9.0
* Initial prerelease
