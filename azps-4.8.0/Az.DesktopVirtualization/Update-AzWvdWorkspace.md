---
external help file: ''
Module Name: Az.DesktopVirtualization
online version: https://docs.microsoft.com/en-us/powershell/module/az.desktopvirtualization/update-azwvdworkspace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Update-AzWvdWorkspace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Update-AzWvdWorkspace.md
ms.openlocfilehash: 30c0734656b79f532c56b47b64e9d7e918f92fa8
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94047789"
---
# <span data-ttu-id="00453-101">Update-AzWvdWorkspace</span><span class="sxs-lookup"><span data-stu-id="00453-101">Update-AzWvdWorkspace</span></span>

## <span data-ttu-id="00453-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="00453-102">SYNOPSIS</span></span>
<span data-ttu-id="00453-103">작업 영역을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="00453-103">Update a workspace.</span></span>

## <span data-ttu-id="00453-104">구문과</span><span class="sxs-lookup"><span data-stu-id="00453-104">SYNTAX</span></span>

### <span data-ttu-id="00453-105">UpdateExpanded 됨 (기본값)</span><span class="sxs-lookup"><span data-stu-id="00453-105">UpdateExpanded (Default)</span></span>
```
Update-AzWvdWorkspace -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-ApplicationGroupReference <String[]>] [-Description <String>] [-FriendlyName <String>] [-Tag <Hashtable>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="00453-106">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="00453-106">UpdateViaIdentityExpanded</span></span>
```
Update-AzWvdWorkspace -InputObject <IDesktopVirtualizationIdentity> [-ApplicationGroupReference <String[]>]
 [-Description <String>] [-FriendlyName <String>] [-Tag <Hashtable>] [-DefaultProfile <PSObject>] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="00453-107">설명은</span><span class="sxs-lookup"><span data-stu-id="00453-107">DESCRIPTION</span></span>
<span data-ttu-id="00453-108">작업 영역을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="00453-108">Update a workspace.</span></span>

## <span data-ttu-id="00453-109">예제의</span><span class="sxs-lookup"><span data-stu-id="00453-109">EXAMPLES</span></span>

### <span data-ttu-id="00453-110">예제 1: 이름으로 Windows 가상 데스크톱 Worksapce 업데이트</span><span class="sxs-lookup"><span data-stu-id="00453-110">Example 1: Update a Windows Virtual Desktop Worksapce by name</span></span>
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

<span data-ttu-id="00453-111">이 명령은 리소스 그룹의 Windows 가상 데스크톱 작업 영역을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="00453-111">This command updates a Windows Virtual Desktop Workspace in a Resource Group.</span></span>

## <span data-ttu-id="00453-112">변수</span><span class="sxs-lookup"><span data-stu-id="00453-112">PARAMETERS</span></span>

### <span data-ttu-id="00453-113">-ApplicationGroupReference 설정</span><span class="sxs-lookup"><span data-stu-id="00453-113">-ApplicationGroupReference</span></span>
<span data-ttu-id="00453-114">ApplicationGroup 링크 목록입니다.</span><span class="sxs-lookup"><span data-stu-id="00453-114">List of applicationGroup links.</span></span>

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

### <span data-ttu-id="00453-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="00453-115">-DefaultProfile</span></span>
<span data-ttu-id="00453-116">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="00453-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="00453-117">-설명</span><span class="sxs-lookup"><span data-stu-id="00453-117">-Description</span></span>
<span data-ttu-id="00453-118">작업 영역에 대 한 설명입니다.</span><span class="sxs-lookup"><span data-stu-id="00453-118">Description of Workspace.</span></span>

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

### <span data-ttu-id="00453-119">-FriendlyName</span><span class="sxs-lookup"><span data-stu-id="00453-119">-FriendlyName</span></span>
<span data-ttu-id="00453-120">작업 영역의 친근 한 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="00453-120">Friendly name of Workspace.</span></span>

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

### <span data-ttu-id="00453-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="00453-121">-InputObject</span></span>
<span data-ttu-id="00453-122">생성할 id 매개 변수는 INPUTOBJECT 속성에 대 한 참고 섹션을 참조 하 고 해시 테이블을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="00453-122">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="00453-123">-이름</span><span class="sxs-lookup"><span data-stu-id="00453-123">-Name</span></span>
<span data-ttu-id="00453-124">작업 영역의 이름</span><span class="sxs-lookup"><span data-stu-id="00453-124">The name of the workspace</span></span>

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

### <span data-ttu-id="00453-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="00453-125">-ResourceGroupName</span></span>
<span data-ttu-id="00453-126">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="00453-126">The name of the resource group.</span></span>
<span data-ttu-id="00453-127">이름은 대/소문자를 구분 합니다.</span><span class="sxs-lookup"><span data-stu-id="00453-127">The name is case insensitive.</span></span>

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

