---
external help file: ''
Module Name: Az.DesktopVirtualization
online version: https://docs.microsoft.com/en-us/powershell/module/az.desktopvirtualization/update-azwvdhostpool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Update-AzWvdHostPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Update-AzWvdHostPool.md
ms.openlocfilehash: ffb38dd20c5bc43c3d243e5a6f320fdc5d48d008
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94217621"
---
# <span data-ttu-id="d2815-101">Update-AzWvdHostPool</span><span class="sxs-lookup"><span data-stu-id="d2815-101">Update-AzWvdHostPool</span></span>

## <span data-ttu-id="d2815-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d2815-102">SYNOPSIS</span></span>
<span data-ttu-id="d2815-103">호스트 풀을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="d2815-103">Update a host pool.</span></span>

## <span data-ttu-id="d2815-104">구문과</span><span class="sxs-lookup"><span data-stu-id="d2815-104">SYNTAX</span></span>

### <span data-ttu-id="d2815-105">UpdateExpanded 됨 (기본값)</span><span class="sxs-lookup"><span data-stu-id="d2815-105">UpdateExpanded (Default)</span></span>
```
Update-AzWvdHostPool -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-CustomRdpProperty <String>] [-Description <String>] [-FriendlyName <String>]
 [-LoadBalancerType <LoadBalancerType>] [-MaxSessionLimit <Int32>]
 [-PersonalDesktopAssignmentType <PersonalDesktopAssignmentType>]
 [-PreferredAppGroupType <PreferredAppGroupType>] [-RegistrationInfoExpirationTime <DateTime>]
 [-RegistrationInfoRegistrationTokenOperation <RegistrationTokenOperation>] [-Ring <Int32>]
 [-SsoContext <String>] [-Tag <Hashtable>] [-ValidationEnvironment] [-DefaultProfile <PSObject>] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="d2815-106">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="d2815-106">UpdateViaIdentityExpanded</span></span>
```
Update-AzWvdHostPool -InputObject <IDesktopVirtualizationIdentity> [-CustomRdpProperty <String>]
 [-Description <String>] [-FriendlyName <String>] [-LoadBalancerType <LoadBalancerType>]
 [-MaxSessionLimit <Int32>] [-PersonalDesktopAssignmentType <PersonalDesktopAssignmentType>]
 [-PreferredAppGroupType <PreferredAppGroupType>] [-RegistrationInfoExpirationTime <DateTime>]
 [-RegistrationInfoRegistrationTokenOperation <RegistrationTokenOperation>] [-Ring <Int32>]
 [-SsoContext <String>] [-Tag <Hashtable>] [-ValidationEnvironment] [-DefaultProfile <PSObject>] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="d2815-107">설명은</span><span class="sxs-lookup"><span data-stu-id="d2815-107">DESCRIPTION</span></span>
<span data-ttu-id="d2815-108">호스트 풀을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="d2815-108">Update a host pool.</span></span>

## <span data-ttu-id="d2815-109">예제의</span><span class="sxs-lookup"><span data-stu-id="d2815-109">EXAMPLES</span></span>

### <span data-ttu-id="d2815-110">예제 1: 이름으로 Windows 가상 데스크톱 호스트 풀 업데이트</span><span class="sxs-lookup"><span data-stu-id="d2815-110">Example 1: Update a Windows Virtual Desktop HostPool by name</span></span>
```powershell
PS C:\> Update-AzWvdHostPool -ResourceGroupName ResourceGroupName `
                            -Name HostPoolName `
                            -LoadBalancerType 'BreadthFirst' `
                            -Description 'Description' `
                            -FriendlyName 'Friendly Name' `
                            -MaxSessionLimit 6 `
                            -SsoContext $null `
                            -CustomRdpProperty $null `
                            -Ring $null `
                            -ValidationEnvironment:$false

