# Build YapperSMP without installing Java or Maven locally

This project includes a GitHub Actions workflow that builds the plugin using Java 21 and Maven.

1. Create a repository on GitHub (you can make it private).
2. Upload the contents of this folder to the repository, including `.github/workflows/build.yml` and `pom.xml`.
3. Open the repository's **Actions** tab and select **Build YapperSMP**.
4. If needed, click **Run workflow**. You can also push/commit a change to trigger it.
5. Open the completed workflow run. Under **Artifacts**, download **YapperSMP-plugin**.
6. Extract the downloaded artifact ZIP. It contains `YapperSMP.jar`.
7. Stop your Falix server, upload `YapperSMP.jar` to the server's `plugins` folder, then start the server.

If the workflow fails, open the run and copy the first compiler/build error so it can be fixed. The plugin source has not been compiled or runtime-tested in this environment.
