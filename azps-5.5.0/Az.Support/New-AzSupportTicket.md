---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Support.dll-Help.xml
Module Name: Az.Support
online version: https://docs.microsoft.com/en-us/powershell/module/az.support/new-azsupportticket
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Support/Support/help/New-AzSupportTicket.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Support/Support/help/New-AzSupportTicket.md
ms.openlocfilehash: 31e529ce30be608c5bd3167044b82f8094c1d248
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100182820"
---
# <span data-ttu-id="87833-101">New-AzSupportTicket</span><span class="sxs-lookup"><span data-stu-id="87833-101">New-AzSupportTicket</span></span>

## <span data-ttu-id="87833-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="87833-102">SYNOPSIS</span></span>
<span data-ttu-id="87833-103">지원 티켓을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="87833-103">Creates a support ticket.</span></span>

## <span data-ttu-id="87833-104">구문</span><span class="sxs-lookup"><span data-stu-id="87833-104">SYNTAX</span></span>

### <span data-ttu-id="87833-105">CreateSupportTicketWithContactDetailParameterSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="87833-105">CreateSupportTicketWithContactDetailParameterSet (Default)</span></span>
```
New-AzSupportTicket -Name <String> -Title <String> -Description <String> -ProblemClassificationId <String>
 -Severity <Severity> -CustomerFirstName <String> -CustomerLastName <String>
 -PreferredContactMethod <ContactMethod> -CustomerPrimaryEmailAddress <String>
 [-AdditionalEmailAddress <String[]>] [-CustomerPhoneNumber <String>] -CustomerPreferredTimeZone <String>
 -CustomerCountry <String> -CustomerPreferredSupportLanguage <String> [-ProblemStartTime <DateTime>]
 [-CSPHomeTenantId <String>] [-Require24X7Response] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="87833-106">CreateSupportTicketWithContactObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="87833-106">CreateSupportTicketWithContactObjectParameterSet</span></span>
```
New-AzSupportTicket -Name <String> -Title <String> -Description <String> -ProblemClassificationId <String>
 -Severity <Severity> -CustomerContactDetail <PSContactProfile> [-ProblemStartTime <DateTime>]
 [-CSPHomeTenantId <String>] [-Require24X7Response] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="87833-107">CreateTechnicalSupportTicketWithContactObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="87833-107">CreateTechnicalSupportTicketWithContactObjectParameterSet</span></span>
```
New-AzSupportTicket -Name <String> -Title <String> -Description <String> -ProblemClassificationId <String>
 -Severity <Severity> -CustomerContactDetail <PSContactProfile> [-ProblemStartTime <DateTime>]
 -TechnicalTicketResourceId <String> [-CSPHomeTenantId <String>] [-Require24X7Response] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="87833-108">CreateQuotaSupportTicketWithContactObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="87833-108">CreateQuotaSupportTicketWithContactObjectParameterSet</span></span>
```
New-AzSupportTicket -Name <String> -Title <String> -Description <String> -ProblemClassificationId <String>
 -Severity <Severity> -CustomerContactDetail <PSContactProfile> [-ProblemStartTime <DateTime>]
 -QuotaTicketDetail <PSQuotaTicketDetail> [-CSPHomeTenantId <String>] [-Require24X7Response] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="87833-109">CreateTechnicalSupportTicketWithContactDetailParameterSet</span><span class="sxs-lookup"><span data-stu-id="87833-109">CreateTechnicalSupportTicketWithContactDetailParameterSet</span></span>
```
New-AzSupportTicket -Name <String> -Title <String> -Description <String> -ProblemClassificationId <String>
 -Severity <Severity> -CustomerFirstName <String> -CustomerLastName <String>
 -PreferredContactMethod <ContactMethod> -CustomerPrimaryEmailAddress <String>
 [-AdditionalEmailAddress <String[]>] [-CustomerPhoneNumber <String>] -CustomerPreferredTimeZone <String>
 -CustomerCountry <String> -CustomerPreferredSupportLanguage <String> [-ProblemStartTime <DateTime>]
 -TechnicalTicketResourceId <String> [-CSPHomeTenantId <String>] [-Require24X7Response] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="87833-110">CreateQuotaSupportTicketWithContactDetailParameterSet</span><span class="sxs-lookup"><span data-stu-id="87833-110">CreateQuotaSupportTicketWithContactDetailParameterSet</span></span>
```
New-AzSupportTicket -Name <String> -Title <String> -Description <String> -ProblemClassificationId <String>
 -Severity <Severity> -CustomerFirstName <String> -CustomerLastName <String>
 -PreferredContactMethod <ContactMethod> -CustomerPrimaryEmailAddress <String>
 [-AdditionalEmailAddress <String[]>] [-CustomerPhoneNumber <String>] -CustomerPreferredTimeZone <String>
 -CustomerCountry <String> -CustomerPreferredSupportLanguage <String> [-ProblemStartTime <DateTime>]
 -QuotaTicketDetail <PSQuotaTicketDetail> [-CSPHomeTenantId <String>] [-Require24X7Response] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="87833-111">설명</span><span class="sxs-lookup"><span data-stu-id="87833-111">DESCRIPTION</span></span>
<span data-ttu-id="87833-112">이 cmdlet은 청구, 구독 관리, 할당량 또는 기술 문제에 대한 지원 티켓을 만드는 데 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="87833-112">This cmdlet can be used to create a support ticket for Billing, Subscription Management, Quota or Technical issues.</span></span> <span data-ttu-id="87833-113">Get-AzSupportService Get-AzSupportProblemClassification 및 cmdlet을 사용하여 지원을 요청하려는 Azure 서비스 및 해당 문제 분류를 각각 식별합니다.</span><span class="sxs-lookup"><span data-stu-id="87833-113">Use Get-AzSupportService and Get-AzSupportProblemClassification cmdlets to identify the Azure service and it's corresponding problem classifications respectively for which you want to request support.</span></span> <span data-ttu-id="87833-114">다음 매개 변수를 지정해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="87833-114">You must specify the following parameters:</span></span> 

    • Title
    • Description
    • Severity level
    • ProblemClassificationId
    • CustomerContactDetail (or individual customer contact parameters)

<span data-ttu-id="87833-115">도우미 cmdlet을 New-AzSupportContactProfileObject CustomerContactDetail 개체를 만들 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="87833-115">You can use New-AzSupportContactProfileObject helper cmdlet to create CustomerContactDetail object.</span></span>

<span data-ttu-id="87833-116">클라우드 솔루션 공급자는 고객의 테넌트에 로그인하고 *CSPHomeTenantId* 매개 변수를 사용하여 홈 테넌트 ID를 지정하여 고객의 구독에 대한 지원 티켓을 만들 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="87833-116">Cloud Solution Providers can create a support ticket for their customer's subscriptions by logging into their customer's tenant and specifying their home tenant id using *CSPHomeTenantId* parameter.</span></span>

