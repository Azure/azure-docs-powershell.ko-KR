---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Support.dll-Help.xml
Module Name: Az.Support
online version: https://docs.microsoft.com/en-us/powershell/module/az.support/new-azsupportticket
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Support/Support/help/New-AzSupportTicket.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Support/Support/help/New-AzSupportTicket.md
ms.openlocfilehash: 31e529ce30be608c5bd3167044b82f8094c1d248
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94212036"
---
# <span data-ttu-id="922fb-101">New-AzSupportTicket</span><span class="sxs-lookup"><span data-stu-id="922fb-101">New-AzSupportTicket</span></span>

## <span data-ttu-id="922fb-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="922fb-102">SYNOPSIS</span></span>
<span data-ttu-id="922fb-103">지원 티켓을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="922fb-103">Creates a support ticket.</span></span>

## <span data-ttu-id="922fb-104">구문과</span><span class="sxs-lookup"><span data-stu-id="922fb-104">SYNTAX</span></span>

### <span data-ttu-id="922fb-105">CreateSupportTicketWithContactDetailParameterSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="922fb-105">CreateSupportTicketWithContactDetailParameterSet (Default)</span></span>
```
New-AzSupportTicket -Name <String> -Title <String> -Description <String> -ProblemClassificationId <String>
 -Severity <Severity> -CustomerFirstName <String> -CustomerLastName <String>
 -PreferredContactMethod <ContactMethod> -CustomerPrimaryEmailAddress <String>
 [-AdditionalEmailAddress <String[]>] [-CustomerPhoneNumber <String>] -CustomerPreferredTimeZone <String>
 -CustomerCountry <String> -CustomerPreferredSupportLanguage <String> [-ProblemStartTime <DateTime>]
 [-CSPHomeTenantId <String>] [-Require24X7Response] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="922fb-106">CreateSupportTicketWithContactObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="922fb-106">CreateSupportTicketWithContactObjectParameterSet</span></span>
```
New-AzSupportTicket -Name <String> -Title <String> -Description <String> -ProblemClassificationId <String>
 -Severity <Severity> -CustomerContactDetail <PSContactProfile> [-ProblemStartTime <DateTime>]
 [-CSPHomeTenantId <String>] [-Require24X7Response] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="922fb-107">CreateTechnicalSupportTicketWithContactObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="922fb-107">CreateTechnicalSupportTicketWithContactObjectParameterSet</span></span>
```
New-AzSupportTicket -Name <String> -Title <String> -Description <String> -ProblemClassificationId <String>
 -Severity <Severity> -CustomerContactDetail <PSContactProfile> [-ProblemStartTime <DateTime>]
 -TechnicalTicketResourceId <String> [-CSPHomeTenantId <String>] [-Require24X7Response] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="922fb-108">CreateQuotaSupportTicketWithContactObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="922fb-108">CreateQuotaSupportTicketWithContactObjectParameterSet</span></span>
```
New-AzSupportTicket -Name <String> -Title <String> -Description <String> -ProblemClassificationId <String>
 -Severity <Severity> -CustomerContactDetail <PSContactProfile> [-ProblemStartTime <DateTime>]
 -QuotaTicketDetail <PSQuotaTicketDetail> [-CSPHomeTenantId <String>] [-Require24X7Response] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="922fb-109">CreateTechnicalSupportTicketWithContactDetailParameterSet</span><span class="sxs-lookup"><span data-stu-id="922fb-109">CreateTechnicalSupportTicketWithContactDetailParameterSet</span></span>
```
New-AzSupportTicket -Name <String> -Title <String> -Description <String> -ProblemClassificationId <String>
 -Severity <Severity> -CustomerFirstName <String> -CustomerLastName <String>
 -PreferredContactMethod <ContactMethod> -CustomerPrimaryEmailAddress <String>
 [-AdditionalEmailAddress <String[]>] [-CustomerPhoneNumber <String>] -CustomerPreferredTimeZone <String>
 -CustomerCountry <String> -CustomerPreferredSupportLanguage <String> [-ProblemStartTime <DateTime>]
 -TechnicalTicketResourceId <String> [-CSPHomeTenantId <String>] [-Require24X7Response] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="922fb-110">CreateQuotaSupportTicketWithContactDetailParameterSet</span><span class="sxs-lookup"><span data-stu-id="922fb-110">CreateQuotaSupportTicketWithContactDetailParameterSet</span></span>
```
New-AzSupportTicket -Name <String> -Title <String> -Description <String> -ProblemClassificationId <String>
 -Severity <Severity> -CustomerFirstName <String> -CustomerLastName <String>
 -PreferredContactMethod <ContactMethod> -CustomerPrimaryEmailAddress <String>
 [-AdditionalEmailAddress <String[]>] [-CustomerPhoneNumber <String>] -CustomerPreferredTimeZone <String>
 -CustomerCountry <String> -CustomerPreferredSupportLanguage <String> [-ProblemStartTime <DateTime>]
 -QuotaTicketDetail <PSQuotaTicketDetail> [-CSPHomeTenantId <String>] [-Require24X7Response] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="922fb-111">설명은</span><span class="sxs-lookup"><span data-stu-id="922fb-111">DESCRIPTION</span></span>
<span data-ttu-id="922fb-112">이 cmdlet을 사용 하 여 청구, 구독 관리, 할당량 또는 기술 문제에 대 한 지원 티켓을 만들 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="922fb-112">This cmdlet can be used to create a support ticket for Billing, Subscription Management, Quota or Technical issues.</span></span> <span data-ttu-id="922fb-113">Get-AzSupportService 및 Get-AzSupportProblemClassification cmdlet을 사용 하 여 Azure 서비스를 식별 하 고 지원 요청을 받을 각각의 해당 문제 분류입니다.</span><span class="sxs-lookup"><span data-stu-id="922fb-113">Use Get-AzSupportService and Get-AzSupportProblemClassification cmdlets to identify the Azure service and it's corresponding problem classifications respectively for which you want to request support.</span></span> <span data-ttu-id="922fb-114">다음 매개 변수를 지정 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="922fb-114">You must specify the following parameters:</span></span> 

    • Title
    • Description
    • Severity level
    • ProblemClassificationId
    • CustomerContactDetail (or individual customer contact parameters)

<span data-ttu-id="922fb-115">New-AzSupportContactProfileObject 도우미 cmdlet을 사용 하 여 Customer연락처 정보 개체를 만들 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="922fb-115">You can use New-AzSupportContactProfileObject helper cmdlet to create CustomerContactDetail object.</span></span>

<span data-ttu-id="922fb-116">클라우드 솔루션 공급자는 고객의 테 넌 트에 로그인 하 고 *CSPHomeTenantId* 매개 변수를 사용 하 여 홈 테 넌 트 id를 지정 하 여 고객의 구독에 대 한 지원 티켓을 만들 수 있습니다</span><span class="sxs-lookup"><span data-stu-id="922fb-116">Cloud Solution Providers can create a support ticket for their customer's subscriptions by logging into their customer's tenant and specifying their home tenant id using *CSPHomeTenantId* parameter.</span></span>

