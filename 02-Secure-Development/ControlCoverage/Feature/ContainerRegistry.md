<html>
<head>

</head>

<body>
    <H2>ContainerRegistry</H2>
    <table>
        <tr>
            <th>Description & Rationale</th>
            <th>ControlSeverity</th>
            <th>Automated</th>
            <th>Fix Script</th>
        </tr>
        <tr>
            <td><b>Admin user in Container Registry must be disabled</b><br />The admin user is designed for a single
                user to access the registry. All users authenticating with the admin account appear as a single user to
                the registry. Admin users are having high privileged role increases the attack surface for the server
                without being tracked. Using AAD based identity ensures that there is a built-in high level of
                assurance in the user identity established for subsequent access control.</td>
            <td>High</td>
            <td>Yes</td>
            <td>Yes</td>
        </tr>
        <tr>
            <td><b>Service principal identity should be used to access container images in Container Registry</b><br />Using
                a 'user' account should be avoided because, in general, a user account will likely have broader set of
                privileges to enterprise assets. Using a dedicated SPN ensures that the SPN does not have permissions
                beyond the ones specifically granted for the given scenario.</td>
            <td>Medium</td>
            <td>Yes</td>
            <td>No</td>
        </tr>
        <tr>
            <td><b>Credentials of service principal used for Container Registry must be stored in Key Vault</b><br />Keeping/sharing
                password in clear text can lead to easy compromise at various avenues during an application's life
                cycle. Storing them in a key vault ensures that they are protected at rest.</td>
            <td>High</td>
            <td>No</td>
            <td>No</td>
        </tr>
        <tr>
            <td><b>All users/identities must be granted minimum required permissions using Role Based Access Control
                    (RBAC)</b><br />Granting minimum access by leveraging RBAC feature ensures that users are granted
                just enough permissions to perform their tasks. This minimizes exposure of the resources in case of
                user/service account compromise.</td>
            <td>Medium</td>
            <td>Yes</td>
            <td>No</td>
        </tr>
        <tr>
            <td><b>Image vulnerability scan should be configured through webhook when images are pushed to Container
                    Registry</b><br />Container image(s) having vulnerability (e.g. missing OS patches in base image,
                open ports in image) can lead to loss of sensitive enterprise data.</td>
            <td>Medium</td>
            <td>Yes</td>
            <td>No</td>
        </tr>
        <tr>
            <td><b>Container Registry must have latest/patched image(s) all the time</b><br />Un-patched images are
                easy targets for compromise from various malware/trojan attacks that exploit known vulnerabilities in
                operating systems and related software.</td>
            <td>Medium</td>
            <td>No</td>
            <td>No</td>
        </tr>
        <tr>
            <td><b>Content trust in Container Registry must be enabled</b><br />Content trust gives the ability to
                verify both the integrity and the publisher of all the data received from a Registry over any channel.
                If a container image is served from an untrusted registry, the image itself may not be
                trustworthy/stable. Running such a compromised image can lead to loss of sensitive enterprise data.</td>
            <td>Medium</td>
            <td>Yes</td>
            <td>No</td>
        </tr>
        <tr>
            <td><b>Activity logs for Data Container Registry should be reviewed periodically</b><br />Periodic reviews
                of activity and audit logs ensures that anomalous activity can be identified early enough instead of
                after a major compromise.</td>
            <td>Medium</td>
            <td>No</td>
            <td>No</td>
        </tr>
        <tr>
            <td><b>Only signed images must be pushed in Container Registry</b><br />Content trust gives the ability to
                verify both the integrity and the publisher of all the data received from a Registry over any channel.
                If a container image is served from an untrusted registry, the image itself may not be
                trustworthy/stable. Running such a compromised image can lead to loss of sensitive enterprise data.</td>
            <td>Medium</td>
            <td>No</td>
            <td>No</td>
        </tr>
    </table>
    <table>
    </table>
</body>

</html>
