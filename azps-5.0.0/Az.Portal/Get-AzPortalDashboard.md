---
external help file: ''
Module Name: Az.Portal
online version: https://docs.microsoft.com/en-us/powershell/module/az.portal/get-azportaldashboard
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Portal/help/Get-AzPortalDashboard.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Portal/help/Get-AzPortalDashboard.md
ms.openlocfilehash: aa11a9828c422069823226b2d5df57efc84f8c7b
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94219183"
---
# <span data-ttu-id="5961a-101">Get-AzPortalDashboard</span><span class="sxs-lookup"><span data-stu-id="5961a-101">Get-AzPortalDashboard</span></span>

## <span data-ttu-id="5961a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5961a-102">SYNOPSIS</span></span>
<span data-ttu-id="5961a-103">대시보드를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="5961a-103">Gets the Dashboard.</span></span>

## <span data-ttu-id="5961a-104">구문과</span><span class="sxs-lookup"><span data-stu-id="5961a-104">SYNTAX</span></span>

### <span data-ttu-id="5961a-105">List1 (기본값)</span><span class="sxs-lookup"><span data-stu-id="5961a-105">List1 (Default)</span></span>
```
Get-AzPortalDashboard [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="5961a-106">가져오기</span><span class="sxs-lookup"><span data-stu-id="5961a-106">Get</span></span>
```
Get-AzPortalDashboard -Name <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="5961a-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="5961a-107">GetViaIdentity</span></span>
```
Get-AzPortalDashboard -InputObject <IPortalIdentity> [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="5961a-108">목록</span><span class="sxs-lookup"><span data-stu-id="5961a-108">List</span></span>
```
Get-AzPortalDashboard -ResourceGroupName <String> [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="5961a-109">설명은</span><span class="sxs-lookup"><span data-stu-id="5961a-109">DESCRIPTION</span></span>
<span data-ttu-id="5961a-110">대시보드를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="5961a-110">Gets the Dashboard.</span></span>

## <span data-ttu-id="5961a-111">예제의</span><span class="sxs-lookup"><span data-stu-id="5961a-111">EXAMPLES</span></span>

### <span data-ttu-id="5961a-112">예제 1: 구독의 모든 대시보드 나열</span><span class="sxs-lookup"><span data-stu-id="5961a-112">Example 1: List all dashboards in a subscription</span></span>
```powershell
PS C:> Get-AzPortalDashboard                                                                                                                     
Location Name                                           Type
-------- ----                                           ----
eastasia my-custom-dashboard1                           Microsoft.Portal/dashboards
westus   my-second-custom-dashboard1                    Microsoft.Portal/dashboards

```

<span data-ttu-id="5961a-113">구독의 모든 대시보드 나열</span><span class="sxs-lookup"><span data-stu-id="5961a-113">List all dashboards in a subscription</span></span>

### <span data-ttu-id="5961a-114">예제 2: 단일 포털 대시보드에 대 한 세부 정보 가져오기</span><span class="sxs-lookup"><span data-stu-id="5961a-114">Example 2: Get details for a single Portal Dashboard</span></span>
```powershell
PS C:\> Get-AzPortalDashboard -ResourceGroupName my-rg -Name mydashboard

Location Name        Type
-------- ----        ----
eastus   mydashboard Microsoft.Portal/dashboards
```

<span data-ttu-id="5961a-115">단일 대시보드에 대 한 세부 정보 가져오기</span><span class="sxs-lookup"><span data-stu-id="5961a-115">Get details for a single dashboard</span></span>

## <span data-ttu-id="5961a-116">변수</span><span class="sxs-lookup"><span data-stu-id="5961a-116">PARAMETERS</span></span>

### <span data-ttu-id="5961a-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5961a-117">-DefaultProfile</span></span>
<span data-ttu-id="5961a-118">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="5961a-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5961a-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="5961a-119">-InputObject</span></span>
<span data-ttu-id="5961a-120">생성할 id 매개 변수는 INPUTOBJECT 속성에 대 한 참고 섹션을 참조 하 고 해시 테이블을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="5961a-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="5961a-121">-이름</span><span class="sxs-lookup"><span data-stu-id="5961a-121">-Name</span></span>
<span data-ttu-id="5961a-122">대시보드의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="5961a-122">The name of the dashboard.</span></span>

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

### <span data-ttu-id="5961a-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5961a-123">-ResourceGroupName</span></span>
<span data-ttu-id="5961a-124">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="5961a-124">The name of the resource group.</span></span>

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

### <span data-ttu-id="5961a-125">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="5961a-125">-SubscriptionId</span></span>
<span data-ttu-id="5961a-126">Azure 구독 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="5961a-126">The Azure subscription ID.</span></span>
<span data-ttu-id="5961a-127">GUID 형식 문자열입니다 (예: 00000000-0000-0000-0000-000000000000).</span><span class="sxs-lookup"><span data-stu-id="5961a-127">This is a GUID-formatted string (e.g. 00000000-0000-0000-0000-000000000000)</span></span>

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

### <span data-ttu-id="5961a-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5961a-128">CommonParameters</span></span>
<span data-ttu-id="5961a-129">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="5961a-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5961a-130">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="5961a-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5961a-131">입력</span><span class="sxs-lookup"><span data-stu-id="5961a-131">INPUTS</span></span>

### <span data-ttu-id="5961a-132">IPortalIdentity (Microsoft. PowerShell. 포털)</span><span class="sxs-lookup"><span data-stu-id="5961a-132">Microsoft.Azure.PowerShell.Cmdlets.Portal.Models.IPortalIdentity</span></span>

## <span data-ttu-id="5961a-133">출력</span><span class="sxs-lookup"><span data-stu-id="5961a-133">OUTPUTS</span></span>

### <span data-ttu-id="5961a-134">Api201901Preview. i i m. i m a. i m a. i a Idashboard</span><span class="sxs-lookup"><span data-stu-id="5961a-134">Microsoft.Azure.PowerShell.Cmdlets.Portal.Models.Api201901Preview.IDashboard</span></span>

## <span data-ttu-id="5961a-135">상속자</span><span class="sxs-lookup"><span data-stu-id="5961a-135">NOTES</span></span>

<span data-ttu-id="5961a-136">별칭과</span><span class="sxs-lookup"><span data-stu-id="5961a-136">ALIASES</span></span>

<span data-ttu-id="5961a-137">복합 매개 변수 속성</span><span class="sxs-lookup"><span data-stu-id="5961a-137">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="5961a-138">아래 설명 된 매개 변수를 만들려면 적절 한 속성을 포함 하는 해시 테이블을 생성 합니다.</span><span class="sxs-lookup"><span data-stu-id="5961a-138">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="5961a-139">해시 테이블에 대 한 자세한 내용은 Get-Help about_Hash_Tables를 실행 하세요.</span><span class="sxs-lookup"><span data-stu-id="5961a-139">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="5961a-140">INPUTOBJECT <IPortalIdentity> : Identity 매개 변수</span><span class="sxs-lookup"><span data-stu-id="5961a-140">INPUTOBJECT <IPortalIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="5961a-141">`[DashboardName <String>]`: 대시보드의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="5961a-141">`[DashboardName <String>]`: The name of the dashboard.</span></span>
  - <span data-ttu-id="5961a-142">`[Id <String>]`: 리소스 id 경로</span><span class="sxs-lookup"><span data-stu-id="5961a-142">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="5961a-143">`[ResourceGroupName <String>]`: 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="5961a-143">`[ResourceGroupName <String>]`: The name of the resource group.</span></span>
  - <span data-ttu-id="5961a-144">`[SubscriptionId <String>]`: Azure 구독 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="5961a-144">`[SubscriptionId <String>]`: The Azure subscription ID.</span></span> <span data-ttu-id="5961a-145">GUID 형식 문자열입니다 (예: 00000000-0000-0000-0000-000000000000).</span><span class="sxs-lookup"><span data-stu-id="5961a-145">This is a GUID-formatted string (e.g. 00000000-0000-0000-0000-000000000000)</span></span>

## <span data-ttu-id="5961a-146">관련 링크</span><span class="sxs-lookup"><span data-stu-id="5961a-146">RELATED LINKS</span></span>