<span data-ttu-id="922fb-117">__기술 티켓:__</span><span class="sxs-lookup"><span data-stu-id="922fb-117">__For technical tickets:__</span></span>

<span data-ttu-id="922fb-118">리소스 이름을 지정 하려면 *TechnicalTicketResourceId* 매개 변수를 사용 하 여 리소스의 ARM 리소스 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="922fb-118">To specify the resource name, specify the ARM resource ID of the resource by using *TechnicalTicketResourceId* parameter.</span></span> <span data-ttu-id="922fb-119">아래 예제를 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="922fb-119">See an example below.</span></span> 

<span data-ttu-id="922fb-120">__할당량 티켓:__</span><span class="sxs-lookup"><span data-stu-id="922fb-120">__For quota tickets:__</span></span>

<span data-ttu-id="922fb-121">**계산 VM 코어** , **일괄 처리** , **Sql 데이터베이스** 및 **sql 데이터 웨어하우스의** 할당량 증가를 요청 하려면 *QuotaTicketDetail* 개체 아래에 추가 세부 정보를 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="922fb-121">To request for quota increase for **Compute VM Cores** , **Batch** , **SQL Database** and **SQL Data Warehouse** , provide additional details under *QuotaTicketDetail* object.</span></span> <span data-ttu-id="922fb-122">QuotaTicketDetail 개체는 아래 설명 된 대로 3 개의 속성으로 구성 됩니다.</span><span class="sxs-lookup"><span data-stu-id="922fb-122">QuotaTicketDetail object consists of 3 properties as described below.</span></span> <span data-ttu-id="922fb-123">자세한 내용은 [여기를 클릭 하세요.](https://aka.ms/supportrpquotarequestpayload)</span><span class="sxs-lookup"><span data-stu-id="922fb-123">For detailed documentation, please [click here.](https://aka.ms/supportrpquotarequestpayload)</span></span>

    • QuotaChangeRequestSubType

        This is required for certain quota types when there is a sub type that you are requesting quota increase for. Example: Batch, SQL Database and SQL Data Warehouse have a sub type.

    • QuotaChangeRequestVersion

        This is required and indicates the version of the quota change request payload.

    • QuotaChangeRequests

        This is required and is a list of PSQuotaChangeRequest objects. PSQuotaChangeRequest object has 2 required properties.

        ○ Region

            This is the Azure location or region for which you are requesting quota increase. This is the Location property of Get-AzLocation cmdlet.
        
        ○ Payload

            This is where you specify the new limits for the selected quota type.


<span data-ttu-id="922fb-124">다양 한 할당량 유형에 대 한 페이로드를 생성 하는 방법에 대 한 자세한 내용은 [여기를 클릭](https://aka.ms/supportrpquotarequestpayload) 하세요.</span><span class="sxs-lookup"><span data-stu-id="922fb-124">For detailed documentation on how to construct Payload for various quota types, please [click here](https://aka.ms/supportrpquotarequestpayload)</span></span>

## <span data-ttu-id="922fb-125">예제의</span><span class="sxs-lookup"><span data-stu-id="922fb-125">EXAMPLES</span></span>

### <span data-ttu-id="922fb-126">예제 1: 청구 또는 구독 관리 지원 티켓을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="922fb-126">Example 1: Create a Billing or Subscription Management support ticket.</span></span> <span data-ttu-id="922fb-127">Get-AzSupportService 및 Get-AzSupportProblemClassification을 사용 하 여 청구 또는 구독 관리 문제 분류에 대 한 올바른 Guid를 검색 하 여 지원을 요청 합니다.</span><span class="sxs-lookup"><span data-stu-id="922fb-127">Use Get-AzSupportService and Get-AzSupportProblemClassification to retrieve correct GUIDs for Billing or Subscription Management problem classification for which you want to request support</span></span> 
```powershell
PS C:\> New-AzSupportTicket -Name "test1" -Title "Test" -Description "Test" -Severity "minimal" -ProblemClassificationId "/providers/Microsoft.Support/services/{billing_service_guid}/problemClassifications/{problemClassification_guid}" -CustomerContactDetail @{FirstName = "first" ; LastName = "last" ; PreferredTimeZone = "pacific standard time" ; PreferredSupportLanguage = "en-us" ; Country = "USA" ; PreferredContactMethod = "Email" ; PrimaryEmailAddress = "user@contoso.com"}

Name  Title SupportTicketId Severity ServiceDisplayName Status CreatedDate
----  ----- --------------- -------- ------------------ ------ -----------
test1 Test  150010521000317 Minimal  Billing            Open   2/5/2020 1:33:53 AM
```

### <span data-ttu-id="922fb-128">예제 2: Windows 용 가상 컴퓨터 리소스에 대 한 기술 지원 티켓 만들기</span><span class="sxs-lookup"><span data-stu-id="922fb-128">Example 2: Create a technical support ticket for Virtual Machine for Windows resource.</span></span> <span data-ttu-id="922fb-129">Get-AzSupportService 및 Get-AzSupportProblemClassification을 사용 하 여 지원 요청에 대 한 Windows 용 가상 컴퓨터의 문제 분류에 대 한 올바른 Guid를 검색 합니다.</span><span class="sxs-lookup"><span data-stu-id="922fb-129">Use Get-AzSupportService and Get-AzSupportProblemClassification to retrieve correct GUIDs for Virtual Machine for Windows problem classification for which you want to request support</span></span> 
```powershell
PS C:\> New-AzSupportTicket -Name "test1" -Title "Test" -Description "Test" -Severity "minimal" -ProblemClassificationId "/providers/Microsoft.Support/services/{vm_windows_service_guid}/problemClassifications/{problemClassification_guid}" -TechnicalTicketResourceId "/subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/testRG/providers/Microsoft.Compute/virtualMachines/testVM" -CustomerContactDetail @{FirstName = "first" ; LastName = "last" ; PreferredTimeZone = "pacific standard time" ; PreferredSupportLanguage = "en-us" ; Country = "USA" ; PreferredContactMethod = "Email" ; PrimaryEmailAddress = "user@contoso.com"}

Name  Title SupportTicketId Severity ServiceDisplayName              Status CreatedDate
----  ----- --------------- -------- ------------------              ------ -----------
test1 Test  150010521000317 Minimal  Virtual Machine running Windows Open   2/5/2020 1:33:53 AM
```

### <span data-ttu-id="922fb-130">예제 3: 할당량 지원 티켓을 만들어 특정 VM 패밀리에 대 한 가상 머신 코어의 할당량을 늘립니다.</span><span class="sxs-lookup"><span data-stu-id="922fb-130">Example 3: Create a quota support ticket to increase quota for Virtual Machine Cores for a specific VM family.</span></span> <span data-ttu-id="922fb-131">Get-AzSupportService 및 Get-AzSupportProblemClassification을 사용 하 여 할당량 계산 VM 코어 문제 분류에 대 한 올바른 Guid를 검색 합니다.</span><span class="sxs-lookup"><span data-stu-id="922fb-131">Use Get-AzSupportService and Get-AzSupportProblemClassification to retrieve correct GUIDs for Quota Compute VM Cores problem classification.</span></span>
```powershell
PS C:\> New-AzSupportTicket -Name "test1" -Title "Test" -Description "Test" -Severity "minimal" -ProblemClassificationId "/providers/Microsoft.Support/services/{quota_service_guid}/problemClassifications/{cores_problemClassification_guid}" -QuotaTicketDetail @{QuotaChangeRequestVersion = "1.0" ; QuotaChangeRequests = (@{Region = "westus"; Payload = "{`"VMFamily`":`"Dv2 Series`",`"NewLimit`":350}"}, @{Region = "eastus"; Payload = "{`"VMFamily`":`"Dv2 Series`",`"NewLimit`":516}"})} -CustomerContactDetail @{FirstName = "first" ; LastName = "last" ; PreferredTimeZone = "pacific standard time" ; PreferredSupportLanguage = "en-us" ; Country = "USA" ; PreferredContactMethod = "Email" ; PrimaryEmailAddress = "user@contoso.com"}

Name  Title SupportTicketId Severity ServiceDisplayName                       Status CreatedDate
----  ----- --------------- -------- ------------------                       ------ -----------
test1 Test  150010521000317 Minimal  Service and subscription limits (quotas) Open   2/5/2020 1:33:53 AM
```

### <span data-ttu-id="922fb-132">예제 4: 일괄 처리 계정의 낮은 우선 순위의 코어에 대 한 할당량을 늘리는 할당량 지원 티켓을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="922fb-132">Example 4: Create a quota support ticket to increase quota for Low-priority cores for a Batch account.</span></span> <span data-ttu-id="922fb-133">Get-AzSupportService 및 Get-AzSupportProblemClassification을 사용 하 여 할당량 일괄 처리 문제 분류에 대 한 올바른 Guid를 검색 합니다.</span><span class="sxs-lookup"><span data-stu-id="922fb-133">Use Get-AzSupportService and Get-AzSupportProblemClassification to retrieve correct GUIDs for Quota Batch problem classification.</span></span>
```powershell
PS C:\> New-AzSupportTicket -Name "test1" -Title "Test" -Description "Test" -Severity "minimal" -ProblemClassificationId "/providers/Microsoft.Support/services/{quota_service_guid}/problemClassifications/{batch_problemClassification_guid}" -QuotaTicketDetail @{QuotaChangeRequestVersion = "1.0" ; QuotaChangeRequestSubType = "Account" ; QuotaChangeRequests = (@{Region = "westus"; Payload = "{`"AccountName`":`"test`",`"NewLimit`":200,`"Type`":`"LowPriority`"}"})} -CustomerContactDetail @{FirstName = "first" ; LastName = "last" ; PreferredTimeZone = "pacific standard time" ; PreferredSupportLanguage = "en-us" ; Country = "USA" ; PreferredContactMethod = "Email" ; PrimaryEmailAddress = "user@contoso.com"}