<span data-ttu-id="87833-117">__기술 티켓의 경우:__</span><span class="sxs-lookup"><span data-stu-id="87833-117">__For technical tickets:__</span></span>

<span data-ttu-id="87833-118">리소스 이름을 지정하기 위해 *TechnicalTicketResourceId* 매개 ARM 리소스의 리소스 ID를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="87833-118">To specify the resource name, specify the ARM resource ID of the resource by using *TechnicalTicketResourceId* parameter.</span></span> <span data-ttu-id="87833-119">아래 예제를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="87833-119">See an example below.</span></span> 

<span data-ttu-id="87833-120">__할당량 티켓의 경우:__</span><span class="sxs-lookup"><span data-stu-id="87833-120">__For quota tickets:__</span></span>

<span data-ttu-id="87833-121">**Compute VM 코어,** **Batch,** **SQL Database 및** SQL Data **Warehouse에** 대한 할당량 증가를 요청하려면 *QuotaTicketDetail* 개체 아래에 추가 세부 정보를 제공합니다.</span><span class="sxs-lookup"><span data-stu-id="87833-121">To request for quota increase for **Compute VM Cores**, **Batch**, **SQL Database** and **SQL Data Warehouse**, provide additional details under *QuotaTicketDetail* object.</span></span> <span data-ttu-id="87833-122">QuotaTicketDetail 개체는 아래에 설명된 3개의 속성으로 구성됩니다.</span><span class="sxs-lookup"><span data-stu-id="87833-122">QuotaTicketDetail object consists of 3 properties as described below.</span></span> <span data-ttu-id="87833-123">자세한 설명서는 여기를 [클릭하세요.](https://aka.ms/supportrpquotarequestpayload)</span><span class="sxs-lookup"><span data-stu-id="87833-123">For detailed documentation, please [click here.](https://aka.ms/supportrpquotarequestpayload)</span></span>

    • QuotaChangeRequestSubType

        This is required for certain quota types when there is a sub type that you are requesting quota increase for. Example: Batch, SQL Database and SQL Data Warehouse have a sub type.

    • QuotaChangeRequestVersion

        This is required and indicates the version of the quota change request payload.

    • QuotaChangeRequests

        This is required and is a list of PSQuotaChangeRequest objects. PSQuotaChangeRequest object has 2 required properties.

        ○ Region

            This is the Azure location or region for which you are requesting quota increase. This is the Location property of Get-AzLocation cmdlet.
        
        ○ Payload

            This is where you specify the new limits for the selected quota type.


<span data-ttu-id="87833-124">다양한 할당량 유형에 대한 페이로드를 생성하는 방법에 대한 자세한 설명서는 [여기를 클릭하세요.](https://aka.ms/supportrpquotarequestpayload)</span><span class="sxs-lookup"><span data-stu-id="87833-124">For detailed documentation on how to construct Payload for various quota types, please [click here](https://aka.ms/supportrpquotarequestpayload)</span></span>

## <span data-ttu-id="87833-125">예제</span><span class="sxs-lookup"><span data-stu-id="87833-125">EXAMPLES</span></span>

### <span data-ttu-id="87833-126">예제 1: 청구 또는 구독 관리 지원 티켓 만들기</span><span class="sxs-lookup"><span data-stu-id="87833-126">Example 1: Create a Billing or Subscription Management support ticket.</span></span> <span data-ttu-id="87833-127">Get-AzSupportService 및 Get-AzSupportProblemClassification 사용하여 지원을 요청하려는 청구 또는 구독 관리 문제 분류에 대한 올바른 GUID를 검색합니다.</span><span class="sxs-lookup"><span data-stu-id="87833-127">Use Get-AzSupportService and Get-AzSupportProblemClassification to retrieve correct GUIDs for Billing or Subscription Management problem classification for which you want to request support</span></span> 
```powershell
PS C:\> New-AzSupportTicket -Name "test1" -Title "Test" -Description "Test" -Severity "minimal" -ProblemClassificationId "/providers/Microsoft.Support/services/{billing_service_guid}/problemClassifications/{problemClassification_guid}" -CustomerContactDetail @{FirstName = "first" ; LastName = "last" ; PreferredTimeZone = "pacific standard time" ; PreferredSupportLanguage = "en-us" ; Country = "USA" ; PreferredContactMethod = "Email" ; PrimaryEmailAddress = "user@contoso.com"}

Name  Title SupportTicketId Severity ServiceDisplayName Status CreatedDate
----  ----- --------------- -------- ------------------ ------ -----------
test1 Test  150010521000317 Minimal  Billing            Open   2/5/2020 1:33:53 AM
```

### <span data-ttu-id="87833-128">예제 2: Windows 리소스용 Virtual Machine에 대한 기술 지원 티켓을 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="87833-128">Example 2: Create a technical support ticket for Virtual Machine for Windows resource.</span></span> <span data-ttu-id="87833-129">지원 Get-AzSupportService Get-AzSupportProblemClassification Windows용 Virtual Machine 문제 분류에 대한 올바른 GUID를 검색하려면 다음을 실행합니다.</span><span class="sxs-lookup"><span data-stu-id="87833-129">Use Get-AzSupportService and Get-AzSupportProblemClassification to retrieve correct GUIDs for Virtual Machine for Windows problem classification for which you want to request support</span></span> 
```powershell
PS C:\> New-AzSupportTicket -Name "test1" -Title "Test" -Description "Test" -Severity "minimal" -ProblemClassificationId "/providers/Microsoft.Support/services/{vm_windows_service_guid}/problemClassifications/{problemClassification_guid}" -TechnicalTicketResourceId "/subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/testRG/providers/Microsoft.Compute/virtualMachines/testVM" -CustomerContactDetail @{FirstName = "first" ; LastName = "last" ; PreferredTimeZone = "pacific standard time" ; PreferredSupportLanguage = "en-us" ; Country = "USA" ; PreferredContactMethod = "Email" ; PrimaryEmailAddress = "user@contoso.com"}

Name  Title SupportTicketId Severity ServiceDisplayName              Status CreatedDate
----  ----- --------------- -------- ------------------              ------ -----------
test1 Test  150010521000317 Minimal  Virtual Machine running Windows Open   2/5/2020 1:33:53 AM
```

### <span data-ttu-id="87833-130">예제 3: 특정 VM 패밀리에 대한 Virtual Machine Cores에 대한 할당량 증가를 위한 할당량 지원 티켓을 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="87833-130">Example 3: Create a quota support ticket to increase quota for Virtual Machine Cores for a specific VM family.</span></span> <span data-ttu-id="87833-131">할당 Get-AzSupportService 및 Get-AzSupportProblemClassification 할당량 Compute VM 코어 문제 분류에 대한 올바른 GUID를 검색합니다.</span><span class="sxs-lookup"><span data-stu-id="87833-131">Use Get-AzSupportService and Get-AzSupportProblemClassification to retrieve correct GUIDs for Quota Compute VM Cores problem classification.</span></span>
```powershell
PS C:\> New-AzSupportTicket -Name "test1" -Title "Test" -Description "Test" -Severity "minimal" -ProblemClassificationId "/providers/Microsoft.Support/services/{quota_service_guid}/problemClassifications/{cores_problemClassification_guid}" -QuotaTicketDetail @{QuotaChangeRequestVersion = "1.0" ; QuotaChangeRequests = (@{Region = "westus"; Payload = "{`"VMFamily`":`"Dv2 Series`",`"NewLimit`":350}"}, @{Region = "eastus"; Payload = "{`"VMFamily`":`"Dv2 Series`",`"NewLimit`":516}"})} -CustomerContactDetail @{FirstName = "first" ; LastName = "last" ; PreferredTimeZone = "pacific standard time" ; PreferredSupportLanguage = "en-us" ; Country = "USA" ; PreferredContactMethod = "Email" ; PrimaryEmailAddress = "user@contoso.com"}

Name  Title SupportTicketId Severity ServiceDisplayName                       Status CreatedDate
----  ----- --------------- -------- ------------------                       ------ -----------
test1 Test  150010521000317 Minimal  Service and subscription limits (quotas) Open   2/5/2020 1:33:53 AM
```

### <span data-ttu-id="87833-132">예제 4: Batch 계정에 대한 우선 순위가 낮은 코어에 대한 할당량 증가를 위한 할당량 지원 티켓을 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="87833-132">Example 4: Create a quota support ticket to increase quota for Low-priority cores for a Batch account.</span></span> <span data-ttu-id="87833-133">할당 Get-AzSupportService 및 Get-AzSupportProblemClassification 할당량 일괄 처리 문제 분류에 대한 올바른 GUID를 검색합니다.</span><span class="sxs-lookup"><span data-stu-id="87833-133">Use Get-AzSupportService and Get-AzSupportProblemClassification to retrieve correct GUIDs for Quota Batch problem classification.</span></span>
```powershell
PS C:\> New-AzSupportTicket -Name "test1" -Title "Test" -Description "Test" -Severity "minimal" -ProblemClassificationId "/providers/Microsoft.Support/services/{quota_service_guid}/problemClassifications/{batch_problemClassification_guid}" -QuotaTicketDetail @{QuotaChangeRequestVersion = "1.0" ; QuotaChangeRequestSubType = "Account" ; QuotaChangeRequests = (@{Region = "westus"; Payload = "{`"AccountName`":`"test`",`"NewLimit`":200,`"Type`":`"LowPriority`"}"})} -CustomerContactDetail @{FirstName = "first" ; LastName = "last" ; PreferredTimeZone = "pacific standard time" ; PreferredSupportLanguage = "en-us" ; Country = "USA" ; PreferredContactMethod = "Email" ; PrimaryEmailAddress = "user@contoso.com"}

