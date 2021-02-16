---
external help file: ''
Module Name: Az.VMware
online version: https://docs.microsoft.com/en-us/powershell/module/az.vmware/update-azvmwareprivatecloud
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/VMware/help/Update-AzVMwarePrivateCloud.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/VMware/help/Update-AzVMwarePrivateCloud.md
ms.openlocfilehash: dbea608c24d8da8fa292316653b3e16953aed8b6
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100208893"
---
# <span data-ttu-id="9994d-101">Update-AzVMwarePrivateCloud</span><span class="sxs-lookup"><span data-stu-id="9994d-101">Update-AzVMwarePrivateCloud</span></span>

## <span data-ttu-id="9994d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9994d-102">SYNOPSIS</span></span>
<span data-ttu-id="9994d-103">사설 클라우드 업데이트</span><span class="sxs-lookup"><span data-stu-id="9994d-103">Update a private cloud</span></span>

## <span data-ttu-id="9994d-104">구문</span><span class="sxs-lookup"><span data-stu-id="9994d-104">SYNTAX</span></span>

### <span data-ttu-id="9994d-105">UpdateExpanded(기본값)</span><span class="sxs-lookup"><span data-stu-id="9994d-105">UpdateExpanded (Default)</span></span>
```
Update-AzVMwarePrivateCloud -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-IdentitySource <IIdentitySource[]>] [-Internet <InternetEnum>] [-ManagementClusterSize <Int32>]
 [-Tag <Hashtable>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="9994d-106">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="9994d-106">UpdateViaIdentityExpanded</span></span>
```
Update-AzVMwarePrivateCloud -InputObject <IVMwareIdentity> [-IdentitySource <IIdentitySource[]>]
 [-Internet <InternetEnum>] [-ManagementClusterSize <Int32>] [-Tag <Hashtable>] [-DefaultProfile <PSObject>]
 [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="9994d-107">설명</span><span class="sxs-lookup"><span data-stu-id="9994d-107">DESCRIPTION</span></span>
<span data-ttu-id="9994d-108">사설 클라우드 업데이트</span><span class="sxs-lookup"><span data-stu-id="9994d-108">Update a private cloud</span></span>

## <span data-ttu-id="9994d-109">예제</span><span class="sxs-lookup"><span data-stu-id="9994d-109">EXAMPLES</span></span>

### <span data-ttu-id="9994d-110">예제 1: 이름으로 사설 클라우드의 크기 업데이트</span><span class="sxs-lookup"><span data-stu-id="9994d-110">Example 1: Update size of private cloud by name</span></span>
```powershell
PS C:\> Update-AzVMwarePrivateCloud -Name azps-test-cloud -ResourceGroupName azps-test-group -ManagementClusterSize 4

Location      Name            Type
--------      ----            ----
australiaeast azps-test-cloud Microsoft.AVS/privateClouds
```

<span data-ttu-id="9994d-111">이름으로 사설 클라우드의 크기 업데이트</span><span class="sxs-lookup"><span data-stu-id="9994d-111">Update size of private cloud by name</span></span>

### <span data-ttu-id="9994d-112">예제 2: 입력 개체로 사설 클라우드의 크기 업데이트</span><span class="sxs-lookup"><span data-stu-id="9994d-112">Example 2: Update size of private cloud by input object</span></span>
```powershell
PS C:\> Get-AzVMwarePrivateCloud -ResourceGroupName azps-test-group -Name azps-test-cloud | Update-AzVMwarePrivateCloud -ManagementClusterSize 4

Location      Name            Type
--------      ----            ----
australiaeast azps-test-cloud Microsoft.AVS/privateClouds
```

<span data-ttu-id="9994d-113">입력 개체에 따라 사설 클라우드의 크기 업데이트</span><span class="sxs-lookup"><span data-stu-id="9994d-113">Update size of private cloud by input object</span></span>

## <span data-ttu-id="9994d-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="9994d-114">PARAMETERS</span></span>

### <span data-ttu-id="9994d-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="9994d-115">-AsJob</span></span>
<span data-ttu-id="9994d-116">작업으로 명령 실행</span><span class="sxs-lookup"><span data-stu-id="9994d-116">Run the command as a job</span></span>

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

### <span data-ttu-id="9994d-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9994d-117">-DefaultProfile</span></span>
<span data-ttu-id="9994d-118">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="9994d-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9994d-119">-IdentitySource</span><span class="sxs-lookup"><span data-stu-id="9994d-119">-IdentitySource</span></span>
<span data-ttu-id="9994d-120">vCenter Single Sign-On ID 원본을 생성하기 위해 IDENTITYSOURCE 속성에 대한 NOTES 섹션을 참조하고 해시 테이블을 만드십시오.</span><span class="sxs-lookup"><span data-stu-id="9994d-120">vCenter Single Sign On Identity Sources To construct, see NOTES section for IDENTITYSOURCE properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.VMware.Models.Api20200320.IIdentitySource[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9994d-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="9994d-121">-InputObject</span></span>
<span data-ttu-id="9994d-122">ID 매개 변수를 생성하는 경우 INPUTOBJECT 속성에 대한 NOTES 섹션을 참조하고 해시 테이블을 만드십시오.</span><span class="sxs-lookup"><span data-stu-id="9994d-122">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.VMware.Models.IVMwareIdentity
Parameter Sets: UpdateViaIdentityExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="9994d-123">-Internet</span><span class="sxs-lookup"><span data-stu-id="9994d-123">-Internet</span></span>
<span data-ttu-id="9994d-124">인터넷에 대한 연결이 설정되거나 사용되지 않도록 설정되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="9994d-124">Connectivity to internet is enabled or disabled</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.VMware.Support.InternetEnum
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9994d-125">-ManagementClusterSize</span><span class="sxs-lookup"><span data-stu-id="9994d-125">-ManagementClusterSize</span></span>
<span data-ttu-id="9994d-126">클러스터 크기</span><span class="sxs-lookup"><span data-stu-id="9994d-126">The cluster size</span></span>

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

### <span data-ttu-id="9994d-127">-Name</span><span class="sxs-lookup"><span data-stu-id="9994d-127">-Name</span></span>
<span data-ttu-id="9994d-128">사설 클라우드의 이름</span><span class="sxs-lookup"><span data-stu-id="9994d-128">Name of the private cloud</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases: PrivateCloudName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9994d-129">-NoWait</span><span class="sxs-lookup"><span data-stu-id="9994d-129">-NoWait</span></span>
<span data-ttu-id="9994d-130">명령을 비동기적으로 실행</span><span class="sxs-lookup"><span data-stu-id="9994d-130">Run the command asynchronously</span></span>

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

### <span data-ttu-id="9994d-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9994d-131">-ResourceGroupName</span></span>
<span data-ttu-id="9994d-132">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="9994d-132">The name of the resource group.</span></span>
<span data-ttu-id="9994d-133">이름은 대소문자 무관합니다.</span><span class="sxs-lookup"><span data-stu-id="9994d-133">The name is case insensitive.</span></span>

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

### <span data-ttu-id="9994d-134">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="9994d-134">-SubscriptionId</span></span>
<span data-ttu-id="9994d-135">대상 구독의 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="9994d-135">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="9994d-136">-Tag</span><span class="sxs-lookup"><span data-stu-id="9994d-136">-Tag</span></span>
<span data-ttu-id="9994d-137">리소스 태그.</span><span class="sxs-lookup"><span data-stu-id="9994d-137">Resource tags.</span></span>

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

### <span data-ttu-id="9994d-138">-Confirm</span><span class="sxs-lookup"><span data-stu-id="9994d-138">-Confirm</span></span>
<span data-ttu-id="9994d-139">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="9994d-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9994d-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9994d-140">-WhatIf</span></span>
<span data-ttu-id="9994d-141">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="9994d-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9994d-142">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="9994d-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9994d-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9994d-143">CommonParameters</span></span>
<span data-ttu-id="9994d-144">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="9994d-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9994d-145">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="9994d-145">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9994d-146">입력</span><span class="sxs-lookup"><span data-stu-id="9994d-146">INPUTS</span></span>

### <span data-ttu-id="9994d-147">Microsoft.Azure.PowerShell.Cmdlets.VMware.Models.IVMwareIdentity</span><span class="sxs-lookup"><span data-stu-id="9994d-147">Microsoft.Azure.PowerShell.Cmdlets.VMware.Models.IVMwareIdentity</span></span>

## <span data-ttu-id="9994d-148">출력</span><span class="sxs-lookup"><span data-stu-id="9994d-148">OUTPUTS</span></span>

### <span data-ttu-id="9994d-149">Microsoft.Azure.PowerShell.Cmdlets.VMware.Models.Api20200320.IPrivateCloud</span><span class="sxs-lookup"><span data-stu-id="9994d-149">Microsoft.Azure.PowerShell.Cmdlets.VMware.Models.Api20200320.IPrivateCloud</span></span>

## <span data-ttu-id="9994d-150">참고 사항</span><span class="sxs-lookup"><span data-stu-id="9994d-150">NOTES</span></span>

<span data-ttu-id="9994d-151">별칭</span><span class="sxs-lookup"><span data-stu-id="9994d-151">ALIASES</span></span>

<span data-ttu-id="9994d-152">복합 매개 변수 속성</span><span class="sxs-lookup"><span data-stu-id="9994d-152">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="9994d-153">아래에 설명된 매개 변수를 만들 수 있도록 적절한 속성을 포함하는 해시 테이블을 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="9994d-153">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="9994d-154">해시 테이블에 대한 자세한 내용은 다음 Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="9994d-154">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="9994d-155">IDENTITYSOURCE <IIdentitySource[]>: vCenter Single Sign-On ID 원본</span><span class="sxs-lookup"><span data-stu-id="9994d-155">IDENTITYSOURCE <IIdentitySource[]>: vCenter Single Sign On Identity Sources</span></span>
  - <span data-ttu-id="9994d-156">`[Alias <String>]`: 도메인의 NetBIOS 이름</span><span class="sxs-lookup"><span data-stu-id="9994d-156">`[Alias <String>]`: The domain's NetBIOS name</span></span>
  - <span data-ttu-id="9994d-157">`[BaseGroupDn <String>]`: 그룹의 기본 고유 이름</span><span class="sxs-lookup"><span data-stu-id="9994d-157">`[BaseGroupDn <String>]`: The base distinguished name for groups</span></span>
  - <span data-ttu-id="9994d-158">`[BaseUserDn <String>]`: 사용자의 기본 고유 이름</span><span class="sxs-lookup"><span data-stu-id="9994d-158">`[BaseUserDn <String>]`: The base distinguished name for users</span></span>
  - <span data-ttu-id="9994d-159">`[Domain <String>]`: 도메인의 dns 이름</span><span class="sxs-lookup"><span data-stu-id="9994d-159">`[Domain <String>]`: The domain's dns name</span></span>
  - <span data-ttu-id="9994d-160">`[Name <String>]`: ID 원본의 이름</span><span class="sxs-lookup"><span data-stu-id="9994d-160">`[Name <String>]`: The name of the identity source</span></span>
  - <span data-ttu-id="9994d-161">`[Password <String>]`: 사용자 및 그룹의 기본 DN에 대한 읽기 전용 액세스 권한이 최소인 Active Directory 사용자의 암호입니다.</span><span class="sxs-lookup"><span data-stu-id="9994d-161">`[Password <String>]`: The password of the Active Directory user with a minimum of read-only access to Base DN for users and groups.</span></span>
  - <span data-ttu-id="9994d-162">`[PrimaryServer <String>]`: 주 서버 URL</span><span class="sxs-lookup"><span data-stu-id="9994d-162">`[PrimaryServer <String>]`: Primary server URL</span></span>
  - <span data-ttu-id="9994d-163">`[SecondaryServer <String>]`: 보조 서버 URL</span><span class="sxs-lookup"><span data-stu-id="9994d-163">`[SecondaryServer <String>]`: Secondary server URL</span></span>
  - <span data-ttu-id="9994d-164">`[Ssl <SslEnum?>]`: SSL 인증서(LDAPS)를 사용하여 LDAP 통신 보호</span><span class="sxs-lookup"><span data-stu-id="9994d-164">`[Ssl <SslEnum?>]`: Protect LDAP communication using SSL certificate (LDAPS)</span></span>
  - <span data-ttu-id="9994d-165">`[Username <String>]`: 사용자 및 그룹의 기본 DN에 대한 읽기 전용 액세스 권한이 최소인 Active Directory 사용자의 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="9994d-165">`[Username <String>]`: The ID of an Active Directory user with a minimum of read-only access to Base DN for users and group</span></span>

<span data-ttu-id="9994d-166">INPUTOBJECT: <IVMwareIdentity> ID 매개 변수</span><span class="sxs-lookup"><span data-stu-id="9994d-166">INPUTOBJECT <IVMwareIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="9994d-167">`[AuthorizationName <String>]`: 사설 클라우드에서 ExpressRoute 회로 권한 부여의 이름</span><span class="sxs-lookup"><span data-stu-id="9994d-167">`[AuthorizationName <String>]`: Name of the ExpressRoute Circuit Authorization in the private cloud</span></span>
  - <span data-ttu-id="9994d-168">`[ClusterName <String>]`: 사설 클라우드의 클러스터 이름</span><span class="sxs-lookup"><span data-stu-id="9994d-168">`[ClusterName <String>]`: Name of the cluster in the private cloud</span></span>
  - <span data-ttu-id="9994d-169">`[HcxEnterpriseSiteName <String>]`: 사설 클라우드의 HCX Enterprise 사이트의 이름</span><span class="sxs-lookup"><span data-stu-id="9994d-169">`[HcxEnterpriseSiteName <String>]`: Name of the HCX Enterprise Site in the private cloud</span></span>
  - <span data-ttu-id="9994d-170">`[Id <String>]`: 리소스 ID 경로</span><span class="sxs-lookup"><span data-stu-id="9994d-170">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="9994d-171">`[Location <String>]`: Azure 지역</span><span class="sxs-lookup"><span data-stu-id="9994d-171">`[Location <String>]`: Azure region</span></span>
  - <span data-ttu-id="9994d-172">`[PrivateCloudName <String>]`: 사설 클라우드의 이름</span><span class="sxs-lookup"><span data-stu-id="9994d-172">`[PrivateCloudName <String>]`: Name of the private cloud</span></span>
  - <span data-ttu-id="9994d-173">`[ResourceGroupName <String>]`: 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="9994d-173">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="9994d-174">이름은 대소문자 무관합니다.</span><span class="sxs-lookup"><span data-stu-id="9994d-174">The name is case insensitive.</span></span>
  - <span data-ttu-id="9994d-175">`[SubscriptionId <String>]`: 대상 구독의 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="9994d-175">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>

## <span data-ttu-id="9994d-176">관련 링크</span><span class="sxs-lookup"><span data-stu-id="9994d-176">RELATED LINKS</span></span>

