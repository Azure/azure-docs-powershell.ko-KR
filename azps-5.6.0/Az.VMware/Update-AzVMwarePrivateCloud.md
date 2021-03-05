---
external help file: ''
Module Name: Az.VMWare
online version: https://docs.microsoft.com/powershell/module/az.vmware/update-azvmwareprivatecloud
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/VMware/help/Update-AzVMwarePrivateCloud.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/VMware/help/Update-AzVMwarePrivateCloud.md
ms.openlocfilehash: fbb45450352a99edc5a89d24ac8eb6bc4bcbf383
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101987149"
---
# <span data-ttu-id="5eab3-101">Update-AzVMWarePrivateCloud</span><span class="sxs-lookup"><span data-stu-id="5eab3-101">Update-AzVMWarePrivateCloud</span></span>

## <span data-ttu-id="5eab3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5eab3-102">SYNOPSIS</span></span>
<span data-ttu-id="5eab3-103">사설 클라우드 업데이트</span><span class="sxs-lookup"><span data-stu-id="5eab3-103">Update a private cloud</span></span>

## <span data-ttu-id="5eab3-104">구문</span><span class="sxs-lookup"><span data-stu-id="5eab3-104">SYNTAX</span></span>

### <span data-ttu-id="5eab3-105">UpdateExpanded(기본값)</span><span class="sxs-lookup"><span data-stu-id="5eab3-105">UpdateExpanded (Default)</span></span>
```
Update-AzVMWarePrivateCloud -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-IdentitySource <IIdentitySource[]>] [-Internet <InternetEnum>] [-ManagementClusterSize <Int32>]
 [-Tag <Hashtable>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="5eab3-106">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="5eab3-106">UpdateViaIdentityExpanded</span></span>
```
Update-AzVMWarePrivateCloud -InputObject <IVMWareIdentity> [-IdentitySource <IIdentitySource[]>]
 [-Internet <InternetEnum>] [-ManagementClusterSize <Int32>] [-Tag <Hashtable>] [-DefaultProfile <PSObject>]
 [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="5eab3-107">설명</span><span class="sxs-lookup"><span data-stu-id="5eab3-107">DESCRIPTION</span></span>
<span data-ttu-id="5eab3-108">사설 클라우드 업데이트</span><span class="sxs-lookup"><span data-stu-id="5eab3-108">Update a private cloud</span></span>

## <span data-ttu-id="5eab3-109">예제</span><span class="sxs-lookup"><span data-stu-id="5eab3-109">EXAMPLES</span></span>

### <span data-ttu-id="5eab3-110">예제 1: 이름에 따라 사설 클라우드의 크기 업데이트</span><span class="sxs-lookup"><span data-stu-id="5eab3-110">Example 1: Update size of private cloud by name</span></span>
```powershell
PS C:\> Update-AzVMWarePrivateCloud -Name azps-test-cloud -ResourceGroupName azps-test-group -ManagementClusterSize 4

Location      Name            Type
--------      ----            ----
australiaeast azps-test-cloud Microsoft.AVS/privateClouds
```

<span data-ttu-id="5eab3-111">이름에 따라 사설 클라우드의 업데이트 크기</span><span class="sxs-lookup"><span data-stu-id="5eab3-111">Update size of private cloud by name</span></span>

### <span data-ttu-id="5eab3-112">예제 2: 입력 개체에 따라 사설 클라우드의 크기 업데이트</span><span class="sxs-lookup"><span data-stu-id="5eab3-112">Example 2: Update size of private cloud by input object</span></span>
```powershell
PS C:\> Get-AzVMWarePrivateCloud -ResourceGroupName azps-test-group -Name azps-test-cloud | Update-AzVMWarePrivateCloud -ManagementClusterSize 4

Location      Name            Type
--------      ----            ----
australiaeast azps-test-cloud Microsoft.AVS/privateClouds
```

<span data-ttu-id="5eab3-113">입력 개체에 따라 사설 클라우드의 크기 업데이트</span><span class="sxs-lookup"><span data-stu-id="5eab3-113">Update size of private cloud by input object</span></span>

## <span data-ttu-id="5eab3-114">매개 변수</span><span class="sxs-lookup"><span data-stu-id="5eab3-114">PARAMETERS</span></span>

### <span data-ttu-id="5eab3-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="5eab3-115">-AsJob</span></span>
<span data-ttu-id="5eab3-116">작업으로 명령을 실행합니다.</span><span class="sxs-lookup"><span data-stu-id="5eab3-116">Run the command as a job</span></span>

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

### <span data-ttu-id="5eab3-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5eab3-117">-DefaultProfile</span></span>
<span data-ttu-id="5eab3-118">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="5eab3-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5eab3-119">-IdentitySource</span><span class="sxs-lookup"><span data-stu-id="5eab3-119">-IdentitySource</span></span>
<span data-ttu-id="5eab3-120">vCenter Single Sign-On ID 원본을 생성하기 위해 IDENTITYSOURCE 속성에 대한 노트 섹션을 참조하고 해시 테이블을 만드십시오.</span><span class="sxs-lookup"><span data-stu-id="5eab3-120">vCenter Single Sign On Identity Sources To construct, see NOTES section for IDENTITYSOURCE properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.VMWare.Models.Api20200320.IIdentitySource[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5eab3-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="5eab3-121">-InputObject</span></span>
<span data-ttu-id="5eab3-122">ID 매개 변수를 생성하는 경우 INPUTOBJECT 속성에 대한 노트 섹션을 참조하고 해시 테이블을 만드십시오.</span><span class="sxs-lookup"><span data-stu-id="5eab3-122">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.VMWare.Models.IVMWareIdentity
Parameter Sets: UpdateViaIdentityExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="5eab3-123">-Internet</span><span class="sxs-lookup"><span data-stu-id="5eab3-123">-Internet</span></span>
<span data-ttu-id="5eab3-124">인터넷에 대한 연결이 활성화되거나 비활성화되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="5eab3-124">Connectivity to internet is enabled or disabled</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.VMWare.Support.InternetEnum
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5eab3-125">-ManagementClusterSize</span><span class="sxs-lookup"><span data-stu-id="5eab3-125">-ManagementClusterSize</span></span>
<span data-ttu-id="5eab3-126">클러스터 크기</span><span class="sxs-lookup"><span data-stu-id="5eab3-126">The cluster size</span></span>

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

### <span data-ttu-id="5eab3-127">-Name</span><span class="sxs-lookup"><span data-stu-id="5eab3-127">-Name</span></span>
<span data-ttu-id="5eab3-128">사설 클라우드의 이름</span><span class="sxs-lookup"><span data-stu-id="5eab3-128">Name of the private cloud</span></span>

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

### <span data-ttu-id="5eab3-129">-NoWait</span><span class="sxs-lookup"><span data-stu-id="5eab3-129">-NoWait</span></span>
<span data-ttu-id="5eab3-130">명령 비동기 실행</span><span class="sxs-lookup"><span data-stu-id="5eab3-130">Run the command asynchronously</span></span>

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

### <span data-ttu-id="5eab3-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5eab3-131">-ResourceGroupName</span></span>
<span data-ttu-id="5eab3-132">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="5eab3-132">The name of the resource group.</span></span>
<span data-ttu-id="5eab3-133">이름은 대소문자와 무관합니다.</span><span class="sxs-lookup"><span data-stu-id="5eab3-133">The name is case insensitive.</span></span>

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

### <span data-ttu-id="5eab3-134">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="5eab3-134">-SubscriptionId</span></span>
<span data-ttu-id="5eab3-135">대상 구독의 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="5eab3-135">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="5eab3-136">-Tag</span><span class="sxs-lookup"><span data-stu-id="5eab3-136">-Tag</span></span>
<span data-ttu-id="5eab3-137">리소스 태그입니다.</span><span class="sxs-lookup"><span data-stu-id="5eab3-137">Resource tags.</span></span>

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

### <span data-ttu-id="5eab3-138">-확인</span><span class="sxs-lookup"><span data-stu-id="5eab3-138">-Confirm</span></span>
<span data-ttu-id="5eab3-139">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="5eab3-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5eab3-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5eab3-140">-WhatIf</span></span>
<span data-ttu-id="5eab3-141">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="5eab3-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5eab3-142">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="5eab3-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5eab3-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5eab3-143">CommonParameters</span></span>
<span data-ttu-id="5eab3-144">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="5eab3-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5eab3-145">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="5eab3-145">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5eab3-146">입력</span><span class="sxs-lookup"><span data-stu-id="5eab3-146">INPUTS</span></span>

### <span data-ttu-id="5eab3-147">Microsoft.Azure.PowerShell.Cmdlets.VMWare.Models.IVMWareIdentity</span><span class="sxs-lookup"><span data-stu-id="5eab3-147">Microsoft.Azure.PowerShell.Cmdlets.VMWare.Models.IVMWareIdentity</span></span>

## <span data-ttu-id="5eab3-148">출력</span><span class="sxs-lookup"><span data-stu-id="5eab3-148">OUTPUTS</span></span>

### <span data-ttu-id="5eab3-149">Microsoft.Azure.PowerShell.Cmdlets.VMWare.Models.Api20200320.IPrivateCloud</span><span class="sxs-lookup"><span data-stu-id="5eab3-149">Microsoft.Azure.PowerShell.Cmdlets.VMWare.Models.Api20200320.IPrivateCloud</span></span>

## <span data-ttu-id="5eab3-150">참고 사항</span><span class="sxs-lookup"><span data-stu-id="5eab3-150">NOTES</span></span>

<span data-ttu-id="5eab3-151">별칭</span><span class="sxs-lookup"><span data-stu-id="5eab3-151">ALIASES</span></span>

<span data-ttu-id="5eab3-152">복잡한 매개 변수 속성</span><span class="sxs-lookup"><span data-stu-id="5eab3-152">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="5eab3-153">아래에 설명된 매개 변수를 만들 경우 적절한 속성을 포함하는 해시 테이블을 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="5eab3-153">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="5eab3-154">해시 테이블에 대한 자세한 내용은 Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="5eab3-154">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="5eab3-155">IDENTITYSOURCE <IIdentitySource[]>: vCenter Single Sign On ID 원본</span><span class="sxs-lookup"><span data-stu-id="5eab3-155">IDENTITYSOURCE <IIdentitySource[]>: vCenter Single Sign On Identity Sources</span></span>
  - <span data-ttu-id="5eab3-156">`[Alias <String>]`: 도메인의 NetBIOS 이름</span><span class="sxs-lookup"><span data-stu-id="5eab3-156">`[Alias <String>]`: The domain's NetBIOS name</span></span>
  - <span data-ttu-id="5eab3-157">`[BaseGroupDn <String>]`: 그룹의 기본 구분 이름</span><span class="sxs-lookup"><span data-stu-id="5eab3-157">`[BaseGroupDn <String>]`: The base distinguished name for groups</span></span>
  - <span data-ttu-id="5eab3-158">`[BaseUserDn <String>]`: 사용자에 대한 기본 구분 이름</span><span class="sxs-lookup"><span data-stu-id="5eab3-158">`[BaseUserDn <String>]`: The base distinguished name for users</span></span>
  - <span data-ttu-id="5eab3-159">`[Domain <String>]`: 도메인의 dns 이름</span><span class="sxs-lookup"><span data-stu-id="5eab3-159">`[Domain <String>]`: The domain's dns name</span></span>
  - <span data-ttu-id="5eab3-160">`[Name <String>]`: ID 원본의 이름</span><span class="sxs-lookup"><span data-stu-id="5eab3-160">`[Name <String>]`: The name of the identity source</span></span>
  - <span data-ttu-id="5eab3-161">`[Password <String>]`: 사용자 및 그룹에 대한 Base DN에 대한 읽기 전용 액세스가 최소인 Active Directory 사용자의 암호입니다.</span><span class="sxs-lookup"><span data-stu-id="5eab3-161">`[Password <String>]`: The password of the Active Directory user with a minimum of read-only access to Base DN for users and groups.</span></span>
  - <span data-ttu-id="5eab3-162">`[PrimaryServer <String>]`: 기본 서버 URL</span><span class="sxs-lookup"><span data-stu-id="5eab3-162">`[PrimaryServer <String>]`: Primary server URL</span></span>
  - <span data-ttu-id="5eab3-163">`[SecondaryServer <String>]`: 보조 서버 URL</span><span class="sxs-lookup"><span data-stu-id="5eab3-163">`[SecondaryServer <String>]`: Secondary server URL</span></span>
  - <span data-ttu-id="5eab3-164">`[Ssl <SslEnum?>]`: SSL 인증서(LDAPS)를 사용하여 LDAP 통신 보호</span><span class="sxs-lookup"><span data-stu-id="5eab3-164">`[Ssl <SslEnum?>]`: Protect LDAP communication using SSL certificate (LDAPS)</span></span>
  - <span data-ttu-id="5eab3-165">`[Username <String>]`: 사용자 및 그룹에 대한 Base DN에 대한 읽기 전용 액세스가 최소인 Active Directory 사용자의 ID</span><span class="sxs-lookup"><span data-stu-id="5eab3-165">`[Username <String>]`: The ID of an Active Directory user with a minimum of read-only access to Base DN for users and group</span></span>

<span data-ttu-id="5eab3-166">INPUTOBJECT <IVMWareIdentity> : ID 매개 변수</span><span class="sxs-lookup"><span data-stu-id="5eab3-166">INPUTOBJECT <IVMWareIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="5eab3-167">`[AuthorizationName <String>]`: 사설 클라우드의 ExpressRoute 회로 권한 부여 이름</span><span class="sxs-lookup"><span data-stu-id="5eab3-167">`[AuthorizationName <String>]`: Name of the ExpressRoute Circuit Authorization in the private cloud</span></span>
  - <span data-ttu-id="5eab3-168">`[ClusterName <String>]`: 사설 클라우드의 클러스터 이름</span><span class="sxs-lookup"><span data-stu-id="5eab3-168">`[ClusterName <String>]`: Name of the cluster in the private cloud</span></span>
  - <span data-ttu-id="5eab3-169">`[HcxEnterpriseSiteName <String>]`: 사설 클라우드의 HCX Enterprise Site 이름</span><span class="sxs-lookup"><span data-stu-id="5eab3-169">`[HcxEnterpriseSiteName <String>]`: Name of the HCX Enterprise Site in the private cloud</span></span>
  - <span data-ttu-id="5eab3-170">`[Id <String>]`: 리소스 ID 경로</span><span class="sxs-lookup"><span data-stu-id="5eab3-170">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="5eab3-171">`[Location <String>]`: Azure 지역</span><span class="sxs-lookup"><span data-stu-id="5eab3-171">`[Location <String>]`: Azure region</span></span>
  - <span data-ttu-id="5eab3-172">`[PrivateCloudName <String>]`: 사설 클라우드의 이름</span><span class="sxs-lookup"><span data-stu-id="5eab3-172">`[PrivateCloudName <String>]`: Name of the private cloud</span></span>
  - <span data-ttu-id="5eab3-173">`[ResourceGroupName <String>]`: 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="5eab3-173">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="5eab3-174">이름은 대소문자와 무관합니다.</span><span class="sxs-lookup"><span data-stu-id="5eab3-174">The name is case insensitive.</span></span>
  - <span data-ttu-id="5eab3-175">`[SubscriptionId <String>]`: 대상 구독의 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="5eab3-175">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>

## <span data-ttu-id="5eab3-176">관련 링크</span><span class="sxs-lookup"><span data-stu-id="5eab3-176">RELATED LINKS</span></span>