Name  Title SupportTicketId Severity ServiceDisplayName                       Status CreatedDate
----  ----- --------------- -------- ------------------                       ------ -----------
test1 Test  150010521000317 Minimal  Service and subscription limits (quotas) Open   2/5/2020 1:33:53 AM
```

### <span data-ttu-id="87833-134">예제 5: Batch 계정에 대한 특정 VM 패밀리에 대한 VM 코어 할당량 증가를 위한 할당량 지원 티켓을 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="87833-134">Example 5: Create a quota support ticket to increase VM cores quota for a specific VM Family for a Batch account.</span></span> <span data-ttu-id="87833-135">할당 Get-AzSupportService 및 Get-AzSupportProblemClassification 할당량 일괄 처리 문제 분류에 대한 올바른 GUID를 검색합니다.</span><span class="sxs-lookup"><span data-stu-id="87833-135">Use Get-AzSupportService and Get-AzSupportProblemClassification to retrieve correct GUIDs for Quota Batch problem classification.</span></span>
```powershell
PS C:\> New-AzSupportTicket -Name "test1" -Title "Test" -Description "Test" -Severity "minimal" -ProblemClassificationId "/providers/Microsoft.Support/services/{quota_service_guid}/problemClassifications/{batch_problemClassification_guid}" -QuotaTicketDetail @{QuotaChangeRequestVersion = "1.0" ; QuotaChangeRequestSubType = "Account" ; QuotaChangeRequests = (@{Region = "westus"; Payload = "{`"AccountName`":`"test`",`"VMFamily`":`"standardA0_A7Family`",`"NewLimit`":200,`"Type`":`"Dedicated`"}"})} -CustomerContactDetail @{FirstName = "first" ; LastName = "last" ; PreferredTimeZone = "pacific standard time" ; PreferredSupportLanguage = "en-us" ; Country = "USA" ; PreferredContactMethod = "Email" ; PrimaryEmailAddress = "user@contoso.com"}

Name  Title SupportTicketId Severity ServiceDisplayName                       Status CreatedDate
----  ----- --------------- -------- ------------------                       ------ -----------
test1 Test  150010521000317 Minimal  Service and subscription limits (quotas) Open   2/5/2020 1:33:53 AM
```

### <span data-ttu-id="87833-136">예제 6: Batch 계정에 대한 풀 할당량 증가를 위한 할당량 지원 티켓을 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="87833-136">Example 6: Create a quota support ticket to increase Pools quota for a Batch account.</span></span> <span data-ttu-id="87833-137">할당 Get-AzSupportService 및 Get-AzSupportProblemClassification 할당량 일괄 처리 문제 분류에 대한 올바른 GUID를 검색합니다.</span><span class="sxs-lookup"><span data-stu-id="87833-137">Use Get-AzSupportService and Get-AzSupportProblemClassification to retrieve correct GUIDs for Quota Batch problem classification.</span></span>
```powershell
PS C:\> New-AzSupportTicket -Name "test1" -Title "Test" -Description "Test" -Severity "minimal" -ProblemClassificationId "/providers/Microsoft.Support/services/{quota_service_guid}/problemClassifications/{batch_problemClassification_guid}" -QuotaTicketDetail @{QuotaChangeRequestVersion = "1.0" ; QuotaChangeRequestSubType = "Account" ; QuotaChangeRequests = (@{Region = "westus"; Payload = "{`"AccountName`":`"test`",`"NewLimit`":120,`"Type`":`"Pools`"}"})} -CustomerContactDetail @{FirstName = "first" ; LastName = "last" ; PreferredTimeZone = "pacific standard time" ; PreferredSupportLanguage = "en-us" ; Country = "USA" ; PreferredContactMethod = "Email" ; PrimaryEmailAddress = "user@contoso.com"}

