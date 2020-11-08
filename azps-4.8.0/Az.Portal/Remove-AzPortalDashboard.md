---
external help file: ''
Module Name: Az.Portal
online version: https://docs.microsoft.com/en-us/powershell/module/az.portal/remove-azportaldashboard
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Portal/help/Remove-AzPortalDashboard.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Portal/help/Remove-AzPortalDashboard.md
ms.openlocfilehash: f0ef681f09caf43ac2f2100d1a30af19b1b3c364
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94214279"
---
# <span data-ttu-id="ccbc9-101">Remove-AzPortalDashboard</span><span class="sxs-lookup"><span data-stu-id="ccbc9-101">Remove-AzPortalDashboard</span></span>

## <span data-ttu-id="ccbc9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ccbc9-102">SYNOPSIS</span></span>
<span data-ttu-id="ccbc9-103">대시보드를 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="ccbc9-103">Deletes the Dashboard.</span></span>

## <span data-ttu-id="ccbc9-104">구문과</span><span class="sxs-lookup"><span data-stu-id="ccbc9-104">SYNTAX</span></span>

### <span data-ttu-id="ccbc9-105">삭제 (기본값)</span><span class="sxs-lookup"><span data-stu-id="ccbc9-105">Delete (Default)</span></span>
```
Remove-AzPortalDashboard -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="ccbc9-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="ccbc9-106">DeleteViaIdentity</span></span>
```
Remove-AzPortalDashboard -InputObject <IPortalIdentity> [-DefaultProfile <PSObject>] [-PassThru] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="ccbc9-107">설명은</span><span class="sxs-lookup"><span data-stu-id="ccbc9-107">DESCRIPTION</span></span>
<span data-ttu-id="ccbc9-108">대시보드를 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="ccbc9-108">Deletes the Dashboard.</span></span>

## <span data-ttu-id="ccbc9-109">예제의</span><span class="sxs-lookup"><span data-stu-id="ccbc9-109">EXAMPLES</span></span>

### <span data-ttu-id="ccbc9-110">예제 1: 대시보드 제거</span><span class="sxs-lookup"><span data-stu-id="ccbc9-110">Example 1: Remove a Dashboard</span></span>
```powershell
PS C:\td\> Remove-AzPortalDashboard -ResourceGroupName my-rg -DashboardName dashbase02
```

<span data-ttu-id="ccbc9-111">리소스 그룹 이름 및 대시보드 이름을 사용 하 여 Dashbaord를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="ccbc9-111">Remove a Dashbaord using resource group name and dashboard name.</span></span>

### <span data-ttu-id="ccbc9-112">예제 2: 파이프라인을 사용 하 여 대시보드 제거</span><span class="sxs-lookup"><span data-stu-id="ccbc9-112">Example 2: Remove a Dashboard using the pipeline</span></span>
```powershell
PS C:\> Get-AzPortalDashboard -ResourceGroupName my-rg -DashboardName dashbase02 | Remove-AzPortalDashboard
```

<span data-ttu-id="ccbc9-113">Get-AzDashboard 호출에서 반환 된 대시보드를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="ccbc9-113">Remove the dashboard returned from a Get-AzDashboard call.</span></span>

## <span data-ttu-id="ccbc9-114">변수</span><span class="sxs-lookup"><span data-stu-id="ccbc9-114">PARAMETERS</span></span>

