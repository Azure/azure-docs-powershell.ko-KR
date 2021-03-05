---
external help file: ''
Module Name: Az.DesktopVirtualization
online version: https://docs.microsoft.com/powershell/module/az.desktopvirtualization/new-azwvdhostpool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/New-AzWvdHostPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/New-AzWvdHostPool.md
ms.openlocfilehash: d90c81e307d56272fb9808760ef969705decb5d5
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101966160"
---
# <span data-ttu-id="7775f-101">New-AzWvdHostPool</span><span class="sxs-lookup"><span data-stu-id="7775f-101">New-AzWvdHostPool</span></span>

## <span data-ttu-id="7775f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7775f-102">SYNOPSIS</span></span>
<span data-ttu-id="7775f-103">호스트 풀을 만들거나 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="7775f-103">Create or update a host pool.</span></span>

## <span data-ttu-id="7775f-104">구문</span><span class="sxs-lookup"><span data-stu-id="7775f-104">SYNTAX</span></span>

### <span data-ttu-id="7775f-105">CreateExpanded(기본값)</span><span class="sxs-lookup"><span data-stu-id="7775f-105">CreateExpanded (Default)</span></span>
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

### <span data-ttu-id="7775f-106">FullSenerioCreate</span><span class="sxs-lookup"><span data-stu-id="7775f-106">FullSenerioCreate</span></span>
```
New-AzWvdHostPool -HostPoolType <HostPoolType> -LoadBalancerType <LoadBalancerType> -Location <String>
 -Name <String> -PreferredAppGroupType <PreferredAppGroupType> -ResourceGroupName <String>
 [-DesktopAppGroupName <String>] [-SubscriptionId <String>] [-WorkspaceName <String>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="7775f-107">설명</span><span class="sxs-lookup"><span data-stu-id="7775f-107">DESCRIPTION</span></span>
<span data-ttu-id="7775f-108">호스트 풀을 만들거나 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="7775f-108">Create or update a host pool.</span></span>

## <span data-ttu-id="7775f-109">예제</span><span class="sxs-lookup"><span data-stu-id="7775f-109">EXAMPLES</span></span>

### <span data-ttu-id="7775f-110">예제 1: 이름으로 Windows Virtual Desktop HostPool 만들기</span><span class="sxs-lookup"><span data-stu-id="7775f-110">Example 1: Create a Windows Virtual Desktop HostPool by name</span></span>
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

<span data-ttu-id="7775f-111">이 명령은 리소스 그룹에 Windows Virtual Desktop HostPool을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="7775f-111">This command creates a Windows Virtual Desktop HostPool in a Resource Group.</span></span>

### <span data-ttu-id="7775f-112">예제 1: 이름으로 Windows Virtual Desktop HostPool 만들기</span><span class="sxs-lookup"><span data-stu-id="7775f-112">Example 1: Create a Windows Virtual Desktop HostPool by name</span></span>
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

<span data-ttu-id="7775f-113">이 명령은 리소스 그룹에 Windows Virtual Desktop HostPool을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="7775f-113">This command creates a Windows Virtual Desktop HostPool in a Resource Group.</span></span>

## <span data-ttu-id="7775f-114">매개 변수</span><span class="sxs-lookup"><span data-stu-id="7775f-114">PARAMETERS</span></span>

### <span data-ttu-id="7775f-115">-CustomRdpProperty</span><span class="sxs-lookup"><span data-stu-id="7775f-115">-CustomRdpProperty</span></span>
<span data-ttu-id="7775f-116">HostPool의 사용자 지정 rdp 속성입니다.</span><span class="sxs-lookup"><span data-stu-id="7775f-116">Custom rdp property of HostPool.</span></span>

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

### <span data-ttu-id="7775f-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7775f-117">-DefaultProfile</span></span>
<span data-ttu-id="7775f-118">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="7775f-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7775f-119">-Description</span><span class="sxs-lookup"><span data-stu-id="7775f-119">-Description</span></span>
<span data-ttu-id="7775f-120">HostPool에 대한 설명입니다.</span><span class="sxs-lookup"><span data-stu-id="7775f-120">Description of HostPool.</span></span>

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

### <span data-ttu-id="7775f-121">-DesktopAppGroupName</span><span class="sxs-lookup"><span data-stu-id="7775f-121">-DesktopAppGroupName</span></span>
<span data-ttu-id="7775f-122">데스크톱 앱 그룹 이름</span><span class="sxs-lookup"><span data-stu-id="7775f-122">Desktop App Group Name</span></span>

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

### <span data-ttu-id="7775f-123">-ExpirationTime</span><span class="sxs-lookup"><span data-stu-id="7775f-123">-ExpirationTime</span></span>
<span data-ttu-id="7775f-124">등록 토큰의 만료 시간입니다.</span><span class="sxs-lookup"><span data-stu-id="7775f-124">Expiration time of registration token.</span></span>

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

### <span data-ttu-id="7775f-125">-FriendlyName</span><span class="sxs-lookup"><span data-stu-id="7775f-125">-FriendlyName</span></span>
<span data-ttu-id="7775f-126">HostPool의 친숙한 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="7775f-126">Friendly name of HostPool.</span></span>

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

### <span data-ttu-id="7775f-127">-HostPoolType</span><span class="sxs-lookup"><span data-stu-id="7775f-127">-HostPoolType</span></span>
<span data-ttu-id="7775f-128">데스크톱용 HostPool 형식입니다.</span><span class="sxs-lookup"><span data-stu-id="7775f-128">HostPool type for desktop.</span></span>

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

### <span data-ttu-id="7775f-129">-LoadBalancerType</span><span class="sxs-lookup"><span data-stu-id="7775f-129">-LoadBalancerType</span></span>
<span data-ttu-id="7775f-130">부하 균형 조정기 유형입니다.</span><span class="sxs-lookup"><span data-stu-id="7775f-130">The type of the load balancer.</span></span>

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

### <span data-ttu-id="7775f-131">-Location</span><span class="sxs-lookup"><span data-stu-id="7775f-131">-Location</span></span>
<span data-ttu-id="7775f-132">리소스가 있는 지리적 위치</span><span class="sxs-lookup"><span data-stu-id="7775f-132">The geo-location where the resource lives</span></span>

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

### <span data-ttu-id="7775f-133">-MaxSessionLimit</span><span class="sxs-lookup"><span data-stu-id="7775f-133">-MaxSessionLimit</span></span>
<span data-ttu-id="7775f-134">HostPool의 최대 세션 제한입니다.</span><span class="sxs-lookup"><span data-stu-id="7775f-134">The max session limit of HostPool.</span></span>

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

### <span data-ttu-id="7775f-135">-Name</span><span class="sxs-lookup"><span data-stu-id="7775f-135">-Name</span></span>
<span data-ttu-id="7775f-136">지정된 리소스 그룹 내의 호스트 풀 이름</span><span class="sxs-lookup"><span data-stu-id="7775f-136">The name of the host pool within the specified resource group</span></span>

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

### <span data-ttu-id="7775f-137">-PersonalDesktopAssignmentType</span><span class="sxs-lookup"><span data-stu-id="7775f-137">-PersonalDesktopAssignmentType</span></span>
<span data-ttu-id="7775f-138">HostPool에 대한 PersonalDesktopAssignment 형식입니다.</span><span class="sxs-lookup"><span data-stu-id="7775f-138">PersonalDesktopAssignment type for HostPool.</span></span>

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

### <span data-ttu-id="7775f-139">-PreferredAppGroupType</span><span class="sxs-lookup"><span data-stu-id="7775f-139">-PreferredAppGroupType</span></span>
<span data-ttu-id="7775f-140">기본 설정 애플리케이션 그룹 유형(데스크톱 애플리케이션 그룹 기본값)</span><span class="sxs-lookup"><span data-stu-id="7775f-140">The type of preferred application group type, default to Desktop Application Group</span></span>

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

### <span data-ttu-id="7775f-141">-RegistrationInfoToken</span><span class="sxs-lookup"><span data-stu-id="7775f-141">-RegistrationInfoToken</span></span>
<span data-ttu-id="7775f-142">등록 토큰 base64 인코딩된 문자열입니다.</span><span class="sxs-lookup"><span data-stu-id="7775f-142">The registration token base64 encoded string.</span></span>

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

### <span data-ttu-id="7775f-143">-RegistrationTokenOperation</span><span class="sxs-lookup"><span data-stu-id="7775f-143">-RegistrationTokenOperation</span></span>
<span data-ttu-id="7775f-144">토큰을 다시 설정하는 형식입니다.</span><span class="sxs-lookup"><span data-stu-id="7775f-144">The type of resetting the token.</span></span>

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

### <span data-ttu-id="7775f-145">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7775f-145">-ResourceGroupName</span></span>
<span data-ttu-id="7775f-146">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="7775f-146">The name of the resource group.</span></span>
<span data-ttu-id="7775f-147">이름은 대소문자와 무관합니다.</span><span class="sxs-lookup"><span data-stu-id="7775f-147">The name is case insensitive.</span></span>

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

### <span data-ttu-id="7775f-148">-Ring</span><span class="sxs-lookup"><span data-stu-id="7775f-148">-Ring</span></span>
<span data-ttu-id="7775f-149">HostPool의 링 번호입니다.</span><span class="sxs-lookup"><span data-stu-id="7775f-149">The ring number of HostPool.</span></span>

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

### <span data-ttu-id="7775f-150">-SsoadfsAuthority</span><span class="sxs-lookup"><span data-stu-id="7775f-150">-SsoadfsAuthority</span></span>
<span data-ttu-id="7775f-151">WVD SSO 인증서에 서명하기 위한 고객 ADFS 서버에 대한 URL입니다.</span><span class="sxs-lookup"><span data-stu-id="7775f-151">URL to customer ADFS server for signing WVD SSO certificates.</span></span>

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

### <span data-ttu-id="7775f-152">-SsoClientId</span><span class="sxs-lookup"><span data-stu-id="7775f-152">-SsoClientId</span></span>
<span data-ttu-id="7775f-153">WVD SSO 인증서를 발급하는 데 사용되는 등록된 Relying Party의 ClientId입니다.</span><span class="sxs-lookup"><span data-stu-id="7775f-153">ClientId for the registered Relying Party used to issue WVD SSO certificates.</span></span>

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

### <span data-ttu-id="7775f-154">-SsoClientSecretKeyVaultPath</span><span class="sxs-lookup"><span data-stu-id="7775f-154">-SsoClientSecretKeyVaultPath</span></span>
<span data-ttu-id="7775f-155">ADFS에 통신하는 데 사용되는 비밀을 저장하는 Azure KeyVault에 대한 경로입니다.</span><span class="sxs-lookup"><span data-stu-id="7775f-155">Path to Azure KeyVault storing the secret used for communication to ADFS.</span></span>

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

### <span data-ttu-id="7775f-156">-SsoContext</span><span class="sxs-lookup"><span data-stu-id="7775f-156">-SsoContext</span></span>
<span data-ttu-id="7775f-157">ssoContext 비밀을 포함하는 keyvault에 대한 경로입니다.</span><span class="sxs-lookup"><span data-stu-id="7775f-157">Path to keyvault containing ssoContext secret.</span></span>

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

### <span data-ttu-id="7775f-158">-SsoSecretType</span><span class="sxs-lookup"><span data-stu-id="7775f-158">-SsoSecretType</span></span>
<span data-ttu-id="7775f-159">비밀 형식의 Single Sign의 형식입니다.</span><span class="sxs-lookup"><span data-stu-id="7775f-159">The type of single sign on Secret Type.</span></span>

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

### <span data-ttu-id="7775f-160">-StartVMOnConnect</span><span class="sxs-lookup"><span data-stu-id="7775f-160">-StartVMOnConnect</span></span>
<span data-ttu-id="7775f-161">StartVMOnConnect 기능을 켜고 끄는 플래그입니다.</span><span class="sxs-lookup"><span data-stu-id="7775f-161">The flag to turn on/off StartVMOnConnect feature.</span></span>

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

### <span data-ttu-id="7775f-162">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="7775f-162">-SubscriptionId</span></span>
<span data-ttu-id="7775f-163">대상 구독의 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="7775f-163">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="7775f-164">-Tag</span><span class="sxs-lookup"><span data-stu-id="7775f-164">-Tag</span></span>
<span data-ttu-id="7775f-165">리소스 태그입니다.</span><span class="sxs-lookup"><span data-stu-id="7775f-165">Resource tags.</span></span>

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

### <span data-ttu-id="7775f-166">-ValidationEnvironment</span><span class="sxs-lookup"><span data-stu-id="7775f-166">-ValidationEnvironment</span></span>
<span data-ttu-id="7775f-167">유효성 검사 환경입니다.</span><span class="sxs-lookup"><span data-stu-id="7775f-167">Is validation environment.</span></span>

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

### <span data-ttu-id="7775f-168">-VMTemplate</span><span class="sxs-lookup"><span data-stu-id="7775f-168">-VMTemplate</span></span>
<span data-ttu-id="7775f-169">hostpool 내의 세션 호스트 구성에 대한 VM 템플릿입니다.</span><span class="sxs-lookup"><span data-stu-id="7775f-169">VM template for sessionhosts configuration within hostpool.</span></span>

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

### <span data-ttu-id="7775f-170">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="7775f-170">-WorkspaceName</span></span>
<span data-ttu-id="7775f-171">작업 영역 이름</span><span class="sxs-lookup"><span data-stu-id="7775f-171">Workspace Name</span></span>

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

### <span data-ttu-id="7775f-172">-확인</span><span class="sxs-lookup"><span data-stu-id="7775f-172">-Confirm</span></span>
<span data-ttu-id="7775f-173">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="7775f-173">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7775f-174">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7775f-174">-WhatIf</span></span>
<span data-ttu-id="7775f-175">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="7775f-175">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7775f-176">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="7775f-176">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7775f-177">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7775f-177">CommonParameters</span></span>
<span data-ttu-id="7775f-178">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="7775f-178">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7775f-179">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="7775f-179">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7775f-180">입력</span><span class="sxs-lookup"><span data-stu-id="7775f-180">INPUTS</span></span>

## <span data-ttu-id="7775f-181">출력</span><span class="sxs-lookup"><span data-stu-id="7775f-181">OUTPUTS</span></span>

### <span data-ttu-id="7775f-182">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.Api20201102Preview.IHostPool</span><span class="sxs-lookup"><span data-stu-id="7775f-182">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.Api20201102Preview.IHostPool</span></span>

## <span data-ttu-id="7775f-183">참고 사항</span><span class="sxs-lookup"><span data-stu-id="7775f-183">NOTES</span></span>

<span data-ttu-id="7775f-184">별칭</span><span class="sxs-lookup"><span data-stu-id="7775f-184">ALIASES</span></span>

## <span data-ttu-id="7775f-185">관련 링크</span><span class="sxs-lookup"><span data-stu-id="7775f-185">RELATED LINKS</span></span>

