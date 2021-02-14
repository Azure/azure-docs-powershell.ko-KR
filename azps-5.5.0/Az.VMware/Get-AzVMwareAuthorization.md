---
external help file: ''
Module Name: Az.VMware
online version: https://docs.microsoft.com/en-us/powershell/module/az.vmware/get-azvmwareauthorization
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/VMware/help/Get-AzVMwareAuthorization.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/VMware/help/Get-AzVMwareAuthorization.md
ms.openlocfilehash: f4e4ea13f6e3fd46b1defa8dbf327024cb7557d6
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100197260"
---
# <span data-ttu-id="85dcd-101">Get-AzVMwareAuthorization</span><span class="sxs-lookup"><span data-stu-id="85dcd-101">Get-AzVMwareAuthorization</span></span>

## <span data-ttu-id="85dcd-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="85dcd-102">SYNOPSIS</span></span>
<span data-ttu-id="85dcd-103">사설 클라우드에서 이름으로 ExpressRoute 회로 권한 부여를 받을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="85dcd-103">Get an ExpressRoute Circuit Authorization by name in a private cloud</span></span>

## <span data-ttu-id="85dcd-104">구문</span><span class="sxs-lookup"><span data-stu-id="85dcd-104">SYNTAX</span></span>

### <span data-ttu-id="85dcd-105">목록(기본값)</span><span class="sxs-lookup"><span data-stu-id="85dcd-105">List (Default)</span></span>
```
Get-AzVMwareAuthorization -PrivateCloudName <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="85dcd-106">가져오기</span><span class="sxs-lookup"><span data-stu-id="85dcd-106">Get</span></span>
```
Get-AzVMwareAuthorization -Name <String> -PrivateCloudName <String> -ResourceGroupName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="85dcd-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="85dcd-107">GetViaIdentity</span></span>
```
Get-AzVMwareAuthorization -InputObject <IVMwareIdentity> [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="85dcd-108">설명</span><span class="sxs-lookup"><span data-stu-id="85dcd-108">DESCRIPTION</span></span>
<span data-ttu-id="85dcd-109">사설 클라우드에서 이름으로 ExpressRoute 회로 권한 부여를 받을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="85dcd-109">Get an ExpressRoute Circuit Authorization by name in a private cloud</span></span>

## <span data-ttu-id="85dcd-110">예제</span><span class="sxs-lookup"><span data-stu-id="85dcd-110">EXAMPLES</span></span>

### <span data-ttu-id="85dcd-111">예제 1: 권한 부여하기</span><span class="sxs-lookup"><span data-stu-id="85dcd-111">Example 1: Get authorization</span></span>
```powershell
PS C:\> Get-AzVMwareAuthorization -Name azps-test-auth -PrivateCloudName azps-test-cloud -ResourceGroupName azps-test-group



Name           Type
----           ----
azps-test-auth Microsoft.AVS/privateClouds/authorizations
```

<span data-ttu-id="85dcd-112">이 cmdlet은 사설 `azps-test-auth` 클라우드에서 권한 부여를 얻습니다. `azps-test-cloud`</span><span class="sxs-lookup"><span data-stu-id="85dcd-112">This cmdlet gets authorization `azps-test-auth` under private cloud `azps-test-cloud`</span></span>

### <span data-ttu-id="85dcd-113">예제 2: 권한 부여 나열</span><span class="sxs-lookup"><span data-stu-id="85dcd-113">Example 2: List authorization</span></span>
```powershell
PS C:\> Get-AzVMwareAuthorization -PrivateCloudName azps-test-cloud -ResourceGroupName azps-test-group



Name           Type
----           ----
azps-test-auth Microsoft.AVS/privateClouds/authorizations
```

<span data-ttu-id="85dcd-114">이 cmdlet은 사설 `azps-test-auth` 클라우드의 권한 부여를 나열합니다. `azps-test-cloud`</span><span class="sxs-lookup"><span data-stu-id="85dcd-114">This cmdlet lists authorization `azps-test-auth` under private cloud `azps-test-cloud`</span></span>

## <span data-ttu-id="85dcd-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="85dcd-115">PARAMETERS</span></span>

### <span data-ttu-id="85dcd-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="85dcd-116">-DefaultProfile</span></span>
<span data-ttu-id="85dcd-117">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="85dcd-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="85dcd-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="85dcd-118">-InputObject</span></span>
<span data-ttu-id="85dcd-119">ID 매개 변수를 생성하는 경우 INPUTOBJECT 속성에 대한 NOTES 섹션을 참조하고 해시 테이블을 만드십시오.</span><span class="sxs-lookup"><span data-stu-id="85dcd-119">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.VMware.Models.IVMwareIdentity
Parameter Sets: GetViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="85dcd-120">-Name</span><span class="sxs-lookup"><span data-stu-id="85dcd-120">-Name</span></span>
<span data-ttu-id="85dcd-121">사설 클라우드의 ExpressRoute 회로 권한 부여 이름</span><span class="sxs-lookup"><span data-stu-id="85dcd-121">Name of the ExpressRoute Circuit Authorization in the private cloud</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases: AuthorizationName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="85dcd-122">-PrivateCloudName</span><span class="sxs-lookup"><span data-stu-id="85dcd-122">-PrivateCloudName</span></span>
<span data-ttu-id="85dcd-123">사설 클라우드의 이름</span><span class="sxs-lookup"><span data-stu-id="85dcd-123">Name of the private cloud</span></span>

```yaml
Type: System.String
Parameter Sets: Get, List
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="85dcd-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="85dcd-124">-ResourceGroupName</span></span>
<span data-ttu-id="85dcd-125">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="85dcd-125">The name of the resource group.</span></span>
<span data-ttu-id="85dcd-126">이름은 대소문자 무관합니다.</span><span class="sxs-lookup"><span data-stu-id="85dcd-126">The name is case insensitive.</span></span>

