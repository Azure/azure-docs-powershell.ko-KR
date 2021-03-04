---
external help file: ''
Module Name: Az.Portal
online version: https://docs.microsoft.com/powershell/module/az.portal/remove-azportaldashboard
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Portal/help/Remove-AzPortalDashboard.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Portal/help/Remove-AzPortalDashboard.md
ms.openlocfilehash: 5422b416d7fc6bf16625625a991e17d65061339e
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101988974"
---
# <span data-ttu-id="70fcc-101">Remove-AzPortalDashboard</span><span class="sxs-lookup"><span data-stu-id="70fcc-101">Remove-AzPortalDashboard</span></span>

## <span data-ttu-id="70fcc-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="70fcc-102">SYNOPSIS</span></span>
<span data-ttu-id="70fcc-103">대시보드를 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="70fcc-103">Deletes the Dashboard.</span></span>

## <span data-ttu-id="70fcc-104">구문</span><span class="sxs-lookup"><span data-stu-id="70fcc-104">SYNTAX</span></span>

### <span data-ttu-id="70fcc-105">삭제(기본값)</span><span class="sxs-lookup"><span data-stu-id="70fcc-105">Delete (Default)</span></span>
```
Remove-AzPortalDashboard -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="70fcc-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="70fcc-106">DeleteViaIdentity</span></span>
```
Remove-AzPortalDashboard -InputObject <IPortalIdentity> [-DefaultProfile <PSObject>] [-PassThru] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="70fcc-107">설명</span><span class="sxs-lookup"><span data-stu-id="70fcc-107">DESCRIPTION</span></span>
<span data-ttu-id="70fcc-108">대시보드를 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="70fcc-108">Deletes the Dashboard.</span></span>

## <span data-ttu-id="70fcc-109">예제</span><span class="sxs-lookup"><span data-stu-id="70fcc-109">EXAMPLES</span></span>

### <span data-ttu-id="70fcc-110">예제 1: 대시보드 제거</span><span class="sxs-lookup"><span data-stu-id="70fcc-110">Example 1: Remove a Dashboard</span></span>
```powershell
PS C:\td\> Remove-AzPortalDashboard -ResourceGroupName my-rg -DashboardName dashbase02
```

<span data-ttu-id="70fcc-111">리소스 그룹 이름 및 대시보드 이름을 사용하여 Dashbaord를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="70fcc-111">Remove a Dashbaord using resource group name and dashboard name.</span></span>

### <span data-ttu-id="70fcc-112">예제 2: 파이프라인을 사용하여 대시보드 제거</span><span class="sxs-lookup"><span data-stu-id="70fcc-112">Example 2: Remove a Dashboard using the pipeline</span></span>
```powershell
PS C:\> Get-AzPortalDashboard -ResourceGroupName my-rg -DashboardName dashbase02 | Remove-AzPortalDashboard
```

<span data-ttu-id="70fcc-113">호출에서 반환된 대시보드를 Get-AzDashboard 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="70fcc-113">Remove the dashboard returned from a Get-AzDashboard call.</span></span>

## <span data-ttu-id="70fcc-114">매개 변수</span><span class="sxs-lookup"><span data-stu-id="70fcc-114">PARAMETERS</span></span>

### <span data-ttu-id="70fcc-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="70fcc-115">-DefaultProfile</span></span>
<span data-ttu-id="70fcc-116">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="70fcc-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="70fcc-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="70fcc-117">-InputObject</span></span>
<span data-ttu-id="70fcc-118">ID 매개 변수를 생성하는 경우 INPUTOBJECT 속성에 대한 노트 섹션을 참조하고 해시 테이블을 만드십시오.</span><span class="sxs-lookup"><span data-stu-id="70fcc-118">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="70fcc-119">-Name</span><span class="sxs-lookup"><span data-stu-id="70fcc-119">-Name</span></span>
<span data-ttu-id="70fcc-120">대시보드의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="70fcc-120">The name of the dashboard.</span></span>

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

