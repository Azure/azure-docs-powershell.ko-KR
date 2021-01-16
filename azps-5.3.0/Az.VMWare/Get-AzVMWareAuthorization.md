---
external help file: ''
Module Name: Az.VMWare
online version: https://docs.microsoft.com/en-us/powershell/module/az.vmware/get-azvmwareauthorization
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/VMWare/help/Get-AzVMWareAuthorization.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/VMWare/help/Get-AzVMWareAuthorization.md
ms.openlocfilehash: fc89f62711744ad1e6bd7182eeb61fffd0478eaf
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98382726"
---
# <span data-ttu-id="03c8b-101">Get-AzVMWareAuthorization</span><span class="sxs-lookup"><span data-stu-id="03c8b-101">Get-AzVMWareAuthorization</span></span>

## <span data-ttu-id="03c8b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="03c8b-102">SYNOPSIS</span></span>
<span data-ttu-id="03c8b-103">사설 클라우드에서 이름으로 ExpressRoute 회로 권한 부여를 받을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="03c8b-103">Get an ExpressRoute Circuit Authorization by name in a private cloud</span></span>

## <span data-ttu-id="03c8b-104">구문</span><span class="sxs-lookup"><span data-stu-id="03c8b-104">SYNTAX</span></span>

### <span data-ttu-id="03c8b-105">목록(기본값)</span><span class="sxs-lookup"><span data-stu-id="03c8b-105">List (Default)</span></span>
```
Get-AzVMWareAuthorization -PrivateCloudName <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="03c8b-106">가져오기</span><span class="sxs-lookup"><span data-stu-id="03c8b-106">Get</span></span>
```
Get-AzVMWareAuthorization -Name <String> -PrivateCloudName <String> -ResourceGroupName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="03c8b-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="03c8b-107">GetViaIdentity</span></span>
```
Get-AzVMWareAuthorization -InputObject <IVMWareIdentity> [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="03c8b-108">설명</span><span class="sxs-lookup"><span data-stu-id="03c8b-108">DESCRIPTION</span></span>
<span data-ttu-id="03c8b-109">사설 클라우드에서 이름으로 ExpressRoute 회로 권한 부여를 받을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="03c8b-109">Get an ExpressRoute Circuit Authorization by name in a private cloud</span></span>

## <span data-ttu-id="03c8b-110">예제</span><span class="sxs-lookup"><span data-stu-id="03c8b-110">EXAMPLES</span></span>

### <span data-ttu-id="03c8b-111">예제 1: 권한 부여하기</span><span class="sxs-lookup"><span data-stu-id="03c8b-111">Example 1: Get authorization</span></span>
```powershell
PS C:\> Get-AzVMWareAuthorization -Name azps-test-auth -PrivateCloudName azps-test-cloud -ResourceGroupName azps-test-group



Name           Type
----           ----
azps-test-auth Microsoft.AVS/privateClouds/authorizations
```

<span data-ttu-id="03c8b-112">이 cmdlet은 사설 `azps-test-auth` 클라우드에서 권한 부여를 얻습니다. `azps-test-cloud`</span><span class="sxs-lookup"><span data-stu-id="03c8b-112">This cmdlet gets authorization `azps-test-auth` under private cloud `azps-test-cloud`</span></span>

### <span data-ttu-id="03c8b-113">예제 2: 권한 부여 나열</span><span class="sxs-lookup"><span data-stu-id="03c8b-113">Example 2: List authorization</span></span>
```powershell
PS C:\> Get-AzVMWareAuthorization -PrivateCloudName azps-test-cloud -ResourceGroupName azps-test-group