```yaml
Type: System.String
Parameter Sets: Get, List
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="85dcd-127">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="85dcd-127">-SubscriptionId</span></span>
<span data-ttu-id="85dcd-128">대상 구독의 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="85dcd-128">The ID of the target subscription.</span></span>

```yaml
Type: System.String[]
Parameter Sets: Get, List
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="85dcd-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="85dcd-129">CommonParameters</span></span>
<span data-ttu-id="85dcd-130">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="85dcd-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="85dcd-131">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="85dcd-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="85dcd-132">입력</span><span class="sxs-lookup"><span data-stu-id="85dcd-132">INPUTS</span></span>

### <span data-ttu-id="85dcd-133">Microsoft.Azure.PowerShell.Cmdlets.VMware.Models.IVMwareIdentity</span><span class="sxs-lookup"><span data-stu-id="85dcd-133">Microsoft.Azure.PowerShell.Cmdlets.VMware.Models.IVMwareIdentity</span></span>

## <span data-ttu-id="85dcd-134">출력</span><span class="sxs-lookup"><span data-stu-id="85dcd-134">OUTPUTS</span></span>

### <span data-ttu-id="85dcd-135">Microsoft.Azure.PowerShell.Cmdlets.VMware.Models.Api20200320.IExpressRouteAuthorization</span><span class="sxs-lookup"><span data-stu-id="85dcd-135">Microsoft.Azure.PowerShell.Cmdlets.VMware.Models.Api20200320.IExpressRouteAuthorization</span></span>

## <span data-ttu-id="85dcd-136">참고 사항</span><span class="sxs-lookup"><span data-stu-id="85dcd-136">NOTES</span></span>

<span data-ttu-id="85dcd-137">별칭</span><span class="sxs-lookup"><span data-stu-id="85dcd-137">ALIASES</span></span>

<span data-ttu-id="85dcd-138">복합 매개 변수 속성</span><span class="sxs-lookup"><span data-stu-id="85dcd-138">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="85dcd-139">아래에 설명된 매개 변수를 만들 수 있도록 적절한 속성을 포함하는 해시 테이블을 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="85dcd-139">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="85dcd-140">해시 테이블에 대한 자세한 내용은 다음 Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="85dcd-140">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="85dcd-141">INPUTOBJECT: <IVMwareIdentity> ID 매개 변수</span><span class="sxs-lookup"><span data-stu-id="85dcd-141">INPUTOBJECT <IVMwareIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="85dcd-142">`[AuthorizationName <String>]`: 사설 클라우드에서 ExpressRoute 회로 권한 부여의 이름</span><span class="sxs-lookup"><span data-stu-id="85dcd-142">`[AuthorizationName <String>]`: Name of the ExpressRoute Circuit Authorization in the private cloud</span></span>
  - <span data-ttu-id="85dcd-143">`[ClusterName <String>]`: 사설 클라우드의 클러스터 이름</span><span class="sxs-lookup"><span data-stu-id="85dcd-143">`[ClusterName <String>]`: Name of the cluster in the private cloud</span></span>
  - <span data-ttu-id="85dcd-144">`[HcxEnterpriseSiteName <String>]`: 사설 클라우드의 HCX Enterprise 사이트의 이름</span><span class="sxs-lookup"><span data-stu-id="85dcd-144">`[HcxEnterpriseSiteName <String>]`: Name of the HCX Enterprise Site in the private cloud</span></span>
  - <span data-ttu-id="85dcd-145">`[Id <String>]`: 리소스 ID 경로</span><span class="sxs-lookup"><span data-stu-id="85dcd-145">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="85dcd-146">`[Location <String>]`: Azure 지역</span><span class="sxs-lookup"><span data-stu-id="85dcd-146">`[Location <String>]`: Azure region</span></span>
  - <span data-ttu-id="85dcd-147">`[PrivateCloudName <String>]`: 사설 클라우드의 이름</span><span class="sxs-lookup"><span data-stu-id="85dcd-147">`[PrivateCloudName <String>]`: Name of the private cloud</span></span>
  - <span data-ttu-id="85dcd-148">`[ResourceGroupName <String>]`: 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="85dcd-148">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="85dcd-149">이름은 대소문자 무관합니다.</span><span class="sxs-lookup"><span data-stu-id="85dcd-149">The name is case insensitive.</span></span>
  - <span data-ttu-id="85dcd-150">`[SubscriptionId <String>]`: 대상 구독의 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="85dcd-150">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>

## <span data-ttu-id="85dcd-151">관련 링크</span><span class="sxs-lookup"><span data-stu-id="85dcd-151">RELATED LINKS</span></span>

