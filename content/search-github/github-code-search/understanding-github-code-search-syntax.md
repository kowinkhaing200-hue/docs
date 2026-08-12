---{
  "openapi": "3.1.0",
  "info": {
    "title": "GitBook API",
    "description": "The GitBook API",
    "termsOfService": "https://policies.gitbook.com",
    "contact": {
      "name": "API Support",
      "url": "https://gitbook.com/support",
      "email": "support@gitbook.com"
    },
    "version": "0.0.1-beta"
  },
  "servers": [
    {
      "url": "{host}/v1",
      "variables": {
        "host": {
          "default": "https://api.gitbook.com"
        }
      }
    }
  ],
  "security": [
    {
      "user": []
    },
    {
      "user-internal": []
    },
    {
      "user-staff": []
    },
    {
      "integration": []
    },
    {
      "integration-installation": []
    }
  ],
  "tags": [
    {
      "name": "organizations",
      "x-page-icon": "building",
      "x-page-title": "Organizations",
      "x-page-description": "Manage your organizations and group your members, spaces, and resources under one collaborative structure.",
      "description": "The Organizations API provides a robust way to handle the administrative structure of your GitBook workspace. By creating and configuring organizations, you can group multiple users, spaces, and collections, simplifying your permission management and fostering efficient collaboration for teams of any size.\n\n{% openapi-schemas spec=\"gitbook\" schemas=\"Organization\" grouped=\"false\" %}\n    The Organization object\n{% endopenapi-schemas %}\n"
    },
    {
      "name": "organization-members",
      "x-page-title": "Organization members",
      "x-page-description": "Handle all aspects of membership within an organization, from listing to role management.",
      "x-parent": "organizations",
      "description": "Organization members can be managed through this API, which lets you invite and manage users under a particular organization. You can define roles and permissions to ensure your team has the right level of access.\n"
    },
    {
      "name": "organization-invites",
      "x-page-title": "Organization invites",
      "x-page-description": "Streamline the invitation process for new members joining your organization.",
      "x-parent": "organizations",
      "description": "Use this API to create and revoke invitations for new members. By automating invite flows, you can maintain a cohesive onboarding experience for collaborators and speed up team expansion.\n"
    },
    {
      "name": "organization-ask",
      "x-page-title": "Organization AI ask",
      "x-page-description": "Unlock AI-driven answers for your organization's content and data.",
      "x-parent": "organizations",
      "description": "Enhance your team's knowledge base with the Organization AI ask endpoint, which allows you to query AI models trained on your organization's GitBook content for quick, intelligent responses.\n"
    },
    {
      "name": "sites",
      "x-page-icon": "globe",
      "x-page-title": "Docs sites",
      "x-page-description": "Manage your published docs sites.",
      "description": "The Docs Sites API lets you programmatically manage published documentation sites within your organization. You can list and update all sites created under a specific organization, making it easy to audit or interact with site metadata at scale.\n\n{% openapi-schemas spec=\"gitbook\" schemas=\"Site\" grouped=\"false\" %}\n    The Site object\n{% endopenapi-schemas %}\n"
    },
    {
      "name": "site-share-links",
      "x-page-title": "Site share links",
      "x-page-description": "Control how you share docs externally by managing share links for a site.",
      "x-parent": "sites",
      "description": "Manage the lifecycle of share links for your published sites. This includes generating new links for external sharing and revoking or updating existing ones.\n\n{% openapi-schemas spec=\"gitbook\" schemas=\"ShareLink\" grouped=\"false\" %}\n    The ShareLink object\n{% endopenapi-schemas %}\n"
    },
    {
      "name": "site-structure",
      "x-page-title": "Site structure",
      "x-page-description": "Retrieve and manipulate the entire hierarchical layout of a site.",
      "x-parent": "sites",
      "description": "Provides a complete overview of how content is organized on a site. With this API, you can discover page nesting, identify sections, and reorder site elements as needed.\n\n{% openapi-schemas spec=\"gitbook\" schemas=\"SiteStructure\" grouped=\"false\" %}\n    The SiteStructure object\n{% endopenapi-schemas %}\n"
    },
    {
      "name": "site-publishing-auth",
      "x-page-title": "Site auth",
      "x-page-description": "Manage the authentication needed for publishing your site.",
      "x-parent": "sites",
      "description": "Configure the credentials or tokens required to publish documentation externally. This helps ensure your site is consistently kept up to date.\n\n{% openapi-schemas spec=\"gitbook\" schemas=\"SitePublishingAuth\" grouped=\"false\" %}\n    The SitePublishingAuth object\n{% endopenapi-schemas %}\n"
    },
    {
      "name": "site-preview",
      "x-page-title": "Site preview",
      "x-page-description": "Fetch an up-to-date preview of your site before publishing.",
      "x-parent": "sites",
      "description": "Quickly generate a preview of how your site's content and layout will appear once published, allowing for final checks and refinement prior to going live.\n"
    },
    {
      "name": "site-customization",
      "x-page-title": "Site customization",
      "x-page-description": "Customize the look and feel of your docs site.",
      "x-parent": "sites",
      "description": "Update your site's branding, styling, and layout to match your organization's identity. This includes theming elements like color palette, logos, and more.\n\n{% openapi-schemas spec=\"gitbook\" schemas=\"SiteCustomizationSettings\" grouped=\"false\" %}\n    The SiteCustomizationSettings object\n{% endopenapi-schemas %}\n"
    },
    {
      "name": "site-agent-settings",
      "x-page-title": "Site agent settings",
      "x-page-description": "Configure site-specific issue remediation behavior and agent instructions.",
      "x-parent": "sites",
      "description": "Configure how site issue remediation should behave and provide site-specific instructions for the editing and topic analyst agents.\n\n{% openapi-schemas spec=\"gitbook\" schemas=\"SiteAgentSettings\" grouped=\"false\" %}\n    The SiteAgentSettings object\n{% endopenapi-schemas %}\n"
    },
    {
      "name": "site-spaces",
      "x-page-title": "Site spaces",
      "x-page-description": "Control which spaces are linked and displayed in a docs site.",
      "x-parent": "sites",
      "description": "Associate or dissociate your organization's spaces to keep your content organized. This is particularly useful for larger organizations with numerous spaces.\n\n{% openapi-schemas spec=\"gitbook\" schemas=\"SiteSpace\" grouped=\"false\" %}\n    The SiteSpace object\n{% endopenapi-schemas %}\n"
    },
    {
      "name": "site-sections",
      "x-page-title": "Site sections",
      "x-page-description": "Create and organize high-level sections for your docs site.",
      "x-parent": "sites",
      "description": "Sections help partition your site's content at the top level. They can be modified, deleted, or reorganized to reflect your site's changing structure.\n\n{% openapi-schemas spec=\"gitbook\" schemas=\"SiteSection\" grouped=\"false\" %}\n    The SiteSection object\n{% endopenapi-schemas %}\n"
    },
    {
      "name": "site-section-groups",
      "x-page-title": "Site section groups",
      "x-page-description": "Group and manage sections of your docs for easier organization.",
      "x-parent": "sites",
      "description": "Section groups let you bundle multiple top-level sections together, offering additional structuring capabilities and simplifying navigation for your readers.\n\n{% openapi-schemas spec=\"gitbook\" schemas=\"SiteSectionGroup\" grouped=\"false\" %}\n    The SiteSectionGroup object\n{% endopenapi-schemas %}\n"
    },
    {
      "name": "site-redirects",
      "x-page-title": "Site redirects",
      "x-page-description": "Establish redirects for pages that have moved or changed in your docs site.",
      "x-parent": "sites",
      "description": "Keep your site's content fresh without breaking old links. This API allows you to create and manage redirection rules.\n\n{% openapi-schemas spec=\"gitbook\" schemas=\"SiteRedirect\" grouped=\"false\" %}\n    The SiteRedirect object\n{% endopenapi-schemas %}\n"
    },
    {
      "name": "site-mcp-servers",
      "x-page-title": "Site MCP servers",
      "x-page-description": "Configure external MCP servers used by your site.",
      "x-parent": "sites",
      "description": "Manage Model Context Protocol (Mcp) servers used by your site.\n\n{% openapi-schemas spec=\"gitbook\" schemas=\"SiteMcpServer\" grouped=\"false\" %}\n    The SiteMcpServer object\n{% endopenapi-schemas %}\n"
    },
    {
      "name": "site-channels",
      "x-page-title": "Site channels",
      "x-page-description": "Configure site channels for your docs site.",
      "x-parent": "sites",
      "description": "Manage the channels used as origins for questions and answers in your site ask data.\n\n{% openapi-schemas spec=\"gitbook\" schemas=\"SiteChannel\" grouped=\"false\" %}\n    The SiteChannel object\n{% endopenapi-schemas %}\n"
    },
    {
      "name": "site-ads",
      "x-page-title": "Site ads",
      "x-page-description": "Control and customize ad placements on your docs site.",
      "x-parent": "sites",
      "description": "Manage the advertisement strategy within your docs. You can specify ad placements, track usage, and adjust settings to best fit your organization's needs.\n"
    },
    {
      "name": "site-permissions",
      "x-page-title": "Site permissions",
      "x-page-description": "Manage which members and teams can access or contribute to a docs site.",
      "x-parent": "sites",
      "description": "Invite, remove, or update users and teams permissions for a site. This provides a way to tightly control collaboration and visibility among your teammates.\n"
    },
    {
      "name": "site-insights",
      "x-page-title": "Site insights",
      "x-page-description": "Analyze traffic and engagement metrics for your docs site.",
      "x-parent": "sites",
      "description": "This API delivers insights about how visitors interact with your site, including page views and user engagement, helping you measure and optimize your content strategy.\n"
    },
    {
      "name": "site-ai",
      "x-page-title": "Site AI",
      "x-page-description": "Build conversational AI agents for your docs site.",
      "x-parent": "sites",
      "description": "Build advanced conversational AI experiences within your docs site that go beyond basic Q&A.\n"
    },
    {
      "name": "site-ask",
      "x-page-title": "Site AI ask",
      "x-page-description": "Allow AI-driven queries within a specific docs site.",
      "x-parent": "sites",
      "description": "Give your users a way to ask content-aware AI queries that are scoped entirely to the site's published documents.\n"
    },
    {
      "name": "site-context",
      "x-page-title": "Site context",
      "x-page-description": "Manage context records, connections, and topics for a docs site.",
      "x-parent": "sites",
      "description": "Manage the contextual records and topics used by your site to power AI experiences and insights.\n\n{% openapi-schemas spec=\"gitbook\" schemas=\"ContextRecord,ContextConnection,SiteTopic,SiteFinding,SiteFindingPage\" grouped=\"false\" %}\n    The Site Context objects\n{% endopenapi-schemas %}\n"
    },
    {
      "name": "site-questions",
      "x-page-title": "Site questions",
      "x-page-description": "Review questions, answers, and sources generated for a docs site.",
      "x-parent": "sites",
      "description": "Inspect the canonical questions asked on your site, the generated answers linked to each question, and the sources used for each answer.\n\n{% openapi-schemas spec=\"gitbook\" schemas=\"SiteQuestion,SiteQuestionAnswer,SiteQuestionAnswerWithResponse,SiteQuestionAnswerSource\" grouped=\"false\" %}\n    The Site Questions objects\n{% endopenapi-schemas %}\n"
    },
    {
      "name": "collections",
      "x-page-icon": "folder",
      "x-page-title": "Collections",
      "x-page-description": "Organize and manage grouped sets of spaces for better content structure.",
      "description": "Collections let you bundle multiple spaces under a unified entity, making large-scale content easier to handle. You can sort content by subject, department, or any grouping logic.\n\n{% openapi-schemas spec=\"gitbook\" schemas=\"Collection\" grouped=\"false\" %}\n    The Collection object\n{% endopenapi-schemas %}\n"
    },
    {
      "name": "collection-permissions",
      "x-page-title": "Collection permissions",
      "x-page-description": "Manage which members and teams can access or contribute to a collection of spaces.",
      "x-parent": "collections",
      "description": "Control which users and teams have access to a collection's spaces. This ensures only the right individuals can view or modify sensitive content.\n"
    },
    {
      "name": "spaces",
      "x-page-icon": "book-sparkles",
      "x-page-title": "Spaces",
      "x-page-description": "Create, maintain, and remove content spaces.",
      "description": "Spaces are containers for your documentation or knowledge base content. Use this API to create new spaces, manage existing ones, and delete or archive spaces you no longer need.\n\n{% openapi-schemas spec=\"gitbook\" schemas=\"Space\" grouped=\"false\" %}\n    The Space object\n{% endopenapi-schemas %}\n"
    },
    {
      "name": "space-content",
      "x-page-title": "Space content",
      "x-page-description": "Import, export, and search content in a space.",
      "x-parent": "spaces",
      "description": "Handle your space content programmatically by creating, updating, or listing pages and files. Ideal for bulk operations or synchronizing with external systems.\n"
    },
    {
      "name": "space-comments",
      "x-page-title": "Space comments",
      "x-page-description": "Integrate and manage user comments in a space.",
      "x-parent": "spaces",
      "description": "Comments are a powerful way to gather feedback on your documentation. Use this API to post, list, update, or delete comments and keep conversations organized.\n\n{% openapi-schemas spec=\"gitbook\" schemas=\"Comment\" grouped=\"false\" %}\n    The Comment object\n{% endopenapi-schemas %}\n"
    },
    {
      "name": "space-embeds",
      "x-page-title": "Space embeds",
      "x-page-description": "Render or resolve embedded content within a space.",
      "x-parent": "spaces",
      "description": "Automatically fetch metadata or previews for embedded resources such as videos, images, or external docs, enabling richer content experiences in your space.\n"
    },
    {
      "name": "space-permissions",
      "x-page-title": "Space permissions",
      "x-page-description": "Manage which members and teams roles and permissions on a per-space basis.",
      "x-parent": "spaces",
      "description": "Give your collaborators the right level of access for specific spaces, or assign entire teams to your spaces and streamline the process of granting or revoking access at scale, without dealing with individual user roles.\n"
    },
    {
      "name": "space-integrations",
      "x-page-title": "Space integrations",
      "x-page-description": "Connect external tools and plugins to enhance your space functionality.",
      "x-parent": "spaces",
      "description": "This API handles the registration and removal of integrations, automating how data flows between GitBook and your chosen external services.\n"
    },
    {
      "name": "space-git",
      "x-page-title": "Git",
      "x-page-description": "Connect Git repositories to your space for seamless version control.",
      "x-parent": "spaces",
      "description": "Manage the linkage between your GitBook space and external Git repositories, enabling commits, merges, and pull requests directly tied to your documentation.\n"
    },
    {
      "name": "change-requests",
      "x-page-icon": "code-pull-request",
      "x-page-title": "Change requests",
      "x-page-description": "Review and collaborate on proposed documentation changes before merging.",
      "description": "This API helps you keep your space clean by letting contributors propose changes, review them, and then merge or discard as needed.\n\n{% openapi-schemas spec=\"gitbook\" schemas=\"ChangeRequest\" grouped=\"false\" %}\n    The ChangeRequest object\n{% endopenapi-schemas %}\n"
    },
    {
      "name": "change-request-content",
      "x-page-title": "Change request content",
      "x-page-description": "Manage the actual content changes associated with a change request.",
      "x-parent": "change-requests",
      "description": "Retrieve or update the pages and files tied to an open change request. This lets you preview alterations and merge them when ready.\n"
    },
    {
      "name": "change-request-contributors",
      "x-page-title": "Change request contributors",
      "x-page-description": "See who's participating in the change request.",
      "x-parent": "change-requests",
      "description": "Quickly access the full list of collaborators and their contributions within a change request for better traceability and communication.\n\n{% openapi-schemas spec=\"gitbook\" schemas=\"UserContributor\" grouped=\"false\" %}\n    The UserContributor object\n{% endopenapi-schemas %}\n"
    },
    {
      "name": "change-request-reviewers",
      "x-page-title": "Change request reviewers",
      "x-page-description": "Assign or list requested reviewers for a change request.",
      "x-parent": "change-requests",
      "description": "Ensure quality by requesting and tracking reviewer feedback in your GitBook flow. This endpoint helps orchestrate the entire review cycle.\n\n{% openapi-schemas spec=\"gitbook\" schemas=\"ChangeRequestRequestedReviewer\" grouped=\"false\" %}\n    The ChangeRequestRequestedReviewer object\n{% endopenapi-schemas %}\n"
    },
    {
      "name": "change-request-comments",
      "x-page-title": "Change request comments",
      "x-page-description": "Engage in threaded conversations on proposed changes.",
      "x-parent": "change-requests",
      "description": "This API powers the inline discussion around any new or updated documentation. Participate in comment threads and resolve them after reaching consensus.\n\n{% openapi-schemas spec=\"gitbook\" schemas=\"Comment\" grouped=\"false\" %}\n    The Comment object\n{% endopenapi-schemas %}\n"
    },
    {
      "name": "analytics",
      "x-page-icon": "chart-line",
      "x-page-title": "Analytics",
      "x-page-description": "Tap into metrics that reveal your content's performance and usage patterns.",
      "description": "Gather data-driven insights on how users interact with your spaces, pages, or entire site. Analytics can highlight trends and guide future content improvements.\n"
    },
    {
      "name": "translations",
      "x-page-icon": "language",
      "x-page-title": "Translations",
      "x-page-description": "Configure multi-language support and translation options for your documentation.",
      "description": "The Translations API provides ways to localize your content into various languages. It supports custom strings, default language settings, and more.\n"
    },
    {
      "name": "translation-languages",
      "x-page-title": "Translations languages",
      "x-page-description": "Manage the individual language configurations for your docs translation setup.",
      "x-parent": "translations",
      "description": "Enable or disable specific languages, configure default text direction, or adjust advanced translation settings to ensure clarity for your global audience.\n\n{% openapi-schemas spec=\"gitbook\" schemas=\"TranslationLanguageSettings\" grouped=\"false\" %}\n    The TranslationLanguageSettings object\n{% endopenapi-schemas %}\n"
    },
    {
      "name": "imports",
      "x-page-icon": "cloud-arrow-up",
      "x-page-title": "Imports",
      "x-page-description": "Import content into GitBook.",
      "description": "The Imports API provides allows you to import content into GitBook.\n"
    },
    {
      "name": "glossary",
      "x-page-title": "Glossary",
      "x-page-description": "Manage custom terms translations used by the translation feature.",
      "x-parent": "translations",
      "description": "Define terms and specify their translations for different languages to ensure consistent wording.\n\n{% openapi-schemas spec=\"gitbook\" schemas=\"GlossaryEntry\" grouped=\"false\" %}\n    The GlossaryEntry object\n{% endopenapi-schemas %}\n"
    },
    {
      "name": "integrations",
      "x-page-icon": "puzzle-piece",
      "x-page-title": "Integrations",
      "x-page-description": "Install and handle third-party integrations for extended GitBook functionality.",
      "description": "Expand the capabilities of GitBook by connecting it with various external platforms—CRM, finding trackers, or CI/CD pipelines—through standardized integration endpoints.\n"
    },
    {
      "name": "urls",
      "x-page-icon": "link",
      "x-page-title": "URLs",
      "x-page-description": "Configure where and how your GitBook content can be accessed.",
      "description": "Manage official endpoints, direct deep links, or short links for your content. This allows you to keep track of multiple custom URLs or vanity links under one system.\n"
    },
    {
      "name": "openapi",
      "x-page-icon": "code",
      "x-page-title": "OpenAPI",
      "x-page-description": "Upload, access, or version-control your OpenAPI specifications directly in GitBook.",
      "description": "The OpenAPI endpoints let you integrate your existing or newly generated OpenAPI definitions into GitBook. This includes uploading, updating, and retrieving specs.\n\n{% openapi-schemas spec=\"gitbook\" schemas=\"OpenAPISpec\" grouped=\"false\" %}\n    The OpenAPISpec object\n{% endopenapi-schemas %}\n"
    },
    {
      "name": "openapi-versions",
      "x-page-title": "OpenAPI spec versions",
      "x-page-description": "Track changes to your OpenAPI documents by versioning them.",
      "x-parent": "openapi",
      "description": "Keep a history of your OpenAPI specs, enabling you to compare different versions, revert, or maintain multiple concurrent versions for testing or documentation.\n\n{% openapi-schemas spec=\"gitbook\" schemas=\"OpenAPISpecVersion\" grouped=\"false\" %}\n    The OpenAPISpecVersion object\n{% endopenapi-schemas %}\n"
    },
    {
      "name": "custom-fonts",
      "x-page-icon": "font",
      "x-page-title": "Custom fonts",
      "x-page-description": "Bring your own fonts to personalize your documentation style.",
      "description": "Upload and manage custom fonts for branding or aesthetic purposes. Once added, fonts can be applied to your spaces or sites to achieve a unique look.\n\n{% openapi-schemas spec=\"gitbook\" schemas=\"CustomizationFontDefinition\" grouped=\"false\" %}\n    The CustomizationFontDefinition object\n{% endopenapi-schemas %}\n"
    },
    {
      "name": "billing",
      "x-page-icon": "credit-card",
      "x-page-title": "Billing",
      "x-page-description": "Organize payment details and subscription plans for your organization.",
      "description": "Centralize billing activities here, including updating payment methods, adjusting subscriptions, or reviewing invoices. Simplify how you track and control costs.\n"
    },
    {
      "name": "hive",
      "x-page-icon": "network-wired",
      "x-page-title": "Hive",
      "x-page-description": "Bring teams together and share resources effectively across GitBook.",
      "description": "Hive is a collaborative layer over your GitBook data, designed to streamline knowledge sharing, cross-project tasks, and reduce duplicate efforts among your teammates.\n"
    },
    {
      "name": "subdomains",
      "x-page-icon": "diagram-project",
      "x-page-title": "Subdomains",
      "x-page-description": "Manage and configure organization-specific subdomains for your docs.",
      "description": "Provide a branded subdomain for each organization to create a consistent user experience. This API supports subdomain creation, DNS checks, and more.\n\n{% openapi-schemas spec=\"gitbook\" schemas=\"Subdomain\" grouped=\"false\" %}\n    The Subdomain object\n{% endopenapi-schemas %}\n"
    },
    {
      "name": "users",
      "x-page-icon": "users",
      "x-page-title": "Users",
      "x-page-description": "Retrieve and manage user information and profiles.",
      "description": "The Users API allows you to fetch data about GitBook users, including the authenticated account or other team members by ID. This is crucial for customizing permissions, personalizing content, or establishing user-specific flows.\n\n{% openapi-schemas spec=\"gitbook\" schemas=\"User\" grouped=\"false\" %}\n    The User object\n{% endopenapi-schemas %}\n"
    },
    {
      "name": "teams",
      "x-page-icon": "people-group",
      "x-page-title": "Teams",
      "x-page-description": "Create and manage teams as reusable groups of users.",
      "description": "Teams offer a convenient way to assign roles and access to multiple users at once. This helps maintain large-scale projects more efficiently by reducing overhead in user-by-user management.\n\n{% openapi-schemas spec=\"gitbook\" schemas=\"Team\" grouped=\"false\" %}\n    The Team object\n{% endopenapi-schemas %}\n"
    },
    {
      "name": "team-members",
      "x-page-title": "Team members",
      "x-page-description": "Control membership at the team level for cohesive role management.",
      "x-parent": "teams",
      "description": "Easily add or remove users from teams, as well as fine-tune their specific roles within a team to ensure secure, well-organized collaboration.\n\n{% openapi-schemas spec=\"gitbook\" schemas=\"TeamMember\" grouped=\"false\" %}\n    The TeamMember object\n{% endopenapi-schemas %}\n"
    },
    {
      "name": "sso",
      "x-page-icon": "lock",
      "x-page-title": "SSO",
      "x-page-description": "Configure Single Sign-On solutions to unify your organization's authentication.",
      "description": "Tie GitBook into your corporate identity management and authentication providers (like SAML or OAuth). This centralizes user authentication and improves security.\n\n{% openapi-schemas spec=\"gitbook\" schemas=\"Subdomain\" grouped=\"false\" %}\n    The Subdomain object\n{% endopenapi-schemas %}\n"
    },
    {
      "name": "storage",
      "x-page-icon": "database",
      "x-page-title": "Storage",
      "x-page-description": "Upload and store files directly within your GitBook organization.",
      "description": "Whether you're hosting images, documents, or other assets, Storage endpoints allow you to integrate those files into your documentation and spaces seamlessly.\n"
    },
    {
      "name": "custom-hostnames",
      "x-page-icon": "server",
      "x-page-title": "Custom hostnames",
      "x-page-description": "Serve your GitBook content from fully branded, custom hostnames.",
      "description": "Extend your brand identity by mapping personalized domain names to your docs. This can help unify your documentation site with your existing company properties.\n\n{% openapi-schemas spec=\"gitbook\" schemas=\"CustomHostname\" grouped=\"false\" %}\n    The CustomHostname object\n{% endopenapi-schemas %}\n"
    },
    {
      "name": "system",
      "x-page-icon": "gears",
      "x-page-title": "System info",
      "x-page-description": "Programmatically check GitBook API system status and version details.",
      "description": "Use these endpoints to monitor the overall health of GitBook's infrastructure or to retrieve version information for debugging and compliance purposes.\n"
    }
  ],
  "paths": {
    "/": {
      "get": {
        "operationId": "getApiInformation",
        "tags": [
          "system"
        ],
        "summary": "Get API information",
        "description": "Access the release version and build date of the GitBook codebase.",
        "responses": {
          "200": {
            "description": "OK",
            "content": {
              "application/json": {
                "schema": {
                  "$ref": "#/components/schemas/ApiInformation"
                }
              }
            }
          }
        }
      }
    },
    "/user": {
      "get": {
        "operationId": "getAuthenticatedUser",
        "summary": "Get profile of authenticated user",
        "tags": [
          "users",
          "critical"
        ],
        "security": [
          {
            "user": []
          },
          {
            "oauth": [
              "user:read"
            ]
          }
        ],
        "description": "Returns details about the user associated with the authentication provided in the request's authorization header.\n",
        "responses": {
          "200": {
            "description": "OK",
            "content": {
              "application/json": {
                "schema": {
                  "$ref": "#/components/schemas/User"
                }
              }
            }
          },
          "404": {
            "description": "User not found",
            "$ref": "#/components/responses/NotFoundError"
          }
        }
      }
    },
    "/user/notifications/token": {
      "post": {
        "operationId": "createUserNotificationsToken",
        "summary": "Create a JWT to access the in-app notifications service",
        "description": "Generates a JWT for the authenticated user. This token is used by the frontend notifications client to access user endpoints.\n",
        "tags": [
          "users"
        ],
        "security": [
          {
            "user-internal": []
          }
        ],
        "responses": {
          "200": {
            "description": "The notifications service User JWT",
            "content": {
              "application/json": {
                "schema": {
                  "$ref": "#/components/schemas/APITemporaryToken"
                }
              }
            }
          }
        }
      }
    },
    "/users/{userId}": {
      "get": {
        "operationId": "getUserById",
        "summary": "Get a user by its ID",
        "tags": [
          "users",
          "critical"
        ],
        "security": [
          {
            "user": []
          }
        ],
        "description": "Provides publicly available information about someone with a GitBook account.\n",
        "parameters": [
          {
            "$ref": "#/components/parameters/userId"
          }
        ],
        "responses": {
          "200": {
            "description": "OK",
            "content": {
              "application/json": {
                "schema": {
                  "$ref": "#/components/schemas/User"
                }
              }
            }
          },
          "404": {
            "description": "User not found",
            "$ref": "#/components/responses/NotFoundError"
          }
        }
      },
      "patch": {
        "operationId": "updateUserById",
        "summary": "Update a user by its ID",
        "tags": [
          "users",
          "critical"
        ],
        "security": [
          {
            "user": []
          }
        ],
        "description": "Update a GitBook account's details.\n",
        "parameters": [
          {
            "$ref": "#/components/parameters/userId"
          }
        ],
        "requestBody": {
          "required": true,
          "content": {
            "application/json": {
              "schema": {
                "type": "object",
                "minProperties": 1,
                "properties": {
                  "displayName": {
                    "type": "string",
                    "description": "Full name for the user",
                    "minLength": 1,
                    "maxLength": 64
                  },
                  "photoURL": {
                    "$ref": "#/components/schemas/URL"
                  }
                }
              }
            }
          }
        },
        "responses": {
          "200": {
            "description": "The user has been updated",
            "content": {
              "application/json": {
                "schema": {
                  "$ref": "#/components/schemas/User"
                }
              }
            }
          },
          "404": {
            "description": "User not found",
            "$ref": "#/components/responses/NotFoundError"
          }
        }
      }
    },
    "/spaces/{spaceId}": {
      "get": {
        "operationId": "getSpaceById",
        "summary": "Get full details of a space by its ID",
        "description": "Returns the full metadata for a space. Use this to resolve a spaceId into a complete Space object. If you only need content, use the content endpoint instead.",
        "x-gitbook-mcp": true,
        "tags": [
          "spaces",
          "critical"
        ],
        "security": [
          {
            "user": []
          },
          {
            "integration": []
          },
          {
            "integration-installation": []
          },
          {
            "oauth": [
              "space:read"
            ]
          }
        ],
        "parameters": [
          {
            "$ref": "#/components/parameters/spaceId"
          },
          {
            "$ref": "#/components/parameters/siteShareKey"
          }
        ],
        "responses": {
          "200": {
            "description": "OK",
            "content": {
              "application/json": {
                "schema": {
                  "$ref": "#/components/schemas/Space"
                }
              }
            }
          }
        }
      },
      "patch": {
        "operationId": "updateSpaceById",
        "summary": "Update a space's title, icon, or settings",
        "description": "Updates a space's metadata and settings. To update page content, use the change-request workflow instead.",
        "x-gitbook-mcp": true,
        "tags": [
          "spaces"
        ],
        "security": [
          {
            "user": []
          },
          {
            "oauth": [
              "space:write"
            ]
          }
        ],
        "parameters": [
          {
            "$ref": "#/components/parameters/spaceId"
          }
        ],
        "requestBody": {
          "required": true,
          "content": {
            "application/json": {
              "schema": {
                "allOf": [
                  {
                    "type": "object",
                    "properties": {
                      "editMode": {
                        "$ref": "#/components/schemas/SpaceEditMode"
                      },
                      "title": {
                        "$ref": "#/components/schemas/SpaceTitle"
                      },
                      "defaultLevel": {
                        "$ref": "#/components/schemas/DefaultLevel"
                      },
                      "language": {
                        "$ref": "#/components/schemas/TranslationLanguage"
                      },
                      "mergeRules": {
                        "$ref": "#/components/schemas/MergeRulesSpaceConfiguration"
                      }
                    }
                  },
                  {
                    "oneOf": [
                      {
                        "type": "object",
                        "title": "Emoji",
                        "properties": {
                          "emoji": {
                            "$ref": "#/components/schemas/Emoji"
                          }
                        },
                        "required": [
                          "emoji"
                        ]
                      },
                      {
                        "type": "object",
                        "title": "Icon",
                        "properties": {
                          "icon": {
                            "$ref": "#/components/schemas/URL"
                          }
                        },
                        "required": [
                          "icon"
                        ]
                      },
                      {
                        "type": "object",
                        "title": "Remove icon or emoji",
                        "properties": {
                          "emoji": {
                            "type": "null"
                          },
                          "icon": {
                            "type": "null"
                          }
                        }
                      }
                    ]
                  }
                ]
              }
            }
          }
        },
        "responses": {
          "200": {
            "description": "The space has been updated",
            "content": {
              "application/json": {
                "schema": {
                  "$ref": "#/components/schemas/Space"
                }
              }
            }
          }
        }
      },
      "delete": {
        "operationId": "deleteSpaceById",
        "summary": "Delete a space",
        "description": "Deleted spaces will be permanently removed after 7 days.",
        "tags": [
          "spaces"
        ],
        "security": [
          {
            "user": []
          },
          {
            "oauth": [
              "space:write"
            ]
          }
        ],
        "parameters": [
          {
            "$ref": "#/components/parameters/spaceId"
          }
        ],
        "responses": {
          "204": {
            "description": "Space did not exist"
          },
          "205": {
            "description": "Space has been deleted"
          }
        }
      }
    },
    "/spaces/{spaceId}/duplicate": {
      "post": {
        "operationId": "duplicateSpace",
        "summary": "Create a full copy of a space",
        "description": "Creates a new space that is a complete copy of the specified space, including all pages and their content. The duplicate is created in the same organization. It does not preserve or create a placement in a site. When duplicating from a site context, use duplicateSiteSpace instead. Use this operation for an organization-level or orphan-space copy.",
        "x-gitbook-mcp": true,
        "tags": [
          "spaces"
        ],
        "security": [
          {
            "user": []
          },
          {
            "oauth": [
              "space:write"
            ]
          }
        ],
        "parameters": [
          {
            "$ref": "#/components/parameters/spaceId"
          }
        ],
        "responses": {
          "201": {
            "description": "Space duplicated",
            "headers": {
              "Location": {
                "description": "API URL for the newly created space",
                "schema": {
                  "type": "string"
                }
              }
            },
            "content": {
              "application/json": {
                "schema": {
                  "$ref": "#/components/schemas/Space"
                }
              }
            }
          }
        }
      }
    },
    "/spaces/{spaceId}/restore": {
      "post": {
        "operationId": "restoreSpace",
        "summary": "Restore a recently deleted space from the trash",
        "description": "Restores a previously deleted space, making it active again. Only spaces deleted within the last 7 days can be restored; after that they are permanently removed. Returns the restored space object. To delete a space, use the space delete endpoint.",
        "x-gitbook-mcp": true,
        "tags": [
          "spaces"
        ],
        "security": [
          {
            "user": []
          },
          {
            "oauth": [
              "space:write"
            ]
          }
        ],
        "parameters": [
          {
            "$ref": "#/components/parameters/spaceId"
          }
        ],
        "responses": {
          "200": {
            "description": "Space restored",
            "content": {
              "application/json": {
                "schema": {
                  "$ref": "#/components/schemas/Space"
                }
              }
            }
          }
        }
      }
    },
    "/spaces/{spaceId}/move": {
      "post": {
        "operationId": "moveSpace",
        "summary": "Move a space to a different collection or position",
        "description": "Moves a space to a new parent collection and/or a new position within the hierarchy.",
        "x-gitbook-mcp": true,
        "tags": [
          "spaces"
        ],
        "security": [
          {
            "user": []
          },
          {
            "oauth": [
              "space:write"
            ]
          }
        ],
        "parameters": [
          {
            "$ref": "#/components/parameters/spaceId"
          }
        ],
        "requestBody": {
          "required": true,
          "content": {
            "application/json": {
              "schema": {
                "type": "object",
                "minProperties": 1,
                "properties": {
                  "parent": {
                    "description": "The unique id of the parent collection",
                    "type": [
                      "string",
                      "null"
                    ]
                  },
                  "position": {
                    "description": "Where to move the space. By default, it will be moved at the end.",
                    "$ref": "#/components/schemas/ContentPosition"
                  }
                }
              }
            }
          }
        },
        "responses": {
          "200": {
            "description": "Space moved",
            "content": {
              "application/json": {
                "schema": {
                  "$ref": "#/components/schemas/Space"
                }
              }
            }
          },
          "400": {
            "description": "Invalid position space or collection provided",
            "$ref": "#/components/responses/BadRequestError"
          },
          "404": {
            "description": "No matching Space found for given ID",
            "$ref": "#/components/responses/NotFoundError"
          },
          "409": {
            "description": "Operation would not result in any update",
            "$ref": "#/components/responses/ConflictError"
          }
        }
      }
    },
    "/spaces/{spaceId}/embed": {
      "get": {
        "operationId": "getEmbedByUrlInSpace",
        "summary": "Resolve a URL to an oEmbed object within a space",
        "description": "Resolves an external URL to an oEmbed representation (title, thumbnail, HTML snippet) within the context of a space. Use this to preview or embed third-party content referenced in a space's pages. Requires the URL as a query parameter.",
        "x-gitbook-mcp": true,
        "tags": [
          "space-embeds"
        ],
        "security": [
          {
            "user": []
          },
          {
            "oauth": [
              "space:read"
            ]
          }
        ],
        "parameters": [
          {
            "$ref": "#/components/parameters/spaceId"
          },
          {
            "name": "url",
            "in": "query",
            "required": true,
            "description": "URL to resolve",
            "schema": {
              "type": "string"
            }
          }
        ],
        "responses": {
          "200": {
            "description": "OK",
            "content": {
              "application/json": {
                "schema": {
                  "$ref": "#/components/schemas/Embed"
                }
              }
            }
          }
        }
      }
    },
    "/spaces/{spaceId}/search": {
      "get": {
        "operationId": "searchSpaceContent",
        "summary": "Full-text search across all pages in a space",
        "description": "Searches the full text of all published pages in a space and returns matching pages with ranked excerpts. Use this to find pages by topic or keyword within a specific space. For site-wide search across all spaces in a site, use the site search endpoint instead.",
        "x-gitbook-mcp": true,
        "tags": [
          "space-content"
        ],
        "security": [
          {
            "user": []
          },
          {
            "oauth": [
              "space:read"
            ]
          }
        ],
        "parameters": [
          {
            "name": "query",
            "in": "query",
            "required": true,
            "schema": {
              "type": "string",
              "maxLength": 512
            }
          },
          {
            "$ref": "#/components/parameters/spaceId"
          },
          {
            "$ref": "#/components/parameters/listPage"
          },
          {
            "$ref": "#/components/parameters/listLimit"
          }
        ],
        "responses": {
          "200": {
            "description": "OK",
            "content": {
              "application/json": {
                "schema": {
                  "allOf": [
                    {
                      "$ref": "#/components/schemas/List"
                    },
                    {
                      "type": "object",
                      "required": [
                        "items"
                      ],
                      "properties": {
                        "items": {
                          "type": "array",
                          "items": {
                            "$ref": "#/components/schemas/SearchPageResult"
                          }
                        }
                      }
                    }
                  ]
                }
              }
            }
          }
        }
      }
    },
    "/spaces/{spaceId}/git/import": {
      "post": {
        "operationId": "importGitRepository",
        "summary": "Pull content into a space from a connected Git repository",
        "description": "Triggers an import from provided Git repository into the space, updating the space's content to match the repository (if not standalone). This is an async operation — it runs in the background after the request returns 204.",
        "x-gitbook-mcp": true,
        "tags": [
          "space-git"
        ],
        "security": [
          {
            "user": []
          },
          {
            "integration": []
          },
          {
            "integration-installation": []
          },
          {
            "oauth": [
              "space:write"
            ]
          }
        ],
        "parameters": [
          {
            "$ref": "#/components/parameters/spaceId"
          }
        ],
        "responses": {
          "204": {
            "description": "Operation to import the repository has been queued."
          }
        },
        "requestBody": {
          "required": true,
          "content": {
            "application/json": {
              "schema": {
                "$ref": "#/components/schemas/ImportGitRepository"
              }
            }
          }
        }
      }
    },
    "/spaces/{spaceId}/git/export": {
      "post": {
        "operationId": "exportToGitRepository",
        "summary": "Push space content to a connected Git repository",
        "description": "Triggers an export of the space's current content to the provided Git repository. This is an async operation — the export runs in the background after the request returns 204.",
        "x-gitbook-mcp": true,
        "tags": [
          "space-git"
        ],
        "security": [
          {
            "user": []
          },
          {
            "integration": []
          },
          {
            "integration-installation": []
          },
          {
            "oauth": [
              "space:write"
            ]
          }
        ],
        "parameters": [
          {
            "$ref": "#/components/parameters/spaceId"
          }
        ],
        "responses": {
          "204": {
            "description": "Operation to export the space has been queued."
          }
        },
        "requestBody": {
          "required": true,
          "content": {
            "application/json": {
              "schema": {
                "$ref": "#/components/schemas/ExportToGitRepository"
              }
            }
          }
        }
      }
    },
    "/spaces/{spaceId}/git/info": {
      "get": {
        "operationId": "getSpaceGitInfo",
        "summary": "Get the Git Sync configuration and status for a space",
        "description": "Returns metadata about the Git Sync provider connected to the space. Returns 404 if no Git provider is configured. Use this to check sync state before triggering an import or export.",
        "x-gitbook-mcp": true,
        "tags": [
          "space-git"
        ],
        "security": [
          {
            "user": []
          },
          {
            "oauth": [
              "space:read"
            ]
          }
        ],
        "parameters": [
          {
            "$ref": "#/components/parameters/spaceId"
          }
        ],
        "responses": {
          "200": {
            "description": "The Git Sync info for the space",
            "content": {
              "application/json": {
                "schema": {
                  "$ref": "#/components/schemas/GitSyncState"
                }
              }
            }
          },
          "404": {
            "description": "No Git provider currently set up on the space",
            "$ref": "#/components/responses/NotFoundError"
          }
        }
      }
    },
    "/spaces/{spaceId}/permissions": {
      "post": {
        "operationId": "inviteToSpace",
        "summary": "Invite a user or a team to a space",
        "tags": [
          "space-permissions"
        ],
        "security": [
          {
            "user": []
          },
          {
            "oauth": [
              "space:permissions:write"
            ]
          }
        ],
        "parameters": [
          {
            "$ref": "#/components/parameters/spaceId"
          }
        ],
        "responses": {
          "204": {
            "description": "OK"
          },
          "404": {
            "description": "No team or user with the provided Id",
            "$ref": "#/components/responses/NotFoundError"
          }
        },
        "requestBody": {
          "required": true,
          "content": {
            "application/json": {
              "schema": {
                "$ref": "#/components/schemas/InviteUsersAndTeams"
              }
            }
          }
        }
      }
    },
    "/spaces/{spaceId}/permissions/teams/{teamId}": {
      "patch": {
        "operationId": "updateTeamPermissionInSpace",
        "summary": "Update an org team's permission in a space",
        "tags": [
          "space-permissions"
        ],
        "security": [
          {
            "user": []
          },
          {
            "oauth": [
              "space:permissions:write"
            ]
          }
        ],
        "parameters": [
          {
            "$ref": "#/components/parameters/spaceId"
          },
          {
            "$ref": "#/components/parameters/teamId"
          }
        ],
        "requestBody": {
          "required": true,
          "content": {
            "application/json": {
              "schema": {
                "type": "object",
                "properties": {
                  "role": {
                    "$ref": "#/components/schemas/MemberRoleOrGuest"
                  }
                }
              }
            }
          }
        },
        "responses": {
          "204": {
            "description": "Team permission was updated"
          },
          "404": {
            "description": "No team found with the given ID",
            "$ref": "#/components/responses/NotFoundError"
          }
        }
      },
      "delete": {
        "operationId": "removeTeamFromSpace",
        "summary": "Remove an org team from a space",
        "tags": [
          "space-permissions"
        ],
        "security": [
          {
            "user": []
          },
          {
            "oauth": [
              "space:permissions:write"
            ]
          }
        ],
        "parameters": [
          {
            "$ref": "#/components/parameters/spaceId"
          },
          {
            "$ref": "#/components/parameters/teamId"
          }
        ],
        "responses": {
          "204": {
            "description": "The team was not found in the space"
          },
          "205": {
            "description": "The team has been removed from the space"
          },
          "400": {
            "description": "Team does not have access to space",
            "$ref": "#/components/responses/BadRequestError"
          }
        }
      }
    },
    "/spaces/{spaceId}/permissions/users": {
      "get": {
        "operationId": "listUserPermissionsInSpace",
        "summary": "List space user permissions",
        "tags": [
          "space-permissions"
        ],
        "security": [
          {
            "user": []
          },
          {
            "oauth": [
              "space:permissions:read"
            ]
          }
        ],
        "parameters": [
          {
            "$ref": "#/components/parameters/spaceId"
          },
          {
            "$ref": "#/components/parameters/listPage"
          },
          {
            "$ref": "#/components/parameters/listLimit"
          }
        ],
        "responses": {
          "200": {
            "description": "Listing of users who have been added to a space.",
            "content": {
              "application/json": {
                "schema": {
                  "allOf": [
                    {
                      "$ref": "#/components/schemas/List"
                    },
                    {
                      "type": "object",
                      "required": [
                        "items"
                      ],
                      "properties": {
                        "items": {
                          "type": "array",
                          "items": {
                            "$ref": "#/components/schemas/UserContentPermission"
                          }
                        }
                      }
                    }
                  ]
                }
              }
            }
          },
          "404": {
            "description": "No space was found with the given Id",
            "$ref": "#/components/responses/NotFoundError"
          }
        }
      }
    },
    "/spaces/{spaceId}/permissions/users/{userId}": {
      "patch": {
        "operationId": "updateUserPermissionInSpace",
        "summary": "Update space user permissions",
        "tags": [
          "space-permissions"
        ],
        "security": [
          {
            "user": []
          },
          {
            "oauth": [
              "space:permissions:write"
            ]
          }
        ],
        "parameters": [
          {
            "$ref": "#/components/parameters/spaceId"
          },
          {
            "$ref": "#/components/parameters/userId"
          }
        ],
        "requestBody": {
          "required": true,
          "content": {
            "application/json": {
              "schema": {
                "type": "object",
                "properties": {
                  "role": {
                    "$ref": "#/components/schemas/MemberRoleOrGuest"
                  }
                }
              }
            }
          }
        },
        "responses": {
          "204": {
            "description": "User permission was updated"
          },
          "404": {
            "description": "No user found with the given ID",
            "$ref": "#/components/responses/NotFoundError"
          }
        }
      },
      "delete": {
        "operationId": "removeUserFromSpace",
        "summary": "Remove a space user",
        "tags": [
          "space-permissions"
        ],
        "security": [
          {
            "user": []
          },
          {
            "oauth": [
              "space:permissions:write"
            ]
          }
        ],
        "parameters": [
          {
            "$ref": "#/components/parameters/spaceId"
          },
          {
            "$ref": "#/components/parameters/userId"
          }
        ],
        "responses": {
          "204": {
            "description": "The user was not found in the space"
          },
          "205": {
            "description": "The user has been removed from the space"
          }
        }
      }
    },
    "/spaces/{spaceId}/permissions/teams": {
      "get": {
        "operationId": "listTeamPermissionsInSpace",
        "summary": "List an org team's permission in a space",
        "tags": [
          "space-permissions"
        ],
        "security": [
          {
            "user": []
          },
          {
            "oauth": [
              "space:permissions:read"
            ]
          }
        ],
        "parameters": [
          {
            "$ref": "#/components/parameters/spaceId"
          },
          {
            "$ref": "#/components/parameters/listPage"
          },
          {
            "$ref": "#/components/parameters/listLimit"
          }
        ],
        "responses": {
          "200": {
            "description": "Listing of teams who have been added to a space.",
            "content": {
              "application/json": {
                "schema": {
                  "allOf": [
                    {
                      "$ref": "#/components/schemas/List"
                    },
                    {
                      "type": "object",
                      "required": [
                        "items"
                      ],
                      "properties": {
                        "items": {
                          "type": "array",
                          "items": {
                            "type": "object",
                            "description": "Permission of a team in a space.",
                            "properties": {
                              "permission": {
                                "$ref": "#/components/schemas/MemberRole"
                              },
                              "team": {
                                "$ref": "#/components/schemas/OrganizationTeam"
                              }
                            },
                            "required": [
                              "permission",
                              "team"
                            ]
                          }
                        }
                      }
                    }
                  ]
                }
              }
            }
          },
          "404": {
            "description": "No space was found with the given Id",
            "$ref": "#/components/responses/NotFoundError"
          }
        }
      }
    },
    "/spaces/{spaceId}/content": {
      "get": {
        "operationId": "getCurrentRevision",
        "summary": "Get the current published content revision of a space",
        "description": "Retrieves the live published revision of a space, which includes the full page tree structure and associated files. Use this to inspect the currently published content state of a space. For in-progress edits, use the change-request content endpoint instead.",
        "x-gitbook-mcp": true,
        "tags": [
          "space-content"
        ],
        "security": [
          {
            "user": []
          },
          {
            "integration": []
          },
          {
            "integration-installation": []
          },
          {
            "oauth": [
              "space:read"
            ]
          }
        ],
        "parameters": [
          {
            "$ref": "#/components/parameters/spaceId"
          },
          {
            "$ref": "#/components/parameters/revisionMetadata"
          },
          {
            "$ref": "#/components/parameters/revisionComputed"
          }
        ],
        "responses": {
          "200": {
            "description": "OK",
            "content": {
              "application/json": {
                "schema": {
                  "$ref": "#/components/schemas/Revision"
                }
              }
            }
          }
        }
      }
    },
    "/spaces/{spaceId}/content/template": {
      "post": {
        "operationId": "applyTemplateToSpace",
        "summary": "Apply a content template to populate a space with initial pages",
        "description": "Populates a space with pages and structure from a specified template, bootstrapping it with a standard documentation layout. Use this to initialise a new space rather than creating pages manually. Optionally apply the template to a specific change request instead of main content by providing the changeRequestId field.",
        "x-gitbook-mcp": true,
        "tags": [
          "space-content"
        ],
        "security": [
          {
            "user": []
          },
          {
            "oauth": [
              "space:write"
            ]
          }
        ],
        "parameters": [
          {
            "$ref": "#/components/parameters/spaceId"
          }
        ],
        "responses": {
          "201": {
            "description": "Template applied to space."
          }
        },
        "requestBody": {
          "required": true,
          "content": {
            "application/json": {
              "schema": {
                "allOf": [
                  {
                    "$ref": "#/components/schemas/ApplySpaceTemplate"
                  },
                  {
                    "type": "object",
                    "properties": {
                      "changeRequestId": {
                        "type": "string",
                        "description": "The ID of the change request to apply the template to. If not provided, the template is applied to the main content."
                      }
                    }
                  }
                ]
              }
            }
          }
        }
      }
    },
    "/spaces/{spaceId}/content/pages": {
      "get": {
        "operationId": "listPages",
        "summary": "List all pages in a space with their hierarchy and metadata",
        "description": "Returns the complete list of all pages in a space's current revision, including their titles, URL paths, and parent-child relationships. Use this to understand the full content structure of a space or build navigation. For the content of a single page, use getPageById or getPageByPath instead.",
        "x-gitbook-mcp": true,
        "tags": [
          "space-content"
        ],
        "security": [
          {
            "user": []
          },
          {
            "oauth": [
              "space:read"
            ]
          }
        ],
        "parameters": [
          {
            "$ref": "#/components/parameters/spaceId"
          },
          {
            "$ref": "#/components/parameters/revisionMetadata"
          },
          {
            "$ref": "#/components/parameters/revisionComputed"
          }
        ],
        "responses": {
          "200": {
            "description": "OK",
            "content": {
              "application/json": {
                "schema": {
                  "type": "object",
                  "properties": {
                    "pages": {
                      "type": "array",
                      "items": {
                        "$ref": "#/components/schemas/RevisionPage"
                      }
                    }
                  },
                  "required": [
                    "pages"
                  ]
                }
              }
            }
          }
        }
      }
    },
    "/spaces/{spaceId}/content/files": {
      "get": {
        "operationId": "listFiles",
        "summary": "List all uploaded files and assets in a space",
        "description": "Returns a paginated list of all files (images, attachments, and other assets) uploaded to a space's current revision. Use this to discover available assets or audit file usage across a space.",
        "x-gitbook-mcp": true,
        "tags": [
          "space-content"
        ],
        "security": [
          {
            "user": []
          },
          {
            "oauth": [
              "space:read"
            ]
          }
        ],
        "parameters": [
          {
            "$ref": "#/components/parameters/spaceId"
          },
          {
            "$ref": "#/components/parameters/listPage"
          },
          {
            "$ref": "#/components/parameters/listLimit"
          },
          {
            "$ref": "#/components/parameters/revisionMetadata"
          },
          {
            "$ref": "#/components/parameters/revisionComputed"
          }
        ],
        "responses": {
          "200": {
            "description": "OK",
            "content": {
              "application/json": {
                "schema": {
                  "allOf": [
                    {
                      "$ref": "#/components/schemas/List"
                    },
                    {
                      "type": "object",
                      "required": [
                        "items"
                      ],
                      "properties": {
                        "items": {
                          "type": "array",
                          "items": {
                            "$ref": "#/components/schemas/RevisionFile"
                          }
                        }
                      }
                    }
                  ]
                }
              }
            }
          }
        }
      }
    },
    "/spaces/{spaceId}/content/files/{fileId}": {
      "get": {
        "operationId": "getFileById",
        "summary": "Get a specific uploaded file from a space by its ID",
        "description": "Retrieves metadata and download URL for a single file (image, attachment, or other asset) in a space's current revision by its file ID. Use this when you have a specific file ID and need its URL, MIME type, or other metadata.",
        "x-gitbook-mcp": true,
        "tags": [
          "space-content"
        ],
        "security": [
          {
            "user": []
          },
          {
            "oauth": [
              "space:read"
            ]
          }
        ],
        "parameters": [
          {
            "$ref": "#/components/parameters/spaceId"
          },
          {
            "$ref": "#/components/parameters/fileId"
          },
          {
            "$ref": "#/components/parameters/revisionMetadata"
          },
          {
            "$ref": "#/components/parameters/revisionComputed"
          }
        ],
        "responses": {
          "200": {
            "description": "OK",
            "content": {
              "application/json": {
                "schema": {
                  "$ref": "#/components/schemas/RevisionFile"
                }
              }
            }
          }
        }
      }
    },
    "/spaces/{spaceId}/content/page/{pageId}": {
      "get": {
        "operationId": "getPageById",
        "summary": "Get a single page from a space by its ID",
        "description": "Retrieves a page's metadata, content, and document structure from a space's current revision by its page ID. Use this when you know the exact page ID and need its content or path. For lookup by URL path, use the content/path endpoint instead.",
        "x-gitbook-mcp": true,
        "tags": [
          "space-content"
        ],
        "security": [
          {
            "user": []
          },
          {
            "oauth": [
              "space:read"
            ]
          }
        ],
        "parameters": [
          {
            "$ref": "#/components/parameters/spaceId"
          },
          {
            "$ref": "#/components/parameters/pageId"
          },
          {
            "$ref": "#/components/parameters/documentFormat"
          },
          {
            "$ref": "#/components/parameters/documentMarkdownRefsFormat"
          },
          {
            "$ref": "#/components/parameters/documentEvaluated"
          },
          {
            "$ref": "#/components/parameters/documentDereferenced"
          },
          {
            "$ref": "#/components/parameters/revisionMetadata"
          },
          {
            "$ref": "#/components/parameters/revisionComputed"
          }
        ],
        "responses": {
          "200": {
            "description": "OK",
            "content": {
              "application/json": {
                "schema": {
                  "$ref": "#/components/schemas/RevisionPage"
                }
              }
            }
          }
        }
      }
    },
    "/spaces/{spaceId}/content/page/{pageId}/meta-links": {
      "get": {
        "operationId": "listSpacePageMetaLinks",
        "summary": "Get navigation metadata links for a page (previous, next, parent)",
        "description": "Returns structural navigation metadata for a page, including references to the previous page, next page, and parent page within the space's hierarchy. Use this to implement or inspect linear navigation flows in a docs site without fetching the full page tree.",
        "x-gitbook-mcp": true,
        "tags": [
          "space-content"
        ],
        "security": [
          {
            "user": []
          },
          {
            "oauth": [
              "space:read"
            ]
          }
        ],
        "parameters": [
          {
            "$ref": "#/components/parameters/spaceId"
          },
          {
            "$ref": "#/components/parameters/pageId"
          }
        ],
        "responses": {
          "200": {
            "description": "OK",
            "content": {
              "application/json": {
                "schema": {
                  "$ref": "#/components/schemas/RevisionPageMetaLinks"
                }
              }
            }
          }
        }
      }
    },
    "/spaces/{spaceId}/content/path/{pagePath}": {
      "get": {
        "operationId": "getPageByPath",
        "summary": "Get a page from a space by its URL path",
        "description": "Retrieves a page by its URL path (e.g. /guides/getting-started) from the space's current revision. Use this when you have a page's path rather than its ID. Returns either a document page or a group/section page depending on the path.",
        "x-gitbook-mcp": true,
        "tags": [
          "space-content"
        ],
        "security": [
          {
            "user": []
          },
          {
            "oauth": [
              "space:read"
            ]
          }
        ],
        "parameters": [
          {
            "$ref": "#/components/parameters/spaceId"
          },
          {
            "$ref": "#/components/parameters/pagePath"
          },
          {
            "$ref": "#/components/parameters/documentFormat"
          },
          {
            "$ref": "#/components/parameters/documentMarkdownRefsFormat"
          },
          {
            "$ref": "#/components/parameters/documentEvaluated"
          },
          {
            "$ref": "#/components/parameters/documentDereferenced"
          },
          {
            "$ref": "#/components/parameters/revisionMetadata"
          },
          {
            "$ref": "#/components/parameters/revisionComputed"
          }
        ],
        "responses": {
          "200": {
            "description": "OK",
            "content": {
              "application/json": {
                "schema": {
                  "oneOf": [
                    {
                      "$ref": "#/components/schemas/RevisionPageDocument"
                    },
                    {
                      "$ref": "#/components/schemas/RevisionPageGroup"
                    }
                  ]
                }
              }
            }
          }
        }
      }
    },
    "/spaces/{spaceId}/content/reusable-contents/{reusableContentId}": {
      "get": {
        "operationId": "getReusableContentById",
        "summary": "Get a reusable content block from a space by its ID",
        "description": "Retrieves a reusable content block (a shared snippet that can be embedded across multiple pages) from a space's current revision by its ID. Use this to read the content of a reusable block when you have its ID.",
        "x-gitbook-mcp": true,
        "tags": [
          "space-content"
        ],
        "security": [
          {
            "user": []
          },
          {
            "oauth": [
              "space:read"
            ]
          }
        ],
        "parameters": [
          {
            "$ref": "#/components/parameters/spaceId"
          },
          {
            "$ref": "#/components/parameters/reusableContentId"
          },
          {
            "$ref": "#/components/parameters/revisionMetadata"
          },
          {
            "$ref": "#/components/parameters/revisionComputed"
          }
        ],
        "responses": {
          "200": {
            "description": "OK",
            "content": {
              "application/json": {
                "schema": {
                  "$ref": "#/components/schemas/RevisionReusableContent"
                }
              }
            }
          }
        }
      }
    },
    "/spaces/{spaceId}/content/computed/document": {
      "post": {
        "operationId": "getComputedDocument",
        "summary": "Compute and render a document from a structured content source",
        "description": "Server-renders a document from a provided content source definition, evaluating template expressions and resolving variables to produce a fully computed document. Use this to preview how dynamic content will look without publishing a full revision.",
        "x-gitbook-mcp": true,
        "tags": [
          "space-content"
        ],
        "security": [
          {
            "user": []
          },
          {
            "oauth": [
              "space:read"
            ]
          }
        ],
        "parameters": [
          {
            "$ref": "#/components/parameters/spaceId"
          },
          {
            "$ref": "#/components/parameters/documentSchema"
          }
        ],
        "requestBody": {
          "required": true,
          "content": {
            "application/json": {
              "schema": {
                "type": "object",
                "properties": {
                  "source": {
                    "$ref": "#/components/schemas/ComputedContentSourceDocument"
                  },
                  "seed": {
                    "type": "string",
                    "description": "Seed to use for the generation of IDs."
                  }
                },
                "required": [
                  "source",
                  "seed"
                ]
              }
            }
          }
        },
        "responses": {
          "200": {
            "description": "Document computed",
            "content": {
              "application/json": {
                "schema": {
                  "$ref": "#/components/schemas/JSONDocument"
                }
              }
            }
          }
        }
      }
    },
    "/spaces/{spaceId}/content/computed/revision": {
      "post": {
        "operationId": "getComputedRevision",
        "summary": "Compute and render a full revision from a structured content source",
        "description": "Server-renders an entire revision — pages, files, and reusable contents — from a provided content source definition, resolving all template expressions and variables. Use this to evaluate and preview computed content before publishing. Returns the full set of pages and files with all dynamic content fully resolved.",
        "x-gitbook-mcp": true,
        "tags": [
          "space-content"
        ],
        "security": [
          {
            "user": []
          },
          {
            "oauth": [
              "space:read"
            ]
          }
        ],
        "parameters": [
          {
            "$ref": "#/components/parameters/spaceId"
          }
        ],
        "requestBody": {
          "required": true,
          "content": {
            "application/json": {
              "schema": {
                "type": "object",
                "properties": {
                  "source": {
                    "$ref": "#/components/schemas/ComputedContentSourceRevision"
                  },
                  "seed": {
                    "type": "string",
                    "description": "Seed to use for the generation of IDs."
                  }
                },
                "required": [
                  "source",
                  "seed"
                ]
              }
            }
          }
        },
        "responses": {
          "200": {
            "description": "Computed pages and files",
            "content": {
              "application/json": {
                "schema": {
                  "type": "object",
                  "properties": {
                    "pages": {
                      "type": "array",
                      "items": {
                        "$ref": "#/components/schemas/RevisionPage"
                      }
                    },
                    "files": {
                      "type": "array",
                      "items": {
                        "$ref": "#/components/schemas/RevisionFile"
                      }
                    },
                    "reusableContents": {
                      "type": "array",
                      "items": {
                        "$ref": "#/components/schemas/RevisionReusableContent"
                      }
                    }
                  },
                  "required": [
                    "pages",
                    "files",
                    "reusableContents"
                  ]
                }
              }
            }
          }
        }
      }
    },
    "/spaces/{spaceId}/documents/{documentId}": {
      "get": {
        "operationId": "getDocumentById",
        "summary": "Get a raw document from a space by its document ID",
        "description": "Returns the structured JSON document for a specific document ID within a space. Documents are the low-level block-based representation of page content. Use this when you have a documentId and need the raw block structure. To retrieve a page's document by pageId, use the page document endpoint instead.",
        "x-gitbook-mcp": true,
        "tags": [
          "space-content"
        ],
        "security": [
          {
            "user": []
          },
          {
            "oauth": [
              "space:read"
            ]
          }
        ],
        "parameters": [
          {
            "$ref": "#/components/parameters/spaceId"
          },
          {
            "name": "documentId",
            "in": "path",
            "required": true,
            "description": "ID of the document in the space",
            "schema": {
              "type": "string"
            }
          },
          {
            "$ref": "#/components/parameters/documentSchema"
          }
        ],
        "responses": {
          "200": {
            "description": "Document",
            "content": {
              "application/json": {
                "schema": {
                  "$ref": "#/components/schemas/JSONDocument"
                }
              }
            }
          }
        }
      }
    },
    "/spaces/{spaceId}/change-requests": {
      "post": {
        "operationId": "createChangeRequest",
        "summary": "Create a new change request in a space",
        "description": "Creates a new change request, which is a draft working copy of the space's content — similar to a Git branch or pull request. Use this before making content edits to avoid modifying the live published content directly. Optionally supply a subject and a template to pre-populate the change request with content. Once created, use the change-request content endpoints to read and modify pages within the draft, then merge it when ready.",
        "x-gitbook-mcp": true,
        "tags": [
          "change-requests"
        ],
        "security": [
          {
            "user": []
          },
          {
            "oauth": [
              "space:write"
            ]
          }
        ],
        "parameters": [
          {
            "$ref": "#/components/parameters/spaceId"
          }
        ],
        "responses": {
          "201": {
            "description": "Change Request Created",
            "headers": {
              "Location": {
                "description": "API URL for the newly created change request",
                "schema": {
                  "type": "string"
                }
              }
            },
            "content": {
              "application/json": {
                "schema": {
                  "$ref": "#/components/schemas/ChangeRequest"
                }
              }
            }
          }
        },
        "requestBody": {
          "required": true,
          "content": {
            "application/json": {
              "schema": {
                "type": "object",
                "properties": {
                  "subject": {
                    "type": "string",
                    "description": "Subject of the change request"
                  },
                  "template": {
                    "$ref": "#/components/schemas/ApplySpaceTemplate",
                    "description": "Template to apply to the change request"
                  }
                },
                "additionalProperties": true
              }
            }
          }
        }
      },
      "get": {
        "operationId": "listChangeRequestsForSpace",
        "summary": "List all change requests for a space",
        "description": "Returns a paginated list of change requests for the given space. Use this to discover existing change requests before creating a new one, or to find change requests assigned to a specific user for review.",
        "x-gitbook-mcp": true,
        "tags": [
          "change-requests"
        ],
        "security": [
          {
            "user": []
          },
          {
            "oauth": [
              "space:read"
            ]
          }
        ],
        "parameters": [
          {
            "$ref": "#/components/parameters/listPage"
          },
          {
            "$ref": "#/components/parameters/listLimit"
          },
          {
            "$ref": "#/components/parameters/spaceId"
          },
          {
            "name": "status",
            "in": "query",
            "required": false,
            "schema": {
              "$ref": "#/components/schemas/ChangeRequestStatus",
              "default": "open"
            },
            "description": "If defined, only change requests matching this status will be returned."
          },
          {
            "name": "creator",
            "in": "query",
            "required": false,
            "schema": {
              "type": "string"
            },
            "description": "If defined, only change requests created by this user will be returned."
          },
          {
            "name": "contributor",
            "in": "query",
            "required": false,
            "schema": {
              "type": "string"
            },
            "description": "If defined, only change requests with contributions from this user will be returned."
          },
          {
            "name": "requestedReviewer",
            "in": "query",
            "required": false,
            "schema": {
              "type": "string"
            },
            "description": "If defined, only change requests with a requested reviewer for this user will be returned."
          },
          {
            "name": "topic",
            "in": "query",
            "required": false,
            "schema": {
              "type": "string"
            },
            "description": "If defined, only change requests linked to this site topic will be returned."
          },
          {
            "name": "orderBy",
            "in": "query",
            "required": false,
            "schema": {
              "$ref": "#/components/schemas/ChangeRequestOrderBy"
            }
          }
        ],
        "responses": {
          "200": {
            "description": "List of the space's change requests",
            "content": {
              "application/json": {
                "schema": {
                  "allOf": [
                    {
                      "$ref": "#/components/schemas/List"
                    },
                    {
                      "type": "object",
                      "required": [
                        "items"
                      ],
                      "properties": {
                        "items": {
                          "type": "array",
                          "items": {
                            "$ref": "#/components/schemas/ChangeRequest"
                          }
                        }
                      }
                    }
                  ]
                }
              }
            }
          }
        }
      }
    },
    "/spaces/{spaceId}/change-requests/{changeRequestId}": {
      "get": {
        "operationId": "getChangeRequestById",
        "summary": "Get a change request by its ID",
        "description": "Retrieves the full details of a single change request, including its status, subject, description, and metadata. Use this to check the current state of a change request before deciding to merge, update, or request a review.",
        "x-gitbook-mcp": true,
        "tags": [
          "change-requests"
        ],
        "security": [
          {
            "user": []
          },
          {
            "oauth": [
              "space:read"
            ]
          }
        ],
        "parameters": [
          {
            "$ref": "#/components/parameters/spaceId"
          },
          {
            "$ref": "#/components/parameters/changeRequestId"
          }
        ],
        "responses": {
          "200": {
            "description": "The matching change request",
            "content": {
              "application/json": {
                "schema": {
                  "$ref": "#/components/schemas/ChangeRequest"
                }
              }
            }
          },
          "404": {
            "description": "The change request could not be found.",
            "$ref": "#/components/responses/NotFoundError"
          }
        }
      },
      "patch": {
        "operationId": "updateChangeRequestById",
        "summary": "Update a change request's subject, description, or status",
        "description": "Updates the metadata of a change request. Use this to rename a change request, add context before requesting a review, or change the workflow status without merging. To update page content within the change request, use the content endpoint instead.",
        "x-gitbook-mcp": true,
        "tags": [
          "change-requests"
        ],
        "security": [
          {
            "user": []
          },
          {
            "oauth": [
              "space:write"
            ]
          }
        ],
        "parameters": [
          {
            "$ref": "#/components/parameters/spaceId"
          },
          {
            "$ref": "#/components/parameters/changeRequestId"
          }
        ],
        "requestBody": {
          "required": true,
          "content": {
            "application/json": {
              "schema": {
                "type": "object",
                "properties": {
                  "subject": {
                    "$ref": "#/components/schemas/ChangeRequestSubject"
                  },
                  "description": {
                    "$ref": "#/components/schemas/JSONDocument"
                  },
                  "links": {
                    "type": "array",
                    "description": "External links associated with the change request.",
                    "items": {
                      "$ref": "#/components/schemas/ChangeRequestLinkInput"
                    },
                    "maxItems": 10
                  },
                  "status": {
                    "type": "string",
                    "enum": [
                      "draft",
                      "open",
                      "archived"
                    ]
                  }
                }
              }
            }
          }
        },
        "responses": {
          "200": {
            "description": "The change request has been updated",
            "content": {
              "application/json": {
                "schema": {
                  "$ref": "#/components/schemas/ChangeRequest"
                }
              }
            }
          }
        }
      }
    },
    "/spaces/{spaceId}/change-requests/{changeRequestId}/merge": {
      "post": {
        "operationId": "mergeChangeRequest",
        "summary": "Merge a change request into the space's live content",
        "description": "Merges the change request's draft content into the space's primary (published) content, making all changes live. If the result is \"conflicts\", the merge was still applied but the space may need manual conflict resolution. Consider running updateChangeRequest first to sync with the latest live content and reduce conflicts.",
        "x-gitbook-mcp": true,
        "tags": [
          "change-requests"
        ],
        "security": [
          {
            "user": []
          },
          {
            "oauth": [
              "change-request:merge"
            ]
          }
        ],
        "parameters": [
          {
            "$ref": "#/components/parameters/spaceId"
          },
          {
            "$ref": "#/components/parameters/changeRequestId"
          }
        ],
        "responses": {
          "200": {
            "description": "OK",
            "content": {
              "application/json": {
                "schema": {
                  "type": "object",
                  "properties": {
                    "revision": {
                      "type": "string",
                      "description": "ID of the resulting revision"
                    },
                    "result": {
                      "type": "string",
                      "enum": [
                        "merge",
                        "conflicts"
                      ]
                    }
                  },
                  "required": [
                    "revision",
                    "result"
                  ]
                }
              }
            }
          }
        }
      }
    },
    "/spaces/{spaceId}/change-requests/{changeRequestId}/update": {
      "post": {
        "operationId": "updateChangeRequest",
        "summary": "Sync a change request with the latest live space content",
        "description": "Rebases the change request onto the latest primary revision of the space, pulling in any changes that were merged to the live space since this change request was created. Run this before merging to minimise conflicts, especially if the change request has been open for a while.",
        "x-gitbook-mcp": true,
        "tags": [
          "change-requests"
        ],
        "security": [
          {
            "user": []
          },
          {
            "oauth": [
              "space:write"
            ]
          }
        ],
        "parameters": [
          {
            "$ref": "#/components/parameters/spaceId"
          },
          {
            "$ref": "#/components/parameters/changeRequestId"
          }
        ],
        "responses": {
          "200": {
            "description": "OK",
            "content": {
              "application/json": {
                "schema": {
                  "type": "object",
                  "properties": {
                    "revision": {
                      "type": "string",
                      "description": "ID of the resulting revision"
                    },
                    "result": {
                      "type": "string",
                      "enum": [
                        "update",
                        "conflicts"
                      ]
                    }
                  },
                  "required": [
                    "revision",
                    "result"
                  ]
                }
              }
            }
          }
        }
      }
    },
    "/spaces/{spaceId}/change-requests/{changeRequestId}/reviews": {
      "get": {
        "operationId": "getReviewsByChangeRequestId",
        "summary": "List all formal reviews submitted for a change request",
        "description": "Returns a paginated list of reviews submitted for the change request. Use this to check the current review status and whether all requested reviewers have responded before merging.",
        "x-gitbook-mcp": true,
        "tags": [
          "change-requests-reviews"
        ],
        "security": [
          {
            "user": []
          },
          {
            "oauth": [
              "space:read"
            ]
          }
        ],
        "parameters": [
          {
            "$ref": "#/components/parameters/spaceId"
          },
          {
            "$ref": "#/components/parameters/changeRequestId"
          },
          {
            "$ref": "#/components/parameters/documentFormat"
          },
          {
            "in": "query",
            "name": "outdated",
            "description": "Filter reviews marked as outdated.",
            "schema": {
              "type": "boolean"
            }
          },
          {
            "$ref": "#/components/parameters/listPage"
          },
          {
            "$ref": "#/components/parameters/listLimit"
          }
        ],
        "responses": {
          "200": {
            "description": "All reviews for the given change request.",
            "content": {
              "application/json": {
                "schema": {
                  "allOf": [
                    {
                      "$ref": "#/components/schemas/List"
                    },
                    {
                      "type": "object",
                      "required": [
                        "items"
                      ],
                      "properties": {
                        "items": {
                          "type": "array",
                          "items": {
                            "$ref": "#/components/schemas/ChangeRequestReview"
                          }
                        }
                      }
                    }
                  ]
                }
              }
            }
          },
          "404": {
            "description": "The change request or space could not be found.",
            "$ref": "#/components/responses/NotFoundError"
          }
        }
      },
      "post": {
        "operationId": "submitChangeRequestReview",
        "summary": "Submit an approve or request-changes review for a change request",
        "description": "Submits a formal review decision (approved or changes-requested) on the change request, optionally with a rich-text comment. Use this to complete a review you were requested to perform. Only users who are requested reviewers or have space review permissions can submit a review.",
        "x-gitbook-mcp": true,
        "tags": [
          "change-requests-reviews"
        ],
        "security": [
          {
            "user": []
          },
          {
            "oauth": [
              "space:write"
            ]
          }
        ],
        "parameters": [
          {
            "$ref": "#/components/parameters/spaceId"
          },
          {
            "$ref": "#/components/parameters/changeRequestId"
          }
        ],
        "responses": {
          "201": {
            "headers": {
              "Location": {
                "description": "API URL for the newly created review",
                "schema": {
                  "type": "string"
                }
              }
            },
            "description": "A new review has been created.",
            "content": {
              "application/json": {
                "schema": {
                  "$ref": "#/components/schemas/ChangeRequestReview"
                }
              }
            }
          }
        },
        "requestBody": {
          "required": true,
          "content": {
            "application/json": {
              "schema": {
                "type": "object",
                "properties": {
                  "status": {
                    "description": "The status of the submitted review.",
                    "$ref": "#/components/schemas/ChangeRequestReviewStatus"
                  },
                  "comment": {
                    "description": "Optionally, provide a comment along with the review.",
                    "$ref": "#/components/schemas/Document"
                  }
                },
                "required": [
                  "status"
                ]
              }
            }
          }
        }
      }
    },
    "/spaces/{spaceId}/change-requests/{changeRequestId}/reviews/{reviewId}": {
      "get": {
        "operationId": "getChangeRequestReviewById",
        "summary": "Get a specific review on a change request by its ID",
        "description": "Retrieves the full details of a single review submission on a change request, including the decision status (approved/changes-requested), reviewer, and any attached comment. Use this when you have a review ID and need its full details.",
        "x-gitbook-mcp": true,
        "tags": [
          "change-requests-reviews"
        ],
        "security": [
          {
            "user": []
          },
          {
            "oauth": [
              "space:read"
            ]
          }
        ],
        "parameters": [
          {
            "$ref": "#/components/parameters/spaceId"
          },
          {
            "$ref": "#/components/parameters/changeRequestId"
          },
          {
            "$ref": "#/components/parameters/reviewId"
          },
          {
            "$ref": "#/components/parameters/documentFormat"
          }
        ],
        "responses": {
          "200": {
            "description": "The matching change request review.",
            "content": {
              "application/json": {
                "schema": {
                  "$ref": "#/components/schemas/ChangeRequestReview"
                }
              }
            }
          },
          "404": {
            "description": "The change request review could not be found.",
            "$ref": "#/components/responses/NotFoundError"
 …
title: Understanding GitHub Code Search syntax
shortTitle: Code search syntax
intro: 'You can build search queries for the results you want with specialized code qualifiers, regular expressions, and boolean operations.'
allowTitleToDifferFromFilename: true
versions:
  feature: code-search-upgrade
category:
  - Search for code
---

## About code search query structure

The search syntax in this article only applies to searching code with {% data variables.product.prodname_dotcom %} code search. {% data reusables.search.non-code-search-explanation %}

Search queries consist of search terms, comprising text you want to search for, and qualifiers, which narrow down the search.

A bare term with no qualifiers will match either the content of a file or the file's path.

For example, the following query:

```text
http-push
```

The above query will match the file `docs/http-push.txt`, even if it doesn't contain the term `http-push`. It will also match a file called `example.txt` if it contains the term `http-push`.

You can enter multiple terms separated by whitespace to search for documents that satisfy both terms.

For example, the following query:

```text
sparse index
```

The search results would include all documents containing both the terms `sparse` and `index`, in any order. As examples, it would match a file containing `SparseIndexVector`, a file with the phrase `index for sparse trees`, and even a file named `index.txt` that contains the term `sparse`.

Searching for multiple terms separated by whitespace is the equivalent to the search `hello AND world`. Other boolean operations, such as `hello OR world`, are also supported. For more information about boolean operations, see [Using boolean operations](#using-boolean-operations).

Code search also supports searching for an exact string, including whitespace. For more information, see [Query for an exact match](#query-for-an-exact-match).

You can narrow your code search with specialized qualifiers, such as `repo:`, `language:` and `path:`. For more information on the qualifiers you can use in code search, see [Using qualifiers](#using-qualifiers).

You can also use regular expressions in your searches by surrounding the expression in slashes. For more information on using regular expressions, see [Using regular expressions](#using-regular-expressions).

## Query for an exact match

To search for an exact string, including whitespace, you can surround the string in quotes. For example:

```text
"sparse index"
```

You can also use quoted strings in qualifiers, for example:

```text
path:git language:"protocol buffers"
```

## Searching for quotes and backslashes

To search for code containing a quotation mark, you can escape the quotation mark using a backslash. For example, to find the exact string `name = "tensorflow"`, you can search:

```text
"name = \"tensorflow\""
```

To search for code containing a backslash, `\`, use a double backslash, `\\`.

The two escape sequences `\\` and `\"` can be used outside of quotes as well. No other escape sequences are recognized, though. A backslash that isn't followed by either `"` or `\` is included in the search, unchanged.

Additional escape sequences, such as `\n` to match a newline character, are supported in regular expressions. See [Using regular expressions](#using-regular-expressions).

## Using boolean operations

Code search supports boolean expressions. You can use the operators `AND`, `OR`, and `NOT` to combine search terms.

By default, adjacent terms separated by whitespace are equivalent to using the `AND` operator. For example, the search query `sparse index` is the same as `sparse AND index`, meaning that the search results will include all documents containing both the terms `sparse` and `index`, in any order.

To search for documents containing either one term or the other, you can use the `OR` operator. For example, the following query will match documents containing either `sparse` or `index`:

```text
sparse OR index
```

To exclude files from your search results, you can use the `NOT` operator. For example, to exclude files in the `__testing__` directory, you can search:

```text
"fatal error" NOT path:__testing__
```

You can use parentheses to express more complicated boolean expressions. For example:

```text
(language:ruby OR language:python) AND NOT path:"/tests/"
```

## Using qualifiers

You can use specialized keywords to qualify your search.
* [Repository qualifier](#repository-qualifier)
* [Organization and user qualifiers](#organization-and-user-qualifiers)
* [Enterprise qualifier](#enterprise-qualifier)
* [Language qualifier](#language-qualifier)
* [License qualifier](#license-qualifier)
* [Path qualifier](#path-qualifier)
* [Symbol qualifier](#symbol-qualifier)
* [Content qualifier](#content-qualifier)
* [Is qualifier](#is-qualifier)

### Repository qualifier

To search within a repository, use the `repo:` qualifier. You must provide the full repository name, including the owner. For example:

```text
repo:github-linguist/linguist
```

To search within a set of repositories, you can combine multiple `repo:` qualifiers with the boolean operator `OR`. For example:

```text
repo:github-linguist/linguist OR repo:tree-sitter/tree-sitter
```

> [!NOTE]
> Code search does not currently support regular expressions or partial matching for repository names, so you will have to type the entire repository name (including the user prefix) for the `repo:` qualifier to work.

### Organization and user qualifiers

To search for files within an organization, use the `org:` qualifier. For example:

```text
org:github
```

To search for files within a personal account, use the `user:` qualifier. For example:

```text
user:octocat
```

> [!NOTE]
> Code search does not currently support regular expressions or partial matching for organization or user names, so you will have to type the entire organization or user name for the qualifier to work.

### Enterprise qualifier

To search for files within an enterprise, use the `enterprise:` qualifier. For example:

```text
enterprise:octocorp
```

This searches repositories owned by organizations in the `octocorp` enterprise. User-owned repositories are not included.

### Language qualifier

To narrow down to a specific language, use the `language:` qualifier. For example:

```text
language:ruby OR language:cpp OR language:csharp
```

For a complete list of supported language names, see [languages.yaml](https://github.com/github-linguist/linguist/blob/main/lib/linguist/languages.yml) in [github-linguist/linguist](https://github.com/github-linguist/linguist). If your preferred language is not on the list, you can open a pull request to add it.

### License qualifier

To filter repositories based on their license or license family, use the `license:` qualifier and the exact license keyword, for example `Apache-2.0`, `CC`, `MIT`.

```text
license:MIT
```

See [AUTOTITLE](/repositories/managing-your-repositorys-settings-and-features/customizing-your-repository/licensing-a-repository#searching-github-by-license-type) for a list of license keywords.

### Path qualifier

To search within file paths, use the `path:` qualifier. This will match files containing the term anywhere in their file path. For example, to find files containing the term `unit_tests` in their path, use:

```text
path:unit_tests
```

The above query will match both `src/unit_tests/my_test.py` and `src/docs/unit_tests.md` since they both contain `unit_test` somewhere in their path.

To match only a specific filename (and not part of the path), you could use a regular expression:

```text
path:/(^|\/)README\.md$/
```

Note that the `.` in the filename is escaped, since `.` has special meaning for regular expressions. For more information about using regular expressions, see [Using regular expressions](#using-regular-expressions).

<br>

You can also use some limited glob expressions in the `path:` qualifier.

For example, to search for files with the extension `txt`, you can use:

```text
path:*.txt
```

<br>
To search for JavaScript files within a `src` directory, you could use:

```text
path:src/*.js
```

* By default, glob expressions are not anchored to the start of the path, so the above expression would still match a path like `app/src/main.js`. But if you prefix the expression with `/`, it will anchor to the start. For example:

    ```text
    path:/src/*.js
    ```

* Note that `*` doesn't match the `/` character, so for the above example, all results will be direct descendants of the `src` directory. To match within subdirectories, so that results include deeply nested files such as `/src/app/testing/utils/example.js`, you can use `**`. For example:

    ```text
    path:/src/**/*.js
    ```

<br>

You can also use the `?` global character. For example, to match the path `file.aac` or `file.abc`, you can use:

```text
path:*.a?c
```

<br>
To search for a filename which contains a special character like `*` or `?`, just use a quoted string:

```text
path:"file?"
```

Glob expressions are disabled for quoted strings, so the above query will only match paths containing the literal string `file?`.

### Symbol qualifier

You can search for symbol definitions in code, such as function or class definitions, using the `symbol:` qualifier. Symbol search is based on parsing your code using the open source [Tree-sitter](https://github.com/tree-sitter) parser ecosystem, so no extra setup or build tool integration is required.

For example, to search for a symbol called `WithContext`:

```text
language:go symbol:WithContext
```

In some languages, you can search for symbols using a prefix (e.g. a prefix of their class name). For example, for a method `deleteRows` on a struct `Maint`, you could search `symbol:Maint.deleteRows` if you are using Go, or `symbol:Maint::deleteRows` in Rust.

You can also use regular expressions with the symbol qualifier. For example, the following query would find conversions people have implemented in Rust for the `String` type:

```text
language:rust symbol:/^String::to_.*/
```

Note that this qualifier only searches for definitions and not references, and not all symbol types or languages are fully supported yet. Symbol extraction is supported for the following languages:

{% data reusables.search.code-nav-supported-languages %}

We are working on adding support for more languages. If you would like to help contribute to this effort, you can add support for your language in the open source [Tree-sitter](https://github.com/tree-sitter) parser ecosystem, upon which symbol search is based.

### Content qualifier

By default, bare terms search both paths and file content. To restrict a search to strictly match the content of a file and not file paths, use the `content:` qualifier. For example:

```text
content:README.md
```

This query would only match files containing the term `README.md`, rather than matching files named `README.md`.

### Is qualifier

To filter based on repository properties, you can use the `is:` qualifier. `is:` supports the following values:

* `archived`: restricts the search to archived repositories.
* `fork`: restricts the search to forked repositories.
* `vendored`: restricts the search to content detected as vendored.
* `generated`: restricts the search to content detected as generated.

For example:

```text
path:/^MIT.txt$/ is:archived
```

Note that the `is:` qualifier can be inverted with the `NOT` operator. To search for non-archived repositories, you can search:

```text
log4j NOT is:archived
```

To exclude forks from your results, you can search:

```text
log4j NOT is:fork
```

## Using regular expressions

Code search supports regular expressions to search for patterns in your code. You can use regular expressions in bare search terms as well as within many qualifiers, by surrounding the regex in slashes.

For example, to search for the regular expression `sparse.*index`, you would use:

```text
/sparse.*index/
```

Note that you'll have to escape any forward slashes within the regular expression. For example, to search for files within the `App/src` directory, you would use:

```text
/^App\/src\//
```

Inside a regular expression, `\n` stands for a newline character, `\t` stands for a tab, and `\x{hhhh}` can be used to escape any Unicode character. This means you can use regular expressions to search for exact strings that contain characters that you can't type into the search bar.

Most common regular expressions features work in code search. However, "look-around" assertions are not supported.

## Separating search terms

All parts of a search, such as search terms, exact strings, regular expressions, qualifiers, parentheses, and the boolean keywords `AND`, `OR`, and `NOT`, must be separated from one another with spaces. The one exception is that items inside parentheses, `(` `)`, don't need to be separated from the parentheses.

If your search contains multiple components that aren't separated by spaces, or other text that does not follow the rules listed above, code search will try to guess what you mean. It often falls back on treating that component of your query as the exact text to search for. For example, the following query:

```text
printf("hello world\n");
```

Code search will give up on interpreting the parentheses and quotes as special characters and will instead search for files containing that exact code.

If code search guesses wrong, you can always get the search you wanted by using quotes and spaces to make the meaning clear.

## Case sensitivity

By default, code search is case-insensitive, and results will include both uppercase and lowercase results. You can do case-sensitive searches by using a regular expression with case insensitivity turned off. For example, to search for the string "True", you would use:

```text
/(?-i)True/
```
