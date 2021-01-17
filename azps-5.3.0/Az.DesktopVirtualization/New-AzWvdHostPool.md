---
external help file: ''
Module Name: Az.DesktopVirtualization
online version: https://docs.microsoft.com/en-us/powershell/module/az.desktopvirtualization/new-azwvdhostpool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/New-AzWvdHostPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/New-AzWvdHostPool.md
ms.openlocfilehash: 6f579dfcba74f68eafaa149be15649e496c46f82
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98492056"
---
# <span data-ttu-id="10cf2-101">New-AzWvdHostPool</span><span class="sxs-lookup"><span data-stu-id="10cf2-101">New-AzWvdHostPool</span></span>

## <span data-ttu-id="10cf2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="10cf2-102">SYNOPSIS</span></span>
<span data-ttu-id="10cf2-103">호스트 풀을 만들거나 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="10cf2-103">Create or update a host pool.</span></span>

## <span data-ttu-id="10cf2-104">구문</span><span class="sxs-lookup"><span data-stu-id="10cf2-104">SYNTAX</span></span>

### <span data-ttu-id="10cf2-105">CreateExpanded(기본값)</span><span class="sxs-lookup"><span data-stu-id="10cf2-105">CreateExpanded (Default)</span></span>
```
New-AzWvdHostPool -HostPoolType <HostPoolType> -LoadBalancerType <LoadBalancerType> -Location <String>
 -Name <String> -PreferredAppGroupType <PreferredAppGroupType> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-CustomRdpProperty <String>] [-Description <String>] [-ExpirationTime <DateTime>]
 [-FriendlyName <String>] [-MaxSessionLimit <Int32>]
 [-PersonalDesktopAssignmentType <PersonalDesktopAssignmentType>] [-RegistrationInfoToken <String>]
 [-RegistrationTokenOperation <RegistrationTokenOperation>] [-Ring <Int32>] [-SsoadfsAuthority <String>]
 [-SsoClientId <String>] [-SsoClientSecretKeyVaultPath <String>] [-SsoContext <String>]
 [-SsoSecretType <SsoSecretType>] [-StartVMOnConnect] [-Tag <Hashtable>] [-ValidationEnvironment]
 [-VMTemplate <String>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="10cf2-106">FullSenerioCreate</span><span class="sxs-lookup"><span data-stu-id="10cf2-106">FullSenerioCreate</span></span>
```
New-AzWvdHostPool -HostPoolType <HostPoolType> -LoadBalancerType <LoadBalancerType> -Location <String>
 -Name <String> -PreferredAppGroupType <PreferredAppGroupType> -ResourceGroupName <String>
 [-DesktopAppGroupName <String>] [-SubscriptionId <String>] [-WorkspaceName <String>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="10cf2-107">설명</span><span class="sxs-lookup"><span data-stu-id="10cf2-107">DESCRIPTION</span></span>
<span data-ttu-id="10cf2-108">호스트 풀을 만들거나 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="10cf2-108">Create or update a host pool.</span></span>

## <span data-ttu-id="10cf2-109">예제</span><span class="sxs-lookup"><span data-stu-id="10cf2-109">EXAMPLES</span></span>

### <span data-ttu-id="10cf2-110">예제 1: 이름으로 Windows Virtual Desktop HostPool 만들기</span><span class="sxs-lookup"><span data-stu-id="10cf2-110">Example 1: Create a Windows Virtual Desktop HostPool by name</span></span>
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
                            -SsoClientId $null `
                            -SsoClientSecretKeyVaultPath $null `
                            -SsoSecretType $null `
                            -SsoadfsAuthority $null `
                            -CustomRdpProperty $null `
                            -Ring $null `
                            -ValidationEnvironment:$false

Location   Name                 Type
--------   ----                 ----
eastus     HostPoolName Microsoft.DesktopVirtualization/hostpools
```

<span data-ttu-id="10cf2-111">이 명령은 리소스 그룹에 Windows Virtual Desktop HostPool을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="10cf2-111">This command creates a Windows Virtual Desktop HostPool in a Resource Group.</span></span>

### <span data-ttu-id="10cf2-112">예제 1: 이름으로 Windows Virtual Desktop HostPool 만들기</span><span class="sxs-lookup"><span data-stu-id="10cf2-112">Example 1: Create a Windows Virtual Desktop HostPool by name</span></span>
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
                            -SsoClientId $null `
                            -SsoClientSecretKeyVaultPath $null `
                            -SsoSecretType $null `
                            -SsoadfsAuthority $null `
                            -CustomRdpProperty $null `
                            -Ring $null `
                            -ValidationEnvironment:$false

Location   Name                 Type
--------   ----                 ----
eastus     HostPoolName Microsoft.DesktopVirtualization/hostpools
```

<span data-ttu-id="10cf2-113">이 명령은 리소스 그룹에 Windows Virtual Desktop HostPool을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="10cf2-113">This command creates a Windows Virtual Desktop HostPool in a Resource Group.</span></span>

## <span data-ttu-id="10cf2-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="10cf2-114">PARAMETERS</span></span>

### <span data-ttu-id="10cf2-115">-CustomRdpProperty</span><span class="sxs-lookup"><span data-stu-id="10cf2-115">-CustomRdpProperty</span></span>
<span data-ttu-id="10cf2-116">HostPool의 사용자 지정 rdp 속성입니다.</span><span class="sxs-lookup"><span data-stu-id="10cf2-116">Custom rdp property of HostPool.</span></span>

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

### <span data-ttu-id="10cf2-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="10cf2-117">-DefaultProfile</span></span>
<span data-ttu-id="10cf2-118">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="10cf2-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="10cf2-119">-Description</span><span class="sxs-lookup"><span data-stu-id="10cf2-119">-Description</span></span>
<span data-ttu-id="10cf2-120">HostPool에 대한 설명입니다.</span><span class="sxs-lookup"><span data-stu-id="10cf2-120">Description of HostPool.</span></span>

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

### <span data-ttu-id="10cf2-121">-DesktopAppGroupName</span><span class="sxs-lookup"><span data-stu-id="10cf2-121">-DesktopAppGroupName</span></span>
<span data-ttu-id="10cf2-122">데스크톱 앱 그룹 이름</span><span class="sxs-lookup"><span data-stu-id="10cf2-122">Desktop App Group Name</span></span>

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

### <span data-ttu-id="10cf2-123">-ExpirationTime</span><span class="sxs-lookup"><span data-stu-id="10cf2-123">-ExpirationTime</span></span>
<span data-ttu-id="10cf2-124">등록 토큰의 만료 시간입니다.</span><span class="sxs-lookup"><span data-stu-id="10cf2-124">Expiration time of registration token.</span></span>

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

### <span data-ttu-id="10cf2-125">-FriendlyName</span><span class="sxs-lookup"><span data-stu-id="10cf2-125">-FriendlyName</span></span>
<span data-ttu-id="10cf2-126">HostPool의 친숙한 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="10cf2-126">Friendly name of HostPool.</span></span>

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

### <span data-ttu-id="10cf2-127">-HostPoolType</span><span class="sxs-lookup"><span data-stu-id="10cf2-127">-HostPoolType</span></span>
<span data-ttu-id="10cf2-128">데스크톱용 HostPool 형식입니다.</span><span class="sxs-lookup"><span data-stu-id="10cf2-128">HostPool type for desktop.</span></span>

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

### <span data-ttu-id="10cf2-129">-LoadBalancerType</span><span class="sxs-lookup"><span data-stu-id="10cf2-129">-LoadBalancerType</span></span>
<span data-ttu-id="10cf2-130">부하 균형 조정의 유형입니다.</span><span class="sxs-lookup"><span data-stu-id="10cf2-130">The type of the load balancer.</span></span>

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

### <span data-ttu-id="10cf2-131">-Location</span><span class="sxs-lookup"><span data-stu-id="10cf2-131">-Location</span></span>
<span data-ttu-id="10cf2-132">리소스가 있는 지리적 위치</span><span class="sxs-lookup"><span data-stu-id="10cf2-132">The geo-location where the resource lives</span></span>

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

### <span data-ttu-id="10cf2-133">-MaxSessionLimit</span><span class="sxs-lookup"><span data-stu-id="10cf2-133">-MaxSessionLimit</span></span>
<span data-ttu-id="10cf2-134">HostPool의 최대 세션 제한입니다.</span><span class="sxs-lookup"><span data-stu-id="10cf2-134">The max session limit of HostPool.</span></span>

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

### <span data-ttu-id="10cf2-135">-Name</span><span class="sxs-lookup"><span data-stu-id="10cf2-135">-Name</span></span>
<span data-ttu-id="10cf2-136">지정된 리소스 그룹 내의 호스트 풀 이름</span><span class="sxs-lookup"><span data-stu-id="10cf2-136">The name of the host pool within the specified resource group</span></span>

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

### <span data-ttu-id="10cf2-137">-PersonalDesktopAssignmentType</span><span class="sxs-lookup"><span data-stu-id="10cf2-137">-PersonalDesktopAssignmentType</span></span>
<span data-ttu-id="10cf2-138">HostPool에 대한 PersonalDesktopAssignment 형식입니다.</span><span class="sxs-lookup"><span data-stu-id="10cf2-138">PersonalDesktopAssignment type for HostPool.</span></span>

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

### <span data-ttu-id="10cf2-139">-PreferredAppGroupType</span><span class="sxs-lookup"><span data-stu-id="10cf2-139">-PreferredAppGroupType</span></span>
<span data-ttu-id="10cf2-140">기본 설정 애플리케이션 그룹 유형(기본적으로 데스크톱 애플리케이션 그룹)입니다.</span><span class="sxs-lookup"><span data-stu-id="10cf2-140">The type of preferred application group type, default to Desktop Application Group</span></span>

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

### <span data-ttu-id="10cf2-141">-RegistrationInfoToken</span><span class="sxs-lookup"><span data-stu-id="10cf2-141">-RegistrationInfoToken</span></span>
<span data-ttu-id="10cf2-142">등록 토큰 base64로 인코딩된 문자열입니다.</span><span class="sxs-lookup"><span data-stu-id="10cf2-142">The registration token base64 encoded string.</span></span>

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

### <span data-ttu-id="10cf2-143">-RegistrationTokenOperation</span><span class="sxs-lookup"><span data-stu-id="10cf2-143">-RegistrationTokenOperation</span></span>
<span data-ttu-id="10cf2-144">토큰을 다시 설정하는 유형입니다.</span><span class="sxs-lookup"><span data-stu-id="10cf2-144">The type of resetting the token.</span></span>

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

### <span data-ttu-id="10cf2-145">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="10cf2-145">-ResourceGroupName</span></span>
<span data-ttu-id="10cf2-146">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="10cf2-146">The name of the resource group.</span></span>
<span data-ttu-id="10cf2-147">이름은 대소문자 무관합니다.</span><span class="sxs-lookup"><span data-stu-id="10cf2-147">The name is case insensitive.</span></span>

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

### <span data-ttu-id="10cf2-148">-Ring</span><span class="sxs-lookup"><span data-stu-id="10cf2-148">-Ring</span></span>
<span data-ttu-id="10cf2-149">HostPool의 링 번호입니다.</span><span class="sxs-lookup"><span data-stu-id="10cf2-149">The ring number of HostPool.</span></span>

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

### <span data-ttu-id="10cf2-150">-SsoadfsAuthority</span><span class="sxs-lookup"><span data-stu-id="10cf2-150">-SsoadfsAuthority</span></span>
<span data-ttu-id="10cf2-151">WVD SSO 인증서 서명을 위한 고객 ADFS 서버에 대한 URL입니다.</span><span class="sxs-lookup"><span data-stu-id="10cf2-151">URL to customer ADFS server for signing WVD SSO certificates.</span></span>

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

### <span data-ttu-id="10cf2-152">-SsoClientId</span><span class="sxs-lookup"><span data-stu-id="10cf2-152">-SsoClientId</span></span>
<span data-ttu-id="10cf2-153">WVD SSO 인증서를 발급하는 데 사용되는 등록된 Relying Party의 ClientId입니다.</span><span class="sxs-lookup"><span data-stu-id="10cf2-153">ClientId for the registered Relying Party used to issue WVD SSO certificates.</span></span>

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

### <span data-ttu-id="10cf2-154">-SsoClientSecretKeyVaultPath</span><span class="sxs-lookup"><span data-stu-id="10cf2-154">-SsoClientSecretKeyVaultPath</span></span>
<span data-ttu-id="10cf2-155">ADFS와의 통신에 사용되는 비밀을 저장하는 Azure KeyVault의 경로입니다.</span><span class="sxs-lookup"><span data-stu-id="10cf2-155">Path to Azure KeyVault storing the secret used for communication to ADFS.</span></span>

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

### <span data-ttu-id="10cf2-156">-SsoContext</span><span class="sxs-lookup"><span data-stu-id="10cf2-156">-SsoContext</span></span>
<span data-ttu-id="10cf2-157">ssoContext 비밀을 포함하는 keyvault에 대한 경로입니다.</span><span class="sxs-lookup"><span data-stu-id="10cf2-157">Path to keyvault containing ssoContext secret.</span></span>

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

### <span data-ttu-id="10cf2-158">-SsoSecretType</span><span class="sxs-lookup"><span data-stu-id="10cf2-158">-SsoSecretType</span></span>
<span data-ttu-id="10cf2-159">비밀 형식에 대한 Single Sign-On의 유형입니다.</span><span class="sxs-lookup"><span data-stu-id="10cf2-159">The type of single sign on Secret Type.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Support.SsoSecretType
Parameter Sets: CreateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="10cf2-160">-StartVMOnConnect</span><span class="sxs-lookup"><span data-stu-id="10cf2-160">-StartVMOnConnect</span></span>
<span data-ttu-id="10cf2-161">StartVMOnConnect 기능을 켜고 끄는 플래그입니다.</span><span class="sxs-lookup"><span data-stu-id="10cf2-161">The flag to turn on/off StartVMOnConnect feature.</span></span>

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

### <span data-ttu-id="10cf2-162">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="10cf2-162">-SubscriptionId</span></span>
<span data-ttu-id="10cf2-163">대상 구독의 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="10cf2-163">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="10cf2-164">-Tag</span><span class="sxs-lookup"><span data-stu-id="10cf2-164">-Tag</span></span>
<span data-ttu-id="10cf2-165">리소스 태그.</span><span class="sxs-lookup"><span data-stu-id="10cf2-165">Resource tags.</span></span>

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

### <span data-ttu-id="10cf2-166">-ValidationEnvironment</span><span class="sxs-lookup"><span data-stu-id="10cf2-166">-ValidationEnvironment</span></span>
<span data-ttu-id="10cf2-167">유효성 검사 환경입니다.</span><span class="sxs-lookup"><span data-stu-id="10cf2-167">Is validation environment.</span></span>

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

### <span data-ttu-id="10cf2-168">-VMTemplate</span><span class="sxs-lookup"><span data-stu-id="10cf2-168">-VMTemplate</span></span>
<span data-ttu-id="10cf2-169">hostpool 내의 sessionhosts 구성에 대한 VM 템플릿입니다.</span><span class="sxs-lookup"><span data-stu-id="10cf2-169">VM template for sessionhosts configuration within hostpool.</span></span>

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

### <span data-ttu-id="10cf2-170">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="10cf2-170">-WorkspaceName</span></span>
<span data-ttu-id="10cf2-171">작업 영역 이름</span><span class="sxs-lookup"><span data-stu-id="10cf2-171">Workspace Name</span></span>

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

### <span data-ttu-id="10cf2-172">-Confirm</span><span class="sxs-lookup"><span data-stu-id="10cf2-172">-Confirm</span></span>
<span data-ttu-id="10cf2-173">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="10cf2-173">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="10cf2-174">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="10cf2-174">-WhatIf</span></span>
<span data-ttu-id="10cf2-175">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="10cf2-175">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="10cf2-176">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="10cf2-176">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="10cf2-177">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="10cf2-177">CommonParameters</span></span>
<span data-ttu-id="10cf2-178">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="10cf2-178">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="10cf2-179">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="10cf2-179">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="10cf2-180">입력</span><span class="sxs-lookup"><span data-stu-id="10cf2-180">INPUTS</span></span>

## <span data-ttu-id="10cf2-181">출력</span><span class="sxs-lookup"><span data-stu-id="10cf2-181">OUTPUTS</span></span>

### <span data-ttu-id="10cf2-182">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.Api20201102Preview.IHostPool</span><span class="sxs-lookup"><span data-stu-id="10cf2-182">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.Api20201102Preview.IHostPool</span></span>

## <span data-ttu-id="10cf2-183">참고 사항</span><span class="sxs-lookup"><span data-stu-id="10cf2-183">NOTES</span></span>

<span data-ttu-id="10cf2-184">별칭</span><span class="sxs-lookup"><span data-stu-id="10cf2-184">ALIASES</span></span>

## <span data-ttu-id="10cf2-185">관련 링크</span><span class="sxs-lookup"><span data-stu-id="10cf2-185">RELATED LINKS</span></span>