Name  Title SupportTicketId Severity ServiceDisplayName                       Status CreatedDate
----  ----- --------------- -------- ------------------                       ------ -----------
test1 Test  150010521000317 Minimal  Service and subscription limits (quotas) Open   2/5/2020 1:33:53 AM
```

### <span data-ttu-id="922fb-134">예제 5: 일괄 처리 계정에 대 한 특정 VM 패밀리에 대 한 VM 코어 할당량을 늘리기 위한 할당량 지원 티켓 만들기</span><span class="sxs-lookup"><span data-stu-id="922fb-134">Example 5: Create a quota support ticket to increase VM cores quota for a specific VM Family for a Batch account.</span></span> <span data-ttu-id="922fb-135">Get-AzSupportService 및 Get-AzSupportProblemClassification을 사용 하 여 할당량 일괄 처리 문제 분류에 대 한 올바른 Guid를 검색 합니다.</span><span class="sxs-lookup"><span data-stu-id="922fb-135">Use Get-AzSupportService and Get-AzSupportProblemClassification to retrieve correct GUIDs for Quota Batch problem classification.</span></span>
```powershell
PS C:\> New-AzSupportTicket -Name "test1" -Title "Test" -Description "Test" -Severity "minimal" -ProblemClassificationId "/providers/Microsoft.Support/services/{quota_service_guid}/problemClassifications/{batch_problemClassification_guid}" -QuotaTicketDetail @{QuotaChangeRequestVersion = "1.0" ; QuotaChangeRequestSubType = "Account" ; QuotaChangeRequests = (@{Region = "westus"; Payload = "{`"AccountName`":`"test`",`"VMFamily`":`"standardA0_A7Family`",`"NewLimit`":200,`"Type`":`"Dedicated`"}"})} -CustomerContactDetail @{FirstName = "first" ; LastName = "last" ; PreferredTimeZone = "pacific standard time" ; PreferredSupportLanguage = "en-us" ; Country = "USA" ; PreferredContactMethod = "Email" ; PrimaryEmailAddress = "user@contoso.com"}

Name  Title SupportTicketId Severity ServiceDisplayName                       Status CreatedDate
----  ----- --------------- -------- ------------------                       ------ -----------
test1 Test  150010521000317 Minimal  Service and subscription limits (quotas) Open   2/5/2020 1:33:53 AM
```

### <span data-ttu-id="922fb-136">예제 6: 일괄 처리 계정에 대 한 풀 할당량을 늘리려면 할당량 지원 티켓을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="922fb-136">Example 6: Create a quota support ticket to increase Pools quota for a Batch account.</span></span> <span data-ttu-id="922fb-137">Get-AzSupportService 및 Get-AzSupportProblemClassification을 사용 하 여 할당량 일괄 처리 문제 분류에 대 한 올바른 Guid를 검색 합니다.</span><span class="sxs-lookup"><span data-stu-id="922fb-137">Use Get-AzSupportService and Get-AzSupportProblemClassification to retrieve correct GUIDs for Quota Batch problem classification.</span></span>
```powershell
PS C:\> New-AzSupportTicket -Name "test1" -Title "Test" -Description "Test" -Severity "minimal" -ProblemClassificationId "/providers/Microsoft.Support/services/{quota_service_guid}/problemClassifications/{batch_problemClassification_guid}" -QuotaTicketDetail @{QuotaChangeRequestVersion = "1.0" ; QuotaChangeRequestSubType = "Account" ; QuotaChangeRequests = (@{Region = "westus"; Payload = "{`"AccountName`":`"test`",`"NewLimit`":120,`"Type`":`"Pools`"}"})} -CustomerContactDetail @{FirstName = "first" ; LastName = "last" ; PreferredTimeZone = "pacific standard time" ; PreferredSupportLanguage = "en-us" ; Country = "USA" ; PreferredContactMethod = "Email" ; PrimaryEmailAddress = "user@contoso.com"}

