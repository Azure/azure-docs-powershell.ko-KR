---
external help file: ''
Module Name: Az.DedicatedHsm
online version: https://docs.microsoft.com/en-us/powershell/module/az.dedicatedhsm/new-azdedicatedhsm
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DedicatedHsm/help/New-AzDedicatedHsm.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DedicatedHsm/help/New-AzDedicatedHsm.md
ms.openlocfilehash: ff1fc53d7fec9a56564bbf536469ea9f745f9265
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94212274"
---
# <span data-ttu-id="91adc-101">New-AzDedicatedHsm</span><span class="sxs-lookup"><span data-stu-id="91adc-101">New-AzDedicatedHsm</span></span>

## <span data-ttu-id="91adc-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="91adc-102">SYNOPSIS</span></span>
<span data-ttu-id="91adc-103">지정 된 구독에서 전용 HSM을 만들거나 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="91adc-103">Create or Update a dedicated HSM in the specified subscription.</span></span>

## <span data-ttu-id="91adc-104">구문과</span><span class="sxs-lookup"><span data-stu-id="91adc-104">SYNTAX</span></span>

```
New-AzDedicatedHsm -Name <String> -ResourceGroupName <String> -Location <String> [-SubscriptionId <String>]
 [-NetworkInterface <INetworkInterface[]>] [-Sku <String>] [-StampId <String>] [-SubnetId <String>]
 [-Tag <Hashtable>] [-Zone <String[]>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

## <span data-ttu-id="91adc-105">설명은</span><span class="sxs-lookup"><span data-stu-id="91adc-105">DESCRIPTION</span></span>
<span data-ttu-id="91adc-106">지정 된 구독에서 전용 HSM을 만들거나 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="91adc-106">Create or Update a dedicated HSM in the specified subscription.</span></span>

## <span data-ttu-id="91adc-107">예제의</span><span class="sxs-lookup"><span data-stu-id="91adc-107">EXAMPLES</span></span>

### <span data-ttu-id="91adc-108">예제 1: 기존 가상 네트워크에 대 한 전용 HSM 만들기</span><span class="sxs-lookup"><span data-stu-id="91adc-108">Example 1: Create a Dedicated HSM into an existing virtual network</span></span>
```powershell
PS C:\> New-AzDedicatedHsm -Name  hsm-n7wfxi -ResourceGroupName dedicatedhsm-rg-n359cz -Location eastus -Sku "SafeNet Luna Network HSM A790" -StampId stamp1 -SubnetId "/subscriptions/xxxx-xxxx-xxx-xxx/resourceGroups/dedicatedhsm-rg-n359cz/providers/Microsoft.Network/virtualNetworks/vnetq30la9/subnets/hsmsubnet" -NetworkInterface @{PrivateIPAddress = '10.2.1.120' }

