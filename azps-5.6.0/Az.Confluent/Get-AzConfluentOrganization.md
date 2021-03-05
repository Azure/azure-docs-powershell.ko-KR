---
external help file: ''
Module Name: Az.Confluent
online version: https://docs.microsoft.com/powershell/module/az.confluent/get-azconfluentorganization
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Confluent/help/Get-AzConfluentOrganization.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Confluent/help/Get-AzConfluentOrganization.md
ms.openlocfilehash: dcac6e7ce7e4c8daed2e2f8b43c44c2da82acd93
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "102012592"
---
# <span data-ttu-id="6702f-101">Get-AzConfluentOrganization</span><span class="sxs-lookup"><span data-stu-id="6702f-101">Get-AzConfluentOrganization</span></span>

## <span data-ttu-id="6702f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6702f-102">SYNOPSIS</span></span>
<span data-ttu-id="6702f-103">특정 조직 리소스의 속성을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="6702f-103">Get the properties of a specific Organization resource.</span></span>

## <span data-ttu-id="6702f-104">구문</span><span class="sxs-lookup"><span data-stu-id="6702f-104">SYNTAX</span></span>

### <span data-ttu-id="6702f-105">목록(기본값)</span><span class="sxs-lookup"><span data-stu-id="6702f-105">List (Default)</span></span>
```
Get-AzConfluentOrganization [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="6702f-106">가져오기</span><span class="sxs-lookup"><span data-stu-id="6702f-106">Get</span></span>
```
Get-AzConfluentOrganization -Name <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="6702f-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="6702f-107">GetViaIdentity</span></span>
```
Get-AzConfluentOrganization -InputObject <IConfluentIdentity> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

### <span data-ttu-id="6702f-108">List1</span><span class="sxs-lookup"><span data-stu-id="6702f-108">List1</span></span>
```
Get-AzConfluentOrganization -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="6702f-109">설명</span><span class="sxs-lookup"><span data-stu-id="6702f-109">DESCRIPTION</span></span>
<span data-ttu-id="6702f-110">특정 조직 리소스의 속성을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="6702f-110">Get the properties of a specific Organization resource.</span></span>

## <span data-ttu-id="6702f-111">예제</span><span class="sxs-lookup"><span data-stu-id="6702f-111">EXAMPLES</span></span>

### <span data-ttu-id="6702f-112">예제 1: 구독 아래에 모든 혼성 조직 나열</span><span class="sxs-lookup"><span data-stu-id="6702f-112">Example 1: List all confluent organizations under a subscription</span></span>
```powershell
PS C:\> Get-AzConfluentOrganization

Location      Name                     Type
--------      ----                     ----
westus2       RegionTestWestUS2        Microsoft.Confluent/organizations
westus2       RohitWUS2                Microsoft.Confluent/organizations
westus2       Rohit-Secret             Microsoft.Confluent/organizations
westus2       Rohit-Secret-2           Microsoft.Confluent/organizations
westus2       Rohit-Secret-WUS2-0      Microsoft.Confluent/organizations
westus2       RohitWus200              Microsoft.Confluent/organizations
westus2       RohitWUS300              Microsoft.Confluent/organizations
westus2       WestUS2-SSOTest          Microsoft.Confluent/organizations
westus2       dri-01-02-postman-stable Microsoft.Confluent/organizations
westus2       dri-02-02                Microsoft.Confluent/organizations
westcentralus RohitWCUS88              Microsoft.Confluent/organizations
```

<span data-ttu-id="6702f-113">이 명령은 구독 아래에 있는 모든 confluent 조직을 나열합니다.</span><span class="sxs-lookup"><span data-stu-id="6702f-113">This command lists all confluent organizations under a subscription.</span></span>

### <span data-ttu-id="6702f-114">예제 2: 리소스 그룹 아래에 모든 혼성 조직 나열</span><span class="sxs-lookup"><span data-stu-id="6702f-114">Example 2: List all confluent organizations under a resource group</span></span>
```powershell
PS C:\> Get-AzConfluentOrganization -ResourceGroupName azure-rg-test

Location    Name          Type
--------    ----          ----
eastus2euap ppe-metrics-2 Microsoft.Confluent/organizations
```

<span data-ttu-id="6702f-115">이 명령은 리소스 그룹 아래에 있는 모든 혼성 조직을 나열합니다.</span><span class="sxs-lookup"><span data-stu-id="6702f-115">This command lists all confluent organizations under a resource group.</span></span>

### <span data-ttu-id="6702f-116">예제 3: 이름에 따라 혼성 조직을 얻다</span><span class="sxs-lookup"><span data-stu-id="6702f-116">Example 3: Get a confluent organization by name</span></span>
```powershell
PS C:\> Get-AzConfluentOrganization -ResourceGroupName azure-rg-test -Name confluentorg-01-portal

Location Name                   Type
-------- ----                   ----
eastus   confluentorg-01-portal Microsoft.Confluent/organizations
```

<span data-ttu-id="6702f-117">이 명령은 이름을 사용하여 confluent 조직을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="6702f-117">This command gets a confluent organization by name.</span></span>