Location   Name                 Type
--------   ----                 ----
eastus     HostPoolName Microsoft.DesktopVirtualization/hostpools
```

<span data-ttu-id="d2815-111">이 명령은 리소스 그룹의 Windows 가상 데스크톱 호스트 풀을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="d2815-111">This command updates a Windows Virtual Desktop HostPool in a Resource Group.</span></span>

## <span data-ttu-id="d2815-112">변수</span><span class="sxs-lookup"><span data-stu-id="d2815-112">PARAMETERS</span></span>

### <span data-ttu-id="d2815-113">-CustomRdpProperty</span><span class="sxs-lookup"><span data-stu-id="d2815-113">-CustomRdpProperty</span></span>
<span data-ttu-id="d2815-114">HostPool의 사용자 지정 rdp 속성입니다.</span><span class="sxs-lookup"><span data-stu-id="d2815-114">Custom rdp property of HostPool.</span></span>

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

### <span data-ttu-id="d2815-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d2815-115">-DefaultProfile</span></span>
<span data-ttu-id="d2815-116">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="d2815-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d2815-117">-설명</span><span class="sxs-lookup"><span data-stu-id="d2815-117">-Description</span></span>
<span data-ttu-id="d2815-118">HostPool에 대 한 설명입니다.</span><span class="sxs-lookup"><span data-stu-id="d2815-118">Description of HostPool.</span></span>

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

### <span data-ttu-id="d2815-119">-FriendlyName</span><span class="sxs-lookup"><span data-stu-id="d2815-119">-FriendlyName</span></span>
<span data-ttu-id="d2815-120">HostPool의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="d2815-120">Friendly name of HostPool.</span></span>

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

### <span data-ttu-id="d2815-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d2815-121">-InputObject</span></span>
<span data-ttu-id="d2815-122">생성할 id 매개 변수는 INPUTOBJECT 속성에 대 한 참고 섹션을 참조 하 고 해시 테이블을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="d2815-122">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="d2815-123">-LoadBalancerType</span><span class="sxs-lookup"><span data-stu-id="d2815-123">-LoadBalancerType</span></span>
<span data-ttu-id="d2815-124">부하 분산의 유형입니다.</span><span class="sxs-lookup"><span data-stu-id="d2815-124">The type of the load balancer.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Support.LoadBalancerType
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d2815-125">-MaxSessionLimit</span><span class="sxs-lookup"><span data-stu-id="d2815-125">-MaxSessionLimit</span></span>
<span data-ttu-id="d2815-126">HostPool의 최대 세션 제한입니다.</span><span class="sxs-lookup"><span data-stu-id="d2815-126">The max session limit of HostPool.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d2815-127">-이름</span><span class="sxs-lookup"><span data-stu-id="d2815-127">-Name</span></span>
<span data-ttu-id="d2815-128">지정 된 리소스 그룹 내에 있는 호스트 풀의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="d2815-128">The name of the host pool within the specified resource group</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases: HostPoolName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d2815-129">-PersonalDesktopAssignmentType</span><span class="sxs-lookup"><span data-stu-id="d2815-129">-PersonalDesktopAssignmentType</span></span>
<span data-ttu-id="d2815-130">HostPool의 PersonalDesktopAssignment 유형입니다.</span><span class="sxs-lookup"><span data-stu-id="d2815-130">PersonalDesktopAssignment type for HostPool.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Support.PersonalDesktopAssignmentType
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d2815-131">-PreferredAppGroupType</span><span class="sxs-lookup"><span data-stu-id="d2815-131">-PreferredAppGroupType</span></span>
<span data-ttu-id="d2815-132">기본 응용 프로그램 그룹 종류, 데스크톱 응용 프로그램 그룹의 기본값</span><span class="sxs-lookup"><span data-stu-id="d2815-132">The type of preferred application group type, default to Desktop Application Group</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Support.PreferredAppGroupType
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d2815-133">-RegistrationInfoExpirationTime</span><span class="sxs-lookup"><span data-stu-id="d2815-133">-RegistrationInfoExpirationTime</span></span>
<span data-ttu-id="d2815-134">등록 토큰의 만료 시간입니다.</span><span class="sxs-lookup"><span data-stu-id="d2815-134">Expiration time of registration token.</span></span>

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

### <span data-ttu-id="d2815-135">-RegistrationInfoRegistrationTokenOperation</span><span class="sxs-lookup"><span data-stu-id="d2815-135">-RegistrationInfoRegistrationTokenOperation</span></span>
<span data-ttu-id="d2815-136">토큰을 다시 설정 하는 형식입니다.</span><span class="sxs-lookup"><span data-stu-id="d2815-136">The type of resetting the token.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Support.RegistrationTokenOperation
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d2815-137">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d2815-137">-ResourceGroupName</span></span>
<span data-ttu-id="d2815-138">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="d2815-138">The name of the resource group.</span></span>
<span data-ttu-id="d2815-139">이름은 대/소문자를 구분 합니다.</span><span class="sxs-lookup"><span data-stu-id="d2815-139">The name is case insensitive.</span></span>

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

### <span data-ttu-id="d2815-140">-링</span><span class="sxs-lookup"><span data-stu-id="d2815-140">-Ring</span></span>
<span data-ttu-id="d2815-141">HostPool의 링 번호입니다.</span><span class="sxs-lookup"><span data-stu-id="d2815-141">The ring number of HostPool.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d2815-142">-SsoContext</span><span class="sxs-lookup"><span data-stu-id="d2815-142">-SsoContext</span></span>
<span data-ttu-id="d2815-143">SsoContext 비밀을 포함 하는 keyvault 경로입니다.</span><span class="sxs-lookup"><span data-stu-id="d2815-143">Path to keyvault containing ssoContext secret.</span></span>

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

### <span data-ttu-id="d2815-144">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="d2815-144">-SubscriptionId</span></span>
<span data-ttu-id="d2815-145">대상 구독의 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="d2815-145">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="d2815-146">태그</span><span class="sxs-lookup"><span data-stu-id="d2815-146">-Tag</span></span>
<span data-ttu-id="d2815-147">업데이트할 태그</span><span class="sxs-lookup"><span data-stu-id="d2815-147">tags to be updated</span></span>

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

### <span data-ttu-id="d2815-148">-ValidationEnvironment</span><span class="sxs-lookup"><span data-stu-id="d2815-148">-ValidationEnvironment</span></span>
<span data-ttu-id="d2815-149">유효성 검사 환경입니다.</span><span class="sxs-lookup"><span data-stu-id="d2815-149">Is validation environment.</span></span>

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

### <span data-ttu-id="d2815-150">-확인</span><span class="sxs-lookup"><span data-stu-id="d2815-150">-Confirm</span></span>
<span data-ttu-id="d2815-151">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="d2815-151">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d2815-152">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d2815-152">-WhatIf</span></span>
<span data-ttu-id="d2815-153">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="d2815-153">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d2815-154">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="d2815-154">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d2815-155">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d2815-155">CommonParameters</span></span>
<span data-ttu-id="d2815-156">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="d2815-156">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d2815-157">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="d2815-157">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d2815-158">입력</span><span class="sxs-lookup"><span data-stu-id="d2815-158">INPUTS</span></span>

### <span data-ttu-id="d2815-159">IDesktopVirtualizationIdentity (Microsoft. PowerShell.)</span><span class="sxs-lookup"><span data-stu-id="d2815-159">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.IDesktopVirtualizationIdentity</span></span>

## <span data-ttu-id="d2815-160">출력</span><span class="sxs-lookup"><span data-stu-id="d2815-160">OUTPUTS</span></span>

### <span data-ttu-id="d2815-161">Api20191210Preview. IHostPool에 대 한 Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="d2815-161">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.Api20191210Preview.IHostPool</span></span>

## <span data-ttu-id="d2815-162">상속자</span><span class="sxs-lookup"><span data-stu-id="d2815-162">NOTES</span></span>

<span data-ttu-id="d2815-163">별칭과</span><span class="sxs-lookup"><span data-stu-id="d2815-163">ALIASES</span></span>

<span data-ttu-id="d2815-164">복합 매개 변수 속성</span><span class="sxs-lookup"><span data-stu-id="d2815-164">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="d2815-165">아래 설명 된 매개 변수를 만들려면 적절 한 속성을 포함 하는 해시 테이블을 생성 합니다.</span><span class="sxs-lookup"><span data-stu-id="d2815-165">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="d2815-166">해시 테이블에 대 한 자세한 내용은 Get-Help about_Hash_Tables를 실행 하세요.</span><span class="sxs-lookup"><span data-stu-id="d2815-166">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="d2815-167">INPUTOBJECT <IDesktopVirtualizationIdentity> : Identity 매개 변수</span><span class="sxs-lookup"><span data-stu-id="d2815-167">INPUTOBJECT <IDesktopVirtualizationIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="d2815-168">`[ApplicationGroupName <String>]`: 응용 프로그램 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="d2815-168">`[ApplicationGroupName <String>]`: The name of the application group</span></span>
  - <span data-ttu-id="d2815-169">`[ApplicationName <String>]`: 지정 된 응용 프로그램 그룹 내 응용 프로그램의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="d2815-169">`[ApplicationName <String>]`: The name of the application within the specified application group</span></span>
  - <span data-ttu-id="d2815-170">`[DesktopName <String>]`: 지정 된 데스크톱 그룹 내의 데스크톱 이름</span><span class="sxs-lookup"><span data-stu-id="d2815-170">`[DesktopName <String>]`: The name of the desktop within the specified desktop group</span></span>
  - <span data-ttu-id="d2815-171">`[HostPoolName <String>]`: 지정 된 리소스 그룹 내에 있는 호스트 풀의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="d2815-171">`[HostPoolName <String>]`: The name of the host pool within the specified resource group</span></span>
  - <span data-ttu-id="d2815-172">`[Id <String>]`: 리소스 id 경로</span><span class="sxs-lookup"><span data-stu-id="d2815-172">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="d2815-173">`[ResourceGroupName <String>]`: 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="d2815-173">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="d2815-174">이름은 대/소문자를 구분 합니다.</span><span class="sxs-lookup"><span data-stu-id="d2815-174">The name is case insensitive.</span></span>
  - <span data-ttu-id="d2815-175">`[SessionHostName <String>]`: 지정 된 호스트 풀 내에 있는 세션 호스트의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="d2815-175">`[SessionHostName <String>]`: The name of the session host within the specified host pool</span></span>
  - <span data-ttu-id="d2815-176">`[SubscriptionId <String>]`: 대상 구독의 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="d2815-176">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="d2815-177">`[UserSessionId <String>]`: 지정 된 세션 호스트 내에 있는 사용자 세션의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="d2815-177">`[UserSessionId <String>]`: The name of the user session within the specified session host</span></span>
  - <span data-ttu-id="d2815-178">`[WorkspaceName <String>]`: 작업 영역의 이름</span><span class="sxs-lookup"><span data-stu-id="d2815-178">`[WorkspaceName <String>]`: The name of the workspace</span></span>

## <span data-ttu-id="d2815-179">관련 링크</span><span class="sxs-lookup"><span data-stu-id="d2815-179">RELATED LINKS</span></span>