Name  Title SupportTicketId Severity ServiceDisplayName                       Status CreatedDate
----  ----- --------------- -------- ------------------                       ------ -----------
test1 Test  150010521000317 Minimal  Service and subscription limits (quotas) Open   2/5/2020 1:33:53 AM
```

### <span data-ttu-id="87833-138">예제 7: 할당량 지원 티켓을 만들어 Batch 계정에 대한 활성 작업 및 작업 일정 할당량 증가</span><span class="sxs-lookup"><span data-stu-id="87833-138">Example 7: Create a quota support ticket to increase active Jobs and job schedules quota for a Batch account.</span></span> <span data-ttu-id="87833-139">할당 Get-AzSupportService 및 Get-AzSupportProblemClassification 할당량 일괄 처리 문제 분류에 대한 올바른 GUID를 검색합니다.</span><span class="sxs-lookup"><span data-stu-id="87833-139">Use Get-AzSupportService and Get-AzSupportProblemClassification to retrieve correct GUIDs for Quota Batch problem classification.</span></span>
```powershell
PS C:\> New-AzSupportTicket -Name "test1" -Title "Test" -Description "Test" -Severity "minimal" -ProblemClassificationId "/providers/Microsoft.Support/services/{quota_service_guid}/problemClassifications/{batch_problemClassification_guid}" -QuotaTicketDetail @{QuotaChangeRequestVersion = "1.0" ; QuotaChangeRequestSubType = "Account" ; QuotaChangeRequests = (@{Region = "westus"; Payload = "{`"AccountName`":`"test`",`"NewLimit`":120,`"Type`":`"Jobs`"}"})} -CustomerContactDetail @{FirstName = "first" ; LastName = "last" ; PreferredTimeZone = "pacific standard time" ; PreferredSupportLanguage = "en-us" ; Country = "USA" ; PreferredContactMethod = "Email" ; PrimaryEmailAddress = "user@contoso.com"}

Name  Title SupportTicketId Severity ServiceDisplayName                       Status CreatedDate
----  ----- --------------- -------- ------------------                       ------ -----------
test1 Test  150010521000317 Minimal  Service and subscription limits (quotas) Open   2/5/2020 1:33:53 AM
```

### <span data-ttu-id="87833-140">예제 8: 구독에 대한 Batch 계정 수를 늘리는 할당량 지원 티켓을 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="87833-140">Example 8: Create a quota support ticket to increase number of Batch accounts for a subscription.</span></span> <span data-ttu-id="87833-141">할당 Get-AzSupportService 및 Get-AzSupportProblemClassification 할당량 일괄 처리 문제 분류에 대한 올바른 GUID를 검색합니다.</span><span class="sxs-lookup"><span data-stu-id="87833-141">Use Get-AzSupportService and Get-AzSupportProblemClassification to retrieve correct GUIDs for Quota Batch problem classification.</span></span>
```powershell
PS C:\> New-AzSupportTicket -Name "test1" -Title "Test" -Description "Test" -Severity "minimal" -ProblemClassificationId "/providers/Microsoft.Support/services/{quota_service_guid}/problemClassifications/{batch_problemClassification_guid}" -QuotaTicketDetail @{QuotaChangeRequestVersion = "1.0" ; QuotaChangeRequestSubType = "Subscription" ; QuotaChangeRequests = (@{Region = "westus"; Payload = "{`"NewLimit`":120,`"Type`":`"Account`"}"})} -CustomerContactDetail @{FirstName = "first" ; LastName = "last" ; PreferredTimeZone = "pacific standard time" ; PreferredSupportLanguage = "en-us" ; Country = "USA" ; PreferredContactMethod = "Email" ; PrimaryEmailAddress = "user@contoso.com"}

Name  Title SupportTicketId Severity ServiceDisplayName                       Status CreatedDate
----  ----- --------------- -------- ------------------                       ------ -----------
test1 Test  150010521000317 Minimal  Service and subscription limits (quotas) Open   2/5/2020 1:33:53 AM
```

### <span data-ttu-id="87833-142">예제 9: 할당량 지원 티켓을 만들어 SQL Database에 대한 할당량 증가</span><span class="sxs-lookup"><span data-stu-id="87833-142">Example 9: Create a quota support ticket to increase quota for DTUs for SQL Database.</span></span> <span data-ttu-id="87833-143">데이터베이스 Get-AzSupportService 및 Get-AzSupportProblemClassification 데이터베이스 문제 분류에 대한 올바른 GUID를 SQL 검색합니다.</span><span class="sxs-lookup"><span data-stu-id="87833-143">Use Get-AzSupportService and Get-AzSupportProblemClassification to retrieve correct GUIDs for Quota SQL Database problem classification.</span></span>
```powershell
PS C:\> New-AzSupportTicket -Name "test1" -Title "Test" -Description "Test" -Severity "minimal" -ProblemClassificationId "/providers/Microsoft.Support/services/{quota_service_guid}/problemClassifications/{sql_database_problemClassification_guid}" -QuotaTicketDetail @{QuotaChangeRequestVersion = "1.0" ; QuotaChangeRequestSubType = "DTUs" ; QuotaChangeRequests = (@{Region = "westus"; Payload = "{`"ServerName`":`"testserver`",`"NewLimit`":54000}"})} -CustomerContactDetail @{FirstName = "first" ; LastName = "last" ; PreferredTimeZone = "pacific standard time" ; PreferredSupportLanguage = "en-us" ; Country = "USA" ; PreferredContactMethod = "Email" ; PrimaryEmailAddress = "user@contoso.com"}

Name  Title SupportTicketId Severity ServiceDisplayName                       Status CreatedDate
----  ----- --------------- -------- ------------------                       ------ -----------
test1 Test  150010521000317 Minimal  Service and subscription limits (quotas) Open   2/5/2020 1:33:53 AM
```

### <span data-ttu-id="87833-144">예제 10: 할당량 지원 티켓을 만들어 SQL 데이터베이스의 서버 할당량 증가</span><span class="sxs-lookup"><span data-stu-id="87833-144">Example 10: Create a quota support ticket to increase quota for Servers for SQL Database.</span></span> <span data-ttu-id="87833-145">데이터베이스 Get-AzSupportService 및 Get-AzSupportProblemClassification 데이터베이스 문제 분류에 대한 올바른 GUID를 SQL 검색합니다.</span><span class="sxs-lookup"><span data-stu-id="87833-145">Use Get-AzSupportService and Get-AzSupportProblemClassification to retrieve correct GUIDs for Quota SQL Database problem classification.</span></span>
```powershell
PS C:\> New-AzSupportTicket -Name "test1" -Title "Test" -Description "Test" -Severity "minimal" -ProblemClassificationId "/providers/Microsoft.Support/services/{quota_service_guid}/problemClassifications/{sql_database_problemClassification_guid}" -QuotaTicketDetail @{QuotaChangeRequestVersion = "1.0" ; QuotaChangeRequestSubType = "Servers" ; QuotaChangeRequests = (@{Region = "westus"; Payload = "{`"NewLimit`":200}"})} -CustomerContactDetail @{FirstName = "first" ; LastName = "last" ; PreferredTimeZone = "pacific standard time" ; PreferredSupportLanguage = "en-us" ; Country = "USA" ; PreferredContactMethod = "Email" ; PrimaryEmailAddress = "user@contoso.com"}

Name  Title SupportTicketId Severity ServiceDisplayName                       Status CreatedDate
----  ----- --------------- -------- ------------------                       ------ -----------
test1 Test  150010521000317 Minimal  Service and subscription limits (quotas) Open   2/5/2020 1:33:53 AM
```

### <span data-ttu-id="87833-146">예제 11: 할당량 지원 티켓을 만들어 데이터 웨어하우스에 대한 D2 할당량 SQL 증가합니다.</span><span class="sxs-lookup"><span data-stu-id="87833-146">Example 11: Create a quota support ticket to increase quota for DTUs for SQL Data Warehouse.</span></span> <span data-ttu-id="87833-147">데이터 Get-AzSupportService 및 Get-AzSupportProblemClassification 사용하여 날짜 웨어하우스 문제 분류에 대한 할당량 SQL 올바른 GUID를 검색합니다.</span><span class="sxs-lookup"><span data-stu-id="87833-147">Use Get-AzSupportService and Get-AzSupportProblemClassification to retrieve correct GUIDs for Quota SQL Date Warehouse problem classification.</span></span>
```powershell
PS C:\> New-AzSupportTicket -Name "test1" -Title "Test" -Description "Test" -Severity "minimal" -ProblemClassificationId "/providers/Microsoft.Support/services/{quota_service_guid}/problemClassifications/{sql_datawarehouse_problemClassification_guid}" -QuotaTicketDetail @{QuotaChangeRequestVersion = "1.0" ; QuotaChangeRequestSubType = "DTUs" ; QuotaChangeRequests = (@{Region = "westus"; Payload = "{`"ServerName`":`"testserver`",`"NewLimit`":54000}"})} -CustomerContactDetail @{FirstName = "first" ; LastName = "last" ; PreferredTimeZone = "pacific standard time" ; PreferredSupportLanguage = "en-us" ; Country = "USA" ; PreferredContactMethod = "Email" ; PrimaryEmailAddress = "user@contoso.com"}

Name  Title SupportTicketId Severity ServiceDisplayName                       Status CreatedDate
----  ----- --------------- -------- ------------------                       ------ -----------
test1 Test  150010521000317 Minimal  Service and subscription limits (quotas) Open   2/5/2020 1:33:53 AM
```

### <span data-ttu-id="87833-148">예제 12: Data Warehouse에 대한 서버에 대한 할당량 증가를 위한 할당량 지원 SQL 만들기</span><span class="sxs-lookup"><span data-stu-id="87833-148">Example 12: Create a quota support ticket to increase quota for Servers for SQL Data Warehouse.</span></span> <span data-ttu-id="87833-149">데이터 Get-AzSupportService Get-AzSupportProblemClassification 데이터 웨어하우스 문제 분류에 대한 올바른 GUID를 SQL 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="87833-149">Use Get-AzSupportService and Get-AzSupportProblemClassification to retrieve correct GUIDs for Quota SQL Data Warehouse problem classification.</span></span>
```powershell
PS C:\> New-AzSupportTicket -Name "test1" -Title "Test" -Description "Test" -Severity "minimal" -ProblemClassificationId "/providers/Microsoft.Support/services/{quota_service_guid}/problemClassifications/{sql_datawarehouse_problemClassification_guid}" -QuotaTicketDetail @{QuotaChangeRequestVersion = "1.0" ; QuotaChangeRequestSubType = "Servers" ; QuotaChangeRequests = (@{Region = "westus"; Payload = "{`"NewLimit`":200}"})} -CustomerContactDetail @{FirstName = "first" ; LastName = "last" ; PreferredTimeZone = "pacific standard time" ; PreferredSupportLanguage = "en-us" ; Country = "USA" ; PreferredContactMethod = "Email" ; PrimaryEmailAddress = "user@contoso.com"}

Name  Title SupportTicketId Severity ServiceDisplayName                       Status CreatedDate
----  ----- --------------- -------- ------------------                       ------ -----------
test1 Test  150010521000317 Minimal  Service and subscription limits (quotas) Open   2/5/2020 1:33:53 AM
```

### <span data-ttu-id="87833-150">예제 13: Machine Learning 서비스에 대한 우선 순위가 낮은 코어에 대한 할당량 증가를 위한 할당량 지원 티켓을 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="87833-150">Example 13: Create a quota support ticket to increase quota for Low-priority cores for Machine Learning service.</span></span> <span data-ttu-id="87833-151">할당 Get-AzSupportService 및 Get-AzSupportProblemClassification 사용하여 할당량 Machine Learning 서비스 문제 분류에 대한 올바른 GUID를 검색합니다.</span><span class="sxs-lookup"><span data-stu-id="87833-151">Use Get-AzSupportService and Get-AzSupportProblemClassification to retrieve correct GUIDs for Quota Machine Learning service problem classification.</span></span>
```powershell
PS C:\> New-AzSupportTicket -Name "test1" -Title "Test" -Description "Test" -Severity "minimal" -ProblemClassificationId "/providers/Microsoft.Support/services/{quota_service_guid}/problemClassifications/{machine_learning_service_problemClassification_guid}" -QuotaTicketDetail @{QuotaChangeRequestVersion = "1.0" ; QuotaChangeRequestSubType = "BatchAml" ; QuotaChangeRequests = (@{Region = "westus"; Payload = "{`"NewLimit`":200,`"Type`":`"LowPriority`" }"})} -CustomerContactDetail @{FirstName = "first" ; LastName = "last" ; PreferredTimeZone = "pacific standard time" ; PreferredSupportLanguage = "en-us" ; Country = "USA" ; PreferredContactMethod = "Email" ; PrimaryEmailAddress = "user@contoso.com"}

Name  Title SupportTicketId Severity ServiceDisplayName                       Status CreatedDate
----  ----- --------------- -------- ------------------                       ------ -----------
test1 Test  150010521000317 Minimal  Service and subscription limits (quotas) Open   2/5/2020 1:33:53 AM
```

### <span data-ttu-id="87833-152">예제 14: Machine Learning 서비스에 대한 특정 VM 패밀리에 대한 VM 코어 할당량 증가를 위한 할당량 지원 티켓을 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="87833-152">Example 14: Create a quota support ticket to increase VM cores quota for a specific VM Family for Machine Learning service.</span></span> <span data-ttu-id="87833-153">할당 Get-AzSupportService 및 Get-AzSupportProblemClassification 사용하여 할당량 Machine Learning 서비스 문제 분류에 대한 올바른 GUID를 검색합니다.</span><span class="sxs-lookup"><span data-stu-id="87833-153">Use Get-AzSupportService and Get-AzSupportProblemClassification to retrieve correct GUIDs for Quota Machine Learning service problem classification.</span></span>
```powershell
PS C:\> New-AzSupportTicket -Name "test1" -Title "Test" -Description "Test" -Severity "minimal" -ProblemClassificationId "/providers/Microsoft.Support/services/{quota_service_guid}/problemClassifications/{machine_learning_service_problemClassification_guid}" -QuotaTicketDetail @{QuotaChangeRequestVersion = "1.0" ; QuotaChangeRequestSubType = "BatchAml" ; QuotaChangeRequests = (@{Region = "westus"; Payload = "{`"VMFamily`":`"standardDFamily`",`"NewLimit`":200,`"Type`":`"Dedicated`" }"})} -CustomerContactDetail @{FirstName = "first" ; LastName = "last" ; PreferredTimeZone = "pacific standard time" ; PreferredSupportLanguage = "en-us" ; Country = "USA" ; PreferredContactMethod = "Email" ; PrimaryEmailAddress = "user@contoso.com"}

Name  Title SupportTicketId Severity ServiceDisplayName                       Status CreatedDate
----  ----- --------------- -------- ------------------                       ------ -----------
test1 Test  150010521000317 Minimal  Service and subscription limits (quotas) Open   2/5/2020 1:33:53 AM
```

### <span data-ttu-id="87833-154">예제 15: 할당량 지원 티켓을 만들어 Azure SQL Managed Instance에 대한 할당량 증가</span><span class="sxs-lookup"><span data-stu-id="87833-154">Example 15: Create a quota support ticket to increase quota for Azure SQL Managed Instance.</span></span> <span data-ttu-id="87833-155">Managed Instance Get-AzSupportService Get-AzSupportProblemClassification 할당량에 대한 올바른 GUID를 SQL Managed Instance 서비스 문제 분류를 검색합니다.</span><span class="sxs-lookup"><span data-stu-id="87833-155">Use Get-AzSupportService and Get-AzSupportProblemClassification to retrieve correct GUIDs for Quota SQL Managed Instance service problem classification.</span></span>
```powershell
PS C:\> New-AzSupportTicket -Name "test1" -Title "Test" -Description "Test" -Severity "minimal" -ProblemClassificationId "/providers/Microsoft.Support/services/{quota_service_guid}/problemClassifications/{sql_managed_instance_problemClassification_guid}" -QuotaTicketDetail @{QuotaChangeRequestVersion = "1.0" ; QuotaChangeRequestSubType = "SQLMI" ; QuotaChangeRequests = (@{Region = "westus"; Payload = "{`"NewLimit`":200,`"Type`":`"vCore`" }"}, @{Region = "westus"; Payload = "{`"NewLimit`":200,`"Type`":`"Subnet`" }"})} -CustomerContactDetail @{FirstName = "first" ; LastName = "last" ; PreferredTimeZone = "pacific standard time" ; PreferredSupportLanguage = "en-us" ; Country = "USA" ; PreferredContactMethod = "Email" ; PrimaryEmailAddress = "user@contoso.com"}

Name  Title SupportTicketId Severity ServiceDisplayName                       Status CreatedDate
----  ----- --------------- -------- ------------------                       ------ -----------
test1 Test  150010521000317 Minimal  Service and subscription limits (quotas) Open   2/5/2020 1:33:53 AM
```

### <span data-ttu-id="87833-156">예제 16: CustomerContactDetail 개체 대신 개별 고객 연락처 매개 변수를 지정하여 지원 티켓을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="87833-156">Example 16: Create a support ticket by specifying individual customer contact parameters instead of CustomerContactDetail object.</span></span> 
```powershell
PS C:\> New-AzSupportTicket -Name "test1" -Title "Test" -Description "Test" -Severity "minimal" -ProblemClassificationId "/providers/Microsoft.Support/services/{billing_service_guid}/problemClassifications/{problemClassification_guid}" -CustomerFirstName "first" -CustomerLastName "last" -CustomerPreferredTimeZone "pacific standard time" -CustomerPreferredSupportLanguage "en-us" -CustomerCountry = "USA" -PreferredContactMethod "Email" -CustomerPrimaryEmailAddress "user@contoso.com"

Name  Title SupportTicketId Severity ServiceDisplayName Status CreatedDate
----  ----- --------------- -------- ------------------ ------ -----------
test1 Test  150010521000317 Minimal  Billing            Open   2/5/2020 1:33:53 AM
```

### <span data-ttu-id="87833-157">예제 17: Azure에서 24 x 7 응답에 대한 요청으로 지원 티켓을 만들 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="87833-157">Example 17: Create a support ticket with request for 24 x 7 response from Azure.</span></span> 
```powershell
PS C:\> New-AzSupportTicket -Name "test1" -Title "Test" -Description "Test" -Severity "critical" -ProblemClassificationId "/providers/Microsoft.Support/services/{billing_service_guid}/problemClassifications/{problemClassification_guid}" -CustomerFirstName "first" -CustomerLastName "last" -CustomerPreferredTimeZone "pacific standard time" -CustomerPreferredSupportLanguage "en-us" -CustomerCountry = "USA" -PreferredContactMethod "Email" -CustomerPrimaryEmailAddress "user@contoso.com" -Require24X7Response 

Name  Title SupportTicketId Severity ServiceDisplayName Status CreatedDate
----  ----- --------------- -------- ------------------ ------ -----------
test1 Test  150010521000317 Critical  Billing            Open   2/5/2020 1:33:53 AM
```

### <span data-ttu-id="87833-158">예제 18: CSP(클라우드 솔루션 공급자)인 경우 고객을 대신하여 지원 티켓을 만드십시오.</span><span class="sxs-lookup"><span data-stu-id="87833-158">Example 18: Create a support ticket on behalf of your customer if you are a Cloud Solution Provider (CSP).</span></span> <span data-ttu-id="87833-159">CSP는 먼저 해당 테넌트에 로그인한 다음 아래 예제와 같이 고객의 테넌트에 로그인해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="87833-159">CSP should first login into their tenant, and then login into customer's tenant as shown in the example below.</span></span> <span data-ttu-id="87833-160">그런 다음 지원 티켓을 만들 때 -CSPHomeTenantId 매개 변수를 사용하여 홈 테넌트 ID를 지정해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="87833-160">They must then use -CSPHomeTenantId parameter to specify their home tenant id at the time of creating a support ticket.</span></span>  
```powershell

PS C:\> Login-AzAccount

PS C:\> Login-AzAccount -TenantId {customer_tenant_id}

PS C:\> New-AzSupportTicket -Name "test1" -Title "Test" -Description "Test" -Severity "minimal" -ProblemClassificationId "/providers/Microsoft.Support/services/{billing_service_guid}/problemClassifications/{problemClassification_guid}" -CustomerFirstName "first" -CustomerLastName "last" -CustomerPreferredTimeZone "pacific standard time" -CustomerPreferredSupportLanguage "en-us" -CustomerCountry = "USA" -PreferredContactMethod "Email" -CustomerPrimaryEmailAddress "user@contoso.com" -CSPHomeTenantId {csp_home_tenant_id} 

Name  Title SupportTicketId Severity ServiceDisplayName Status CreatedDate
----  ----- --------------- -------- ------------------ ------ -----------
test1 Test  150010521000317 Minimal  Billing            Open   2/5/2020 1:33:53 AM
```

## <span data-ttu-id="87833-161">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="87833-161">PARAMETERS</span></span>

### <span data-ttu-id="87833-162">-AdditionalEmailAddress</span><span class="sxs-lookup"><span data-stu-id="87833-162">-AdditionalEmailAddress</span></span>
<span data-ttu-id="87833-163">추가 전자 메일 주소.</span><span class="sxs-lookup"><span data-stu-id="87833-163">Additional email addresses.</span></span>
<span data-ttu-id="87833-164">여기에 나열된 전자 메일 주소는 지원 티켓에 대한 모든 대응에 복사됩니다.</span><span class="sxs-lookup"><span data-stu-id="87833-164">Email addresses listed here will be copied on any correspondence about the support ticket.</span></span>

```yaml
Type: System.String[]
Parameter Sets: CreateSupportTicketWithContactDetailParameterSet, CreateTechnicalSupportTicketWithContactDetailParameterSet, CreateQuotaSupportTicketWithContactDetailParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="87833-165">-AsJob</span><span class="sxs-lookup"><span data-stu-id="87833-165">-AsJob</span></span>
<span data-ttu-id="87833-166">백그라운드에서 cmdlet을 실행합니다.</span><span class="sxs-lookup"><span data-stu-id="87833-166">Run cmdlet in the background.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="87833-167">-CSPHomeTenantId</span><span class="sxs-lookup"><span data-stu-id="87833-167">-CSPHomeTenantId</span></span>
<span data-ttu-id="87833-168">고객에 대한 지원 티켓을 만들려고 하는 클라우드 솔루션 공급자 사용자의 홈 테넌트 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="87833-168">This is the home tenant id of the Cloud Solution Provider user trying to create a support ticket for their customer.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="87833-169">-CustomerContactDetail</span><span class="sxs-lookup"><span data-stu-id="87833-169">-CustomerContactDetail</span></span>
<span data-ttu-id="87833-170">SupportTicket 리소스와 연결된 고객 연락처 세부 정보입니다.</span><span class="sxs-lookup"><span data-stu-id="87833-170">Customer contact details associated with SupportTicket resource.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Support.Models.PSContactProfile
Parameter Sets: CreateSupportTicketWithContactObjectParameterSet, CreateTechnicalSupportTicketWithContactObjectParameterSet, CreateQuotaSupportTicketWithContactObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="87833-171">-CustomerCountry</span><span class="sxs-lookup"><span data-stu-id="87833-171">-CustomerCountry</span></span>
<span data-ttu-id="87833-172">고객 국가입니다.</span><span class="sxs-lookup"><span data-stu-id="87833-172">Customer country.</span></span>
<span data-ttu-id="87833-173">유효한 ISO Alpha-3 국가 코드(ISO 3166)입니다.</span><span class="sxs-lookup"><span data-stu-id="87833-173">This must be a valid ISO Alpha-3 country code (ISO 3166).</span></span>

```yaml
Type: System.String
Parameter Sets: CreateSupportTicketWithContactDetailParameterSet, CreateTechnicalSupportTicketWithContactDetailParameterSet, CreateQuotaSupportTicketWithContactDetailParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="87833-174">-CustomerFirstName</span><span class="sxs-lookup"><span data-stu-id="87833-174">-CustomerFirstName</span></span>
<span data-ttu-id="87833-175">고객 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="87833-175">Customer first name.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateSupportTicketWithContactDetailParameterSet, CreateTechnicalSupportTicketWithContactDetailParameterSet, CreateQuotaSupportTicketWithContactDetailParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="87833-176">-CustomerLastName</span><span class="sxs-lookup"><span data-stu-id="87833-176">-CustomerLastName</span></span>
<span data-ttu-id="87833-177">고객 성입니다.</span><span class="sxs-lookup"><span data-stu-id="87833-177">Customer last name.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateSupportTicketWithContactDetailParameterSet, CreateTechnicalSupportTicketWithContactDetailParameterSet, CreateQuotaSupportTicketWithContactDetailParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="87833-178">-CustomerPhoneNumber</span><span class="sxs-lookup"><span data-stu-id="87833-178">-CustomerPhoneNumber</span></span>
<span data-ttu-id="87833-179">고객 전화 번호입니다.</span><span class="sxs-lookup"><span data-stu-id="87833-179">Customer phone number.</span></span>
<span data-ttu-id="87833-180">기본 연락 방법이 전화인 경우 필요합니다.</span><span class="sxs-lookup"><span data-stu-id="87833-180">This is required if preferred contact method is phone.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateSupportTicketWithContactDetailParameterSet, CreateTechnicalSupportTicketWithContactDetailParameterSet, CreateQuotaSupportTicketWithContactDetailParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="87833-181">-CustomerPreferredSupportLanguage</span><span class="sxs-lookup"><span data-stu-id="87833-181">-CustomerPreferredSupportLanguage</span></span>
<span data-ttu-id="87833-182">사용자 지정의 유추 언어입니다.</span><span class="sxs-lookup"><span data-stu-id="87833-182">Peferred language of the custom.</span></span>
<span data-ttu-id="87833-183">이 코드는 여기에 나열된 지원되는 언어 중 하나에 대한 유효한 언어 contry 코드가 되어야 https://azure.microsoft.com/en-us/support/faq/ 합니다.</span><span class="sxs-lookup"><span data-stu-id="87833-183">This must be a valid language-contry code for one of the supported languages listed here https://azure.microsoft.com/en-us/support/faq/.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateSupportTicketWithContactDetailParameterSet, CreateTechnicalSupportTicketWithContactDetailParameterSet, CreateQuotaSupportTicketWithContactDetailParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="87833-184">-CustomerPreferredTimeZone</span><span class="sxs-lookup"><span data-stu-id="87833-184">-CustomerPreferredTimeZone</span></span>
<span data-ttu-id="87833-185">고객이 선호하는 표준 시간대입니다.</span><span class="sxs-lookup"><span data-stu-id="87833-185">Customer preferred time zone.</span></span>
<span data-ttu-id="87833-186">이 값은 유효한 System.TimeZoneInfo.Id 합니다.</span><span class="sxs-lookup"><span data-stu-id="87833-186">This must be a valid System.TimeZoneInfo.Id value.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateSupportTicketWithContactDetailParameterSet, CreateTechnicalSupportTicketWithContactDetailParameterSet, CreateQuotaSupportTicketWithContactDetailParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="87833-187">-CustomerPrimaryEmailAddress</span><span class="sxs-lookup"><span data-stu-id="87833-187">-CustomerPrimaryEmailAddress</span></span>
<span data-ttu-id="87833-188">고객 기본 전자 메일 주소입니다.</span><span class="sxs-lookup"><span data-stu-id="87833-188">Customer primary email address.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateSupportTicketWithContactDetailParameterSet, CreateTechnicalSupportTicketWithContactDetailParameterSet, CreateQuotaSupportTicketWithContactDetailParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="87833-189">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="87833-189">-DefaultProfile</span></span>
<span data-ttu-id="87833-190">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="87833-190">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="87833-191">-Description</span><span class="sxs-lookup"><span data-stu-id="87833-191">-Description</span></span>
<span data-ttu-id="87833-192">질문 또는 문제의 자세한 설명입니다.</span><span class="sxs-lookup"><span data-stu-id="87833-192">Detailed description of the question or issue.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="87833-193">-Name</span><span class="sxs-lookup"><span data-stu-id="87833-193">-Name</span></span>
<span data-ttu-id="87833-194">이 cmdlet이 만드는 지원 티켓의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="87833-194">Name of support ticket that this cmdlet creates.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="87833-195">-PreferredContactMethod</span><span class="sxs-lookup"><span data-stu-id="87833-195">-PreferredContactMethod</span></span>
<span data-ttu-id="87833-196">기본 연락 방법.</span><span class="sxs-lookup"><span data-stu-id="87833-196">Preferred contact method.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Support.Models.ContactMethod
Parameter Sets: CreateSupportTicketWithContactDetailParameterSet, CreateTechnicalSupportTicketWithContactDetailParameterSet, CreateQuotaSupportTicketWithContactDetailParameterSet
Aliases:
Accepted values: Email, Phone

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="87833-197">-ProblemClassificationId</span><span class="sxs-lookup"><span data-stu-id="87833-197">-ProblemClassificationId</span></span>
<span data-ttu-id="87833-198">각 Azure 서비스에는 발생하는 문제 유형에 해당하는 문제 분류라는 자체 문제 범주 집합이 있습니다.</span><span class="sxs-lookup"><span data-stu-id="87833-198">Each Azure service has its own set of issue category called problem classification that corresponds to the type of problem you're experiencing.</span></span>
<span data-ttu-id="87833-199">이 매개 변수는 ProblemClassification ARM 리소스의 리소스 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="87833-199">This parameter is the ARM resource id of ProblemClassification resource.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="87833-200">-ProblemStartTime</span><span class="sxs-lookup"><span data-stu-id="87833-200">-ProblemStartTime</span></span>
<span data-ttu-id="87833-201">문제가 시작된 날짜 및 시간입니다.</span><span class="sxs-lookup"><span data-stu-id="87833-201">Date and time when the problem started.</span></span>

```yaml
Type: System.DateTime
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="87833-202">-QuotaTicketDetail</span><span class="sxs-lookup"><span data-stu-id="87833-202">-QuotaTicketDetail</span></span>
<span data-ttu-id="87833-203">할당량 지원 티켓에 대한 추가 세부 정보입니다.</span><span class="sxs-lookup"><span data-stu-id="87833-203">Additional details for a Quota support ticket.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Support.Models.PSQuotaTicketDetail
Parameter Sets: CreateQuotaSupportTicketWithContactObjectParameterSet, CreateQuotaSupportTicketWithContactDetailParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="87833-204">-Require24X7Response</span><span class="sxs-lookup"><span data-stu-id="87833-204">-Require24X7Response</span></span>
<span data-ttu-id="87833-205">이 지원 티켓에 Azure에서 24x7 응답이 필요한지 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="87833-205">Indicates if this support ticket requires a 24x7 response from Azure.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="87833-206">-심각도</span><span class="sxs-lookup"><span data-stu-id="87833-206">-Severity</span></span>
<span data-ttu-id="87833-207">지원 티켓의 심각도입니다.</span><span class="sxs-lookup"><span data-stu-id="87833-207">Severity of the support ticket.</span></span>
<span data-ttu-id="87833-208">이는 사례의 긴급도에 따라 Azure에 있는 기술 지원 계획의 서비스 수준 계약에 따라 응답 시간이 결정됩니다.</span><span class="sxs-lookup"><span data-stu-id="87833-208">This indicates the urgency of the case, which in turn determines the response time according to the service level agreement of the technical support plan you have with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Support.Models.Severity
Parameter Sets: (All)
Aliases:
Accepted values: Minimal, Moderate, Critical, HighestCriticalImpact

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="87833-209">-TechnicalTicketResourceId</span><span class="sxs-lookup"><span data-stu-id="87833-209">-TechnicalTicketResourceId</span></span>
<span data-ttu-id="87833-210">지원 티켓이 생성되는 Azure 서비스 리소스(예: 가상 머신 리소스 또는 HDInsight 리소스)의 리소스 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="87833-210">This is the resource id of the Azure service resource (For example: A virtual machine resource or an HDInsight resource) for which the support ticket is created.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateTechnicalSupportTicketWithContactObjectParameterSet, CreateTechnicalSupportTicketWithContactDetailParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="87833-211">-Title</span><span class="sxs-lookup"><span data-stu-id="87833-211">-Title</span></span>
<span data-ttu-id="87833-212">지원 티켓의 제목입니다.</span><span class="sxs-lookup"><span data-stu-id="87833-212">Title of support ticket.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="87833-213">-Confirm</span><span class="sxs-lookup"><span data-stu-id="87833-213">-Confirm</span></span>
<span data-ttu-id="87833-214">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="87833-214">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="87833-215">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="87833-215">-WhatIf</span></span>
<span data-ttu-id="87833-216">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="87833-216">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="87833-217">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="87833-217">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="87833-218">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="87833-218">CommonParameters</span></span>
<span data-ttu-id="87833-219">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="87833-219">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="87833-220">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="87833-220">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="87833-221">입력</span><span class="sxs-lookup"><span data-stu-id="87833-221">INPUTS</span></span>

### <span data-ttu-id="87833-222">없음</span><span class="sxs-lookup"><span data-stu-id="87833-222">None</span></span>

## <span data-ttu-id="87833-223">출력</span><span class="sxs-lookup"><span data-stu-id="87833-223">OUTPUTS</span></span>

### <span data-ttu-id="87833-224">Microsoft.Azure.Commands.Support.Models.PSSupportTicket</span><span class="sxs-lookup"><span data-stu-id="87833-224">Microsoft.Azure.Commands.Support.Models.PSSupportTicket</span></span>

## <span data-ttu-id="87833-225">참고 사항</span><span class="sxs-lookup"><span data-stu-id="87833-225">NOTES</span></span>

## <span data-ttu-id="87833-226">관련 링크</span><span class="sxs-lookup"><span data-stu-id="87833-226">RELATED LINKS</span></span>