### <span data-ttu-id="6702f-118">예제 4: 파이프라인에 따라 confluent 조직을 얻다</span><span class="sxs-lookup"><span data-stu-id="6702f-118">Example 4: Get a confluent organization by pipeline</span></span>
```powershell
PS C:\> New-AzConfluentOrganization -ResourceGroupName azure-rg-test -Name confluentorg-02-pwsh -Location eastus -OfferDetailId "confluent-cloud-azure-prod" -OfferDetailPlanId "confluent-cloud-azure-payg-prod" -OfferDetailPlanName "Confluent Cloud - Pay as you Go" -OfferDetailPublisherId "confluentinc" -OfferDetailTermUnit "P1M" | Get-AzConfluentOrganization

Location Name                   Type
-------- ----                   ----
eastus   confluentorg-02-pwsh Microsoft.Confluent/organizations
```

<span data-ttu-id="6702f-119">이 명령은 파이프라인에 따라 confluent 조직을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="6702f-119">This command gets a confluent organization by pipeline.</span></span>

## <span data-ttu-id="6702f-120">매개 변수</span><span class="sxs-lookup"><span data-stu-id="6702f-120">PARAMETERS</span></span>

### <span data-ttu-id="6702f-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6702f-121">-DefaultProfile</span></span>
<span data-ttu-id="6702f-122">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="6702f-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: AzureRMContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6702f-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="6702f-123">-InputObject</span></span>
<span data-ttu-id="6702f-124">ID 매개 변수를 생성하는 경우 INPUTOBJECT 속성에 대한 노트 섹션을 참조하고 해시 테이블을 만드십시오.</span><span class="sxs-lookup"><span data-stu-id="6702f-124">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Confluent.Models.IConfluentIdentity
Parameter Sets: GetViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="6702f-125">-Name</span><span class="sxs-lookup"><span data-stu-id="6702f-125">-Name</span></span>
<span data-ttu-id="6702f-126">조직 리소스 이름</span><span class="sxs-lookup"><span data-stu-id="6702f-126">Organization resource name</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases: OrganizationName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6702f-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6702f-127">-ResourceGroupName</span></span>
<span data-ttu-id="6702f-128">리소스 그룹 이름</span><span class="sxs-lookup"><span data-stu-id="6702f-128">Resource group name</span></span>

```yaml
Type: System.String
Parameter Sets: Get, List1
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6702f-129">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="6702f-129">-SubscriptionId</span></span>
<span data-ttu-id="6702f-130">Microsoft Azure 구독 ID</span><span class="sxs-lookup"><span data-stu-id="6702f-130">Microsoft Azure subscription id</span></span>

```yaml
Type: System.String[]
Parameter Sets: Get, List, List1
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6702f-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6702f-131">CommonParameters</span></span>
<span data-ttu-id="6702f-132">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="6702f-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6702f-133">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="6702f-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6702f-134">입력</span><span class="sxs-lookup"><span data-stu-id="6702f-134">INPUTS</span></span>

### <span data-ttu-id="6702f-135">Microsoft.Azure.PowerShell.Cmdlets.Confluent.Models.IConfluentIdentity</span><span class="sxs-lookup"><span data-stu-id="6702f-135">Microsoft.Azure.PowerShell.Cmdlets.Confluent.Models.IConfluentIdentity</span></span>

## <span data-ttu-id="6702f-136">출력</span><span class="sxs-lookup"><span data-stu-id="6702f-136">OUTPUTS</span></span>

### <span data-ttu-id="6702f-137">Microsoft.Azure.PowerShell.Cmdlets.Confluent.Models.Api20200301.IOrganizationResource</span><span class="sxs-lookup"><span data-stu-id="6702f-137">Microsoft.Azure.PowerShell.Cmdlets.Confluent.Models.Api20200301.IOrganizationResource</span></span>

## <span data-ttu-id="6702f-138">참고 사항</span><span class="sxs-lookup"><span data-stu-id="6702f-138">NOTES</span></span>

<span data-ttu-id="6702f-139">별칭</span><span class="sxs-lookup"><span data-stu-id="6702f-139">ALIASES</span></span>

<span data-ttu-id="6702f-140">복잡한 매개 변수 속성</span><span class="sxs-lookup"><span data-stu-id="6702f-140">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="6702f-141">아래에 설명된 매개 변수를 만들 경우 적절한 속성을 포함하는 해시 테이블을 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="6702f-141">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="6702f-142">해시 테이블에 대한 자세한 내용은 Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="6702f-142">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="6702f-143">INPUTOBJECT <IConfluentIdentity> : ID 매개 변수</span><span class="sxs-lookup"><span data-stu-id="6702f-143">INPUTOBJECT <IConfluentIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="6702f-144">`[Id <String>]`: 리소스 ID 경로</span><span class="sxs-lookup"><span data-stu-id="6702f-144">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="6702f-145">`[OrganizationName <String>]`: 조직 리소스 이름</span><span class="sxs-lookup"><span data-stu-id="6702f-145">`[OrganizationName <String>]`: Organization resource name</span></span>
  - <span data-ttu-id="6702f-146">`[ResourceGroupName <String>]`: 리소스 그룹 이름</span><span class="sxs-lookup"><span data-stu-id="6702f-146">`[ResourceGroupName <String>]`: Resource group name</span></span>
  - <span data-ttu-id="6702f-147">`[SubscriptionId <String>]`: Microsoft Azure 구독 ID</span><span class="sxs-lookup"><span data-stu-id="6702f-147">`[SubscriptionId <String>]`: Microsoft Azure subscription id</span></span>

## <span data-ttu-id="6702f-148">관련 링크</span><span class="sxs-lookup"><span data-stu-id="6702f-148">RELATED LINKS</span></span>

