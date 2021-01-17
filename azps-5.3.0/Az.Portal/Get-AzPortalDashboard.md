---
external help file: ''
Module Name: Az.Portal
online version: https://docs.microsoft.com/en-us/powershell/module/az.portal/get-azportaldashboard
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Portal/help/Get-AzPortalDashboard.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Portal/help/Get-AzPortalDashboard.md
ms.openlocfilehash: aa11a9828c422069823226b2d5df57efc84f8c7b
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98384539"
---
# <span data-ttu-id="26f97-101">Get-AzPortalDashboard</span><span class="sxs-lookup"><span data-stu-id="26f97-101">Get-AzPortalDashboard</span></span>

## <span data-ttu-id="26f97-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="26f97-102">SYNOPSIS</span></span>
<span data-ttu-id="26f97-103">대시보드를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="26f97-103">Gets the Dashboard.</span></span>

## <span data-ttu-id="26f97-104">구문</span><span class="sxs-lookup"><span data-stu-id="26f97-104">SYNTAX</span></span>

### <span data-ttu-id="26f97-105">List1(기본값)</span><span class="sxs-lookup"><span data-stu-id="26f97-105">List1 (Default)</span></span>
```
Get-AzPortalDashboard [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="26f97-106">가져오기</span><span class="sxs-lookup"><span data-stu-id="26f97-106">Get</span></span>
```
Get-AzPortalDashboard -Name <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="26f97-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="26f97-107">GetViaIdentity</span></span>
```
Get-AzPortalDashboard -InputObject <IPortalIdentity> [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="26f97-108">목록</span><span class="sxs-lookup"><span data-stu-id="26f97-108">List</span></span>
```
Get-AzPortalDashboard -ResourceGroupName <String> [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="26f97-109">설명</span><span class="sxs-lookup"><span data-stu-id="26f97-109">DESCRIPTION</span></span>
<span data-ttu-id="26f97-110">대시보드를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="26f97-110">Gets the Dashboard.</span></span>

## <span data-ttu-id="26f97-111">예제</span><span class="sxs-lookup"><span data-stu-id="26f97-111">EXAMPLES</span></span>

### <span data-ttu-id="26f97-112">예제 1: 구독의 모든 대시보드 나열</span><span class="sxs-lookup"><span data-stu-id="26f97-112">Example 1: List all dashboards in a subscription</span></span>
```powershell
PS C:> Get-AzPortalDashboard                                                                                                                     
Location Name                                           Type
-------- ----                                           ----
eastasia my-custom-dashboard1                           Microsoft.Portal/dashboards
westus   my-second-custom-dashboard1                    Microsoft.Portal/dashboards

```

<span data-ttu-id="26f97-113">구독의 모든 대시보드 나열</span><span class="sxs-lookup"><span data-stu-id="26f97-113">List all dashboards in a subscription</span></span>

### <span data-ttu-id="26f97-114">예제 2: 단일 포털 대시보드에 대한 세부 정보 보기</span><span class="sxs-lookup"><span data-stu-id="26f97-114">Example 2: Get details for a single Portal Dashboard</span></span>
```powershell
PS C:\> Get-AzPortalDashboard -ResourceGroupName my-rg -Name mydashboard

Location Name        Type
-------- ----        ----
eastus   mydashboard Microsoft.Portal/dashboards
```

<span data-ttu-id="26f97-115">단일 대시보드에 대한 세부 정보 보기</span><span class="sxs-lookup"><span data-stu-id="26f97-115">Get details for a single dashboard</span></span>

## <span data-ttu-id="26f97-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="26f97-116">PARAMETERS</span></span>

### <span data-ttu-id="26f97-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="26f97-117">-DefaultProfile</span></span>
<span data-ttu-id="26f97-118">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="26f97-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="26f97-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="26f97-119">-InputObject</span></span>
<span data-ttu-id="26f97-120">ID 매개 변수를 생성하는 경우 INPUTOBJECT 속성에 대한 NOTES 섹션을 참조하고 해시 테이블을 만드십시오.</span><span class="sxs-lookup"><span data-stu-id="26f97-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="26f97-121">-Name</span><span class="sxs-lookup"><span data-stu-id="26f97-121">-Name</span></span>
<span data-ttu-id="26f97-122">대시보드의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="26f97-122">The name of the dashboard.</span></span>

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

### <span data-ttu-id="26f97-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="26f97-123">-ResourceGroupName</span></span>
<span data-ttu-id="26f97-124">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="26f97-124">The name of the resource group.</span></span>

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

### <span data-ttu-id="26f97-125">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="26f97-125">-SubscriptionId</span></span>
<span data-ttu-id="26f97-126">Azure 구독 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="26f97-126">The Azure subscription ID.</span></span>
<span data-ttu-id="26f97-127">GUID 형식 문자열입니다(예: 00000000-0000-0000-0000-000000000000)</span><span class="sxs-lookup"><span data-stu-id="26f97-127">This is a GUID-formatted string (e.g. 00000000-0000-0000-0000-000000000000)</span></span>

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

### <span data-ttu-id="26f97-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="26f97-128">CommonParameters</span></span>
<span data-ttu-id="26f97-129">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="26f97-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="26f97-130">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="26f97-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="26f97-131">입력</span><span class="sxs-lookup"><span data-stu-id="26f97-131">INPUTS</span></span>

### <span data-ttu-id="26f97-132">Microsoft.Azure.PowerShell.Cmdlets.Portal.Models.IPortalIdentity</span><span class="sxs-lookup"><span data-stu-id="26f97-132">Microsoft.Azure.PowerShell.Cmdlets.Portal.Models.IPortalIdentity</span></span>

## <span data-ttu-id="26f97-133">출력</span><span class="sxs-lookup"><span data-stu-id="26f97-133">OUTPUTS</span></span>

### <span data-ttu-id="26f97-134">Microsoft.Azure.PowerShell.Cmdlets.Portal.Models.Api201901Preview.IDashboard</span><span class="sxs-lookup"><span data-stu-id="26f97-134">Microsoft.Azure.PowerShell.Cmdlets.Portal.Models.Api201901Preview.IDashboard</span></span>

## <span data-ttu-id="26f97-135">참고 사항</span><span class="sxs-lookup"><span data-stu-id="26f97-135">NOTES</span></span>

<span data-ttu-id="26f97-136">별칭</span><span class="sxs-lookup"><span data-stu-id="26f97-136">ALIASES</span></span>

<span data-ttu-id="26f97-137">복합 매개 변수 속성</span><span class="sxs-lookup"><span data-stu-id="26f97-137">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="26f97-138">아래에 설명된 매개 변수를 만들 수 있도록 적절한 속성을 포함하는 해시 테이블을 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="26f97-138">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="26f97-139">해시 테이블에 대한 자세한 내용은 다음 Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="26f97-139">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="26f97-140">INPUTOBJECT: <IPortalIdentity> ID 매개 변수</span><span class="sxs-lookup"><span data-stu-id="26f97-140">INPUTOBJECT <IPortalIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="26f97-141">`[DashboardName <String>]`: 대시보드의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="26f97-141">`[DashboardName <String>]`: The name of the dashboard.</span></span>
  - <span data-ttu-id="26f97-142">`[Id <String>]`: 리소스 ID 경로</span><span class="sxs-lookup"><span data-stu-id="26f97-142">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="26f97-143">`[ResourceGroupName <String>]`: 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="26f97-143">`[ResourceGroupName <String>]`: The name of the resource group.</span></span>
  - <span data-ttu-id="26f97-144">`[SubscriptionId <String>]`: Azure 구독 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="26f97-144">`[SubscriptionId <String>]`: The Azure subscription ID.</span></span> <span data-ttu-id="26f97-145">GUID 형식 문자열입니다(예: 00000000-0000-0000-0000-000000000000)</span><span class="sxs-lookup"><span data-stu-id="26f97-145">This is a GUID-formatted string (e.g. 00000000-0000-0000-0000-000000000000)</span></span>

## <span data-ttu-id="26f97-146">관련 링크</span><span class="sxs-lookup"><span data-stu-id="26f97-146">RELATED LINKS</span></span>

