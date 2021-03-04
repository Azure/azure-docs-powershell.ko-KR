---
external help file: ''
Module Name: Az.Portal
online version: https://docs.microsoft.com/powershell/module/az.portal/get-azportaldashboard
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Portal/help/Get-AzPortalDashboard.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Portal/help/Get-AzPortalDashboard.md
ms.openlocfilehash: fc888161df56e3edbf1a51014c7173542e395ad3
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101989030"
---
# <span data-ttu-id="fc585-101">Get-AzPortalDashboard</span><span class="sxs-lookup"><span data-stu-id="fc585-101">Get-AzPortalDashboard</span></span>

## <span data-ttu-id="fc585-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fc585-102">SYNOPSIS</span></span>
<span data-ttu-id="fc585-103">대시보드를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="fc585-103">Gets the Dashboard.</span></span>

## <span data-ttu-id="fc585-104">구문</span><span class="sxs-lookup"><span data-stu-id="fc585-104">SYNTAX</span></span>

### <span data-ttu-id="fc585-105">List1(기본값)</span><span class="sxs-lookup"><span data-stu-id="fc585-105">List1 (Default)</span></span>
```
Get-AzPortalDashboard [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="fc585-106">가져오기</span><span class="sxs-lookup"><span data-stu-id="fc585-106">Get</span></span>
```
Get-AzPortalDashboard -Name <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="fc585-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="fc585-107">GetViaIdentity</span></span>
```
Get-AzPortalDashboard -InputObject <IPortalIdentity> [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="fc585-108">목록</span><span class="sxs-lookup"><span data-stu-id="fc585-108">List</span></span>
```
Get-AzPortalDashboard -ResourceGroupName <String> [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="fc585-109">설명</span><span class="sxs-lookup"><span data-stu-id="fc585-109">DESCRIPTION</span></span>
<span data-ttu-id="fc585-110">대시보드를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="fc585-110">Gets the Dashboard.</span></span>

## <span data-ttu-id="fc585-111">예제</span><span class="sxs-lookup"><span data-stu-id="fc585-111">EXAMPLES</span></span>

### <span data-ttu-id="fc585-112">예제 1: 구독의 모든 대시보드 나열</span><span class="sxs-lookup"><span data-stu-id="fc585-112">Example 1: List all dashboards in a subscription</span></span>
```powershell
PS C:> Get-AzPortalDashboard                                                                                                                     
Location Name                                           Type
-------- ----                                           ----
eastasia my-custom-dashboard1                           Microsoft.Portal/dashboards
westus   my-second-custom-dashboard1                    Microsoft.Portal/dashboards

```

<span data-ttu-id="fc585-113">구독의 모든 대시보드 나열</span><span class="sxs-lookup"><span data-stu-id="fc585-113">List all dashboards in a subscription</span></span>

### <span data-ttu-id="fc585-114">예제 2: 단일 포털 대시보드에 대한 세부 정보 보기</span><span class="sxs-lookup"><span data-stu-id="fc585-114">Example 2: Get details for a single Portal Dashboard</span></span>
```powershell
PS C:\> Get-AzPortalDashboard -ResourceGroupName my-rg -Name mydashboard

Location Name        Type
-------- ----        ----
eastus   mydashboard Microsoft.Portal/dashboards
```

<span data-ttu-id="fc585-115">단일 대시보드에 대한 세부 정보 보기</span><span class="sxs-lookup"><span data-stu-id="fc585-115">Get details for a single dashboard</span></span>

## <span data-ttu-id="fc585-116">매개 변수</span><span class="sxs-lookup"><span data-stu-id="fc585-116">PARAMETERS</span></span>

### <span data-ttu-id="fc585-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fc585-117">-DefaultProfile</span></span>
<span data-ttu-id="fc585-118">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="fc585-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fc585-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="fc585-119">-InputObject</span></span>
<span data-ttu-id="fc585-120">ID 매개 변수를 생성하는 경우 INPUTOBJECT 속성에 대한 노트 섹션을 참조하고 해시 테이블을 만드십시오.</span><span class="sxs-lookup"><span data-stu-id="fc585-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Portal.Models.IPortalIdentity
Parameter Sets: GetViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="fc585-121">-Name</span><span class="sxs-lookup"><span data-stu-id="fc585-121">-Name</span></span>
<span data-ttu-id="fc585-122">대시보드의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="fc585-122">The name of the dashboard.</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases: DashboardName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fc585-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fc585-123">-ResourceGroupName</span></span>
<span data-ttu-id="fc585-124">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="fc585-124">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: Get, List
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fc585-125">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="fc585-125">-SubscriptionId</span></span>
<span data-ttu-id="fc585-126">Azure 구독 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="fc585-126">The Azure subscription ID.</span></span>
<span data-ttu-id="fc585-127">GUID 형식 문자열입니다(예: 00000000-0000-0000-000000000)입니다.</span><span class="sxs-lookup"><span data-stu-id="fc585-127">This is a GUID-formatted string (e.g. 00000000-0000-0000-0000-000000000000)</span></span>

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

### <span data-ttu-id="fc585-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fc585-128">CommonParameters</span></span>
<span data-ttu-id="fc585-129">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="fc585-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fc585-130">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="fc585-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fc585-131">입력</span><span class="sxs-lookup"><span data-stu-id="fc585-131">INPUTS</span></span>

### <span data-ttu-id="fc585-132">Microsoft.Azure.PowerShell.Cmdlets.Portal.Models.IPortalIdentity</span><span class="sxs-lookup"><span data-stu-id="fc585-132">Microsoft.Azure.PowerShell.Cmdlets.Portal.Models.IPortalIdentity</span></span>

## <span data-ttu-id="fc585-133">출력</span><span class="sxs-lookup"><span data-stu-id="fc585-133">OUTPUTS</span></span>

### <span data-ttu-id="fc585-134">Microsoft.Azure.PowerShell.Cmdlets.Portal.Models.Api201901Preview.IDashboard</span><span class="sxs-lookup"><span data-stu-id="fc585-134">Microsoft.Azure.PowerShell.Cmdlets.Portal.Models.Api201901Preview.IDashboard</span></span>

## <span data-ttu-id="fc585-135">참고 사항</span><span class="sxs-lookup"><span data-stu-id="fc585-135">NOTES</span></span>

<span data-ttu-id="fc585-136">별칭</span><span class="sxs-lookup"><span data-stu-id="fc585-136">ALIASES</span></span>

<span data-ttu-id="fc585-137">복잡한 매개 변수 속성</span><span class="sxs-lookup"><span data-stu-id="fc585-137">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="fc585-138">아래에 설명된 매개 변수를 만들 경우 적절한 속성을 포함하는 해시 테이블을 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="fc585-138">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="fc585-139">해시 테이블에 대한 자세한 내용은 Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="fc585-139">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="fc585-140">INPUTOBJECT <IPortalIdentity> : ID 매개 변수</span><span class="sxs-lookup"><span data-stu-id="fc585-140">INPUTOBJECT <IPortalIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="fc585-141">`[DashboardName <String>]`: 대시보드의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="fc585-141">`[DashboardName <String>]`: The name of the dashboard.</span></span>
  - <span data-ttu-id="fc585-142">`[Id <String>]`: 리소스 ID 경로</span><span class="sxs-lookup"><span data-stu-id="fc585-142">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="fc585-143">`[ResourceGroupName <String>]`: 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="fc585-143">`[ResourceGroupName <String>]`: The name of the resource group.</span></span>
  - <span data-ttu-id="fc585-144">`[SubscriptionId <String>]`: Azure 구독 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="fc585-144">`[SubscriptionId <String>]`: The Azure subscription ID.</span></span> <span data-ttu-id="fc585-145">GUID 형식 문자열입니다(예: 00000000-0000-0000-000000000)입니다.</span><span class="sxs-lookup"><span data-stu-id="fc585-145">This is a GUID-formatted string (e.g. 00000000-0000-0000-0000-000000000000)</span></span>

## <span data-ttu-id="fc585-146">관련 링크</span><span class="sxs-lookup"><span data-stu-id="fc585-146">RELATED LINKS</span></span>

