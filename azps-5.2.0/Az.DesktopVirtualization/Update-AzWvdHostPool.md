---
external help file: ''
Module Name: Az.DesktopVirtualization
online version: https://docs.microsoft.com/en-us/powershell/module/az.desktopvirtualization/update-azwvdhostpool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Update-AzWvdHostPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Update-AzWvdHostPool.md
ms.openlocfilehash: a6c7572808184f3c83037932f45d36c7af3ff7a5
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98341073"
---
# <span data-ttu-id="cb951-101">Update-AzWvdHostPool</span><span class="sxs-lookup"><span data-stu-id="cb951-101">Update-AzWvdHostPool</span></span>

## <span data-ttu-id="cb951-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="cb951-102">SYNOPSIS</span></span>
<span data-ttu-id="cb951-103">호스트 풀을 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="cb951-103">Update a host pool.</span></span>

## <span data-ttu-id="cb951-104">구문</span><span class="sxs-lookup"><span data-stu-id="cb951-104">SYNTAX</span></span>

### <span data-ttu-id="cb951-105">UpdateExpanded(기본값)</span><span class="sxs-lookup"><span data-stu-id="cb951-105">UpdateExpanded (Default)</span></span>
```
Update-AzWvdHostPool -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-CustomRdpProperty <String>] [-Description <String>] [-FriendlyName <String>]
 [-LoadBalancerType <LoadBalancerType>] [-MaxSessionLimit <Int32>]
 [-PersonalDesktopAssignmentType <PersonalDesktopAssignmentType>]
 [-PreferredAppGroupType <PreferredAppGroupType>] [-RegistrationInfoExpirationTime <DateTime>]
 [-RegistrationInfoRegistrationTokenOperation <RegistrationTokenOperation>] [-Ring <Int32>]
 [-SsoadfsAuthority <String>] [-SsoClientId <String>] [-SsoClientSecretKeyVaultPath <String>]
 [-SsoContext <String>] [-SsoSecretType <SsoSecretType>] [-Tag <Hashtable>] [-ValidationEnvironment]
 [-VMTemplate <String>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="cb951-106">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="cb951-106">UpdateViaIdentityExpanded</span></span>
```
Update-AzWvdHostPool -InputObject <IDesktopVirtualizationIdentity> [-CustomRdpProperty <String>]
 [-Description <String>] [-FriendlyName <String>] [-LoadBalancerType <LoadBalancerType>]
 [-MaxSessionLimit <Int32>] [-PersonalDesktopAssignmentType <PersonalDesktopAssignmentType>]
 [-PreferredAppGroupType <PreferredAppGroupType>] [-RegistrationInfoExpirationTime <DateTime>]
 [-RegistrationInfoRegistrationTokenOperation <RegistrationTokenOperation>] [-Ring <Int32>]
 [-SsoadfsAuthority <String>] [-SsoClientId <String>] [-SsoClientSecretKeyVaultPath <String>]
 [-SsoContext <String>] [-SsoSecretType <SsoSecretType>] [-Tag <Hashtable>] [-ValidationEnvironment]
 [-VMTemplate <String>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="cb951-107">설명</span><span class="sxs-lookup"><span data-stu-id="cb951-107">DESCRIPTION</span></span>
<span data-ttu-id="cb951-108">호스트 풀을 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="cb951-108">Update a host pool.</span></span>

## <span data-ttu-id="cb951-109">예제</span><span class="sxs-lookup"><span data-stu-id="cb951-109">EXAMPLES</span></span>

### <span data-ttu-id="cb951-110">예제 1: 이름으로 Windows Virtual Desktop HostPool 업데이트</span><span class="sxs-lookup"><span data-stu-id="cb951-110">Example 1: Update a Windows Virtual Desktop HostPool by name</span></span>
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

<span data-ttu-id="cb951-111">이 명령은 리소스 그룹의 Windows Virtual Desktop HostPool을 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="cb951-111">This command updates a Windows Virtual Desktop HostPool in a Resource Group.</span></span>

## <span data-ttu-id="cb951-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="cb951-112">PARAMETERS</span></span>

### <span data-ttu-id="cb951-113">-CustomRdpProperty</span><span class="sxs-lookup"><span data-stu-id="cb951-113">-CustomRdpProperty</span></span>
<span data-ttu-id="cb951-114">HostPool의 사용자 지정 rdp 속성입니다.</span><span class="sxs-lookup"><span data-stu-id="cb951-114">Custom rdp property of HostPool.</span></span>

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

### <span data-ttu-id="cb951-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cb951-115">-DefaultProfile</span></span>
<span data-ttu-id="cb951-116">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="cb951-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="cb951-117">-Description</span><span class="sxs-lookup"><span data-stu-id="cb951-117">-Description</span></span>
<span data-ttu-id="cb951-118">HostPool에 대한 설명입니다.</span><span class="sxs-lookup"><span data-stu-id="cb951-118">Description of HostPool.</span></span>

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

### <span data-ttu-id="cb951-119">-FriendlyName</span><span class="sxs-lookup"><span data-stu-id="cb951-119">-FriendlyName</span></span>
<span data-ttu-id="cb951-120">HostPool의 친숙한 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="cb951-120">Friendly name of HostPool.</span></span>

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

### <span data-ttu-id="cb951-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="cb951-121">-InputObject</span></span>
<span data-ttu-id="cb951-122">ID 매개 변수를 생성하는 경우 INPUTOBJECT 속성에 대한 NOTES 섹션을 참조하고 해시 테이블을 만드십시오.</span><span class="sxs-lookup"><span data-stu-id="cb951-122">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="cb951-123">-LoadBalancerType</span><span class="sxs-lookup"><span data-stu-id="cb951-123">-LoadBalancerType</span></span>
<span data-ttu-id="cb951-124">부하 균형 조정의 유형입니다.</span><span class="sxs-lookup"><span data-stu-id="cb951-124">The type of the load balancer.</span></span>

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

### <span data-ttu-id="cb951-125">-MaxSessionLimit</span><span class="sxs-lookup"><span data-stu-id="cb951-125">-MaxSessionLimit</span></span>
<span data-ttu-id="cb951-126">HostPool의 최대 세션 제한입니다.</span><span class="sxs-lookup"><span data-stu-id="cb951-126">The max session limit of HostPool.</span></span>

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

### <span data-ttu-id="cb951-127">-Name</span><span class="sxs-lookup"><span data-stu-id="cb951-127">-Name</span></span>
<span data-ttu-id="cb951-128">지정된 리소스 그룹 내의 호스트 풀 이름</span><span class="sxs-lookup"><span data-stu-id="cb951-128">The name of the host pool within the specified resource group</span></span>

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

### <span data-ttu-id="cb951-129">-PersonalDesktopAssignmentType</span><span class="sxs-lookup"><span data-stu-id="cb951-129">-PersonalDesktopAssignmentType</span></span>
<span data-ttu-id="cb951-130">HostPool에 대한 PersonalDesktopAssignment 형식입니다.</span><span class="sxs-lookup"><span data-stu-id="cb951-130">PersonalDesktopAssignment type for HostPool.</span></span>

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

### <span data-ttu-id="cb951-131">-PreferredAppGroupType</span><span class="sxs-lookup"><span data-stu-id="cb951-131">-PreferredAppGroupType</span></span>
<span data-ttu-id="cb951-132">기본 설정 애플리케이션 그룹 유형(기본적으로 데스크톱 애플리케이션 그룹)입니다.</span><span class="sxs-lookup"><span data-stu-id="cb951-132">The type of preferred application group type, default to Desktop Application Group</span></span>

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

### <span data-ttu-id="cb951-133">-RegistrationInfoExpirationTime</span><span class="sxs-lookup"><span data-stu-id="cb951-133">-RegistrationInfoExpirationTime</span></span>
<span data-ttu-id="cb951-134">등록 토큰의 만료 시간입니다.</span><span class="sxs-lookup"><span data-stu-id="cb951-134">Expiration time of registration token.</span></span>

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

### <span data-ttu-id="cb951-135">-RegistrationInfoRegistrationTokenOperation</span><span class="sxs-lookup"><span data-stu-id="cb951-135">-RegistrationInfoRegistrationTokenOperation</span></span>
<span data-ttu-id="cb951-136">토큰을 다시 설정하는 유형입니다.</span><span class="sxs-lookup"><span data-stu-id="cb951-136">The type of resetting the token.</span></span>

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

### <span data-ttu-id="cb951-137">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cb951-137">-ResourceGroupName</span></span>
<span data-ttu-id="cb951-138">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="cb951-138">The name of the resource group.</span></span>
<span data-ttu-id="cb951-139">이름은 대소문자 무관합니다.</span><span class="sxs-lookup"><span data-stu-id="cb951-139">The name is case insensitive.</span></span>

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

### <span data-ttu-id="cb951-140">-Ring</span><span class="sxs-lookup"><span data-stu-id="cb951-140">-Ring</span></span>
<span data-ttu-id="cb951-141">HostPool의 링 번호입니다.</span><span class="sxs-lookup"><span data-stu-id="cb951-141">The ring number of HostPool.</span></span>

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

### <span data-ttu-id="cb951-142">-SsoadfsAuthority</span><span class="sxs-lookup"><span data-stu-id="cb951-142">-SsoadfsAuthority</span></span>
<span data-ttu-id="cb951-143">WVD SSO 인증서 서명을 위한 고객 ADFS 서버에 대한 URL입니다.</span><span class="sxs-lookup"><span data-stu-id="cb951-143">URL to customer ADFS server for signing WVD SSO certificates.</span></span>

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

### <span data-ttu-id="cb951-144">-SsoClientId</span><span class="sxs-lookup"><span data-stu-id="cb951-144">-SsoClientId</span></span>
<span data-ttu-id="cb951-145">WVD SSO 인증서를 발급하는 데 사용되는 등록된 Relying Party의 ClientId입니다.</span><span class="sxs-lookup"><span data-stu-id="cb951-145">ClientId for the registered Relying Party used to issue WVD SSO certificates.</span></span>

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

### <span data-ttu-id="cb951-146">-SsoClientSecretKeyVaultPath</span><span class="sxs-lookup"><span data-stu-id="cb951-146">-SsoClientSecretKeyVaultPath</span></span>
<span data-ttu-id="cb951-147">ADFS와의 통신에 사용되는 비밀을 저장하는 Azure KeyVault의 경로입니다.</span><span class="sxs-lookup"><span data-stu-id="cb951-147">Path to Azure KeyVault storing the secret used for communication to ADFS.</span></span>

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

### <span data-ttu-id="cb951-148">-SsoContext</span><span class="sxs-lookup"><span data-stu-id="cb951-148">-SsoContext</span></span>
<span data-ttu-id="cb951-149">ssoContext 비밀을 포함하는 keyvault에 대한 경로입니다.</span><span class="sxs-lookup"><span data-stu-id="cb951-149">Path to keyvault containing ssoContext secret.</span></span>

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

### <span data-ttu-id="cb951-150">-SsoSecretType</span><span class="sxs-lookup"><span data-stu-id="cb951-150">-SsoSecretType</span></span>
<span data-ttu-id="cb951-151">비밀 형식에 대한 Single Sign-On의 유형입니다.</span><span class="sxs-lookup"><span data-stu-id="cb951-151">The type of single sign on Secret Type.</span></span>

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

### <span data-ttu-id="cb951-152">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="cb951-152">-SubscriptionId</span></span>
<span data-ttu-id="cb951-153">대상 구독의 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="cb951-153">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="cb951-154">-Tag</span><span class="sxs-lookup"><span data-stu-id="cb951-154">-Tag</span></span>
<span data-ttu-id="cb951-155">업데이트할 태그</span><span class="sxs-lookup"><span data-stu-id="cb951-155">tags to be updated</span></span>

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

### <span data-ttu-id="cb951-156">-ValidationEnvironment</span><span class="sxs-lookup"><span data-stu-id="cb951-156">-ValidationEnvironment</span></span>
<span data-ttu-id="cb951-157">유효성 검사 환경입니다.</span><span class="sxs-lookup"><span data-stu-id="cb951-157">Is validation environment.</span></span>

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

### <span data-ttu-id="cb951-158">-VMTemplate</span><span class="sxs-lookup"><span data-stu-id="cb951-158">-VMTemplate</span></span>
<span data-ttu-id="cb951-159">hostpool 내의 sessionhosts 구성에 대한 VM 템플릿입니다.</span><span class="sxs-lookup"><span data-stu-id="cb951-159">VM template for sessionhosts configuration within hostpool.</span></span>

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

### <span data-ttu-id="cb951-160">-Confirm</span><span class="sxs-lookup"><span data-stu-id="cb951-160">-Confirm</span></span>
<span data-ttu-id="cb951-161">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="cb951-161">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cb951-162">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cb951-162">-WhatIf</span></span>
<span data-ttu-id="cb951-163">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="cb951-163">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="cb951-164">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="cb951-164">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cb951-165">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cb951-165">CommonParameters</span></span>
<span data-ttu-id="cb951-166">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="cb951-166">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cb951-167">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="cb951-167">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cb951-168">입력</span><span class="sxs-lookup"><span data-stu-id="cb951-168">INPUTS</span></span>

### <span data-ttu-id="cb951-169">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.IDesktopVirtualizationIdentity</span><span class="sxs-lookup"><span data-stu-id="cb951-169">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.IDesktopVirtualizationIdentity</span></span>

## <span data-ttu-id="cb951-170">출력</span><span class="sxs-lookup"><span data-stu-id="cb951-170">OUTPUTS</span></span>

### <span data-ttu-id="cb951-171">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.Api20201019Preview.IHostPool</span><span class="sxs-lookup"><span data-stu-id="cb951-171">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.Api20201019Preview.IHostPool</span></span>

## <span data-ttu-id="cb951-172">참고 사항</span><span class="sxs-lookup"><span data-stu-id="cb951-172">NOTES</span></span>

<span data-ttu-id="cb951-173">별칭</span><span class="sxs-lookup"><span data-stu-id="cb951-173">ALIASES</span></span>

<span data-ttu-id="cb951-174">복합 매개 변수 속성</span><span class="sxs-lookup"><span data-stu-id="cb951-174">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="cb951-175">아래에 설명된 매개 변수를 만들 수 있도록 적절한 속성을 포함하는 해시 테이블을 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="cb951-175">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="cb951-176">해시 테이블에 대한 자세한 내용은 다음 Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="cb951-176">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="cb951-177">INPUTOBJECT: <IDesktopVirtualizationIdentity> ID 매개 변수</span><span class="sxs-lookup"><span data-stu-id="cb951-177">INPUTOBJECT <IDesktopVirtualizationIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="cb951-178">`[ApplicationGroupName <String>]`: 애플리케이션 그룹의 이름</span><span class="sxs-lookup"><span data-stu-id="cb951-178">`[ApplicationGroupName <String>]`: The name of the application group</span></span>
  - <span data-ttu-id="cb951-179">`[ApplicationName <String>]`: 지정된 애플리케이션 그룹 내의 애플리케이션 이름</span><span class="sxs-lookup"><span data-stu-id="cb951-179">`[ApplicationName <String>]`: The name of the application within the specified application group</span></span>
  - <span data-ttu-id="cb951-180">`[DesktopName <String>]`: 지정된 데스크톱 그룹 내에서 데스크톱의 이름</span><span class="sxs-lookup"><span data-stu-id="cb951-180">`[DesktopName <String>]`: The name of the desktop within the specified desktop group</span></span>
  - <span data-ttu-id="cb951-181">`[HostPoolName <String>]`: 지정된 리소스 그룹 내에서 호스트 풀의 이름</span><span class="sxs-lookup"><span data-stu-id="cb951-181">`[HostPoolName <String>]`: The name of the host pool within the specified resource group</span></span>
  - <span data-ttu-id="cb951-182">`[Id <String>]`: 리소스 ID 경로</span><span class="sxs-lookup"><span data-stu-id="cb951-182">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="cb951-183">`[MsixPackageFullName <String>]`: 지정된 호스트 풀 내의 MSIX 패키지의 버전별 패키지 전체 이름</span><span class="sxs-lookup"><span data-stu-id="cb951-183">`[MsixPackageFullName <String>]`: The version specific package full name of the MSIX package within specified hostpool</span></span>
  - <span data-ttu-id="cb951-184">`[ResourceGroupName <String>]`: 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="cb951-184">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="cb951-185">이름은 대소문자 무관합니다.</span><span class="sxs-lookup"><span data-stu-id="cb951-185">The name is case insensitive.</span></span>
  - <span data-ttu-id="cb951-186">`[SessionHostName <String>]`: 지정된 호스트 풀 내의 세션 호스트 이름</span><span class="sxs-lookup"><span data-stu-id="cb951-186">`[SessionHostName <String>]`: The name of the session host within the specified host pool</span></span>
  - <span data-ttu-id="cb951-187">`[SubscriptionId <String>]`: 대상 구독의 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="cb951-187">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="cb951-188">`[UserSessionId <String>]`: 지정된 세션 호스트 내의 사용자 세션 이름</span><span class="sxs-lookup"><span data-stu-id="cb951-188">`[UserSessionId <String>]`: The name of the user session within the specified session host</span></span>
  - <span data-ttu-id="cb951-189">`[WorkspaceName <String>]`: 작업 영역의 이름</span><span class="sxs-lookup"><span data-stu-id="cb951-189">`[WorkspaceName <String>]`: The name of the workspace</span></span>

## <span data-ttu-id="cb951-190">관련 링크</span><span class="sxs-lookup"><span data-stu-id="cb951-190">RELATED LINKS</span></span>

