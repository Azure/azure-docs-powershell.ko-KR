---
external help file: ''
Module Name: Az.DesktopVirtualization
online version: https://docs.microsoft.com/powershell/module/az.desktopvirtualization/update-azwvdworkspace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Update-AzWvdWorkspace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Update-AzWvdWorkspace.md
ms.openlocfilehash: 1da28d0003de88d9e8c10da1692ca4f61079f488
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "102009632"
---
# <span data-ttu-id="ae2b5-101">Update-AzWvdWorkspace</span><span class="sxs-lookup"><span data-stu-id="ae2b5-101">Update-AzWvdWorkspace</span></span>

## <span data-ttu-id="ae2b5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ae2b5-102">SYNOPSIS</span></span>
<span data-ttu-id="ae2b5-103">작업 영역 업데이트</span><span class="sxs-lookup"><span data-stu-id="ae2b5-103">Update a workspace.</span></span>

## <span data-ttu-id="ae2b5-104">구문</span><span class="sxs-lookup"><span data-stu-id="ae2b5-104">SYNTAX</span></span>

### <span data-ttu-id="ae2b5-105">UpdateExpanded(기본값)</span><span class="sxs-lookup"><span data-stu-id="ae2b5-105">UpdateExpanded (Default)</span></span>
```
Update-AzWvdWorkspace -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-ApplicationGroupReference <String[]>] [-Description <String>] [-FriendlyName <String>] [-Tag <Hashtable>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="ae2b5-106">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="ae2b5-106">UpdateViaIdentityExpanded</span></span>
```
Update-AzWvdWorkspace -InputObject <IDesktopVirtualizationIdentity> [-ApplicationGroupReference <String[]>]
 [-Description <String>] [-FriendlyName <String>] [-Tag <Hashtable>] [-DefaultProfile <PSObject>] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="ae2b5-107">설명</span><span class="sxs-lookup"><span data-stu-id="ae2b5-107">DESCRIPTION</span></span>
<span data-ttu-id="ae2b5-108">작업 영역 업데이트</span><span class="sxs-lookup"><span data-stu-id="ae2b5-108">Update a workspace.</span></span>

## <span data-ttu-id="ae2b5-109">예제</span><span class="sxs-lookup"><span data-stu-id="ae2b5-109">EXAMPLES</span></span>

### <span data-ttu-id="ae2b5-110">예제 1: 이름에 따라 Windows Virtual Desktop 작업 영역 업데이트</span><span class="sxs-lookup"><span data-stu-id="ae2b5-110">Example 1: Update a Windows Virtual Desktop Workspace by name</span></span>
```powershell
PS C:\> Update-AzWvdWorkspace -ResourceGroupName ResourceGroupName `
                        -Name WorkspaceName `
                        -FriendlyName 'Friendly Name' `
                        -ApplicationGroupReference "/subscriptions/SubscriptionId/resourceGroups/ResourceGroupName/providers/Microsoft.DesktopVirtualization/applicationGroups/ApplicationGroupName1","/subscriptions/SubscriptionId/resourceGroups/ResourceGroupName/providers/Microsoft.DesktopVirtualization/applicationGroups/ApplicationGroupName2" `
                        -Description 'Description'

Location   Name                 Type
--------   ----                 ----
eastus     WorkspaceName Microsoft.DesktopVirtualization/workspaces
```

<span data-ttu-id="ae2b5-111">이 명령은 리소스 그룹의 Windows Virtual Desktop 작업 영역이 업데이트됩니다.</span><span class="sxs-lookup"><span data-stu-id="ae2b5-111">This command updates a Windows Virtual Desktop Workspace in a Resource Group.</span></span>

## <span data-ttu-id="ae2b5-112">매개 변수</span><span class="sxs-lookup"><span data-stu-id="ae2b5-112">PARAMETERS</span></span>

