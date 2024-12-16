---
title: Setting up and managing your GitHub profile
intro: You can customize your GitHub profile and manage your contribution graph.
shortTitle: Profiles
redirect_from:---
title: About searching on GitHub
intro: 'Our integrated search covers the many repositories, users, and lines of code on {% data variables.product.product_name %}.'
redirect_from:
  - /articles/using-the-command-bar
  - /articles/github-search-basics
  - /articles/search-basics
  - /articles/searching-github
  - /articles/advanced-search
  - /articles/about-searching-on-github
  - /github/searching-for-information-on-github/about-searching-on-github
  - /github/searching-for-information-on-github/getting-started-with-searching-on-github/about-searching-on-github
versions:
  fpt: '*'
  ghes: '*'
  ghec: '*'
topics:
  - GitHub search
---

## About searching on {% data variables.product.prodname_dotcom %}

{% data reusables.search.you-can-search-globally %}

* To search globally across all of {% data variables.product.product_name %}, type what you're looking for into the search field at the top of any page, and choose "Search all of {% data variables.product.prodname_dotcom %}"{% ifversion fpt or ghec or ghes < 3.12 %} in the search dropdown menu{% endif %}.
* To search within a particular repository or organization, navigate to the repository or organization page, type what you're looking for into the search field at the top of the page, and press **Enter**.

  {% ifversion code-search-upgrade %}You can also use suggestions and completions in the search bar to quickly find what you need.

* If you click on the search bar in the top navigation of GitHub.com, you will see a list of suggestions organized by category, including recent searches and suggested repositories, teams, and projects that you have access to.
* Clicking on any of the specific suggestions will take you directly to the page for that suggestion (for example, the repository or project page). If you click on a recent search, depending on the type of search, the search term will appear in the search bar or you will be taken to the search results page for the search term.
* Once you start typing, you will see a list of completions and suggestions that match your query. You can click on a suggestion to jump to a specific location. As you continue to type, you will see more specific suggestions, such as code files you can jump to directly.