### <span data-ttu-id="70fcc-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="70fcc-121">-PassThru</span></span>
<span data-ttu-id="70fcc-122">명령이 성공하면 true를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="70fcc-122">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="70fcc-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="70fcc-123">-ResourceGroupName</span></span>
<span data-ttu-id="70fcc-124">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="70fcc-124">The name of the resource group.</span></span>

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

### <span data-ttu-id="70fcc-125">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="70fcc-125">-SubscriptionId</span></span>
<span data-ttu-id="70fcc-126">Azure 구독 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="70fcc-126">The Azure subscription ID.</span></span>
<span data-ttu-id="70fcc-127">GUID 형식 문자열입니다(예: 00000000-0000-0000-000000000)입니다.</span><span class="sxs-lookup"><span data-stu-id="70fcc-127">This is a GUID-formatted string (e.g. 00000000-0000-0000-0000-000000000000)</span></span>

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

### <span data-ttu-id="70fcc-128">-확인</span><span class="sxs-lookup"><span data-stu-id="70fcc-128">-Confirm</span></span>
<span data-ttu-id="70fcc-129">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="70fcc-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="70fcc-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="70fcc-130">-WhatIf</span></span>
<span data-ttu-id="70fcc-131">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="70fcc-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="70fcc-132">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="70fcc-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="70fcc-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="70fcc-133">CommonParameters</span></span>
<span data-ttu-id="70fcc-134">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="70fcc-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="70fcc-135">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="70fcc-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="70fcc-136">입력</span><span class="sxs-lookup"><span data-stu-id="70fcc-136">INPUTS</span></span>

### <span data-ttu-id="70fcc-137">Microsoft.Azure.PowerShell.Cmdlets.Portal.Models.IPortalIdentity</span><span class="sxs-lookup"><span data-stu-id="70fcc-137">Microsoft.Azure.PowerShell.Cmdlets.Portal.Models.IPortalIdentity</span></span>

## <span data-ttu-id="70fcc-138">출력</span><span class="sxs-lookup"><span data-stu-id="70fcc-138">OUTPUTS</span></span>

### <span data-ttu-id="70fcc-139">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="70fcc-139">System.Boolean</span></span>

## <span data-ttu-id="70fcc-140">참고 사항</span><span class="sxs-lookup"><span data-stu-id="70fcc-140">NOTES</span></span>

<span data-ttu-id="70fcc-141">별칭</span><span class="sxs-lookup"><span data-stu-id="70fcc-141">ALIASES</span></span>

<span data-ttu-id="70fcc-142">복잡한 매개 변수 속성</span><span class="sxs-lookup"><span data-stu-id="70fcc-142">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="70fcc-143">아래에 설명된 매개 변수를 만들 경우 적절한 속성을 포함하는 해시 테이블을 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="70fcc-143">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="70fcc-144">해시 테이블에 대한 자세한 내용은 Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="70fcc-144">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="70fcc-145">INPUTOBJECT <IPortalIdentity> : ID 매개 변수</span><span class="sxs-lookup"><span data-stu-id="70fcc-145">INPUTOBJECT <IPortalIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="70fcc-146">`[DashboardName <String>]`: 대시보드의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="70fcc-146">`[DashboardName <String>]`: The name of the dashboard.</span></span>
  - <span data-ttu-id="70fcc-147">`[Id <String>]`: 리소스 ID 경로</span><span class="sxs-lookup"><span data-stu-id="70fcc-147">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="70fcc-148">`[ResourceGroupName <String>]`: 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="70fcc-148">`[ResourceGroupName <String>]`: The name of the resource group.</span></span>
  - <span data-ttu-id="70fcc-149">`[SubscriptionId <String>]`: Azure 구독 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="70fcc-149">`[SubscriptionId <String>]`: The Azure subscription ID.</span></span> <span data-ttu-id="70fcc-150">GUID 형식 문자열입니다(예: 00000000-0000-0000-000000000)입니다.</span><span class="sxs-lookup"><span data-stu-id="70fcc-150">This is a GUID-formatted string (e.g. 00000000-0000-0000-0000-000000000000)</span></span>

## <span data-ttu-id="70fcc-151">관련 링크</span><span class="sxs-lookup"><span data-stu-id="70fcc-151">RELATED LINKS</span></span>

