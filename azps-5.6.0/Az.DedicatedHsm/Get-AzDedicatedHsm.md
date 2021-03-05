---
external help file: ''
Module Name: Az.DedicatedHsm
online version: https://docs.microsoft.com/powershell/module/az.dedicatedhsm/get-azdedicatedhsm
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DedicatedHsm/help/Get-AzDedicatedHsm.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DedicatedHsm/help/Get-AzDedicatedHsm.md
ms.openlocfilehash: b4e00745655be6eb050141bb04dcef4797bde256
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101966411"
---
# <span data-ttu-id="bf9d9-101">Get-AzDedicatedHsm</span><span class="sxs-lookup"><span data-stu-id="bf9d9-101">Get-AzDedicatedHsm</span></span>

## <span data-ttu-id="bf9d9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="bf9d9-102">SYNOPSIS</span></span>
<span data-ttu-id="bf9d9-103">지정된 Azure 전용 HSM을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="bf9d9-103">Gets the specified Azure dedicated HSM.</span></span>

## <span data-ttu-id="bf9d9-104">구문</span><span class="sxs-lookup"><span data-stu-id="bf9d9-104">SYNTAX</span></span>

### <span data-ttu-id="bf9d9-105">List1(기본값)</span><span class="sxs-lookup"><span data-stu-id="bf9d9-105">List1 (Default)</span></span>
```
Get-AzDedicatedHsm [-SubscriptionId <String[]>] [-Top <Int32>] [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

### <span data-ttu-id="bf9d9-106">가져오기</span><span class="sxs-lookup"><span data-stu-id="bf9d9-106">Get</span></span>
```
Get-AzDedicatedHsm -Name <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="bf9d9-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="bf9d9-107">GetViaIdentity</span></span>
```
Get-AzDedicatedHsm -InputObject <IDedicatedHsmIdentity> [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="bf9d9-108">목록</span><span class="sxs-lookup"><span data-stu-id="bf9d9-108">List</span></span>
```
Get-AzDedicatedHsm -ResourceGroupName <String> [-SubscriptionId <String[]>] [-Top <Int32>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="bf9d9-109">설명</span><span class="sxs-lookup"><span data-stu-id="bf9d9-109">DESCRIPTION</span></span>
<span data-ttu-id="bf9d9-110">지정된 Azure 전용 HSM을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="bf9d9-110">Gets the specified Azure dedicated HSM.</span></span>

## <span data-ttu-id="bf9d9-111">예제</span><span class="sxs-lookup"><span data-stu-id="bf9d9-111">EXAMPLES</span></span>

### <span data-ttu-id="bf9d9-112">예제 1: 구독에서 모든 전용 HSM을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="bf9d9-112">Example 1: Get all Dedicated HSM under a subscription</span></span>
```powershell
PS C:\> Get-AzDedicatedHsm

Name       Provisioning State SKU                           Location
----       ------------------ ---                           --------
hsm-7t2xaf Succeeded          SafeNet Luna Network HSM A790 eastus
yeminghsm  Succeeded          SafeNet Luna Network HSM A790 eastus
```

<span data-ttu-id="bf9d9-113">이 명령은 구독에서 모든 전용 HSM을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="bf9d9-113">This command gets all Dedicated HSM under a subscription</span></span>

### <span data-ttu-id="bf9d9-114">예제 2: 리소스 그룹에서 모든 전용 HSM을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="bf9d9-114">Example 2: Get all Dedicated HSM under a resource group.</span></span>
```powershell
PS C:\> Get-AzDedicatedHsm -ResourceGroupName dedicatedhsm-rg-n359cz

Name       Provisioning State SKU                           Location
----       ------------------ ---                           --------
hsm-7t2xaf Succeeded          SafeNet Luna Network HSM A790 eastus
```

<span data-ttu-id="bf9d9-115">이 명령은 리소스 그룹 아래에서 모든 전용 HSM을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="bf9d9-115">This command gets all Dedicated HSM under a resource group.</span></span>

### <span data-ttu-id="bf9d9-116">예제 3: 이름에 의해 전용 HSM을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="bf9d9-116">Example 3: Get a Dedicated HSM by name</span></span>
```powershell
PS C:\> Get-AzDedicatedHsm -Name hsm-7t2xaf -ResourceGroupName dedicatedhsm-rg-n359cz

Name       Provisioning State SKU                           Location
----       ------------------ ---                           --------
hsm-7t2xaf Succeeded          SafeNet Luna Network HSM A790 eastus
```

<span data-ttu-id="bf9d9-117">이 명령은 이름으로 전용 HSM을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="bf9d9-117">This command gets a Dedicated HSM by name.</span></span>

### <span data-ttu-id="bf9d9-118">예제 4: 개체에 따라 전용 HSM을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="bf9d9-118">Example 4: Get a Dedicated HSM by object</span></span>
```powershell
PS C:\> $hsm = New-AzDedicatedHsm -Name  hsm-n7wfxi -ResourceGroupName dedicatedhsm-rg-n359cz -Location eastus -Sku "SafeNet Luna Network HSM A790" -StampId stamp1 -SubnetId "/subscriptions/xxxx-xxxx-xxx-xxx/resourceGroups/dedicatedhsm-rg-n359cz/providers/Microsoft.Network/virtualNetworks/vnetq30la9/subnets/hsmsubnet" -NetworkInterface @{PrivateIPAddress = '10.2.1.120' }
PS C:\> Get-AzDedicatedHsm -InputObject $hsm

Name       Provisioning State SKU                           Location
----       ------------------ ---                           --------
hsm-n7wfxi Succeeded          SafeNet Luna Network HSM A790 eastus
```

<span data-ttu-id="bf9d9-119">이 명령은 개체에 따라 전용 HSM을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="bf9d9-119">This command gets a Dedicated HSM by object.</span></span>

## <span data-ttu-id="bf9d9-120">매개 변수</span><span class="sxs-lookup"><span data-stu-id="bf9d9-120">PARAMETERS</span></span>

### <span data-ttu-id="bf9d9-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bf9d9-121">-DefaultProfile</span></span>
<span data-ttu-id="bf9d9-122">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="bf9d9-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="bf9d9-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="bf9d9-123">-InputObject</span></span>
<span data-ttu-id="bf9d9-124">ID 매개 변수를 생성하는 경우 INPUTOBJECT 속성에 대한 노트 섹션을 참조하고 해시 테이블을 만드십시오.</span><span class="sxs-lookup"><span data-stu-id="bf9d9-124">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DedicatedHsm.Models.IDedicatedHsmIdentity
Parameter Sets: GetViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="bf9d9-125">-Name</span><span class="sxs-lookup"><span data-stu-id="bf9d9-125">-Name</span></span>
<span data-ttu-id="bf9d9-126">전용 HSM의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="bf9d9-126">The name of the dedicated HSM.</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bf9d9-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bf9d9-127">-ResourceGroupName</span></span>
<span data-ttu-id="bf9d9-128">전용 hsm이 속한 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="bf9d9-128">The name of the Resource Group to which the dedicated hsm belongs.</span></span>

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

### <span data-ttu-id="bf9d9-129">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="bf9d9-129">-SubscriptionId</span></span>
<span data-ttu-id="bf9d9-130">Microsoft Azure 구독을 고유하게 식별하는 구독 자격 증명입니다.</span><span class="sxs-lookup"><span data-stu-id="bf9d9-130">Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="bf9d9-131">구독 ID는 모든 서비스 호출에 대한 URI의 일부를 형성합니다.</span><span class="sxs-lookup"><span data-stu-id="bf9d9-131">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String[]
Parameter Sets: Get, List, List1
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bf9d9-132">-Top</span><span class="sxs-lookup"><span data-stu-id="bf9d9-132">-Top</span></span>
<span data-ttu-id="bf9d9-133">반환할 최대 결과 수입니다.</span><span class="sxs-lookup"><span data-stu-id="bf9d9-133">Maximum number of results to return.</span></span>

```yaml
Type: System.Int32
Parameter Sets: List, List1
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bf9d9-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bf9d9-134">CommonParameters</span></span>
<span data-ttu-id="bf9d9-135">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="bf9d9-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bf9d9-136">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="bf9d9-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bf9d9-137">입력</span><span class="sxs-lookup"><span data-stu-id="bf9d9-137">INPUTS</span></span>

### <span data-ttu-id="bf9d9-138">Microsoft.Azure.PowerShell.Cmdlets.DedicatedHsm.Models.IDedicatedHsmIdentity</span><span class="sxs-lookup"><span data-stu-id="bf9d9-138">Microsoft.Azure.PowerShell.Cmdlets.DedicatedHsm.Models.IDedicatedHsmIdentity</span></span>

## <span data-ttu-id="bf9d9-139">출력</span><span class="sxs-lookup"><span data-stu-id="bf9d9-139">OUTPUTS</span></span>

### <span data-ttu-id="bf9d9-140">Microsoft.Azure.PowerShell.Cmdlets.DedicatedHsm.Models.Api20181031.IDedicatedHsm</span><span class="sxs-lookup"><span data-stu-id="bf9d9-140">Microsoft.Azure.PowerShell.Cmdlets.DedicatedHsm.Models.Api20181031.IDedicatedHsm</span></span>

## <span data-ttu-id="bf9d9-141">참고 사항</span><span class="sxs-lookup"><span data-stu-id="bf9d9-141">NOTES</span></span>

<span data-ttu-id="bf9d9-142">별칭</span><span class="sxs-lookup"><span data-stu-id="bf9d9-142">ALIASES</span></span>

<span data-ttu-id="bf9d9-143">복잡한 매개 변수 속성</span><span class="sxs-lookup"><span data-stu-id="bf9d9-143">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="bf9d9-144">아래에 설명된 매개 변수를 만들 경우 적절한 속성을 포함하는 해시 테이블을 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="bf9d9-144">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="bf9d9-145">해시 테이블에 대한 자세한 내용은 Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="bf9d9-145">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="bf9d9-146">INPUTOBJECT <IDedicatedHsmIdentity> : ID 매개 변수</span><span class="sxs-lookup"><span data-stu-id="bf9d9-146">INPUTOBJECT <IDedicatedHsmIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="bf9d9-147">`[Id <String>]`: 리소스 ID 경로</span><span class="sxs-lookup"><span data-stu-id="bf9d9-147">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="bf9d9-148">`[Name <String>]`: 전용 Hsm의 이름</span><span class="sxs-lookup"><span data-stu-id="bf9d9-148">`[Name <String>]`: Name of the dedicated Hsm</span></span>
  - <span data-ttu-id="bf9d9-149">`[ResourceGroupName <String>]`: 리소스가 속한 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="bf9d9-149">`[ResourceGroupName <String>]`: The name of the Resource Group to which the resource belongs.</span></span>
  - <span data-ttu-id="bf9d9-150">`[SubscriptionId <String>]`: Microsoft Azure 구독을 고유하게 식별하는 구독 자격 증명입니다.</span><span class="sxs-lookup"><span data-stu-id="bf9d9-150">`[SubscriptionId <String>]`: Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="bf9d9-151">구독 ID는 모든 서비스 호출에 대한 URI의 일부를 형성합니다.</span><span class="sxs-lookup"><span data-stu-id="bf9d9-151">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="bf9d9-152">관련 링크</span><span class="sxs-lookup"><span data-stu-id="bf9d9-152">RELATED LINKS</span></span>

