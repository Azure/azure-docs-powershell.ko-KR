---
external help file: ''
Module Name: Az.DedicatedHsm
online version: https://docs.microsoft.com/en-us/powershell/module/az.dedicatedhsm/get-azdedicatedhsm
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DedicatedHsm/help/Get-AzDedicatedHsm.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DedicatedHsm/help/Get-AzDedicatedHsm.md
ms.openlocfilehash: a8f6e3d6d7818a03f0e284b9c08a1ffdcd646710
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94214558"
---
# <span data-ttu-id="4f3e6-101">Get-AzDedicatedHsm</span><span class="sxs-lookup"><span data-stu-id="4f3e6-101">Get-AzDedicatedHsm</span></span>

## <span data-ttu-id="4f3e6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4f3e6-102">SYNOPSIS</span></span>
<span data-ttu-id="4f3e6-103">지정 된 Azure 전용 HSM을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="4f3e6-103">Gets the specified Azure dedicated HSM.</span></span>

## <span data-ttu-id="4f3e6-104">구문과</span><span class="sxs-lookup"><span data-stu-id="4f3e6-104">SYNTAX</span></span>

### <span data-ttu-id="4f3e6-105">List1 (기본값)</span><span class="sxs-lookup"><span data-stu-id="4f3e6-105">List1 (Default)</span></span>
```
Get-AzDedicatedHsm [-SubscriptionId <String[]>] [-Top <Int32>] [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

### <span data-ttu-id="4f3e6-106">가져오기</span><span class="sxs-lookup"><span data-stu-id="4f3e6-106">Get</span></span>
```
Get-AzDedicatedHsm -Name <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="4f3e6-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="4f3e6-107">GetViaIdentity</span></span>
```
Get-AzDedicatedHsm -InputObject <IDedicatedHsmIdentity> [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="4f3e6-108">목록</span><span class="sxs-lookup"><span data-stu-id="4f3e6-108">List</span></span>
```
Get-AzDedicatedHsm -ResourceGroupName <String> [-SubscriptionId <String[]>] [-Top <Int32>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="4f3e6-109">설명은</span><span class="sxs-lookup"><span data-stu-id="4f3e6-109">DESCRIPTION</span></span>
<span data-ttu-id="4f3e6-110">지정 된 Azure 전용 HSM을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="4f3e6-110">Gets the specified Azure dedicated HSM.</span></span>

## <span data-ttu-id="4f3e6-111">예제의</span><span class="sxs-lookup"><span data-stu-id="4f3e6-111">EXAMPLES</span></span>

### <span data-ttu-id="4f3e6-112">예제 1: 구독 하에 모든 전용 HSM 가져오기</span><span class="sxs-lookup"><span data-stu-id="4f3e6-112">Example 1: Get all Dedicated HSM under a subscription</span></span>
```powershell
PS C:\> Get-AzDedicatedHsm

Name       Provisioning State SKU                           Location
----       ------------------ ---                           --------
hsm-7t2xaf Succeeded          SafeNet Luna Network HSM A790 eastus
yeminghsm  Succeeded          SafeNet Luna Network HSM A790 eastus
```

<span data-ttu-id="4f3e6-113">이 명령은 구독에서 모든 전용 HSM을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="4f3e6-113">This command gets all Dedicated HSM under a subscription</span></span>

### <span data-ttu-id="4f3e6-114">예제 2: 리소스 그룹에 있는 모든 전용 HSM 가져오기</span><span class="sxs-lookup"><span data-stu-id="4f3e6-114">Example 2: Get all Dedicated HSM under a resource group.</span></span>
```powershell
PS C:\> Get-AzDedicatedHsm -ResourceGroupName dedicatedhsm-rg-n359cz

Name       Provisioning State SKU                           Location
----       ------------------ ---                           --------
hsm-7t2xaf Succeeded          SafeNet Luna Network HSM A790 eastus
```

<span data-ttu-id="4f3e6-115">이 명령은 리소스 그룹에 있는 모든 전용 HSM을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="4f3e6-115">This command gets all Dedicated HSM under a resource group.</span></span>

### <span data-ttu-id="4f3e6-116">예제 3: 이름으로 전용 HSM 가져오기</span><span class="sxs-lookup"><span data-stu-id="4f3e6-116">Example 3: Get a Dedicated HSM by name</span></span>
```powershell
PS C:\> Get-AzDedicatedHsm -Name hsm-7t2xaf -ResourceGroupName dedicatedhsm-rg-n359cz

Name       Provisioning State SKU                           Location
----       ------------------ ---                           --------
hsm-7t2xaf Succeeded          SafeNet Luna Network HSM A790 eastus
```

<span data-ttu-id="4f3e6-117">이 명령은 이름으로 전용 HSM을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="4f3e6-117">This command gets a Dedicated HSM by name.</span></span>

### <span data-ttu-id="4f3e6-118">예제 4: 개체 별로 전용 HSM 가져오기</span><span class="sxs-lookup"><span data-stu-id="4f3e6-118">Example 4: Get a Dedicated HSM by object</span></span>
```powershell
PS C:\> $hsm = New-AzDedicatedHsm -Name  hsm-n7wfxi -ResourceGroupName dedicatedhsm-rg-n359cz -Location eastus -Sku "SafeNet Luna Network HSM A790" -StampId stamp1 -SubnetId "/subscriptions/xxxx-xxxx-xxx-xxx/resourceGroups/dedicatedhsm-rg-n359cz/providers/Microsoft.Network/virtualNetworks/vnetq30la9/subnets/hsmsubnet" -NetworkInterface @{PrivateIPAddress = '10.2.1.120' }
PS C:\> Get-AzDedicatedHsm -InputObject $hsm

Name       Provisioning State SKU                           Location
----       ------------------ ---                           --------
hsm-n7wfxi Succeeded          SafeNet Luna Network HSM A790 eastus
```

<span data-ttu-id="4f3e6-119">이 명령은 전용 HSM을 개체 별로 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="4f3e6-119">This command gets a Dedicated HSM by object.</span></span>

## <span data-ttu-id="4f3e6-120">변수</span><span class="sxs-lookup"><span data-stu-id="4f3e6-120">PARAMETERS</span></span>

### <span data-ttu-id="4f3e6-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4f3e6-121">-DefaultProfile</span></span>
<span data-ttu-id="4f3e6-122">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="4f3e6-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4f3e6-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="4f3e6-123">-InputObject</span></span>
<span data-ttu-id="4f3e6-124">생성할 id 매개 변수는 INPUTOBJECT 속성에 대 한 참고 섹션을 참조 하 고 해시 테이블을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="4f3e6-124">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="4f3e6-125">-이름</span><span class="sxs-lookup"><span data-stu-id="4f3e6-125">-Name</span></span>
<span data-ttu-id="4f3e6-126">전용 HSM의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="4f3e6-126">The name of the dedicated HSM.</span></span>

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

### <span data-ttu-id="4f3e6-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4f3e6-127">-ResourceGroupName</span></span>
<span data-ttu-id="4f3e6-128">전용 hsm이 속한 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="4f3e6-128">The name of the Resource Group to which the dedicated hsm belongs.</span></span>

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

### <span data-ttu-id="4f3e6-129">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="4f3e6-129">-SubscriptionId</span></span>
<span data-ttu-id="4f3e6-130">Microsoft Azure 구독을 고유 하 게 식별 하는 구독 자격 증명입니다.</span><span class="sxs-lookup"><span data-stu-id="4f3e6-130">Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="4f3e6-131">구독 ID는 모든 서비스 호출에 대 한 URI의 일부를 형성 합니다.</span><span class="sxs-lookup"><span data-stu-id="4f3e6-131">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="4f3e6-132">-위쪽</span><span class="sxs-lookup"><span data-stu-id="4f3e6-132">-Top</span></span>
<span data-ttu-id="4f3e6-133">반환할 결과의 최대 수입니다.</span><span class="sxs-lookup"><span data-stu-id="4f3e6-133">Maximum number of results to return.</span></span>

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

### <span data-ttu-id="4f3e6-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4f3e6-134">CommonParameters</span></span>
<span data-ttu-id="4f3e6-135">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="4f3e6-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4f3e6-136">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="4f3e6-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4f3e6-137">입력</span><span class="sxs-lookup"><span data-stu-id="4f3e6-137">INPUTS</span></span>

### <span data-ttu-id="4f3e6-138">DedicatedHsm. IDedicatedHsmIdentity에 대 한 Microsoft PowerShell</span><span class="sxs-lookup"><span data-stu-id="4f3e6-138">Microsoft.Azure.PowerShell.Cmdlets.DedicatedHsm.Models.IDedicatedHsmIdentity</span></span>

## <span data-ttu-id="4f3e6-139">출력</span><span class="sxs-lookup"><span data-stu-id="4f3e6-139">OUTPUTS</span></span>

### <span data-ttu-id="4f3e6-140">DedicatedHsm. Api20181031. IDedicatedHsm에 대 한</span><span class="sxs-lookup"><span data-stu-id="4f3e6-140">Microsoft.Azure.PowerShell.Cmdlets.DedicatedHsm.Models.Api20181031.IDedicatedHsm</span></span>

## <span data-ttu-id="4f3e6-141">상속자</span><span class="sxs-lookup"><span data-stu-id="4f3e6-141">NOTES</span></span>

<span data-ttu-id="4f3e6-142">별칭과</span><span class="sxs-lookup"><span data-stu-id="4f3e6-142">ALIASES</span></span>

<span data-ttu-id="4f3e6-143">복합 매개 변수 속성</span><span class="sxs-lookup"><span data-stu-id="4f3e6-143">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="4f3e6-144">아래 설명 된 매개 변수를 만들려면 적절 한 속성을 포함 하는 해시 테이블을 생성 합니다.</span><span class="sxs-lookup"><span data-stu-id="4f3e6-144">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="4f3e6-145">해시 테이블에 대 한 자세한 내용은 Get-Help about_Hash_Tables를 실행 하세요.</span><span class="sxs-lookup"><span data-stu-id="4f3e6-145">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="4f3e6-146">INPUTOBJECT <IDedicatedHsmIdentity> : Identity 매개 변수</span><span class="sxs-lookup"><span data-stu-id="4f3e6-146">INPUTOBJECT <IDedicatedHsmIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="4f3e6-147">`[Id <String>]`: 리소스 id 경로</span><span class="sxs-lookup"><span data-stu-id="4f3e6-147">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="4f3e6-148">`[Name <String>]`: 전용 Hsm의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="4f3e6-148">`[Name <String>]`: Name of the dedicated Hsm</span></span>
  - <span data-ttu-id="4f3e6-149">`[ResourceGroupName <String>]`: 리소스가 속한 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="4f3e6-149">`[ResourceGroupName <String>]`: The name of the Resource Group to which the resource belongs.</span></span>
  - <span data-ttu-id="4f3e6-150">`[SubscriptionId <String>]`: Microsoft Azure 구독을 고유 하 게 식별 하는 구독 자격 증명입니다.</span><span class="sxs-lookup"><span data-stu-id="4f3e6-150">`[SubscriptionId <String>]`: Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="4f3e6-151">구독 ID는 모든 서비스 호출에 대 한 URI의 일부를 형성 합니다.</span><span class="sxs-lookup"><span data-stu-id="4f3e6-151">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="4f3e6-152">관련 링크</span><span class="sxs-lookup"><span data-stu-id="4f3e6-152">RELATED LINKS</span></span>

