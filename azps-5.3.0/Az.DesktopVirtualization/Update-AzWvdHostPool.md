---
external help file: ''
Module Name: Az.DesktopVirtualization
online version: https://docs.microsoft.com/en-us/powershell/module/az.desktopvirtualization/update-azwvdhostpool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Update-AzWvdHostPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Update-AzWvdHostPool.md
ms.openlocfilehash: e6b77d9d779931d9b50de2b504b357ecd22a2b92
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98493057"
---
# <span data-ttu-id="8902b-101">Update-AzWvdHostPool</span><span class="sxs-lookup"><span data-stu-id="8902b-101">Update-AzWvdHostPool</span></span>

## <span data-ttu-id="8902b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8902b-102">SYNOPSIS</span></span>
<span data-ttu-id="8902b-103">호스트 풀을 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="8902b-103">Update a host pool.</span></span>

## <span data-ttu-id="8902b-104">구문</span><span class="sxs-lookup"><span data-stu-id="8902b-104">SYNTAX</span></span>

### <span data-ttu-id="8902b-105">UpdateExpanded(기본값)</span><span class="sxs-lookup"><span data-stu-id="8902b-105">UpdateExpanded (Default)</span></span>
```
Update-AzWvdHostPool -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-CustomRdpProperty <String>] [-Description <String>] [-FriendlyName <String>]
 [-LoadBalancerType <LoadBalancerType>] [-MaxSessionLimit <Int32>]
 [-PersonalDesktopAssignmentType <PersonalDesktopAssignmentType>]
 [-PreferredAppGroupType <PreferredAppGroupType>] [-RegistrationInfoExpirationTime <DateTime>]
 [-RegistrationInfoRegistrationTokenOperation <RegistrationTokenOperation>] [-Ring <Int32>]
 [-SsoadfsAuthority <String>] [-SsoClientId <String>] [-SsoClientSecretKeyVaultPath <String>]
 [-SsoContext <String>] [-SsoSecretType <SsoSecretType>] [-StartVMOnConnect] [-Tag <Hashtable>]
 [-ValidationEnvironment] [-VMTemplate <String>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="8902b-106">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="8902b-106">UpdateViaIdentityExpanded</span></span>
```
Update-AzWvdHostPool -InputObject <IDesktopVirtualizationIdentity> [-CustomRdpProperty <String>]
 [-Description <String>] [-FriendlyName <String>] [-LoadBalancerType <LoadBalancerType>]
 [-MaxSessionLimit <Int32>] [-PersonalDesktopAssignmentType <PersonalDesktopAssignmentType>]
 [-PreferredAppGroupType <PreferredAppGroupType>] [-RegistrationInfoExpirationTime <DateTime>]
 [-RegistrationInfoRegistrationTokenOperation <RegistrationTokenOperation>] [-Ring <Int32>]
 [-SsoadfsAuthority <String>] [-SsoClientId <String>] [-SsoClientSecretKeyVaultPath <String>]
 [-SsoContext <String>] [-SsoSecretType <SsoSecretType>] [-StartVMOnConnect] [-Tag <Hashtable>]
 [-ValidationEnvironment] [-VMTemplate <String>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

## <span data-ttu-id="8902b-107">설명</span><span class="sxs-lookup"><span data-stu-id="8902b-107">DESCRIPTION</span></span>
<span data-ttu-id="8902b-108">호스트 풀을 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="8902b-108">Update a host pool.</span></span>

## <span data-ttu-id="8902b-109">예제</span><span class="sxs-lookup"><span data-stu-id="8902b-109">EXAMPLES</span></span>

### <span data-ttu-id="8902b-110">예제 1: 이름으로 Windows Virtual Desktop HostPool 업데이트</span><span class="sxs-lookup"><span data-stu-id="8902b-110">Example 1: Update a Windows Virtual Desktop HostPool by name</span></span>
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

<span data-ttu-id="8902b-111">이 명령은 리소스 그룹의 Windows Virtual Desktop HostPool을 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="8902b-111">This command updates a Windows Virtual Desktop HostPool in a Resource Group.</span></span>

## <span data-ttu-id="8902b-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="8902b-112">PARAMETERS</span></span>

### <span data-ttu-id="8902b-113">-CustomRdpProperty</span><span class="sxs-lookup"><span data-stu-id="8902b-113">-CustomRdpProperty</span></span>
<span data-ttu-id="8902b-114">HostPool의 사용자 지정 rdp 속성입니다.</span><span class="sxs-lookup"><span data-stu-id="8902b-114">Custom rdp property of HostPool.</span></span>

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

### <span data-ttu-id="8902b-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8902b-115">-DefaultProfile</span></span>
<span data-ttu-id="8902b-116">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="8902b-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8902b-117">-Description</span><span class="sxs-lookup"><span data-stu-id="8902b-117">-Description</span></span>
<span data-ttu-id="8902b-118">HostPool에 대한 설명입니다.</span><span class="sxs-lookup"><span data-stu-id="8902b-118">Description of HostPool.</span></span>

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

### <span data-ttu-id="8902b-119">-FriendlyName</span><span class="sxs-lookup"><span data-stu-id="8902b-119">-FriendlyName</span></span>
<span data-ttu-id="8902b-120">HostPool의 친숙한 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="8902b-120">Friendly name of HostPool.</span></span>

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

### <span data-ttu-id="8902b-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="8902b-121">-InputObject</span></span>
<span data-ttu-id="8902b-122">ID 매개 변수를 생성하는 경우 INPUTOBJECT 속성에 대한 NOTES 섹션을 참조하고 해시 테이블을 만드십시오.</span><span class="sxs-lookup"><span data-stu-id="8902b-122">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="8902b-123">-LoadBalancerType</span><span class="sxs-lookup"><span data-stu-id="8902b-123">-LoadBalancerType</span></span>
<span data-ttu-id="8902b-124">부하 균형 조정의 유형입니다.</span><span class="sxs-lookup"><span data-stu-id="8902b-124">The type of the load balancer.</span></span>

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

### <span data-ttu-id="8902b-125">-MaxSessionLimit</span><span class="sxs-lookup"><span data-stu-id="8902b-125">-MaxSessionLimit</span></span>
<span data-ttu-id="8902b-126">HostPool의 최대 세션 제한입니다.</span><span class="sxs-lookup"><span data-stu-id="8902b-126">The max session limit of HostPool.</span></span>

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

### <span data-ttu-id="8902b-127">-Name</span><span class="sxs-lookup"><span data-stu-id="8902b-127">-Name</span></span>
<span data-ttu-id="8902b-128">지정된 리소스 그룹 내의 호스트 풀 이름</span><span class="sxs-lookup"><span data-stu-id="8902b-128">The name of the host pool within the specified resource group</span></span>

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

### <span data-ttu-id="8902b-129">-PersonalDesktopAssignmentType</span><span class="sxs-lookup"><span data-stu-id="8902b-129">-PersonalDesktopAssignmentType</span></span>
<span data-ttu-id="8902b-130">HostPool에 대한 PersonalDesktopAssignment 형식입니다.</span><span class="sxs-lookup"><span data-stu-id="8902b-130">PersonalDesktopAssignment type for HostPool.</span></span>

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

### <span data-ttu-id="8902b-131">-PreferredAppGroupType</span><span class="sxs-lookup"><span data-stu-id="8902b-131">-PreferredAppGroupType</span></span>
<span data-ttu-id="8902b-132">기본 설정 애플리케이션 그룹 유형(기본적으로 데스크톱 애플리케이션 그룹)입니다.</span><span class="sxs-lookup"><span data-stu-id="8902b-132">The type of preferred application group type, default to Desktop Application Group</span></span>

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

### <span data-ttu-id="8902b-133">-RegistrationInfoExpirationTime</span><span class="sxs-lookup"><span data-stu-id="8902b-133">-RegistrationInfoExpirationTime</span></span>
<span data-ttu-id="8902b-134">등록 토큰의 만료 시간입니다.</span><span class="sxs-lookup"><span data-stu-id="8902b-134">Expiration time of registration token.</span></span>

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

### <span data-ttu-id="8902b-135">-RegistrationInfoRegistrationTokenOperation</span><span class="sxs-lookup"><span data-stu-id="8902b-135">-RegistrationInfoRegistrationTokenOperation</span></span>
<span data-ttu-id="8902b-136">토큰을 다시 설정하는 유형입니다.</span><span class="sxs-lookup"><span data-stu-id="8902b-136">The type of resetting the token.</span></span>

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

### <span data-ttu-id="8902b-137">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8902b-137">-ResourceGroupName</span></span>
<span data-ttu-id="8902b-138">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="8902b-138">The name of the resource group.</span></span>
<span data-ttu-id="8902b-139">이름은 대소문자 무관합니다.</span><span class="sxs-lookup"><span data-stu-id="8902b-139">The name is case insensitive.</span></span>

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

### <span data-ttu-id="8902b-140">-Ring</span><span class="sxs-lookup"><span data-stu-id="8902b-140">-Ring</span></span>
<span data-ttu-id="8902b-141">HostPool의 링 번호입니다.</span><span class="sxs-lookup"><span data-stu-id="8902b-141">The ring number of HostPool.</span></span>

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

### <span data-ttu-id="8902b-142">-SsoadfsAuthority</span><span class="sxs-lookup"><span data-stu-id="8902b-142">-SsoadfsAuthority</span></span>
<span data-ttu-id="8902b-143">WVD SSO 인증서 서명을 위한 고객 ADFS 서버에 대한 URL입니다.</span><span class="sxs-lookup"><span data-stu-id="8902b-143">URL to customer ADFS server for signing WVD SSO certificates.</span></span>

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

### <span data-ttu-id="8902b-144">-SsoClientId</span><span class="sxs-lookup"><span data-stu-id="8902b-144">-SsoClientId</span></span>
<span data-ttu-id="8902b-145">WVD SSO 인증서를 발급하는 데 사용되는 등록된 Relying Party의 ClientId입니다.</span><span class="sxs-lookup"><span data-stu-id="8902b-145">ClientId for the registered Relying Party used to issue WVD SSO certificates.</span></span>

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

### <span data-ttu-id="8902b-146">-SsoClientSecretKeyVaultPath</span><span class="sxs-lookup"><span data-stu-id="8902b-146">-SsoClientSecretKeyVaultPath</span></span>
<span data-ttu-id="8902b-147">ADFS와의 통신에 사용되는 비밀을 저장하는 Azure KeyVault의 경로입니다.</span><span class="sxs-lookup"><span data-stu-id="8902b-147">Path to Azure KeyVault storing the secret used for communication to ADFS.</span></span>

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

### <span data-ttu-id="8902b-148">-SsoContext</span><span class="sxs-lookup"><span data-stu-id="8902b-148">-SsoContext</span></span>
<span data-ttu-id="8902b-149">ssoContext 비밀을 포함하는 keyvault에 대한 경로입니다.</span><span class="sxs-lookup"><span data-stu-id="8902b-149">Path to keyvault containing ssoContext secret.</span></span>

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

### <span data-ttu-id="8902b-150">-SsoSecretType</span><span class="sxs-lookup"><span data-stu-id="8902b-150">-SsoSecretType</span></span>
<span data-ttu-id="8902b-151">비밀 형식에 대한 Single Sign-On의 유형입니다.</span><span class="sxs-lookup"><span data-stu-id="8902b-151">The type of single sign on Secret Type.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Support.SsoSecretType
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8902b-152">-StartVMOnConnect</span><span class="sxs-lookup"><span data-stu-id="8902b-152">-StartVMOnConnect</span></span>
<span data-ttu-id="8902b-153">StartVMOnConnect 기능을 켜고 끄는 플래그입니다.</span><span class="sxs-lookup"><span data-stu-id="8902b-153">The flag to turn on/off StartVMOnConnect feature.</span></span>

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

### <span data-ttu-id="8902b-154">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="8902b-154">-SubscriptionId</span></span>
<span data-ttu-id="8902b-155">대상 구독의 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="8902b-155">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="8902b-156">-Tag</span><span class="sxs-lookup"><span data-stu-id="8902b-156">-Tag</span></span>
<span data-ttu-id="8902b-157">업데이트할 태그</span><span class="sxs-lookup"><span data-stu-id="8902b-157">tags to be updated</span></span>

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

### <span data-ttu-id="8902b-158">-ValidationEnvironment</span><span class="sxs-lookup"><span data-stu-id="8902b-158">-ValidationEnvironment</span></span>
<span data-ttu-id="8902b-159">유효성 검사 환경입니다.</span><span class="sxs-lookup"><span data-stu-id="8902b-159">Is validation environment.</span></span>

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

### <span data-ttu-id="8902b-160">-VMTemplate</span><span class="sxs-lookup"><span data-stu-id="8902b-160">-VMTemplate</span></span>
<span data-ttu-id="8902b-161">hostpool 내의 sessionhosts 구성에 대한 VM 템플릿입니다.</span><span class="sxs-lookup"><span data-stu-id="8902b-161">VM template for sessionhosts configuration within hostpool.</span></span>

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

### <span data-ttu-id="8902b-162">-Confirm</span><span class="sxs-lookup"><span data-stu-id="8902b-162">-Confirm</span></span>
<span data-ttu-id="8902b-163">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="8902b-163">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8902b-164">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8902b-164">-WhatIf</span></span>
<span data-ttu-id="8902b-165">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="8902b-165">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8902b-166">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="8902b-166">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8902b-167">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8902b-167">CommonParameters</span></span>
<span data-ttu-id="8902b-168">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="8902b-168">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8902b-169">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="8902b-169">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8902b-170">입력</span><span class="sxs-lookup"><span data-stu-id="8902b-170">INPUTS</span></span>

### <span data-ttu-id="8902b-171">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.IDesktopVirtualizationIdentity</span><span class="sxs-lookup"><span data-stu-id="8902b-171">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.IDesktopVirtualizationIdentity</span></span>

## <span data-ttu-id="8902b-172">출력</span><span class="sxs-lookup"><span data-stu-id="8902b-172">OUTPUTS</span></span>

### <span data-ttu-id="8902b-173">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.Api20201102Preview.IHostPool</span><span class="sxs-lookup"><span data-stu-id="8902b-173">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.Api20201102Preview.IHostPool</span></span>

## <span data-ttu-id="8902b-174">참고 사항</span><span class="sxs-lookup"><span data-stu-id="8902b-174">NOTES</span></span>

<span data-ttu-id="8902b-175">별칭</span><span class="sxs-lookup"><span data-stu-id="8902b-175">ALIASES</span></span>

<span data-ttu-id="8902b-176">복합 매개 변수 속성</span><span class="sxs-lookup"><span data-stu-id="8902b-176">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="8902b-177">아래에 설명된 매개 변수를 만들 수 있도록 적절한 속성을 포함하는 해시 테이블을 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="8902b-177">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="8902b-178">해시 테이블에 대한 자세한 내용은 다음 Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="8902b-178">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="8902b-179">INPUTOBJECT: <IDesktopVirtualizationIdentity> ID 매개 변수</span><span class="sxs-lookup"><span data-stu-id="8902b-179">INPUTOBJECT <IDesktopVirtualizationIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="8902b-180">`[ApplicationGroupName <String>]`: 애플리케이션 그룹의 이름</span><span class="sxs-lookup"><span data-stu-id="8902b-180">`[ApplicationGroupName <String>]`: The name of the application group</span></span>
  - <span data-ttu-id="8902b-181">`[ApplicationName <String>]`: 지정된 애플리케이션 그룹 내의 애플리케이션 이름</span><span class="sxs-lookup"><span data-stu-id="8902b-181">`[ApplicationName <String>]`: The name of the application within the specified application group</span></span>
  - <span data-ttu-id="8902b-182">`[DesktopName <String>]`: 지정된 데스크톱 그룹 내에서 데스크톱의 이름</span><span class="sxs-lookup"><span data-stu-id="8902b-182">`[DesktopName <String>]`: The name of the desktop within the specified desktop group</span></span>
  - <span data-ttu-id="8902b-183">`[HostPoolName <String>]`: 지정된 리소스 그룹 내에서 호스트 풀의 이름</span><span class="sxs-lookup"><span data-stu-id="8902b-183">`[HostPoolName <String>]`: The name of the host pool within the specified resource group</span></span>
  - <span data-ttu-id="8902b-184">`[Id <String>]`: 리소스 ID 경로</span><span class="sxs-lookup"><span data-stu-id="8902b-184">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="8902b-185">`[MsixPackageFullName <String>]`: 지정된 호스트 풀 내의 MSIX 패키지의 버전별 패키지 전체 이름</span><span class="sxs-lookup"><span data-stu-id="8902b-185">`[MsixPackageFullName <String>]`: The version specific package full name of the MSIX package within specified hostpool</span></span>
  - <span data-ttu-id="8902b-186">`[ResourceGroupName <String>]`: 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="8902b-186">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="8902b-187">이름은 대소문자 무관합니다.</span><span class="sxs-lookup"><span data-stu-id="8902b-187">The name is case insensitive.</span></span>
  - <span data-ttu-id="8902b-188">`[SessionHostName <String>]`: 지정된 호스트 풀 내의 세션 호스트 이름</span><span class="sxs-lookup"><span data-stu-id="8902b-188">`[SessionHostName <String>]`: The name of the session host within the specified host pool</span></span>
  - <span data-ttu-id="8902b-189">`[SubscriptionId <String>]`: 대상 구독의 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="8902b-189">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="8902b-190">`[UserSessionId <String>]`: 지정된 세션 호스트 내의 사용자 세션 이름</span><span class="sxs-lookup"><span data-stu-id="8902b-190">`[UserSessionId <String>]`: The name of the user session within the specified session host</span></span>
  - <span data-ttu-id="8902b-191">`[WorkspaceName <String>]`: 작업 영역의 이름</span><span class="sxs-lookup"><span data-stu-id="8902b-191">`[WorkspaceName <String>]`: The name of the workspace</span></span>

## <span data-ttu-id="8902b-192">관련 링크</span><span class="sxs-lookup"><span data-stu-id="8902b-192">RELATED LINKS</span></span>

