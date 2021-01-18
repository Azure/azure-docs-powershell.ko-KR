---
external help file: ''
Module Name: Az.DesktopVirtualization
online version: https://docs.microsoft.com/en-us/powershell/module/az.desktopvirtualization/update-azwvdsessionhost
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Update-AzWvdSessionHost.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Update-AzWvdSessionHost.md
ms.openlocfilehash: ddc8dee2e553701fc8f7660fe72b4070ff9eafa1
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98493058"
---
# <span data-ttu-id="ac850-101">Update-AzWvdSessionHost</span><span class="sxs-lookup"><span data-stu-id="ac850-101">Update-AzWvdSessionHost</span></span>

## <span data-ttu-id="ac850-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ac850-102">SYNOPSIS</span></span>
<span data-ttu-id="ac850-103">세션 호스트를 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="ac850-103">Update a session host.</span></span>

## <span data-ttu-id="ac850-104">구문</span><span class="sxs-lookup"><span data-stu-id="ac850-104">SYNTAX</span></span>

### <span data-ttu-id="ac850-105">UpdateExpanded(기본값)</span><span class="sxs-lookup"><span data-stu-id="ac850-105">UpdateExpanded (Default)</span></span>
```
Update-AzWvdSessionHost -HostPoolName <String> -Name <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-AllowNewSession] [-AssignedUser <String>] [-DefaultProfile <PSObject>]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="ac850-106">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="ac850-106">UpdateViaIdentityExpanded</span></span>
```
Update-AzWvdSessionHost -InputObject <IDesktopVirtualizationIdentity> [-AllowNewSession]
 [-AssignedUser <String>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="ac850-107">설명</span><span class="sxs-lookup"><span data-stu-id="ac850-107">DESCRIPTION</span></span>
<span data-ttu-id="ac850-108">세션 호스트를 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="ac850-108">Update a session host.</span></span>

## <span data-ttu-id="ac850-109">예제</span><span class="sxs-lookup"><span data-stu-id="ac850-109">EXAMPLES</span></span>

### <span data-ttu-id="ac850-110">예제 1: 이름으로 Windows Virtual Desktop SessionHost 업데이트</span><span class="sxs-lookup"><span data-stu-id="ac850-110">Example 1: Update a Windows Virtual Desktop SessionHost by name</span></span>
```powershell
PS C:\> Update-AzWvdSessionHost -ResourceGroupName ResourceGroupName `
                            -HostPoolName HostPoolName `
                            -Name SessionHostName `
                            -AllowNewSession:$false

Name                                               Type
----                                               ----
HostPoolName/SessionHostName Microsoft.DesktopVirtualization/hostpools/sessionhosts
```

<span data-ttu-id="ac850-111">이 명령은 호스트 풀에서 Windows Virtual Desktop SessionHost를 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="ac850-111">This command updates a Windows Virtual Desktop SessionHost in a Host Pool.</span></span>

## <span data-ttu-id="ac850-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ac850-112">PARAMETERS</span></span>

### <span data-ttu-id="ac850-113">-AllowNewSession</span><span class="sxs-lookup"><span data-stu-id="ac850-113">-AllowNewSession</span></span>
<span data-ttu-id="ac850-114">새 세션을 허용합니다.</span><span class="sxs-lookup"><span data-stu-id="ac850-114">Allow a new session.</span></span>

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

### <span data-ttu-id="ac850-115">-AssignedUser</span><span class="sxs-lookup"><span data-stu-id="ac850-115">-AssignedUser</span></span>
<span data-ttu-id="ac850-116">SessionHost에 할당된 사용자입니다.</span><span class="sxs-lookup"><span data-stu-id="ac850-116">User assigned to SessionHost.</span></span>

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

### <span data-ttu-id="ac850-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ac850-117">-DefaultProfile</span></span>
<span data-ttu-id="ac850-118">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="ac850-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ac850-119">-HostPoolName</span><span class="sxs-lookup"><span data-stu-id="ac850-119">-HostPoolName</span></span>
<span data-ttu-id="ac850-120">지정된 리소스 그룹 내의 호스트 풀 이름</span><span class="sxs-lookup"><span data-stu-id="ac850-120">The name of the host pool within the specified resource group</span></span>

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

### <span data-ttu-id="ac850-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ac850-121">-InputObject</span></span>
<span data-ttu-id="ac850-122">ID 매개 변수를 생성하는 경우 INPUTOBJECT 속성에 대한 NOTES 섹션을 참조하고 해시 테이블을 만드십시오.</span><span class="sxs-lookup"><span data-stu-id="ac850-122">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="ac850-123">-Name</span><span class="sxs-lookup"><span data-stu-id="ac850-123">-Name</span></span>
<span data-ttu-id="ac850-124">지정된 호스트 풀 내의 세션 호스트 이름</span><span class="sxs-lookup"><span data-stu-id="ac850-124">The name of the session host within the specified host pool</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases: SessionHostName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ac850-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ac850-125">-ResourceGroupName</span></span>
<span data-ttu-id="ac850-126">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="ac850-126">The name of the resource group.</span></span>
<span data-ttu-id="ac850-127">이름은 대소문자 무관합니다.</span><span class="sxs-lookup"><span data-stu-id="ac850-127">The name is case insensitive.</span></span>

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

### <span data-ttu-id="ac850-128">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="ac850-128">-SubscriptionId</span></span>
<span data-ttu-id="ac850-129">대상 구독의 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="ac850-129">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="ac850-130">-Confirm</span><span class="sxs-lookup"><span data-stu-id="ac850-130">-Confirm</span></span>
<span data-ttu-id="ac850-131">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="ac850-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ac850-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ac850-132">-WhatIf</span></span>
<span data-ttu-id="ac850-133">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="ac850-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ac850-134">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="ac850-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ac850-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ac850-135">CommonParameters</span></span>
<span data-ttu-id="ac850-136">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="ac850-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ac850-137">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="ac850-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ac850-138">입력</span><span class="sxs-lookup"><span data-stu-id="ac850-138">INPUTS</span></span>

### <span data-ttu-id="ac850-139">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.IDesktopVirtualizationIdentity</span><span class="sxs-lookup"><span data-stu-id="ac850-139">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.IDesktopVirtualizationIdentity</span></span>

## <span data-ttu-id="ac850-140">출력</span><span class="sxs-lookup"><span data-stu-id="ac850-140">OUTPUTS</span></span>

### <span data-ttu-id="ac850-141">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.Api20201102Preview.ISessionHost</span><span class="sxs-lookup"><span data-stu-id="ac850-141">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.Api20201102Preview.ISessionHost</span></span>

## <span data-ttu-id="ac850-142">참고 사항</span><span class="sxs-lookup"><span data-stu-id="ac850-142">NOTES</span></span>

<span data-ttu-id="ac850-143">별칭</span><span class="sxs-lookup"><span data-stu-id="ac850-143">ALIASES</span></span>

<span data-ttu-id="ac850-144">복합 매개 변수 속성</span><span class="sxs-lookup"><span data-stu-id="ac850-144">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="ac850-145">아래에 설명된 매개 변수를 만들 수 있도록 적절한 속성을 포함하는 해시 테이블을 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="ac850-145">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="ac850-146">해시 테이블에 대한 자세한 내용은 다음 Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="ac850-146">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="ac850-147">INPUTOBJECT: <IDesktopVirtualizationIdentity> ID 매개 변수</span><span class="sxs-lookup"><span data-stu-id="ac850-147">INPUTOBJECT <IDesktopVirtualizationIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="ac850-148">`[ApplicationGroupName <String>]`: 애플리케이션 그룹의 이름</span><span class="sxs-lookup"><span data-stu-id="ac850-148">`[ApplicationGroupName <String>]`: The name of the application group</span></span>
  - <span data-ttu-id="ac850-149">`[ApplicationName <String>]`: 지정된 애플리케이션 그룹 내의 애플리케이션 이름</span><span class="sxs-lookup"><span data-stu-id="ac850-149">`[ApplicationName <String>]`: The name of the application within the specified application group</span></span>
  - <span data-ttu-id="ac850-150">`[DesktopName <String>]`: 지정된 데스크톱 그룹 내에서 데스크톱의 이름</span><span class="sxs-lookup"><span data-stu-id="ac850-150">`[DesktopName <String>]`: The name of the desktop within the specified desktop group</span></span>
  - <span data-ttu-id="ac850-151">`[HostPoolName <String>]`: 지정된 리소스 그룹 내에서 호스트 풀의 이름</span><span class="sxs-lookup"><span data-stu-id="ac850-151">`[HostPoolName <String>]`: The name of the host pool within the specified resource group</span></span>
  - <span data-ttu-id="ac850-152">`[Id <String>]`: 리소스 ID 경로</span><span class="sxs-lookup"><span data-stu-id="ac850-152">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="ac850-153">`[MsixPackageFullName <String>]`: 지정된 호스트 풀 내의 MSIX 패키지의 버전별 패키지 전체 이름</span><span class="sxs-lookup"><span data-stu-id="ac850-153">`[MsixPackageFullName <String>]`: The version specific package full name of the MSIX package within specified hostpool</span></span>
  - <span data-ttu-id="ac850-154">`[ResourceGroupName <String>]`: 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="ac850-154">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="ac850-155">이름은 대소문자 무관합니다.</span><span class="sxs-lookup"><span data-stu-id="ac850-155">The name is case insensitive.</span></span>
  - <span data-ttu-id="ac850-156">`[SessionHostName <String>]`: 지정된 호스트 풀 내의 세션 호스트 이름</span><span class="sxs-lookup"><span data-stu-id="ac850-156">`[SessionHostName <String>]`: The name of the session host within the specified host pool</span></span>
  - <span data-ttu-id="ac850-157">`[SubscriptionId <String>]`: 대상 구독의 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="ac850-157">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="ac850-158">`[UserSessionId <String>]`: 지정된 세션 호스트 내의 사용자 세션 이름</span><span class="sxs-lookup"><span data-stu-id="ac850-158">`[UserSessionId <String>]`: The name of the user session within the specified session host</span></span>
  - <span data-ttu-id="ac850-159">`[WorkspaceName <String>]`: 작업 영역의 이름</span><span class="sxs-lookup"><span data-stu-id="ac850-159">`[WorkspaceName <String>]`: The name of the workspace</span></span>

## <span data-ttu-id="ac850-160">관련 링크</span><span class="sxs-lookup"><span data-stu-id="ac850-160">RELATED LINKS</span></span>

