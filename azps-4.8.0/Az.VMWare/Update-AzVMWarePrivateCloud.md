---
external help file: ''
Module Name: Az.VMWare
online version: https://docs.microsoft.com/en-us/powershell/module/az.vmware/update-azvmwareprivatecloud
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/VMWare/help/Update-AzVMWarePrivateCloud.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/VMWare/help/Update-AzVMWarePrivateCloud.md
ms.openlocfilehash: e47cf4fe3eef11664640e947b7093dc302f90ea3
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94212452"
---
# <span data-ttu-id="13313-101">Update-AzVMWarePrivateCloud</span><span class="sxs-lookup"><span data-stu-id="13313-101">Update-AzVMWarePrivateCloud</span></span>

## <span data-ttu-id="13313-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="13313-102">SYNOPSIS</span></span>
<span data-ttu-id="13313-103">사설 클라우드 업데이트</span><span class="sxs-lookup"><span data-stu-id="13313-103">Update a private cloud</span></span>

## <span data-ttu-id="13313-104">구문과</span><span class="sxs-lookup"><span data-stu-id="13313-104">SYNTAX</span></span>

### <span data-ttu-id="13313-105">UpdateExpanded 됨 (기본값)</span><span class="sxs-lookup"><span data-stu-id="13313-105">UpdateExpanded (Default)</span></span>
```
Update-AzVMWarePrivateCloud -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-IdentitySource <IIdentitySource[]>] [-Internet <InternetEnum>] [-ManagementClusterSize <Int32>]
 [-Tag <Hashtable>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="13313-106">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="13313-106">UpdateViaIdentityExpanded</span></span>
```
Update-AzVMWarePrivateCloud -InputObject <IVMWareIdentity> [-IdentitySource <IIdentitySource[]>]
 [-Internet <InternetEnum>] [-ManagementClusterSize <Int32>] [-Tag <Hashtable>] [-DefaultProfile <PSObject>]
 [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="13313-107">설명은</span><span class="sxs-lookup"><span data-stu-id="13313-107">DESCRIPTION</span></span>
<span data-ttu-id="13313-108">사설 클라우드 업데이트</span><span class="sxs-lookup"><span data-stu-id="13313-108">Update a private cloud</span></span>

## <span data-ttu-id="13313-109">예제의</span><span class="sxs-lookup"><span data-stu-id="13313-109">EXAMPLES</span></span>

### <span data-ttu-id="13313-110">예제 1: 이름으로 사설 클라우드의 크기 업데이트</span><span class="sxs-lookup"><span data-stu-id="13313-110">Example 1: Update size of private cloud by name</span></span>
```powershell
PS C:\> Update-AzVMWarePrivateCloud -Name azps-test-cloud -ResourceGroupName azps-test-group -ManagementClusterSize 4

Location      Name            Type
--------      ----            ----
australiaeast azps-test-cloud Microsoft.AVS/privateClouds
```

<span data-ttu-id="13313-111">이름으로 사설 클라우드의 크기 업데이트</span><span class="sxs-lookup"><span data-stu-id="13313-111">Update size of private cloud by name</span></span>

### <span data-ttu-id="13313-112">예제 2: 입력 개체 별로 사설 클라우드의 크기 업데이트</span><span class="sxs-lookup"><span data-stu-id="13313-112">Example 2: Update size of private cloud by input object</span></span>
```powershell
PS C:\> Get-AzVMWarePrivateCloud -ResourceGroupName azps-test-group -Name azps-test-cloud | Update-AzVMWarePrivateCloud -ManagementClusterSize 4

Location      Name            Type
--------      ----            ----
australiaeast azps-test-cloud Microsoft.AVS/privateClouds
```

<span data-ttu-id="13313-113">입력 개체를 기준으로 사설 클라우드의 크기 업데이트</span><span class="sxs-lookup"><span data-stu-id="13313-113">Update size of private cloud by input object</span></span>

## <span data-ttu-id="13313-114">변수</span><span class="sxs-lookup"><span data-stu-id="13313-114">PARAMETERS</span></span>

### <span data-ttu-id="13313-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="13313-115">-AsJob</span></span>
<span data-ttu-id="13313-116">작업으로 명령 실행</span><span class="sxs-lookup"><span data-stu-id="13313-116">Run the command as a job</span></span>

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

### <span data-ttu-id="13313-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="13313-117">-DefaultProfile</span></span>
<span data-ttu-id="13313-118">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="13313-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="13313-119">-IdentitySource</span><span class="sxs-lookup"><span data-stu-id="13313-119">-IdentitySource</span></span>
<span data-ttu-id="13313-120">생성을 위한 vCenter Single Sign On Id 원본 IDENTITYSOURCE 속성에 대 한 참고 섹션을 참조 하 고 해시 테이블을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="13313-120">vCenter Single Sign On Identity Sources To construct, see NOTES section for IDENTITYSOURCE properties and create a hash table.</span></span>

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

### <span data-ttu-id="13313-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="13313-121">-InputObject</span></span>
<span data-ttu-id="13313-122">생성할 id 매개 변수는 INPUTOBJECT 속성에 대 한 참고 섹션을 참조 하 고 해시 테이블을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="13313-122">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="13313-123">-인터넷</span><span class="sxs-lookup"><span data-stu-id="13313-123">-Internet</span></span>
<span data-ttu-id="13313-124">인터넷 연결을 사용 하거나 사용 하지 않도록 설정</span><span class="sxs-lookup"><span data-stu-id="13313-124">Connectivity to internet is enabled or disabled</span></span>

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

### <span data-ttu-id="13313-125">-ManagementClusterSize</span><span class="sxs-lookup"><span data-stu-id="13313-125">-ManagementClusterSize</span></span>
<span data-ttu-id="13313-126">클러스터 크기</span><span class="sxs-lookup"><span data-stu-id="13313-126">The cluster size</span></span>

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

### <span data-ttu-id="13313-127">-이름</span><span class="sxs-lookup"><span data-stu-id="13313-127">-Name</span></span>
<span data-ttu-id="13313-128">사설 클라우드의 이름</span><span class="sxs-lookup"><span data-stu-id="13313-128">Name of the private cloud</span></span>

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

### <span data-ttu-id="13313-129">-NoWait</span><span class="sxs-lookup"><span data-stu-id="13313-129">-NoWait</span></span>
<span data-ttu-id="13313-130">비동기적으로 명령 실행</span><span class="sxs-lookup"><span data-stu-id="13313-130">Run the command asynchronously</span></span>

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

### <span data-ttu-id="13313-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="13313-131">-ResourceGroupName</span></span>
<span data-ttu-id="13313-132">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="13313-132">The name of the resource group.</span></span>
<span data-ttu-id="13313-133">이름은 대/소문자를 구분 합니다.</span><span class="sxs-lookup"><span data-stu-id="13313-133">The name is case insensitive.</span></span>

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

### <span data-ttu-id="13313-134">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="13313-134">-SubscriptionId</span></span>
<span data-ttu-id="13313-135">대상 구독의 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="13313-135">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="13313-136">태그</span><span class="sxs-lookup"><span data-stu-id="13313-136">-Tag</span></span>
<span data-ttu-id="13313-137">리소스 태그.</span><span class="sxs-lookup"><span data-stu-id="13313-137">Resource tags.</span></span>

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

### <span data-ttu-id="13313-138">-확인</span><span class="sxs-lookup"><span data-stu-id="13313-138">-Confirm</span></span>
<span data-ttu-id="13313-139">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="13313-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="13313-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="13313-140">-WhatIf</span></span>
<span data-ttu-id="13313-141">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="13313-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="13313-142">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="13313-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="13313-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="13313-143">CommonParameters</span></span>
<span data-ttu-id="13313-144">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="13313-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="13313-145">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="13313-145">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="13313-146">입력</span><span class="sxs-lookup"><span data-stu-id="13313-146">INPUTS</span></span>

### <span data-ttu-id="13313-147">IVMWareIdentity (Microsoft. v.</span><span class="sxs-lookup"><span data-stu-id="13313-147">Microsoft.Azure.PowerShell.Cmdlets.VMWare.Models.IVMWareIdentity</span></span>

## <span data-ttu-id="13313-148">출력</span><span class="sxs-lookup"><span data-stu-id="13313-148">OUTPUTS</span></span>

### <span data-ttu-id="13313-149">Api20200320. IPrivateCloud에 대 한 Microsoft.</span><span class="sxs-lookup"><span data-stu-id="13313-149">Microsoft.Azure.PowerShell.Cmdlets.VMWare.Models.Api20200320.IPrivateCloud</span></span>

## <span data-ttu-id="13313-150">상속자</span><span class="sxs-lookup"><span data-stu-id="13313-150">NOTES</span></span>

<span data-ttu-id="13313-151">별칭과</span><span class="sxs-lookup"><span data-stu-id="13313-151">ALIASES</span></span>

<span data-ttu-id="13313-152">복합 매개 변수 속성</span><span class="sxs-lookup"><span data-stu-id="13313-152">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="13313-153">아래 설명 된 매개 변수를 만들려면 적절 한 속성을 포함 하는 해시 테이블을 생성 합니다.</span><span class="sxs-lookup"><span data-stu-id="13313-153">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="13313-154">해시 테이블에 대 한 자세한 내용은 Get-Help about_Hash_Tables를 실행 하세요.</span><span class="sxs-lookup"><span data-stu-id="13313-154">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="13313-155">IDENTITYSOURCE <IIdentitySource [] >: vCenter Single Sign On Id 원본</span><span class="sxs-lookup"><span data-stu-id="13313-155">IDENTITYSOURCE <IIdentitySource[]>: vCenter Single Sign On Identity Sources</span></span>
  - <span data-ttu-id="13313-156">`[Alias <String>]`: 도메인의 NetBIOS 이름</span><span class="sxs-lookup"><span data-stu-id="13313-156">`[Alias <String>]`: The domain's NetBIOS name</span></span>
  - <span data-ttu-id="13313-157">`[BaseGroupDn <String>]`: 그룹의 기본 고유 이름</span><span class="sxs-lookup"><span data-stu-id="13313-157">`[BaseGroupDn <String>]`: The base distinguished name for groups</span></span>
  - <span data-ttu-id="13313-158">`[BaseUserDn <String>]`: 사용자의 기본 고유 이름</span><span class="sxs-lookup"><span data-stu-id="13313-158">`[BaseUserDn <String>]`: The base distinguished name for users</span></span>
  - <span data-ttu-id="13313-159">`[Domain <String>]`: 도메인의 dns 이름</span><span class="sxs-lookup"><span data-stu-id="13313-159">`[Domain <String>]`: The domain's dns name</span></span>
  - <span data-ttu-id="13313-160">`[Name <String>]`: Id 원본의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="13313-160">`[Name <String>]`: The name of the identity source</span></span>
  - <span data-ttu-id="13313-161">`[Password <String>]`: 사용자 및 그룹의 기본 DN에 대 한 최소 읽기 전용 액세스 권한이 있는 Active Directory 사용자의 암호입니다.</span><span class="sxs-lookup"><span data-stu-id="13313-161">`[Password <String>]`: The password of the Active Directory user with a minimum of read-only access to Base DN for users and groups.</span></span>
  - <span data-ttu-id="13313-162">`[PrimaryServer <String>]`: 주 서버 URL</span><span class="sxs-lookup"><span data-stu-id="13313-162">`[PrimaryServer <String>]`: Primary server URL</span></span>
  - <span data-ttu-id="13313-163">`[SecondaryServer <String>]`: 보조 서버 URL</span><span class="sxs-lookup"><span data-stu-id="13313-163">`[SecondaryServer <String>]`: Secondary server URL</span></span>
  - <span data-ttu-id="13313-164">`[Ssl <SslEnum?>]`: SSL 인증서를 사용 하 여 LDAP 통신 보호 (LDAPS)</span><span class="sxs-lookup"><span data-stu-id="13313-164">`[Ssl <SslEnum?>]`: Protect LDAP communication using SSL certificate (LDAPS)</span></span>
  - <span data-ttu-id="13313-165">`[Username <String>]`: 사용자 및 그룹의 기본 DN에 대 한 최소 읽기 전용 액세스 권한이 있는 Active Directory 사용자의 ID</span><span class="sxs-lookup"><span data-stu-id="13313-165">`[Username <String>]`: The ID of an Active Directory user with a minimum of read-only access to Base DN for users and group</span></span>

<span data-ttu-id="13313-166">INPUTOBJECT <IVMWareIdentity> : Identity 매개 변수</span><span class="sxs-lookup"><span data-stu-id="13313-166">INPUTOBJECT <IVMWareIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="13313-167">`[AuthorizationName <String>]`: 사설 클라우드의 Express 경로 권한 부여 이름</span><span class="sxs-lookup"><span data-stu-id="13313-167">`[AuthorizationName <String>]`: Name of the ExpressRoute Circuit Authorization in the private cloud</span></span>
  - <span data-ttu-id="13313-168">`[ClusterName <String>]`: 사설 클라우드의 클러스터 이름</span><span class="sxs-lookup"><span data-stu-id="13313-168">`[ClusterName <String>]`: Name of the cluster in the private cloud</span></span>
  - <span data-ttu-id="13313-169">`[HcxEnterpriseSiteName <String>]`: 사설 클라우드의 HCX Enterprise 사이트의 이름</span><span class="sxs-lookup"><span data-stu-id="13313-169">`[HcxEnterpriseSiteName <String>]`: Name of the HCX Enterprise Site in the private cloud</span></span>
  - <span data-ttu-id="13313-170">`[Id <String>]`: 리소스 id 경로</span><span class="sxs-lookup"><span data-stu-id="13313-170">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="13313-171">`[Location <String>]`: Azure 지역</span><span class="sxs-lookup"><span data-stu-id="13313-171">`[Location <String>]`: Azure region</span></span>
  - <span data-ttu-id="13313-172">`[PrivateCloudName <String>]`: 사설 클라우드의 이름</span><span class="sxs-lookup"><span data-stu-id="13313-172">`[PrivateCloudName <String>]`: Name of the private cloud</span></span>
  - <span data-ttu-id="13313-173">`[ResourceGroupName <String>]`: 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="13313-173">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="13313-174">이름은 대/소문자를 구분 합니다.</span><span class="sxs-lookup"><span data-stu-id="13313-174">The name is case insensitive.</span></span>
  - <span data-ttu-id="13313-175">`[SubscriptionId <String>]`: 대상 구독의 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="13313-175">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>

## <span data-ttu-id="13313-176">관련 링크</span><span class="sxs-lookup"><span data-stu-id="13313-176">RELATED LINKS</span></span>