### <span data-ttu-id="ae2b5-113">-ApplicationGroupReference</span><span class="sxs-lookup"><span data-stu-id="ae2b5-113">-ApplicationGroupReference</span></span>
<span data-ttu-id="ae2b5-114">applicationGroup 링크 목록입니다.</span><span class="sxs-lookup"><span data-stu-id="ae2b5-114">List of applicationGroup links.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ae2b5-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ae2b5-115">-DefaultProfile</span></span>
<span data-ttu-id="ae2b5-116">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="ae2b5-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ae2b5-117">-Description</span><span class="sxs-lookup"><span data-stu-id="ae2b5-117">-Description</span></span>
<span data-ttu-id="ae2b5-118">작업 영역의 설명입니다.</span><span class="sxs-lookup"><span data-stu-id="ae2b5-118">Description of Workspace.</span></span>

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

### <span data-ttu-id="ae2b5-119">-FriendlyName</span><span class="sxs-lookup"><span data-stu-id="ae2b5-119">-FriendlyName</span></span>
<span data-ttu-id="ae2b5-120">작업 영역의 친숙한 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="ae2b5-120">Friendly name of Workspace.</span></span>

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

### <span data-ttu-id="ae2b5-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ae2b5-121">-InputObject</span></span>
<span data-ttu-id="ae2b5-122">ID 매개 변수를 생성하는 경우 INPUTOBJECT 속성에 대한 노트 섹션을 참조하고 해시 테이블을 만드십시오.</span><span class="sxs-lookup"><span data-stu-id="ae2b5-122">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.IDesktopVirtualizationIdentity
Parameter Sets: UpdateViaIdentityExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ae2b5-123">-Name</span><span class="sxs-lookup"><span data-stu-id="ae2b5-123">-Name</span></span>
<span data-ttu-id="ae2b5-124">작업 영역의 이름</span><span class="sxs-lookup"><span data-stu-id="ae2b5-124">The name of the workspace</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases: WorkspaceName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ae2b5-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ae2b5-125">-ResourceGroupName</span></span>
<span data-ttu-id="ae2b5-126">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="ae2b5-126">The name of the resource group.</span></span>
<span data-ttu-id="ae2b5-127">이름은 대소문자와 무관합니다.</span><span class="sxs-lookup"><span data-stu-id="ae2b5-127">The name is case insensitive.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ae2b5-128">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="ae2b5-128">-SubscriptionId</span></span>
<span data-ttu-id="ae2b5-129">대상 구독의 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="ae2b5-129">The ID of the target subscription.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ae2b5-130">-Tag</span><span class="sxs-lookup"><span data-stu-id="ae2b5-130">-Tag</span></span>
<span data-ttu-id="ae2b5-131">업데이트할 태그</span><span class="sxs-lookup"><span data-stu-id="ae2b5-131">tags to be updated</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ae2b5-132">-확인</span><span class="sxs-lookup"><span data-stu-id="ae2b5-132">-Confirm</span></span>
<span data-ttu-id="ae2b5-133">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="ae2b5-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ae2b5-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ae2b5-134">-WhatIf</span></span>
<span data-ttu-id="ae2b5-135">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="ae2b5-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ae2b5-136">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="ae2b5-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ae2b5-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ae2b5-137">CommonParameters</span></span>
<span data-ttu-id="ae2b5-138">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="ae2b5-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ae2b5-139">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="ae2b5-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ae2b5-140">입력</span><span class="sxs-lookup"><span data-stu-id="ae2b5-140">INPUTS</span></span>

### <span data-ttu-id="ae2b5-141">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.IDesktopVirtualizationIdentity</span><span class="sxs-lookup"><span data-stu-id="ae2b5-141">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.IDesktopVirtualizationIdentity</span></span>

## <span data-ttu-id="ae2b5-142">출력</span><span class="sxs-lookup"><span data-stu-id="ae2b5-142">OUTPUTS</span></span>

### <span data-ttu-id="ae2b5-143">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.Api20201102Preview.IWorkspace</span><span class="sxs-lookup"><span data-stu-id="ae2b5-143">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.Api20201102Preview.IWorkspace</span></span>

## <span data-ttu-id="ae2b5-144">참고 사항</span><span class="sxs-lookup"><span data-stu-id="ae2b5-144">NOTES</span></span>