Name           Type
----           ----
azps-test-auth Microsoft.AVS/privateClouds/authorizations
```

<span data-ttu-id="03c8b-114">이 cmdlet은 사설 `azps-test-auth` 클라우드의 권한 부여를 나열합니다. `azps-test-cloud`</span><span class="sxs-lookup"><span data-stu-id="03c8b-114">This cmdlet lists authorization `azps-test-auth` under private cloud `azps-test-cloud`</span></span>

## <span data-ttu-id="03c8b-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="03c8b-115">PARAMETERS</span></span>

### <span data-ttu-id="03c8b-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="03c8b-116">-DefaultProfile</span></span>
<span data-ttu-id="03c8b-117">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="03c8b-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="03c8b-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="03c8b-118">-InputObject</span></span>
<span data-ttu-id="03c8b-119">ID 매개 변수를 생성하는 경우 INPUTOBJECT 속성에 대한 NOTES 섹션을 참조하고 해시 테이블을 만드십시오.</span><span class="sxs-lookup"><span data-stu-id="03c8b-119">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.VMWare.Models.IVMWareIdentity
Parameter Sets: GetViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="03c8b-120">-Name</span><span class="sxs-lookup"><span data-stu-id="03c8b-120">-Name</span></span>
<span data-ttu-id="03c8b-121">사설 클라우드의 ExpressRoute 회로 권한 부여 이름</span><span class="sxs-lookup"><span data-stu-id="03c8b-121">Name of the ExpressRoute Circuit Authorization in the private cloud</span></span>

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

### <span data-ttu-id="03c8b-122">-PrivateCloudName</span><span class="sxs-lookup"><span data-stu-id="03c8b-122">-PrivateCloudName</span></span>
<span data-ttu-id="03c8b-123">사설 클라우드의 이름</span><span class="sxs-lookup"><span data-stu-id="03c8b-123">Name of the private cloud</span></span>

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

### <span data-ttu-id="03c8b-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="03c8b-124">-ResourceGroupName</span></span>
<span data-ttu-id="03c8b-125">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="03c8b-125">The name of the resource group.</span></span>
<span data-ttu-id="03c8b-126">이름은 대소문자 무관합니다.</span><span class="sxs-lookup"><span data-stu-id="03c8b-126">The name is case insensitive.</span></span>

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

### <span data-ttu-id="03c8b-127">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="03c8b-127">-SubscriptionId</span></span>
<span data-ttu-id="03c8b-128">대상 구독의 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="03c8b-128">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="03c8b-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="03c8b-129">CommonParameters</span></span>
<span data-ttu-id="03c8b-130">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="03c8b-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="03c8b-131">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="03c8b-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="03c8b-132">입력</span><span class="sxs-lookup"><span data-stu-id="03c8b-132">INPUTS</span></span>

### <span data-ttu-id="03c8b-133">Microsoft.Azure.PowerShell.Cmdlets.VMWare.Models.IVMWareIdentity</span><span class="sxs-lookup"><span data-stu-id="03c8b-133">Microsoft.Azure.PowerShell.Cmdlets.VMWare.Models.IVMWareIdentity</span></span>

## <span data-ttu-id="03c8b-134">출력</span><span class="sxs-lookup"><span data-stu-id="03c8b-134">OUTPUTS</span></span>

### <span data-ttu-id="03c8b-135">Microsoft.Azure.PowerShell.Cmdlets.VMWare.Models.Api20200320.IExpressRouteAuthorization</span><span class="sxs-lookup"><span data-stu-id="03c8b-135">Microsoft.Azure.PowerShell.Cmdlets.VMWare.Models.Api20200320.IExpressRouteAuthorization</span></span>

## <span data-ttu-id="03c8b-136">참고 사항</span><span class="sxs-lookup"><span data-stu-id="03c8b-136">NOTES</span></span>

<span data-ttu-id="03c8b-137">별칭</span><span class="sxs-lookup"><span data-stu-id="03c8b-137">ALIASES</span></span>

<span data-ttu-id="03c8b-138">복합 매개 변수 속성</span><span class="sxs-lookup"><span data-stu-id="03c8b-138">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="03c8b-139">아래에 설명된 매개 변수를 만들 수 있도록 적절한 속성을 포함하는 해시 테이블을 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="03c8b-139">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="03c8b-140">해시 테이블에 대한 자세한 내용은 다음 Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="03c8b-140">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="03c8b-141">INPUTOBJECT: <IVMWareIdentity> ID 매개 변수</span><span class="sxs-lookup"><span data-stu-id="03c8b-141">INPUTOBJECT <IVMWareIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="03c8b-142">`[AuthorizationName <String>]`: 사설 클라우드에서 ExpressRoute 회로 권한 부여의 이름</span><span class="sxs-lookup"><span data-stu-id="03c8b-142">`[AuthorizationName <String>]`: Name of the ExpressRoute Circuit Authorization in the private cloud</span></span>
  - <span data-ttu-id="03c8b-143">`[ClusterName <String>]`: 사설 클라우드의 클러스터 이름</span><span class="sxs-lookup"><span data-stu-id="03c8b-143">`[ClusterName <String>]`: Name of the cluster in the private cloud</span></span>
  - <span data-ttu-id="03c8b-144">`[HcxEnterpriseSiteName <String>]`: 사설 클라우드의 HCX Enterprise 사이트의 이름</span><span class="sxs-lookup"><span data-stu-id="03c8b-144">`[HcxEnterpriseSiteName <String>]`: Name of the HCX Enterprise Site in the private cloud</span></span>
  - <span data-ttu-id="03c8b-145">`[Id <String>]`: 리소스 ID 경로</span><span class="sxs-lookup"><span data-stu-id="03c8b-145">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="03c8b-146">`[Location <String>]`: Azure 지역</span><span class="sxs-lookup"><span data-stu-id="03c8b-146">`[Location <String>]`: Azure region</span></span>
  - <span data-ttu-id="03c8b-147">`[PrivateCloudName <String>]`: 사설 클라우드의 이름</span><span class="sxs-lookup"><span data-stu-id="03c8b-147">`[PrivateCloudName <String>]`: Name of the private cloud</span></span>
  - <span data-ttu-id="03c8b-148">`[ResourceGroupName <String>]`: 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="03c8b-148">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="03c8b-149">이름은 대소문자 무관합니다.</span><span class="sxs-lookup"><span data-stu-id="03c8b-149">The name is case insensitive.</span></span>
  - <span data-ttu-id="03c8b-150">`[SubscriptionId <String>]`: 대상 구독의 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="03c8b-150">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>

## <span data-ttu-id="03c8b-151">관련 링크</span><span class="sxs-lookup"><span data-stu-id="03c8b-151">RELATED LINKS</span></span>