Name  Title SupportTicketId Severity ServiceDisplayName                       Status CreatedDate
----  ----- --------------- -------- ------------------                       ------ -----------
test1 Test  150010521000317 Minimal  Service and subscription limits (quotas) Open   2/5/2020 1:33:53 AM
```

### <span data-ttu-id="922fb-138">예제 7: 할당량 지원 티켓을 만들어 일괄 처리 계정에 대 한 활성 작업 및 작업 일정 할당량을 늘립니다.</span><span class="sxs-lookup"><span data-stu-id="922fb-138">Example 7: Create a quota support ticket to increase active Jobs and job schedules quota for a Batch account.</span></span> <span data-ttu-id="922fb-139">Get-AzSupportService 및 Get-AzSupportProblemClassification을 사용 하 여 할당량 일괄 처리 문제 분류에 대 한 올바른 Guid를 검색 합니다.</span><span class="sxs-lookup"><span data-stu-id="922fb-139">Use Get-AzSupportService and Get-AzSupportProblemClassification to retrieve correct GUIDs for Quota Batch problem classification.</span></span>
```powershell
PS C:\> New-AzSupportTicket -Name "test1" -Title "Test" -Description "Test" -Severity "minimal" -ProblemClassificationId "/providers/Microsoft.Support/services/{quota_service_guid}/problemClassifications/{batch_problemClassification_guid}" -QuotaTicketDetail @{QuotaChangeRequestVersion = "1.0" ; QuotaChangeRequestSubType = "Account" ; QuotaChangeRequests = (@{Region = "westus"; Payload = "{`"AccountName`":`"test`",`"NewLimit`":120,`"Type`":`"Jobs`"}"})} -CustomerContactDetail @{FirstName = "first" ; LastName = "last" ; PreferredTimeZone = "pacific standard time" ; PreferredSupportLanguage = "en-us" ; Country = "USA" ; PreferredContactMethod = "Email" ; PrimaryEmailAddress = "user@contoso.com"}

Name  Title SupportTicketId Severity ServiceDisplayName                       Status CreatedDate
----  ----- --------------- -------- ------------------                       ------ -----------
test1 Test  150010521000317 Minimal  Service and subscription limits (quotas) Open   2/5/2020 1:33:53 AM
```

### <span data-ttu-id="922fb-140">예제 8: 구독에 대 한 일괄 처리 계정 수를 늘리려면 할당량 지원 티켓을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="922fb-140">Example 8: Create a quota support ticket to increase number of Batch accounts for a subscription.</span></span> <span data-ttu-id="922fb-141">Get-AzSupportService 및 Get-AzSupportProblemClassification을 사용 하 여 할당량 일괄 처리 문제 분류에 대 한 올바른 Guid를 검색 합니다.</span><span class="sxs-lookup"><span data-stu-id="922fb-141">Use Get-AzSupportService and Get-AzSupportProblemClassification to retrieve correct GUIDs for Quota Batch problem classification.</span></span>
```powershell
PS C:\> New-AzSupportTicket -Name "test1" -Title "Test" -Description "Test" -Severity "minimal" -ProblemClassificationId "/providers/Microsoft.Support/services/{quota_service_guid}/problemClassifications/{batch_problemClassification_guid}" -QuotaTicketDetail @{QuotaChangeRequestVersion = "1.0" ; QuotaChangeRequestSubType = "Subscription" ; QuotaChangeRequests = (@{Region = "westus"; Payload = "{`"NewLimit`":120,`"Type`":`"Account`"}"})} -CustomerContactDetail @{FirstName = "first" ; LastName = "last" ; PreferredTimeZone = "pacific standard time" ; PreferredSupportLanguage = "en-us" ; Country = "USA" ; PreferredContactMethod = "Email" ; PrimaryEmailAddress = "user@contoso.com"}

Name  Title SupportTicketId Severity ServiceDisplayName                       Status CreatedDate
----  ----- --------------- -------- ------------------                       ------ -----------
test1 Test  150010521000317 Minimal  Service and subscription limits (quotas) Open   2/5/2020 1:33:53 AM
```

### <span data-ttu-id="922fb-142">예제 9: SQL 데이터베이스용 Dtu에 대 한 할당량을 늘리기 위한 할당량 지원 티켓 만들기</span><span class="sxs-lookup"><span data-stu-id="922fb-142">Example 9: Create a quota support ticket to increase quota for DTUs for SQL Database.</span></span> <span data-ttu-id="922fb-143">Get-AzSupportService 및 Get-AzSupportProblemClassification을 사용 하 여 할당량 SQL 데이터베이스 문제 분류에 대 한 올바른 Guid를 검색 합니다.</span><span class="sxs-lookup"><span data-stu-id="922fb-143">Use Get-AzSupportService and Get-AzSupportProblemClassification to retrieve correct GUIDs for Quota SQL Database problem classification.</span></span>
```powershell
PS C:\> New-AzSupportTicket -Name "test1" -Title "Test" -Description "Test" -Severity "minimal" -ProblemClassificationId "/providers/Microsoft.Support/services/{quota_service_guid}/problemClassifications/{sql_database_problemClassification_guid}" -QuotaTicketDetail @{QuotaChangeRequestVersion = "1.0" ; QuotaChangeRequestSubType = "DTUs" ; QuotaChangeRequests = (@{Region = "westus"; Payload = "{`"ServerName`":`"testserver`",`"NewLimit`":54000}"})} -CustomerContactDetail @{FirstName = "first" ; LastName = "last" ; PreferredTimeZone = "pacific standard time" ; PreferredSupportLanguage = "en-us" ; Country = "USA" ; PreferredContactMethod = "Email" ; PrimaryEmailAddress = "user@contoso.com"}

Name  Title SupportTicketId Severity ServiceDisplayName                       Status CreatedDate
----  ----- --------------- -------- ------------------                       ------ -----------
test1 Test  150010521000317 Minimal  Service and subscription limits (quotas) Open   2/5/2020 1:33:53 AM
```

### <span data-ttu-id="922fb-144">예제 10: SQL 데이터베이스용 서버의 할당량을 늘리려면 할당량 지원 티켓을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="922fb-144">Example 10: Create a quota support ticket to increase quota for Servers for SQL Database.</span></span> <span data-ttu-id="922fb-145">Get-AzSupportService 및 Get-AzSupportProblemClassification을 사용 하 여 할당량 SQL 데이터베이스 문제 분류에 대 한 올바른 Guid를 검색 합니다.</span><span class="sxs-lookup"><span data-stu-id="922fb-145">Use Get-AzSupportService and Get-AzSupportProblemClassification to retrieve correct GUIDs for Quota SQL Database problem classification.</span></span>
```powershell
PS C:\> New-AzSupportTicket -Name "test1" -Title "Test" -Description "Test" -Severity "minimal" -ProblemClassificationId "/providers/Microsoft.Support/services/{quota_service_guid}/problemClassifications/{sql_database_problemClassification_guid}" -QuotaTicketDetail @{QuotaChangeRequestVersion = "1.0" ; QuotaChangeRequestSubType = "Servers" ; QuotaChangeRequests = (@{Region = "westus"; Payload = "{`"NewLimit`":200}"})} -CustomerContactDetail @{FirstName = "first" ; LastName = "last" ; PreferredTimeZone = "pacific standard time" ; PreferredSupportLanguage = "en-us" ; Country = "USA" ; PreferredContactMethod = "Email" ; PrimaryEmailAddress = "user@contoso.com"}

Name  Title SupportTicketId Severity ServiceDisplayName                       Status CreatedDate
----  ----- --------------- -------- ------------------                       ------ -----------
test1 Test  150010521000317 Minimal  Service and subscription limits (quotas) Open   2/5/2020 1:33:53 AM
```

### <span data-ttu-id="922fb-146">예제 11: SQL 데이터 웨어하우스에 대 한 Dtu 할당량을 늘리기 위한 할당량 지원 티켓을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="922fb-146">Example 11: Create a quota support ticket to increase quota for DTUs for SQL Data Warehouse.</span></span> <span data-ttu-id="922fb-147">Get-AzSupportService 및 Get-AzSupportProblemClassification을 사용 하 여 할당량 SQL 날짜 웨어하우스 문제 분류에 대 한 올바른 Guid를 검색 합니다.</span><span class="sxs-lookup"><span data-stu-id="922fb-147">Use Get-AzSupportService and Get-AzSupportProblemClassification to retrieve correct GUIDs for Quota SQL Date Warehouse problem classification.</span></span>
```powershell
PS C:\> New-AzSupportTicket -Name "test1" -Title "Test" -Description "Test" -Severity "minimal" -ProblemClassificationId "/providers/Microsoft.Support/services/{quota_service_guid}/problemClassifications/{sql_datawarehouse_problemClassification_guid}" -QuotaTicketDetail @{QuotaChangeRequestVersion = "1.0" ; QuotaChangeRequestSubType = "DTUs" ; QuotaChangeRequests = (@{Region = "westus"; Payload = "{`"ServerName`":`"testserver`",`"NewLimit`":54000}"})} -CustomerContactDetail @{FirstName = "first" ; LastName = "last" ; PreferredTimeZone = "pacific standard time" ; PreferredSupportLanguage = "en-us" ; Country = "USA" ; PreferredContactMethod = "Email" ; PrimaryEmailAddress = "user@contoso.com"}

Name  Title SupportTicketId Severity ServiceDisplayName                       Status CreatedDate
----  ----- --------------- -------- ------------------                       ------ -----------
test1 Test  150010521000317 Minimal  Service and subscription limits (quotas) Open   2/5/2020 1:33:53 AM
```

### <span data-ttu-id="922fb-148">예제 12: SQL 데이터 웨어하우스의 서버 할당량을 늘리기 위한 할당량 지원 티켓을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="922fb-148">Example 12: Create a quota support ticket to increase quota for Servers for SQL Data Warehouse.</span></span> <span data-ttu-id="922fb-149">Get-AzSupportService 및 Get-AzSupportProblemClassification을 사용 하 여 할당량 SQL 데이터 웨어하우스 문제 분류에 대 한 올바른 Guid를 검색 합니다.</span><span class="sxs-lookup"><span data-stu-id="922fb-149">Use Get-AzSupportService and Get-AzSupportProblemClassification to retrieve correct GUIDs for Quota SQL Data Warehouse problem classification.</span></span>
```powershell
PS C:\> New-AzSupportTicket -Name "test1" -Title "Test" -Description "Test" -Severity "minimal" -ProblemClassificationId "/providers/Microsoft.Support/services/{quota_service_guid}/problemClassifications/{sql_datawarehouse_problemClassification_guid}" -QuotaTicketDetail @{QuotaChangeRequestVersion = "1.0" ; QuotaChangeRequestSubType = "Servers" ; QuotaChangeRequests = (@{Region = "westus"; Payload = "{`"NewLimit`":200}"})} -CustomerContactDetail @{FirstName = "first" ; LastName = "last" ; PreferredTimeZone = "pacific standard time" ; PreferredSupportLanguage = "en-us" ; Country = "USA" ; PreferredContactMethod = "Email" ; PrimaryEmailAddress = "user@contoso.com"}

Name  Title SupportTicketId Severity ServiceDisplayName                       Status CreatedDate
----  ----- --------------- -------- ------------------                       ------ -----------
test1 Test  150010521000317 Minimal  Service and subscription limits (quotas) Open   2/5/2020 1:33:53 AM
```

### <span data-ttu-id="922fb-150">예제 13: 기계 학습 서비스에 대 한 낮은 우선 순위의 코어의 할당량을 늘리려면 할당량 지원 티켓을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="922fb-150">Example 13: Create a quota support ticket to increase quota for Low-priority cores for Machine Learning service.</span></span> <span data-ttu-id="922fb-151">Get-AzSupportService 및 Get-AzSupportProblemClassification을 사용 하 여 할당량 기계 학습 서비스 문제 분류에 대 한 올바른 Guid를 검색 합니다.</span><span class="sxs-lookup"><span data-stu-id="922fb-151">Use Get-AzSupportService and Get-AzSupportProblemClassification to retrieve correct GUIDs for Quota Machine Learning service problem classification.</span></span>
```powershell
PS C:\> New-AzSupportTicket -Name "test1" -Title "Test" -Description "Test" -Severity "minimal" -ProblemClassificationId "/providers/Microsoft.Support/services/{quota_service_guid}/problemClassifications/{machine_learning_service_problemClassification_guid}" -QuotaTicketDetail @{QuotaChangeRequestVersion = "1.0" ; QuotaChangeRequestSubType = "BatchAml" ; QuotaChangeRequests = (@{Region = "westus"; Payload = "{`"NewLimit`":200,`"Type`":`"LowPriority`" }"})} -CustomerContactDetail @{FirstName = "first" ; LastName = "last" ; PreferredTimeZone = "pacific standard time" ; PreferredSupportLanguage = "en-us" ; Country = "USA" ; PreferredContactMethod = "Email" ; PrimaryEmailAddress = "user@contoso.com"}

Name  Title SupportTicketId Severity ServiceDisplayName                       Status CreatedDate
----  ----- --------------- -------- ------------------                       ------ -----------
test1 Test  150010521000317 Minimal  Service and subscription limits (quotas) Open   2/5/2020 1:33:53 AM
```

### <span data-ttu-id="922fb-152">예 14: 기계 학습 서비스의 특정 VM 패밀리에 대 한 VM 코어 할당량을 늘리기 위한 할당량 지원 티켓을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="922fb-152">Example 14: Create a quota support ticket to increase VM cores quota for a specific VM Family for Machine Learning service.</span></span> <span data-ttu-id="922fb-153">Get-AzSupportService 및 Get-AzSupportProblemClassification을 사용 하 여 할당량 기계 학습 서비스 문제 분류에 대 한 올바른 Guid를 검색 합니다.</span><span class="sxs-lookup"><span data-stu-id="922fb-153">Use Get-AzSupportService and Get-AzSupportProblemClassification to retrieve correct GUIDs for Quota Machine Learning service problem classification.</span></span>
```powershell
PS C:\> New-AzSupportTicket -Name "test1" -Title "Test" -Description "Test" -Severity "minimal" -ProblemClassificationId "/providers/Microsoft.Support/services/{quota_service_guid}/problemClassifications/{machine_learning_service_problemClassification_guid}" -QuotaTicketDetail @{QuotaChangeRequestVersion = "1.0" ; QuotaChangeRequestSubType = "BatchAml" ; QuotaChangeRequests = (@{Region = "westus"; Payload = "{`"VMFamily`":`"standardDFamily`",`"NewLimit`":200,`"Type`":`"Dedicated`" }"})} -CustomerContactDetail @{FirstName = "first" ; LastName = "last" ; PreferredTimeZone = "pacific standard time" ; PreferredSupportLanguage = "en-us" ; Country = "USA" ; PreferredContactMethod = "Email" ; PrimaryEmailAddress = "user@contoso.com"}

Name  Title SupportTicketId Severity ServiceDisplayName                       Status CreatedDate
----  ----- --------------- -------- ------------------                       ------ -----------
test1 Test  150010521000317 Minimal  Service and subscription limits (quotas) Open   2/5/2020 1:33:53 AM
```

### <span data-ttu-id="922fb-154">예 15: Azure SQL 관리 인스턴스의 할당량을 늘리려면 할당량 지원 티켓을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="922fb-154">Example 15: Create a quota support ticket to increase quota for Azure SQL Managed Instance.</span></span> <span data-ttu-id="922fb-155">Get-AzSupportService 및 Get-AzSupportProblemClassification을 사용 하 여 할당량 SQL 관리 되는 인스턴스 서비스 문제 분류에 대 한 올바른 Guid를 검색 합니다.</span><span class="sxs-lookup"><span data-stu-id="922fb-155">Use Get-AzSupportService and Get-AzSupportProblemClassification to retrieve correct GUIDs for Quota SQL Managed Instance service problem classification.</span></span>
```powershell
PS C:\> New-AzSupportTicket -Name "test1" -Title "Test" -Description "Test" -Severity "minimal" -ProblemClassificationId "/providers/Microsoft.Support/services/{quota_service_guid}/problemClassifications/{sql_managed_instance_problemClassification_guid}" -QuotaTicketDetail @{QuotaChangeRequestVersion = "1.0" ; QuotaChangeRequestSubType = "SQLMI" ; QuotaChangeRequests = (@{Region = "westus"; Payload = "{`"NewLimit`":200,`"Type`":`"vCore`" }"}, @{Region = "westus"; Payload = "{`"NewLimit`":200,`"Type`":`"Subnet`" }"})} -CustomerContactDetail @{FirstName = "first" ; LastName = "last" ; PreferredTimeZone = "pacific standard time" ; PreferredSupportLanguage = "en-us" ; Country = "USA" ; PreferredContactMethod = "Email" ; PrimaryEmailAddress = "user@contoso.com"}

Name  Title SupportTicketId Severity ServiceDisplayName                       Status CreatedDate
----  ----- --------------- -------- ------------------                       ------ -----------
test1 Test  150010521000317 Minimal  Service and subscription limits (quotas) Open   2/5/2020 1:33:53 AM
```

### <span data-ttu-id="922fb-156">예제 16: Customer연락처 정보 개체 대신 개별 고객 연락처 매개 변수를 지정 하 여 지원 티켓을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="922fb-156">Example 16: Create a support ticket by specifying individual customer contact parameters instead of CustomerContactDetail object.</span></span> 
```powershell
PS C:\> New-AzSupportTicket -Name "test1" -Title "Test" -Description "Test" -Severity "minimal" -ProblemClassificationId "/providers/Microsoft.Support/services/{billing_service_guid}/problemClassifications/{problemClassification_guid}" -CustomerFirstName "first" -CustomerLastName "last" -CustomerPreferredTimeZone "pacific standard time" -CustomerPreferredSupportLanguage "en-us" -CustomerCountry = "USA" -PreferredContactMethod "Email" -CustomerPrimaryEmailAddress "user@contoso.com"

Name  Title SupportTicketId Severity ServiceDisplayName Status CreatedDate
----  ----- --------------- -------- ------------------ ------ -----------
test1 Test  150010521000317 Minimal  Billing            Open   2/5/2020 1:33:53 AM
```

### <span data-ttu-id="922fb-157">예제 17: Azure에서 24 x 7 응답을 요청 하 여 지원 티켓을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="922fb-157">Example 17: Create a support ticket with request for 24 x 7 response from Azure.</span></span> 
```powershell
PS C:\> New-AzSupportTicket -Name "test1" -Title "Test" -Description "Test" -Severity "critical" -ProblemClassificationId "/providers/Microsoft.Support/services/{billing_service_guid}/problemClassifications/{problemClassification_guid}" -CustomerFirstName "first" -CustomerLastName "last" -CustomerPreferredTimeZone "pacific standard time" -CustomerPreferredSupportLanguage "en-us" -CustomerCountry = "USA" -PreferredContactMethod "Email" -CustomerPrimaryEmailAddress "user@contoso.com" -Require24X7Response 

Name  Title SupportTicketId Severity ServiceDisplayName Status CreatedDate
----  ----- --------------- -------- ------------------ ------ -----------
test1 Test  150010521000317 Critical  Billing            Open   2/5/2020 1:33:53 AM
```

### <span data-ttu-id="922fb-158">예제 18: CSP (Cloud Solution Provider) 인 경우 고객을 대신 하 여 지원 티켓을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="922fb-158">Example 18: Create a support ticket on behalf of your customer if you are a Cloud Solution Provider (CSP).</span></span> <span data-ttu-id="922fb-159">CSP는 먼저 테 넌 트에 로그인 한 후 아래 예제에 표시 된 대로 고객의 테 넌 트에 로그인 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="922fb-159">CSP should first login into their tenant, and then login into customer's tenant as shown in the example below.</span></span> <span data-ttu-id="922fb-160">그런 다음 지원 티켓을 만들 때-CSPHomeTenantId 매개 변수를 사용 하 여 홈 테 넌 트 id를 지정 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="922fb-160">They must then use -CSPHomeTenantId parameter to specify their home tenant id at the time of creating a support ticket.</span></span>  
```powershell

PS C:\> Login-AzAccount

PS C:\> Login-AzAccount -TenantId {customer_tenant_id}

PS C:\> New-AzSupportTicket -Name "test1" -Title "Test" -Description "Test" -Severity "minimal" -ProblemClassificationId "/providers/Microsoft.Support/services/{billing_service_guid}/problemClassifications/{problemClassification_guid}" -CustomerFirstName "first" -CustomerLastName "last" -CustomerPreferredTimeZone "pacific standard time" -CustomerPreferredSupportLanguage "en-us" -CustomerCountry = "USA" -PreferredContactMethod "Email" -CustomerPrimaryEmailAddress "user@contoso.com" -CSPHomeTenantId {csp_home_tenant_id} 

Name  Title SupportTicketId Severity ServiceDisplayName Status CreatedDate
----  ----- --------------- -------- ------------------ ------ -----------
test1 Test  150010521000317 Minimal  Billing            Open   2/5/2020 1:33:53 AM
```

## <span data-ttu-id="922fb-161">변수</span><span class="sxs-lookup"><span data-stu-id="922fb-161">PARAMETERS</span></span>

### <span data-ttu-id="922fb-162">-AdditionalEmailAddress</span><span class="sxs-lookup"><span data-stu-id="922fb-162">-AdditionalEmailAddress</span></span>
<span data-ttu-id="922fb-163">추가 전자 메일 주소입니다.</span><span class="sxs-lookup"><span data-stu-id="922fb-163">Additional email addresses.</span></span>
<span data-ttu-id="922fb-164">여기에 나열 된 전자 메일 주소는 지원 티켓에 대 한 모든 서신에 복사 됩니다.</span><span class="sxs-lookup"><span data-stu-id="922fb-164">Email addresses listed here will be copied on any correspondence about the support ticket.</span></span>

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

### <span data-ttu-id="922fb-165">-AsJob</span><span class="sxs-lookup"><span data-stu-id="922fb-165">-AsJob</span></span>
<span data-ttu-id="922fb-166">백그라운드에서 cmdlet을 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="922fb-166">Run cmdlet in the background.</span></span>

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

### <span data-ttu-id="922fb-167">-CSPHomeTenantId</span><span class="sxs-lookup"><span data-stu-id="922fb-167">-CSPHomeTenantId</span></span>
<span data-ttu-id="922fb-168">클라우드 솔루션 공급자 사용자의 홈 테 넌 트 id로, 고객에 대 한 지원 티켓을 만들려고 합니다.</span><span class="sxs-lookup"><span data-stu-id="922fb-168">This is the home tenant id of the Cloud Solution Provider user trying to create a support ticket for their customer.</span></span>

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

### <span data-ttu-id="922fb-169">-Customer연락처 세부 정보</span><span class="sxs-lookup"><span data-stu-id="922fb-169">-CustomerContactDetail</span></span>
<span data-ttu-id="922fb-170">지원 티켓 리소스와 연결 된 고객 연락처 정보입니다.</span><span class="sxs-lookup"><span data-stu-id="922fb-170">Customer contact details associated with SupportTicket resource.</span></span>

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

### <span data-ttu-id="922fb-171">-고객 국가</span><span class="sxs-lookup"><span data-stu-id="922fb-171">-CustomerCountry</span></span>
<span data-ttu-id="922fb-172">고객 국가.</span><span class="sxs-lookup"><span data-stu-id="922fb-172">Customer country.</span></span>
<span data-ttu-id="922fb-173">유효한 ISO Alpha-3 국가 코드 (ISO 3166) 여야 합니다.</span><span class="sxs-lookup"><span data-stu-id="922fb-173">This must be a valid ISO Alpha-3 country code (ISO 3166).</span></span>

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

### <span data-ttu-id="922fb-174">-CustomerFirstName</span><span class="sxs-lookup"><span data-stu-id="922fb-174">-CustomerFirstName</span></span>
<span data-ttu-id="922fb-175">고객 성.</span><span class="sxs-lookup"><span data-stu-id="922fb-175">Customer first name.</span></span>

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

### <span data-ttu-id="922fb-176">-CustomerLastName</span><span class="sxs-lookup"><span data-stu-id="922fb-176">-CustomerLastName</span></span>
<span data-ttu-id="922fb-177">고객 성.</span><span class="sxs-lookup"><span data-stu-id="922fb-177">Customer last name.</span></span>

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

### <span data-ttu-id="922fb-178">-CustomerPhoneNumber</span><span class="sxs-lookup"><span data-stu-id="922fb-178">-CustomerPhoneNumber</span></span>
<span data-ttu-id="922fb-179">고객 전화 번호입니다.</span><span class="sxs-lookup"><span data-stu-id="922fb-179">Customer phone number.</span></span>
<span data-ttu-id="922fb-180">이는 기본 연락 방법이 휴대폰 인 경우 필요 합니다.</span><span class="sxs-lookup"><span data-stu-id="922fb-180">This is required if preferred contact method is phone.</span></span>

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

### <span data-ttu-id="922fb-181">-CustomerPreferredSupportLanguage</span><span class="sxs-lookup"><span data-stu-id="922fb-181">-CustomerPreferredSupportLanguage</span></span>
<span data-ttu-id="922fb-182">Peferred 사용자 지정의 언어입니다.</span><span class="sxs-lookup"><span data-stu-id="922fb-182">Peferred language of the custom.</span></span>
<span data-ttu-id="922fb-183">여기에 나열 된 지원 언어 중 하나에 대 한 올바른 언어 contry 코드 여야 합니다 https://azure.microsoft.com/en-us/support/faq/ .</span><span class="sxs-lookup"><span data-stu-id="922fb-183">This must be a valid language-contry code for one of the supported languages listed here https://azure.microsoft.com/en-us/support/faq/.</span></span>

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

### <span data-ttu-id="922fb-184">-CustomerPreferredTimeZone</span><span class="sxs-lookup"><span data-stu-id="922fb-184">-CustomerPreferredTimeZone</span></span>
<span data-ttu-id="922fb-185">고객 기본 설정 표준 시간대</span><span class="sxs-lookup"><span data-stu-id="922fb-185">Customer preferred time zone.</span></span>
<span data-ttu-id="922fb-186">유효한 System.TimeZoneInfo.Id 값 이어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="922fb-186">This must be a valid System.TimeZoneInfo.Id value.</span></span>

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

### <span data-ttu-id="922fb-187">-CustomerPrimaryEmailAddress</span><span class="sxs-lookup"><span data-stu-id="922fb-187">-CustomerPrimaryEmailAddress</span></span>
<span data-ttu-id="922fb-188">고객 기본 전자 메일 주소입니다.</span><span class="sxs-lookup"><span data-stu-id="922fb-188">Customer primary email address.</span></span>

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

### <span data-ttu-id="922fb-189">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="922fb-189">-DefaultProfile</span></span>
<span data-ttu-id="922fb-190">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="922fb-190">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="922fb-191">-설명</span><span class="sxs-lookup"><span data-stu-id="922fb-191">-Description</span></span>
<span data-ttu-id="922fb-192">질문 또는 문제에 대 한 자세한 설명입니다.</span><span class="sxs-lookup"><span data-stu-id="922fb-192">Detailed description of the question or issue.</span></span>

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

### <span data-ttu-id="922fb-193">-이름</span><span class="sxs-lookup"><span data-stu-id="922fb-193">-Name</span></span>
<span data-ttu-id="922fb-194">이 cmdlet이 만드는 지원 티켓의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="922fb-194">Name of support ticket that this cmdlet creates.</span></span>

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

### <span data-ttu-id="922fb-195">-PreferredContactMethod</span><span class="sxs-lookup"><span data-stu-id="922fb-195">-PreferredContactMethod</span></span>
<span data-ttu-id="922fb-196">선호 연락 방법.</span><span class="sxs-lookup"><span data-stu-id="922fb-196">Preferred contact method.</span></span>

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

### <span data-ttu-id="922fb-197">-ProblemClassificationId</span><span class="sxs-lookup"><span data-stu-id="922fb-197">-ProblemClassificationId</span></span>
<span data-ttu-id="922fb-198">각 Azure 서비스에는 발생 하는 문제 유형에 해당 하는 문제 분류 라는 고유한 문제 범주가 있습니다.</span><span class="sxs-lookup"><span data-stu-id="922fb-198">Each Azure service has its own set of issue category called problem classification that corresponds to the type of problem you're experiencing.</span></span>
<span data-ttu-id="922fb-199">이 매개 변수는 ProblemClassification 리소스의 ARM 리소스 id입니다.</span><span class="sxs-lookup"><span data-stu-id="922fb-199">This parameter is the ARM resource id of ProblemClassification resource.</span></span>

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

### <span data-ttu-id="922fb-200">-ProblemStartTime</span><span class="sxs-lookup"><span data-stu-id="922fb-200">-ProblemStartTime</span></span>
<span data-ttu-id="922fb-201">문제가 시작 된 날짜 및 시간입니다.</span><span class="sxs-lookup"><span data-stu-id="922fb-201">Date and time when the problem started.</span></span>

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

### <span data-ttu-id="922fb-202">-QuotaTicketDetail</span><span class="sxs-lookup"><span data-stu-id="922fb-202">-QuotaTicketDetail</span></span>
<span data-ttu-id="922fb-203">할당량 지원 티켓에 대 한 추가 정보입니다.</span><span class="sxs-lookup"><span data-stu-id="922fb-203">Additional details for a Quota support ticket.</span></span>

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

### <span data-ttu-id="922fb-204">-Require24X7Response</span><span class="sxs-lookup"><span data-stu-id="922fb-204">-Require24X7Response</span></span>
<span data-ttu-id="922fb-205">이 지원 티켓에 Azure에서 24 시간 응답을 요구 하는지 여부를 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="922fb-205">Indicates if this support ticket requires a 24x7 response from Azure.</span></span>

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

### <span data-ttu-id="922fb-206">-심각도</span><span class="sxs-lookup"><span data-stu-id="922fb-206">-Severity</span></span>
<span data-ttu-id="922fb-207">지원 티켓의 심각도입니다.</span><span class="sxs-lookup"><span data-stu-id="922fb-207">Severity of the support ticket.</span></span>
<span data-ttu-id="922fb-208">이는 서비스 케이스의 긴급성을 나타내며, Azure와 함께 사용 하는 기술 지원 계획의 서비스 수준 계약에 따라 응답 시간을 결정 합니다.</span><span class="sxs-lookup"><span data-stu-id="922fb-208">This indicates the urgency of the case, which in turn determines the response time according to the service level agreement of the technical support plan you have with Azure.</span></span>

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

### <span data-ttu-id="922fb-209">-TechnicalTicketResourceId</span><span class="sxs-lookup"><span data-stu-id="922fb-209">-TechnicalTicketResourceId</span></span>
<span data-ttu-id="922fb-210">지원 티켓이 생성 되는 Azure 서비스 리소스의 리소스 id (예: 가상 컴퓨터 리소스 또는 HDInsight 리소스)입니다.</span><span class="sxs-lookup"><span data-stu-id="922fb-210">This is the resource id of the Azure service resource (For example: A virtual machine resource or an HDInsight resource) for which the support ticket is created.</span></span>

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

### <span data-ttu-id="922fb-211">-Title</span><span class="sxs-lookup"><span data-stu-id="922fb-211">-Title</span></span>
<span data-ttu-id="922fb-212">지원 티켓의 제목입니다.</span><span class="sxs-lookup"><span data-stu-id="922fb-212">Title of support ticket.</span></span>

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

### <span data-ttu-id="922fb-213">-확인</span><span class="sxs-lookup"><span data-stu-id="922fb-213">-Confirm</span></span>
<span data-ttu-id="922fb-214">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="922fb-214">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="922fb-215">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="922fb-215">-WhatIf</span></span>
<span data-ttu-id="922fb-216">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="922fb-216">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="922fb-217">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="922fb-217">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="922fb-218">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="922fb-218">CommonParameters</span></span>
<span data-ttu-id="922fb-219">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="922fb-219">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="922fb-220">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="922fb-220">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="922fb-221">입력</span><span class="sxs-lookup"><span data-stu-id="922fb-221">INPUTS</span></span>

### <span data-ttu-id="922fb-222">않아야</span><span class="sxs-lookup"><span data-stu-id="922fb-222">None</span></span>

## <span data-ttu-id="922fb-223">출력</span><span class="sxs-lookup"><span data-stu-id="922fb-223">OUTPUTS</span></span>

### <span data-ttu-id="922fb-224">Microsoft. PSSupportTicket을 통해 지원 되는 모델</span><span class="sxs-lookup"><span data-stu-id="922fb-224">Microsoft.Azure.Commands.Support.Models.PSSupportTicket</span></span>

## <span data-ttu-id="922fb-225">상속자</span><span class="sxs-lookup"><span data-stu-id="922fb-225">NOTES</span></span>

## <span data-ttu-id="922fb-226">관련 링크</span><span class="sxs-lookup"><span data-stu-id="922fb-226">RELATED LINKS</span></span>