<span data-ttu-id="ae2b5-145">별칭</span><span class="sxs-lookup"><span data-stu-id="ae2b5-145">ALIASES</span></span>

<span data-ttu-id="ae2b5-146">복잡한 매개 변수 속성</span><span class="sxs-lookup"><span data-stu-id="ae2b5-146">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="ae2b5-147">아래에 설명된 매개 변수를 만들 경우 적절한 속성을 포함하는 해시 테이블을 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="ae2b5-147">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="ae2b5-148">해시 테이블에 대한 자세한 내용은 Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="ae2b5-148">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="ae2b5-149">INPUTOBJECT <IDesktopVirtualizationIdentity> : ID 매개 변수</span><span class="sxs-lookup"><span data-stu-id="ae2b5-149">INPUTOBJECT <IDesktopVirtualizationIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="ae2b5-150">`[ApplicationGroupName <String>]`: 애플리케이션 그룹의 이름</span><span class="sxs-lookup"><span data-stu-id="ae2b5-150">`[ApplicationGroupName <String>]`: The name of the application group</span></span>
  - <span data-ttu-id="ae2b5-151">`[ApplicationName <String>]`: 지정된 애플리케이션 그룹 내의 애플리케이션 이름</span><span class="sxs-lookup"><span data-stu-id="ae2b5-151">`[ApplicationName <String>]`: The name of the application within the specified application group</span></span>
  - <span data-ttu-id="ae2b5-152">`[DesktopName <String>]`: 지정된 데스크톱 그룹 내의 데스크톱 이름</span><span class="sxs-lookup"><span data-stu-id="ae2b5-152">`[DesktopName <String>]`: The name of the desktop within the specified desktop group</span></span>
  - <span data-ttu-id="ae2b5-153">`[HostPoolName <String>]`: 지정된 리소스 그룹 내의 호스트 풀의 이름</span><span class="sxs-lookup"><span data-stu-id="ae2b5-153">`[HostPoolName <String>]`: The name of the host pool within the specified resource group</span></span>
  - <span data-ttu-id="ae2b5-154">`[Id <String>]`: 리소스 ID 경로</span><span class="sxs-lookup"><span data-stu-id="ae2b5-154">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="ae2b5-155">`[MsixPackageFullName <String>]`: 지정된 호스트풀 내의 MSIX 패키지의 버전별 패키지 전체 이름</span><span class="sxs-lookup"><span data-stu-id="ae2b5-155">`[MsixPackageFullName <String>]`: The version specific package full name of the MSIX package within specified hostpool</span></span>
  - <span data-ttu-id="ae2b5-156">`[ResourceGroupName <String>]`: 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="ae2b5-156">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="ae2b5-157">이름은 대소문자와 무관합니다.</span><span class="sxs-lookup"><span data-stu-id="ae2b5-157">The name is case insensitive.</span></span>
  - <span data-ttu-id="ae2b5-158">`[SessionHostName <String>]`: 지정된 호스트 풀 내의 세션 호스트 이름</span><span class="sxs-lookup"><span data-stu-id="ae2b5-158">`[SessionHostName <String>]`: The name of the session host within the specified host pool</span></span>
  - <span data-ttu-id="ae2b5-159">`[SubscriptionId <String>]`: 대상 구독의 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="ae2b5-159">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="ae2b5-160">`[UserSessionId <String>]`: 지정된 세션 호스트 내의 사용자 세션 이름</span><span class="sxs-lookup"><span data-stu-id="ae2b5-160">`[UserSessionId <String>]`: The name of the user session within the specified session host</span></span>
  - <span data-ttu-id="ae2b5-161">`[WorkspaceName <String>]`: 작업 영역의 이름</span><span class="sxs-lookup"><span data-stu-id="ae2b5-161">`[WorkspaceName <String>]`: The name of the workspace</span></span>

## <span data-ttu-id="ae2b5-162">관련 링크</span><span class="sxs-lookup"><span data-stu-id="ae2b5-162">RELATED LINKS</span></span>

