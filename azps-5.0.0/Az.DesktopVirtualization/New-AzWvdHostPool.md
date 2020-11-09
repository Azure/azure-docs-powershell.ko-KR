---
external help file: ''
Module Name: Az.DesktopVirtualization
online version: https://docs.microsoft.com/en-us/powershell/module/az.desktopvirtualization/new-azwvdhostpool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/New-AzWvdHostPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/New-AzWvdHostPool.md
ms.openlocfilehash: b91332fe8867283b5fff9cbbf1f5df96209fa2f9
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94304793"
---
# <span data-ttu-id="6596a-101">New-AzWvdHostPool</span><span class="sxs-lookup"><span data-stu-id="6596a-101">New-AzWvdHostPool</span></span>

## <span data-ttu-id="6596a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6596a-102">SYNOPSIS</span></span>
<span data-ttu-id="6596a-103">호스트 풀을 만들거나 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="6596a-103">Create or update a host pool.</span></span>

## <span data-ttu-id="6596a-104">구문과</span><span class="sxs-lookup"><span data-stu-id="6596a-104">SYNTAX</span></span>

### <span data-ttu-id="6596a-105">CreateExpanded (기본값)</span><span class="sxs-lookup"><span data-stu-id="6596a-105">CreateExpanded (Default)</span></span>
```
New-AzWvdHostPool -HostPoolType <HostPoolType> -LoadBalancerType <LoadBalancerType> -Location <String>
 -Name <String> -PreferredAppGroupType <PreferredAppGroupType> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-CustomRdpProperty <String>] [-Description <String>] [-ExpirationTime <DateTime>]
 [-FriendlyName <String>] [-MaxSessionLimit <Int32>]
 [-PersonalDesktopAssignmentType <PersonalDesktopAssignmentType>] [-RegistrationInfoToken <String>]
 [-RegistrationTokenOperation <RegistrationTokenOperation>] [-Ring <Int32>] [-SsoContext <String>]
 [-Tag <Hashtable>] [-ValidationEnvironment] [-VMTemplate <String>] [-DefaultProfile <PSObject>] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="6596a-106">FullSenerioCreate</span><span class="sxs-lookup"><span data-stu-id="6596a-106">FullSenerioCreate</span></span>
```
New-AzWvdHostPool -HostPoolType <HostPoolType> -LoadBalancerType <LoadBalancerType> -Location <String>
 -Name <String> -PreferredAppGroupType <PreferredAppGroupType> -ResourceGroupName <String>
 [-DesktopAppGroupName <String>] [-SubscriptionId <String>] [-WorkspaceName <String>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="6596a-107">설명은</span><span class="sxs-lookup"><span data-stu-id="6596a-107">DESCRIPTION</span></span>
<span data-ttu-id="6596a-108">호스트 풀을 만들거나 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="6596a-108">Create or update a host pool.</span></span>

## <span data-ttu-id="6596a-109">예제의</span><span class="sxs-lookup"><span data-stu-id="6596a-109">EXAMPLES</span></span>

### <span data-ttu-id="6596a-110">예제 1: 이름으로 Windows 가상 데스크톱 호스트 풀 만들기</span><span class="sxs-lookup"><span data-stu-id="6596a-110">Example 1: Create a Windows Virtual Desktop HostPool by name</span></span>
```powershell
PS C:\> New-AzWvdHostPool -ResourceGroupName ResourceGroupName `
                            -Name HostPoolName `
                            -Location 'eastus' `
                            -HostPoolType 'Pooled' `
                            -LoadBalancerType 'DepthFirst' `
                            -RegistrationTokenOperation 'Update' `
                            -ExpirationTime $((get-date).ToUniversalTime().AddDays(1).ToString('yyyy-MM-ddTHH:mm:ss.fffffffZ')) `
                            -Description 'Description' `
                            -FriendlyName 'Friendly Name' `
                            -MaxSessionLimit 5 `
                            -VMTemplate $null `
                            -SsoContext $null `
                            -CustomRdpProperty $null `
                            -Ring $null `
                            -ValidationEnvironment:$false

Location   Name                 Type
--------   ----                 ----
eastus     HostPoolName Microsoft.DesktopVirtualization/hostpools
```

<span data-ttu-id="6596a-111">이 명령은 리소스 그룹에 Windows 가상 데스크톱 호스트 풀을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="6596a-111">This command creates a Windows Virtual Desktop HostPool in a Resource Group.</span></span>

### <span data-ttu-id="6596a-112">예제 1: 이름으로 Windows 가상 데스크톱 호스트 풀 만들기</span><span class="sxs-lookup"><span data-stu-id="6596a-112">Example 1: Create a Windows Virtual Desktop HostPool by name</span></span>
```powershell
PS C:\> New-AzWvdHostPool -ResourceGroupName ResourceGroupName `
                            -Name HostPoolName `
                            -Location 'eastus' `
                            -HostPoolType 'Personal' `
                            -LoadBalancerType 'Persistent' `
                            -RegistrationTokenOperation 'Update' `
                            -ExpirationTime $((get-date).ToUniversalTime().AddDays(1).ToString('yyyy-MM-ddTHH:mm:ss.fffffffZ')) `
                            -Description 'Description' `
                            -FriendlyName 'Friendly Name' `
                            -MaxSessionLimit 5 `
                            -VMTemplate $null `
                            -SsoContext $null `
                            -CustomRdpProperty $null `
                            -Ring $null `
                            -ValidationEnvironment:$false

Location   Name                 Type
--------   ----                 ----
eastus     HostPoolName Microsoft.DesktopVirtualization/hostpools
```

<span data-ttu-id="6596a-113">이 명령은 리소스 그룹에 Windows 가상 데스크톱 호스트 풀을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="6596a-113">This command creates a Windows Virtual Desktop HostPool in a Resource Group.</span></span>

## <span data-ttu-id="6596a-114">변수</span><span class="sxs-lookup"><span data-stu-id="6596a-114">PARAMETERS</span></span>

### <span data-ttu-id="6596a-115">-CustomRdpProperty</span><span class="sxs-lookup"><span data-stu-id="6596a-115">-CustomRdpProperty</span></span>
<span data-ttu-id="6596a-116">HostPool의 사용자 지정 rdp 속성입니다.</span><span class="sxs-lookup"><span data-stu-id="6596a-116">Custom rdp property of HostPool.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6596a-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6596a-117">-DefaultProfile</span></span>
<span data-ttu-id="6596a-118">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="6596a-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6596a-119">-설명</span><span class="sxs-lookup"><span data-stu-id="6596a-119">-Description</span></span>
<span data-ttu-id="6596a-120">HostPool에 대 한 설명입니다.</span><span class="sxs-lookup"><span data-stu-id="6596a-120">Description of HostPool.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6596a-121">-DesktopAppGroupName</span><span class="sxs-lookup"><span data-stu-id="6596a-121">-DesktopAppGroupName</span></span>
<span data-ttu-id="6596a-122">데스크톱 앱 그룹 이름</span><span class="sxs-lookup"><span data-stu-id="6596a-122">Desktop App Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: FullSenerioCreate
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6596a-123">-ExpirationTime</span><span class="sxs-lookup"><span data-stu-id="6596a-123">-ExpirationTime</span></span>
<span data-ttu-id="6596a-124">등록 토큰의 만료 시간입니다.</span><span class="sxs-lookup"><span data-stu-id="6596a-124">Expiration time of registration token.</span></span>

```yaml
Type: System.DateTime
Parameter Sets: CreateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6596a-125">-FriendlyName</span><span class="sxs-lookup"><span data-stu-id="6596a-125">-FriendlyName</span></span>
<span data-ttu-id="6596a-126">HostPool의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="6596a-126">Friendly name of HostPool.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6596a-127">-HostPoolType</span><span class="sxs-lookup"><span data-stu-id="6596a-127">-HostPoolType</span></span>
<span data-ttu-id="6596a-128">데스크톱용 HostPool 형식.</span><span class="sxs-lookup"><span data-stu-id="6596a-128">HostPool type for desktop.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Support.HostPoolType
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6596a-129">-LoadBalancerType</span><span class="sxs-lookup"><span data-stu-id="6596a-129">-LoadBalancerType</span></span>
<span data-ttu-id="6596a-130">부하 분산의 유형입니다.</span><span class="sxs-lookup"><span data-stu-id="6596a-130">The type of the load balancer.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Support.LoadBalancerType
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6596a-131">-위치</span><span class="sxs-lookup"><span data-stu-id="6596a-131">-Location</span></span>
<span data-ttu-id="6596a-132">리소스가 상주 하는 지리적 위치</span><span class="sxs-lookup"><span data-stu-id="6596a-132">The geo-location where the resource lives</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6596a-133">-MaxSessionLimit</span><span class="sxs-lookup"><span data-stu-id="6596a-133">-MaxSessionLimit</span></span>
<span data-ttu-id="6596a-134">HostPool의 최대 세션 제한입니다.</span><span class="sxs-lookup"><span data-stu-id="6596a-134">The max session limit of HostPool.</span></span>

```yaml
Type: System.Int32
Parameter Sets: CreateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6596a-135">-이름</span><span class="sxs-lookup"><span data-stu-id="6596a-135">-Name</span></span>
<span data-ttu-id="6596a-136">지정 된 리소스 그룹 내에 있는 호스트 풀의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="6596a-136">The name of the host pool within the specified resource group</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: HostPoolName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6596a-137">-PersonalDesktopAssignmentType</span><span class="sxs-lookup"><span data-stu-id="6596a-137">-PersonalDesktopAssignmentType</span></span>
<span data-ttu-id="6596a-138">HostPool의 PersonalDesktopAssignment 유형입니다.</span><span class="sxs-lookup"><span data-stu-id="6596a-138">PersonalDesktopAssignment type for HostPool.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Support.PersonalDesktopAssignmentType
Parameter Sets: CreateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6596a-139">-PreferredAppGroupType</span><span class="sxs-lookup"><span data-stu-id="6596a-139">-PreferredAppGroupType</span></span>
<span data-ttu-id="6596a-140">기본 응용 프로그램 그룹 종류, 데스크톱 응용 프로그램 그룹의 기본값</span><span class="sxs-lookup"><span data-stu-id="6596a-140">The type of preferred application group type, default to Desktop Application Group</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Support.PreferredAppGroupType
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6596a-141">-RegistrationInfoToken</span><span class="sxs-lookup"><span data-stu-id="6596a-141">-RegistrationInfoToken</span></span>
<span data-ttu-id="6596a-142">등록 토큰 base64 인코딩된 문자열입니다.</span><span class="sxs-lookup"><span data-stu-id="6596a-142">The registration token base64 encoded string.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6596a-143">-RegistrationTokenOperation</span><span class="sxs-lookup"><span data-stu-id="6596a-143">-RegistrationTokenOperation</span></span>
<span data-ttu-id="6596a-144">토큰을 다시 설정 하는 형식입니다.</span><span class="sxs-lookup"><span data-stu-id="6596a-144">The type of resetting the token.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Support.RegistrationTokenOperation
Parameter Sets: CreateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6596a-145">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6596a-145">-ResourceGroupName</span></span>
<span data-ttu-id="6596a-146">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="6596a-146">The name of the resource group.</span></span>
<span data-ttu-id="6596a-147">이름은 대/소문자를 구분 합니다.</span><span class="sxs-lookup"><span data-stu-id="6596a-147">The name is case insensitive.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6596a-148">-링</span><span class="sxs-lookup"><span data-stu-id="6596a-148">-Ring</span></span>
<span data-ttu-id="6596a-149">HostPool의 링 번호입니다.</span><span class="sxs-lookup"><span data-stu-id="6596a-149">The ring number of HostPool.</span></span>

```yaml
Type: System.Int32
Parameter Sets: CreateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6596a-150">-SsoContext</span><span class="sxs-lookup"><span data-stu-id="6596a-150">-SsoContext</span></span>
<span data-ttu-id="6596a-151">SsoContext 비밀을 포함 하는 keyvault 경로입니다.</span><span class="sxs-lookup"><span data-stu-id="6596a-151">Path to keyvault containing ssoContext secret.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6596a-152">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="6596a-152">-SubscriptionId</span></span>
<span data-ttu-id="6596a-153">대상 구독의 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="6596a-153">The ID of the target subscription.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6596a-154">태그</span><span class="sxs-lookup"><span data-stu-id="6596a-154">-Tag</span></span>
<span data-ttu-id="6596a-155">리소스 태그.</span><span class="sxs-lookup"><span data-stu-id="6596a-155">Resource tags.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: CreateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6596a-156">-ValidationEnvironment</span><span class="sxs-lookup"><span data-stu-id="6596a-156">-ValidationEnvironment</span></span>
<span data-ttu-id="6596a-157">유효성 검사 환경입니다.</span><span class="sxs-lookup"><span data-stu-id="6596a-157">Is validation environment.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: CreateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6596a-158">-VMTemplate</span><span class="sxs-lookup"><span data-stu-id="6596a-158">-VMTemplate</span></span>
<span data-ttu-id="6596a-159">Hostpool의 sessionhosts 구성에 대 한 VM 템플릿입니다.</span><span class="sxs-lookup"><span data-stu-id="6596a-159">VM template for sessionhosts configuration within hostpool.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6596a-160">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="6596a-160">-WorkspaceName</span></span>
<span data-ttu-id="6596a-161">작업 영역 이름</span><span class="sxs-lookup"><span data-stu-id="6596a-161">Workspace Name</span></span>

```yaml
Type: System.String
Parameter Sets: FullSenerioCreate
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6596a-162">-확인</span><span class="sxs-lookup"><span data-stu-id="6596a-162">-Confirm</span></span>
<span data-ttu-id="6596a-163">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="6596a-163">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6596a-164">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6596a-164">-WhatIf</span></span>
<span data-ttu-id="6596a-165">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="6596a-165">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6596a-166">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="6596a-166">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6596a-167">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6596a-167">CommonParameters</span></span>
<span data-ttu-id="6596a-168">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="6596a-168">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6596a-169">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="6596a-169">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6596a-170">입력</span><span class="sxs-lookup"><span data-stu-id="6596a-170">INPUTS</span></span>

## <span data-ttu-id="6596a-171">출력</span><span class="sxs-lookup"><span data-stu-id="6596a-171">OUTPUTS</span></span>

### <span data-ttu-id="6596a-172">Api20191210Preview. IHostPool에 대 한 Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="6596a-172">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.Api20191210Preview.IHostPool</span></span>

## <span data-ttu-id="6596a-173">상속자</span><span class="sxs-lookup"><span data-stu-id="6596a-173">NOTES</span></span>

<span data-ttu-id="6596a-174">별칭과</span><span class="sxs-lookup"><span data-stu-id="6596a-174">ALIASES</span></span>

## <span data-ttu-id="6596a-175">관련 링크</span><span class="sxs-lookup"><span data-stu-id="6596a-175">RELATED LINKS</span></span>