### <span data-ttu-id="00453-128">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="00453-128">-SubscriptionId</span></span>
<span data-ttu-id="00453-129">대상 구독의 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="00453-129">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="00453-130">태그</span><span class="sxs-lookup"><span data-stu-id="00453-130">-Tag</span></span>
<span data-ttu-id="00453-131">업데이트할 태그</span><span class="sxs-lookup"><span data-stu-id="00453-131">tags to be updated</span></span>

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

### <span data-ttu-id="00453-132">-확인</span><span class="sxs-lookup"><span data-stu-id="00453-132">-Confirm</span></span>
<span data-ttu-id="00453-133">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="00453-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="00453-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="00453-134">-WhatIf</span></span>
<span data-ttu-id="00453-135">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="00453-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="00453-136">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="00453-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="00453-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="00453-137">CommonParameters</span></span>
<span data-ttu-id="00453-138">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="00453-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="00453-139">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="00453-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="00453-140">입력</span><span class="sxs-lookup"><span data-stu-id="00453-140">INPUTS</span></span>

### <span data-ttu-id="00453-141">IDesktopVirtualizationIdentity (Microsoft. PowerShell.)</span><span class="sxs-lookup"><span data-stu-id="00453-141">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.IDesktopVirtualizationIdentity</span></span>

## <span data-ttu-id="00453-142">출력</span><span class="sxs-lookup"><span data-stu-id="00453-142">OUTPUTS</span></span>

### <span data-ttu-id="00453-143">Api20191210Preview. i i m. .exe 작업 영역</span><span class="sxs-lookup"><span data-stu-id="00453-143">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.Api20191210Preview.IWorkspace</span></span>

## <span data-ttu-id="00453-144">상속자</span><span class="sxs-lookup"><span data-stu-id="00453-144">NOTES</span></span>

<span data-ttu-id="00453-145">별칭과</span><span class="sxs-lookup"><span data-stu-id="00453-145">ALIASES</span></span>

<span data-ttu-id="00453-146">복합 매개 변수 속성</span><span class="sxs-lookup"><span data-stu-id="00453-146">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="00453-147">아래 설명 된 매개 변수를 만들려면 적절 한 속성을 포함 하는 해시 테이블을 생성 합니다.</span><span class="sxs-lookup"><span data-stu-id="00453-147">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="00453-148">해시 테이블에 대 한 자세한 내용은 Get-Help about_Hash_Tables를 실행 하세요.</span><span class="sxs-lookup"><span data-stu-id="00453-148">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="00453-149">INPUTOBJECT <IDesktopVirtualizationIdentity> : Identity 매개 변수</span><span class="sxs-lookup"><span data-stu-id="00453-149">INPUTOBJECT <IDesktopVirtualizationIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="00453-150">`[ApplicationGroupName <String>]`: 응용 프로그램 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="00453-150">`[ApplicationGroupName <String>]`: The name of the application group</span></span>
  - <span data-ttu-id="00453-151">`[ApplicationName <String>]`: 지정 된 응용 프로그램 그룹 내 응용 프로그램의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="00453-151">`[ApplicationName <String>]`: The name of the application within the specified application group</span></span>
  - <span data-ttu-id="00453-152">`[DesktopName <String>]`: 지정 된 데스크톱 그룹 내의 데스크톱 이름</span><span class="sxs-lookup"><span data-stu-id="00453-152">`[DesktopName <String>]`: The name of the desktop within the specified desktop group</span></span>
  - <span data-ttu-id="00453-153">`[HostPoolName <String>]`: 지정 된 리소스 그룹 내에 있는 호스트 풀의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="00453-153">`[HostPoolName <String>]`: The name of the host pool within the specified resource group</span></span>
  - <span data-ttu-id="00453-154">`[Id <String>]`: 리소스 id 경로</span><span class="sxs-lookup"><span data-stu-id="00453-154">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="00453-155">`[ResourceGroupName <String>]`: 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="00453-155">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="00453-156">이름은 대/소문자를 구분 합니다.</span><span class="sxs-lookup"><span data-stu-id="00453-156">The name is case insensitive.</span></span>
  - <span data-ttu-id="00453-157">`[SessionHostName <String>]`: 지정 된 호스트 풀 내에 있는 세션 호스트의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="00453-157">`[SessionHostName <String>]`: The name of the session host within the specified host pool</span></span>
  - <span data-ttu-id="00453-158">`[SubscriptionId <String>]`: 대상 구독의 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="00453-158">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="00453-159">`[UserSessionId <String>]`: 지정 된 세션 호스트 내에 있는 사용자 세션의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="00453-159">`[UserSessionId <String>]`: The name of the user session within the specified session host</span></span>
  - <span data-ttu-id="00453-160">`[WorkspaceName <String>]`: 작업 영역의 이름</span><span class="sxs-lookup"><span data-stu-id="00453-160">`[WorkspaceName <String>]`: The name of the workspace</span></span>

## <span data-ttu-id="00453-161">관련 링크</span><span class="sxs-lookup"><span data-stu-id="00453-161">RELATED LINKS</span></span>