After typing a search query, you can press **Enter** to go to the full search results view, where you can see each match and a visual interface for applying filters. For more information, see [Searching using a visual interface](#searching-using-a-visual-interface).
{% endif %}

> [!NOTE]
> * {% data reusables.search.required_login %}
> * {% data variables.product.prodname_pages %} sites are not searchable on {% data variables.product.product_name %}. However you can search the source content if it exists in the default branch of a repository, using code search. For more information, see "[AUTOTITLE]{% ifversion code-search-upgrade %}(/search-github/github-code-search/understanding-github-code-search-syntax){% else %}(/search-github/searching-on-github/searching-code){% endif %}." For more information about {% data variables.product.prodname_pages %}, see [AUTOTITLE](/pages/getting-started-with-github-pages/about-github-pages)
> * Currently our search doesn't support exact matching.{% ifversion ghes %}
> * Whenever you are searching in code files, only the first two results in each file will be returned.{% endif %}

After running a search on {% data variables.product.product_name %}, you can sort the results, or further refine them by clicking one of the languages in the sidebar. For more information, see [AUTOTITLE](/search-github/getting-started-with-searching-on-github/sorting-search-results).

{% data variables.product.product_name %} search uses an ElasticSearch cluster to index projects every time a change is pushed to {% data variables.product.product_name %}. Issues and pull requests are indexed when they are created or modified.

## Types of searches on {% data variables.product.prodname_dotcom %}

You can search for the following information across all repositories you can access on {% data variables.product.prodname_dotcom %}.

* [Repositories](/search-github/searching-on-github/searching-for-repositories)
* [Topics](/search-github/searching-on-github/searching-topics)
* [Issues and pull requests](/search-github/searching-on-github/searching-issues-and-pull-requests){% ifversion fpt or ghec %}
* [Discussions](/search-github/searching-on-github/searching-discussions){% endif %}
* {% ifversion code-search-upgrade %}[Code](/search-github/github-code-search/understanding-github-code-search-syntax){% else %}[Code](/search-github/searching-on-github/searching-code){% endif %}
* [Commits](/search-github/searching-on-github/searching-commits)
* [Users](/search-github/searching-on-github/searching-users)
* [Packages](/search-github/searching-on-github/searching-for-packages)
* [Wikis](/search-github/searching-on-github/searching-wikis)

## Searching using a visual interface

In addition to the search bar, you can search {% data variables.product.product_name %} using the {% data variables.search.search_page_url %} or {% data variables.search.advanced_url %}. {% ifversion command-palette %}Alternatively, you can use the interactive search in the {% data variables.product.prodname_command_palette %} to search your current location in the UI, a specific user, repository or organization, and globally across all of {% data variables.product.product_name %}, without leaving the keyboard. For more information, see [AUTOTITLE](/get-started/accessibility/github-command-palette).{% endif %}

The {% data variables.search.advanced_url %} provides a visual interface for constructing search queries. You can filter your searches by a variety of factors, such as the number of stars or number of forks a repository has. As you fill in the advanced search fields, your query will automatically be constructed in the top search bar.

![Advanced Search page. Top search bar holds "kittens user:octocat" query. Under "Advanced options", "From these owners" text box holds term "octocat".](/assets/images/help/search/advanced-search.png)

## Searching repositories on {% data variables.product.prodname_dotcom_the_website %} from your private enterprise environment

{% ifversion fpt or ghec %}

If you use both {% data variables.product.prodname_dotcom_the_website %} and {% data variables.product.prodname_ghe_server %}, and an enterprise owner has enabled {% data variables.enterprise.prodname_unified_search %}, you can search across both environments at the same time from {% data variables.product.prodname_ghe_server %}. For more information, see [AUTOTITLE](/enterprise-server@latest/search-github/getting-started-with-searching-on-github/about-searching-on-github#searching-repositories-on-githubcom-from-your-private-enterprise-environment) in the {% data variables.product.prodname_ghe_server %} documentation.

{% else %}

If you use both {% data variables.product.prodname_dotcom_the_website %} and {% data variables.product.product_name %}, and an enterprise owner has enabled {% data variables.enterprise.prodname_unified_search %}, you can search across both environments at the same time from {% data variables.product.product_name %}. For more information about how enterprise owners can enable {% data variables.enterprise.prodname_unified_search %}, see [AUTOTITLE](/admin/configuration/configuring-github-connect/enabling-unified-search-for-your-enterprise).

Your enterprise owner on {% data variables.product.product_name %} can separately enable {% data variables.enterprise.prodname_unified_search %} for all public repositories on {% data variables.product.prodname_dotcom_the_website %} and for private repositories owned by the organization or enterprise on {% data variables.product.prodname_dotcom_the_website %} that is connected to {% data variables.product.product_name %} through {% data variables.product.prodname_github_connect %}.

Before you can use {% data variables.enterprise.prodname_unified_search %} for private repositories, you must connect your personal accounts on {% data variables.product.prodname_dotcom_the_website %} and {% data variables.product.product_name %}. For more information, see [AUTOTITLE](/search-github/getting-started-with-searching-on-github/enabling-githubcom-repository-search-from-your-private-enterprise-environment).

When you search from {% data variables.product.product_name %}, only private repositories that you have access to and that are owned by the connected organization or enterprise account will be included in search results. Neither you nor anyone else will be able to search private repositories owned by your personal account on {% data variables.product.prodname_dotcom_the_website %} from {% data variables.product.product_name %}.

To limit your search to one environment, you can use a filter option on the {% data variables.search.advanced_url %} or you can use the `environment:` search prefix. To only search for content on {% data variables.product.product_name %}, use the search syntax `environment:local`. To only search for content on {% data variables.product.prodname_dotcom_the_website %}, use `environment:github`.
{% endif %}

## Further reading

* [AUTOTITLE](/search-github/getting-started-with-searching-on-github/understanding-the-search-syntax)
* [AUTOTITLE](/search-github/searching-on-github)
  - /categories/setting-up-and-managing-your-github-profile
  - /github/setting-up-and-managing-your-github-profile
versions:
  fpt: '*'
  ghes: '*'
  ghec: '*'
topics:
  - Profiles
children:
  - /customizing-your-profile
  - /managing-contribution-settings-on-your-profile
---

---
title: About billing for GitHub Actions
intro: 'If you want to use {% data variables.product.prodname_actions %} beyond the storage or minutes included in your account, you will be billed for additional usage.'
redirect_from:
  - /github/setting-up-and-managing-billing-and-payments-on-github/about-billing-for-github-actions
  - /github/setting-up-and-managing-billing-and-payments-on-github/managing-billing-for-github-actions/about-billing-for-github-actions
  - /billing/managing-billing-for-github-actions/about-billing-for-github-actions
versions:
  fpt: '*'
  ghec: '*'
type: overview
topics:
  - Actions
  - Spending limits
shortTitle: Billing for GitHub Actions
---

{% data reusables.billing.enhanced-billing-platform %}

## About billing for {% data variables.product.prodname_actions %}

{% ifversion billing-auth-and-capture %}

{% data reusables.billing.authorization-charge %}

{% endif %}

{% data reusables.actions.actions-billing %}

{% data reusables.actions.actions-spending-limit-brief %} For more information, see [About spending limits](#about-spending-limits).

If you are an organization owner{% ifversion ghec %} or enterprise owner{% endif %}, you can connect an Azure Subscription ID to your organization {% ifversion ghec %}or enterprise{% endif %} account to enable and pay for {% data variables.product.prodname_actions %} usage beyond the amounts included with your account. For more information, see [AUTOTITLE](/billing/managing-the-plan-for-your-github-account/connecting-an-azure-subscription).

Minutes reset every month, while storage usage does not.

### Included storage and minutes

> [!NOTE]
> * Included minutes cannot be used for larger runners. These runners will always be charged for, including in public repositories. For more information, see [AUTOTITLE](/billing/managing-billing-for-github-actions/about-billing-for-github-actions#per-minute-rates).
> * Logs and job summaries do not count towards storage usage.

|Plan | Storage | Minutes (per month)|
|------- | ------- | ---------|
| {% data variables.product.prodname_free_user %} | 500 MB | 2,000 |
| {% data variables.product.prodname_pro %} | 1 GB | 3,000 |
| {% data variables.product.prodname_free_team %} for organizations | 500 MB | 2,000 |
| {% data variables.product.prodname_team %} | 2 GB | 3,000 |
| {% data variables.product.prodname_ghe_cloud %} | 50 GB | 50,000 |

The storage used by a repository is the total storage used by {% data variables.product.prodname_actions %} artifacts and {% data variables.product.prodname_registry %}. Your storage cost is the total usage for all repositories owned by your account. For more information about pricing for {% data variables.product.prodname_registry %}, see [AUTOTITLE](/billing/managing-billing-for-github-packages/about-billing-for-github-packages).

If your account's usage surpasses these limits and you have set a spending limit above $0 USD, you will pay $0.008 USD per GB of storage per day and per-minute usage depending on the operating system used by the {% data variables.product.prodname_dotcom %}-hosted runner. {% data variables.product.prodname_dotcom %} rounds the minutes and partial minutes each job uses up to the nearest whole minute.

### Minute multipliers

Jobs that run on Windows and macOS runners that {% data variables.product.prodname_dotcom %} hosts consume minutes at 2 and 10 times the rate that jobs on Linux runners consume. For example, using 1,000 Windows minutes would consume 2,000 of the minutes included in your account. Using 1,000 macOS minutes, would consume 10,000 minutes included in your account.

| Operating system | Minute multiplier |
|----------------- | ------------------|
| Linux            | 1                 |
| Windows          | 2                 |
| macOS            | 10                |

> [!NOTE]
> Minute multipliers do not apply to the per-minute rates shown below.

### Per-minute rates

#### Per-minute rates for standard runners

| Operating system                      | Per-minute rate (USD) |
|---------------------------------------| ----------------------|
|  Linux 2-core                         |   $0.008              |
|  Windows 2-core                       |   $0.016              |
|  macOS 3-core or 4-core (M1 or Intel) |   $0.08               |

#### Per-minute rates for x64-powered {% data variables.actions.hosted_runners %}

| Operating system       | Per-minute rate (USD) |
|------------------------| ----------------------|
|  Linux Advanced 2-core |   $0.008   |
|  Linux 4-core          |   $0.016   |
|  Linux 8-core          |   $0.032   |
|  Linux 16-core         |   $0.064   |
|  Linux 32-core         |   $0.128   |
|  Linux 64-core         |   $0.256   |
|  Windows 4-core        |   $0.032   |
|  Windows 8-core        |   $0.064   |
|  Windows 16-core       |   $0.128   |
|  Windows 32-core       |   $0.256   |
|  Windows 64-core       |   $0.512   |
|  Windows 4-core GPU    |   $0.14    |
|  macOS 12-core         |   $0.12    |

#### Per-minute rates for arm64-powered {% data variables.actions.hosted_runners %}

| Operating system    | Per-minute rate (USD) |
|---------------------| -----------|
|  Linux 2-core       |   $0.005   |
|  Linux 4-core       |   $0.01    |
|  Linux 8-core       |   $0.02    |
|  Linux 16-core      |   $0.04    |
|  Linux 32-core      |   $0.08    |
|  Linux 64-core      |   $0.16    |
|  Windows 2-core     |   $0.01    |
|  Windows 4-core     |   $0.02    |
|  Windows 8-core     |   $0.04    |
|  Windows 16-core    |   $0.08    |
|  Windows 32-core    |   $0.16    |
|  Windows 64-core    |   $0.32    |
|  macOS 6-core (M1)  |   $0.16    |

#### Per-minute rates for GPU-powered {% data variables.actions.hosted_runners %}

| Operating system    | Per-minute rate (USD) |
|---------------------| -----------|
|  Linux 4-core       |   $0.07    |
|  Windows 4-core     |   $0.14    |

#### Points to note about rates for runners

* The number of jobs you can run concurrently across all repositories in your user or organization account depends on your {% data variables.product.prodname_dotcom %} plan. For more information, see [AUTOTITLE](/actions/learn-github-actions/usage-limits-billing-and-administration) for {% data variables.product.prodname_dotcom %}-hosted runners and [AUTOTITLE](/actions/hosting-your-own-runners/managing-self-hosted-runners/about-self-hosted-runners#usage-limits) for self-hosted runner usage limits.
* {% data reusables.user-settings.context_switcher %}
* {% data reusables.actions.larger-runner-permissions %}
* {% data reusables.actions.about-larger-runners-billing %}
* For {% data variables.actions.hosted_runner %}s, there is no additional cost for configurations that assign public static IP addresses to a {% data variables.actions.hosted_runner %}. For more information on {% data variables.actions.hosted_runner %}s, see [AUTOTITLE](/actions/using-github-hosted-runners/using-larger-runners/about-larger-runners).
* Included minutes cannot be used for {% data variables.actions.hosted_runner %}s.
* The {% data variables.actions.hosted_runner %}s are not free for public repositories.

## Calculating minute and storage spending

{% data reusables.dotcom_billing.pricing_calculator.pricing_cal_actions %}

At the end of the month, {% data variables.product.prodname_dotcom %} calculates the cost of minutes and storage used over the amount included in your account.

### Sample minutes cost calculation

For example, if your organization uses {% data variables.product.prodname_team %} and allows unlimited spending, using 5,000 minutes could have a total storage and minute overage cost of $56 USD, depending on the operating systems used to run jobs.

* 5,000 (3,000 Linux and 2,000 Windows) minutes = $56 USD ($24 USD + $32 USD).
  * 3,000 Linux minutes at $0.008 USD per minute = $24 USD.
  * 2,000 Windows minutes at $0.016 USD per minute = $32 USD.

{% data variables.product.prodname_dotcom %} calculates your storage usage for each month based on hourly usage during that month.

### Sample storage cost calculation

> [!NOTE]
> {% data variables.product.company_short %} updates your storage space within a 6 to 12-hour window. If you delete artifacts, the available space will be reflected in your account during the next scheduled update.

For example, if you use 3 GB of storage for 10 days of March and 12 GB for 21 days of March, your storage usage would be:

* 3 GB x 10 days x (24 hours per day) = 720 GB-Hours
* 12 GB x 21 days x (24 hours per day) = 6,048 GB-Hours
* 720 GB-Hours + 6,048 GB-Hours = 6,768 GB-Hours
* 6,768 GB-Hours / (744 hours per month) = 9.0967 GB-Months

At the end of the month, {% data variables.product.prodname_dotcom %} rounds your storage to the nearest MB. Therefore, your storage usage for March would be 9.097 GB.

Your {% data variables.product.prodname_actions %} usage shares your account's existing billing date, payment method, and receipt. {% data reusables.dotcom_billing.view-all-subscriptions %}

## About spending limits

{% data reusables.actions.actions-spending-limit-detailed %}

For information on managing and changing your account's spending limit, see [AUTOTITLE](/billing/managing-billing-for-github-actions/managing-your-spending-limit-for-github-actions).

{% data reusables.dotcom_billing.actions-packages-unpaid-account %}