### <span data-ttu-id="ccbc9-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ccbc9-115">-DefaultProfile</span></span>
<span data-ttu-id="ccbc9-116">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="ccbc9-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ccbc9-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ccbc9-117">-InputObject</span></span>
<span data-ttu-id="ccbc9-118">생성할 id 매개 변수는 INPUTOBJECT 속성에 대 한 참고 섹션을 참조 하 고 해시 테이블을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="ccbc9-118">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Portal.Models.IPortalIdentity
Parameter Sets: DeleteViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ccbc9-119">-이름</span><span class="sxs-lookup"><span data-stu-id="ccbc9-119">-Name</span></span>
<span data-ttu-id="ccbc9-120">대시보드의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="ccbc9-120">The name of the dashboard.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases: DashboardName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ccbc9-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="ccbc9-121">-PassThru</span></span>
<span data-ttu-id="ccbc9-122">명령이 성공 하면 true를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="ccbc9-122">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="ccbc9-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ccbc9-123">-ResourceGroupName</span></span>
<span data-ttu-id="ccbc9-124">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="ccbc9-124">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ccbc9-125">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="ccbc9-125">-SubscriptionId</span></span>
<span data-ttu-id="ccbc9-126">Azure 구독 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="ccbc9-126">The Azure subscription ID.</span></span>
<span data-ttu-id="ccbc9-127">GUID 형식 문자열입니다 (예: 00000000-0000-0000-0000-000000000000).</span><span class="sxs-lookup"><span data-stu-id="ccbc9-127">This is a GUID-formatted string (e.g. 00000000-0000-0000-0000-000000000000)</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ccbc9-128">-확인</span><span class="sxs-lookup"><span data-stu-id="ccbc9-128">-Confirm</span></span>
<span data-ttu-id="ccbc9-129">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="ccbc9-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ccbc9-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ccbc9-130">-WhatIf</span></span>
<span data-ttu-id="ccbc9-131">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="ccbc9-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ccbc9-132">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="ccbc9-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ccbc9-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ccbc9-133">CommonParameters</span></span>
<span data-ttu-id="ccbc9-134">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="ccbc9-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ccbc9-135">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="ccbc9-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ccbc9-136">입력</span><span class="sxs-lookup"><span data-stu-id="ccbc9-136">INPUTS</span></span>

### <span data-ttu-id="ccbc9-137">IPortalIdentity (Microsoft. PowerShell. 포털)</span><span class="sxs-lookup"><span data-stu-id="ccbc9-137">Microsoft.Azure.PowerShell.Cmdlets.Portal.Models.IPortalIdentity</span></span>

## <span data-ttu-id="ccbc9-138">출력</span><span class="sxs-lookup"><span data-stu-id="ccbc9-138">OUTPUTS</span></span>

### <span data-ttu-id="ccbc9-139">시스템 부울</span><span class="sxs-lookup"><span data-stu-id="ccbc9-139">System.Boolean</span></span>

## <span data-ttu-id="ccbc9-140">상속자</span><span class="sxs-lookup"><span data-stu-id="ccbc9-140">NOTES</span></span>

<span data-ttu-id="ccbc9-141">별칭과</span><span class="sxs-lookup"><span data-stu-id="ccbc9-141">ALIASES</span></span>

<span data-ttu-id="ccbc9-142">복합 매개 변수 속성</span><span class="sxs-lookup"><span data-stu-id="ccbc9-142">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="ccbc9-143">아래 설명 된 매개 변수를 만들려면 적절 한 속성을 포함 하는 해시 테이블을 생성 합니다.</span><span class="sxs-lookup"><span data-stu-id="ccbc9-143">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="ccbc9-144">해시 테이블에 대 한 자세한 내용은 Get-Help about_Hash_Tables를 실행 하세요.</span><span class="sxs-lookup"><span data-stu-id="ccbc9-144">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="ccbc9-145">INPUTOBJECT <IPortalIdentity> : Identity 매개 변수</span><span class="sxs-lookup"><span data-stu-id="ccbc9-145">INPUTOBJECT <IPortalIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="ccbc9-146">`[DashboardName <String>]`: 대시보드의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="ccbc9-146">`[DashboardName <String>]`: The name of the dashboard.</span></span>
  - <span data-ttu-id="ccbc9-147">`[Id <String>]`: 리소스 id 경로</span><span class="sxs-lookup"><span data-stu-id="ccbc9-147">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="ccbc9-148">`[ResourceGroupName <String>]`: 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="ccbc9-148">`[ResourceGroupName <String>]`: The name of the resource group.</span></span>
  - <span data-ttu-id="ccbc9-149">`[SubscriptionId <String>]`: Azure 구독 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="ccbc9-149">`[SubscriptionId <String>]`: The Azure subscription ID.</span></span> <span data-ttu-id="ccbc9-150">GUID 형식 문자열입니다 (예: 00000000-0000-0000-0000-000000000000).</span><span class="sxs-lookup"><span data-stu-id="ccbc9-150">This is a GUID-formatted string (e.g. 00000000-0000-0000-0000-000000000000)</span></span>

## <span data-ttu-id="ccbc9-151">관련 링크</span><span class="sxs-lookup"><span data-stu-id="ccbc9-151">RELATED LINKS</span></span>