Name       Provisioning State SKU                           Location
----       ------------------ ---                           --------
hsm-n7wfxi Succeeded          SafeNet Luna Network HSM A790 eastus
```

<span data-ttu-id="91adc-109">이 명령은 기존 가상 네트워크에 대 한 전용 HSM을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="91adc-109">This command creates a Dedicated HSM into an existing virtual network.</span></span>

<span data-ttu-id="91adc-110">**참고:** 현재는 `New-AzDedicatedHsm` HSM이 Azure에 완전히 프로 비전 되기 전에 반환 되는 제한이 있습니다.</span><span class="sxs-lookup"><span data-stu-id="91adc-110">**NOTE:** Currently `New-AzDedicatedHsm` has a limitation that it returns before the HSM is fully provisioned on Azure.</span></span>
<span data-ttu-id="91adc-111">따라서 새 HSM을 만든 후에 `Get-AzDedicatedHsm` `Provisioning State` 는이를 사용 하기 전에 해당 상태를 쿼리하여 확인 하세요 `Succeeded` .</span><span class="sxs-lookup"><span data-stu-id="91adc-111">Therefore after creating a new HSM, please query its state by `Get-AzDedicatedHsm` and make sure its `Provisioning State` is `Succeeded` before using it.</span></span>

## <span data-ttu-id="91adc-112">변수</span><span class="sxs-lookup"><span data-stu-id="91adc-112">PARAMETERS</span></span>

### <span data-ttu-id="91adc-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="91adc-113">-AsJob</span></span>
<span data-ttu-id="91adc-114">작업으로 명령 실행</span><span class="sxs-lookup"><span data-stu-id="91adc-114">Run the command as a job</span></span>

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

### <span data-ttu-id="91adc-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="91adc-115">-DefaultProfile</span></span>
<span data-ttu-id="91adc-116">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="91adc-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="91adc-117">-위치</span><span class="sxs-lookup"><span data-stu-id="91adc-117">-Location</span></span>
<span data-ttu-id="91adc-118">전용 HSM을 만들어야 하는 지원 되는 Azure 위치입니다.</span><span class="sxs-lookup"><span data-stu-id="91adc-118">The supported Azure location where the dedicated HSM should be created.</span></span>

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

### <span data-ttu-id="91adc-119">-이름</span><span class="sxs-lookup"><span data-stu-id="91adc-119">-Name</span></span>
<span data-ttu-id="91adc-120">전용 Hsm의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="91adc-120">Name of the dedicated Hsm</span></span>

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

### <span data-ttu-id="91adc-121">-NetworkInterface</span><span class="sxs-lookup"><span data-stu-id="91adc-121">-NetworkInterface</span></span>
<span data-ttu-id="91adc-122">전용 HSM과 연결 된 네트워크 인터페이스에 대 한 리소스 Id 목록을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="91adc-122">Specifies the list of resource Ids for the network interfaces associated with the dedicated HSM.</span></span>
<span data-ttu-id="91adc-123">생성 하려면 NETWORKINTERFACE 속성에 대 한 메모 섹션을 참조 하 고 해시 테이블을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="91adc-123">To construct, see NOTES section for NETWORKINTERFACE properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DedicatedHsm.Models.Api20181031.INetworkInterface[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="91adc-124">-NoWait</span><span class="sxs-lookup"><span data-stu-id="91adc-124">-NoWait</span></span>
<span data-ttu-id="91adc-125">비동기적으로 명령 실행</span><span class="sxs-lookup"><span data-stu-id="91adc-125">Run the command asynchronously</span></span>

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

### <span data-ttu-id="91adc-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="91adc-126">-ResourceGroupName</span></span>
<span data-ttu-id="91adc-127">리소스가 속한 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="91adc-127">The name of the Resource Group to which the resource belongs.</span></span>

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

### <span data-ttu-id="91adc-128">-Sku</span><span class="sxs-lookup"><span data-stu-id="91adc-128">-Sku</span></span>
<span data-ttu-id="91adc-129">전용 HSM의 SKU</span><span class="sxs-lookup"><span data-stu-id="91adc-129">SKU of the dedicated HSM</span></span>

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

### <span data-ttu-id="91adc-130">-StampId</span><span class="sxs-lookup"><span data-stu-id="91adc-130">-StampId</span></span>
<span data-ttu-id="91adc-131">이 필드는 RP가 가용성 영역을 지원 하지 않는 경우에 사용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="91adc-131">This field will be used when RP does not support Availability zones.</span></span>

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

### <span data-ttu-id="91adc-132">-SubnetId</span><span class="sxs-lookup"><span data-stu-id="91adc-132">-SubnetId</span></span>
<span data-ttu-id="91adc-133">/Subscriptions/{SubscriptionId}/resourceGroups/{ResourceGroupName}/...의 형식으로 된 팔 리소스 id</span><span class="sxs-lookup"><span data-stu-id="91adc-133">The ARM resource id in the form of /subscriptions/{SubscriptionId}/resourceGroups/{ResourceGroupName}/...</span></span>

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

### <span data-ttu-id="91adc-134">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="91adc-134">-SubscriptionId</span></span>
<span data-ttu-id="91adc-135">Microsoft Azure 구독을 고유 하 게 식별 하는 구독 자격 증명입니다.</span><span class="sxs-lookup"><span data-stu-id="91adc-135">Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="91adc-136">구독 ID는 모든 서비스 호출에 대 한 URI의 일부를 형성 합니다.</span><span class="sxs-lookup"><span data-stu-id="91adc-136">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="91adc-137">태그</span><span class="sxs-lookup"><span data-stu-id="91adc-137">-Tag</span></span>
<span data-ttu-id="91adc-138">리소스 태그</span><span class="sxs-lookup"><span data-stu-id="91adc-138">Resource tags</span></span>

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

### <span data-ttu-id="91adc-139">-Zone</span><span class="sxs-lookup"><span data-stu-id="91adc-139">-Zone</span></span>
<span data-ttu-id="91adc-140">전용 Hsm 영역입니다.</span><span class="sxs-lookup"><span data-stu-id="91adc-140">The Dedicated Hsm zones.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="91adc-141">-확인</span><span class="sxs-lookup"><span data-stu-id="91adc-141">-Confirm</span></span>
<span data-ttu-id="91adc-142">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="91adc-142">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="91adc-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="91adc-143">-WhatIf</span></span>
<span data-ttu-id="91adc-144">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="91adc-144">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="91adc-145">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="91adc-145">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="91adc-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="91adc-146">CommonParameters</span></span>
<span data-ttu-id="91adc-147">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="91adc-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="91adc-148">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="91adc-148">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="91adc-149">입력</span><span class="sxs-lookup"><span data-stu-id="91adc-149">INPUTS</span></span>

## <span data-ttu-id="91adc-150">출력</span><span class="sxs-lookup"><span data-stu-id="91adc-150">OUTPUTS</span></span>

### <span data-ttu-id="91adc-151">DedicatedHsm. Api20181031. IDedicatedHsm에 대 한</span><span class="sxs-lookup"><span data-stu-id="91adc-151">Microsoft.Azure.PowerShell.Cmdlets.DedicatedHsm.Models.Api20181031.IDedicatedHsm</span></span>

## <span data-ttu-id="91adc-152">상속자</span><span class="sxs-lookup"><span data-stu-id="91adc-152">NOTES</span></span>

<span data-ttu-id="91adc-153">별칭과</span><span class="sxs-lookup"><span data-stu-id="91adc-153">ALIASES</span></span>

<span data-ttu-id="91adc-154">복합 매개 변수 속성</span><span class="sxs-lookup"><span data-stu-id="91adc-154">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="91adc-155">아래 설명 된 매개 변수를 만들려면 적절 한 속성을 포함 하는 해시 테이블을 생성 합니다.</span><span class="sxs-lookup"><span data-stu-id="91adc-155">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="91adc-156">해시 테이블에 대 한 자세한 내용은 Get-Help about_Hash_Tables를 실행 하세요.</span><span class="sxs-lookup"><span data-stu-id="91adc-156">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="91adc-157">NETWORKINTERFACE <INetworkInterface [] >: 전용 HSM과 연결 된 네트워크 인터페이스에 대 한 리소스 Id 목록을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="91adc-157">NETWORKINTERFACE <INetworkInterface[]>: Specifies the list of resource Ids for the network interfaces associated with the dedicated HSM.</span></span>
  - <span data-ttu-id="91adc-158">`[PrivateIPAddress <String>]`: 인터페이스의 개인 Ip 주소</span><span class="sxs-lookup"><span data-stu-id="91adc-158">`[PrivateIPAddress <String>]`: Private Ip address of the interface</span></span>

## <span data-ttu-id="91adc-159">관련 링크</span><span class="sxs-lookup"><span data-stu-id="91adc-159">RELATED LINKS</span></span>

