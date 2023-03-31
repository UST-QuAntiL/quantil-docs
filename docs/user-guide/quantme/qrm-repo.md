## QRM Repositories

In the following the structure of a QRM repository as well as its configuration and usage is shown.

### Configuration

The QRM repository must be a publicly accessible Github repository. 
It can be configured using the [configuration file](https://github.com/UST-QuAntiL/QuantME-TransformationFramework/blob/develop/app/lib/quantme/qrm-manager/RepositoryConfig.js).
Therefore, `githubUsername` should be used to configure the username or organisation name under which the Github repository is located.
Furthermore, `githubRepositoryName` has to specify the name of the Github repository.
Finally, `githubRepositoryPath` can be used to specify a subfolder in the Github repository containing the QRMs.
It not set, the root folder is used to retrieve the QRMs.

Another possibility to configure the QRM repository is using environment variables (QRM_USERNAME, QRM_REPONAME, QRM_REPOPATH) when starting the framework or by updating the repository via the REST API.

### Structure

The QRM repository can contain an arbitrary number of QRMs, each of which has to be located in a separate folder in the Github repository.
In the following, an example QRM repository containing three QRMs is shown:

![Repository Overview](/user-guide/quantme/images/repository-overview.png){: style="width:700px" .center}

Each of the folders has to contain at least the two files `detector.bpmn` and `replacement.bpmn`, which represent the QRM.
If one of the two files is missing or contains invalid content, the QRM is ignored during transformation.
Additionally, other files can be added to the folders, e.g., a readme file describing the QRM:

![Repository Content](/user-guide/quantme/images/repository-folder-content.png){: style="width:900px" .center}

### Updating the QRM repository

When starting the QuantME Modeling and Transformation Framework, the QRM repository is loaded once.
However, if the repository is changed during runtime of the framework, the QRMs have to be reloaded.
For this, use the `Plugins` menu entry, go to `QuantME`, and click on the `Update from QRM repository` button:

![Reload Repository](/user-guide/quantme/images/reload-repository.png){: style="width:900px" .center}

If the defined Github username and repository name are invalid and result in an error when loading the QRMs, a notification is displayed in the modeler and the configuration should be fixed.