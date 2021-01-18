---
external help file: ''
Module Name: Az.DedicatedHsm
online version: https://docs.microsoft.com/en-us/powershell/module/az.dedicatedhsm/new-azdedicatedhsm
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DedicatedHsm/help/New-AzDedicatedHsm.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DedicatedHsm/help/New-AzDedicatedHsm.md
ms.openlocfilehash: ff1fc53d7fec9a56564bbf536469ea9f745f9265
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98494604"
---
# <span data-ttu-id="3950c-101">New-AzDedicatedHsm</span><span class="sxs-lookup"><span data-stu-id="3950c-101">New-AzDedicatedHsm</span></span>

## <span data-ttu-id="3950c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3950c-102">SYNOPSIS</span></span>
<span data-ttu-id="3950c-103">지정된 구독에서 전용 HSM을 만들거나 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="3950c-103">Create or Update a dedicated HSM in the specified subscription.</span></span>

## <span data-ttu-id="3950c-104">구문</span><span class="sxs-lookup"><span data-stu-id="3950c-104">SYNTAX</span></span>

```
New-AzDedicatedHsm -Name <String> -ResourceGroupName <String> -Location <String> [-SubscriptionId <String>]
 [-NetworkInterface <INetworkInterface[]>] [-Sku <String>] [-StampId <String>] [-SubnetId <String>]
 [-Tag <Hashtable>] [-Zone <String[]>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

## <span data-ttu-id="3950c-105">설명</span><span class="sxs-lookup"><span data-stu-id="3950c-105">DESCRIPTION</span></span>
<span data-ttu-id="3950c-106">지정된 구독에서 전용 HSM을 만들거나 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="3950c-106">Create or Update a dedicated HSM in the specified subscription.</span></span>

## <span data-ttu-id="3950c-107">예제</span><span class="sxs-lookup"><span data-stu-id="3950c-107">EXAMPLES</span></span>

### <span data-ttu-id="3950c-108">예제 1: 기존 가상 네트워크에 전용 HSM 만들기</span><span class="sxs-lookup"><span data-stu-id="3950c-108">Example 1: Create a Dedicated HSM into an existing virtual network</span></span>
```powershell
PS C:\> New-AzDedicatedHsm -Name  hsm-n7wfxi -ResourceGroupName dedicatedhsm-rg-n359cz -Location eastus -Sku "SafeNet Luna Network HSM A790" -StampId stamp1 -SubnetId "/subscriptions/xxxx-xxxx-xxx-xxx/resourceGroups/dedicatedhsm-rg-n359cz/providers/Microsoft.Network/virtualNetworks/vnetq30la9/subnets/hsmsubnet" -NetworkInterface @{PrivateIPAddress = '10.2.1.120' }

Name       Provisioning State SKU                           Location
----       ------------------ ---                           --------
hsm-n7wfxi Succeeded          SafeNet Luna Network HSM A790 eastus
```

<span data-ttu-id="3950c-109">이 명령은 전용 HSM을 기존 가상 네트워크에 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="3950c-109">This command creates a Dedicated HSM into an existing virtual network.</span></span>

<span data-ttu-id="3950c-110">**참고:** 현재 HSM이 Azure에서 완전히 프로비전되기 전에 반환하는 제한 `New-AzDedicatedHsm` 사항이 있습니다.</span><span class="sxs-lookup"><span data-stu-id="3950c-110">**NOTE:** Currently `New-AzDedicatedHsm` has a limitation that it returns before the HSM is fully provisioned on Azure.</span></span>
<span data-ttu-id="3950c-111">따라서 새 HSM을 만들고 나면 해당 상태를 쿼리하고 사용 전에 해당 상태를 `Get-AzDedicatedHsm` `Provisioning State` `Succeeded` 확인하시기 바랍니다.</span><span class="sxs-lookup"><span data-stu-id="3950c-111">Therefore after creating a new HSM, please query its state by `Get-AzDedicatedHsm` and make sure its `Provisioning State` is `Succeeded` before using it.</span></span>

## <span data-ttu-id="3950c-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="3950c-112">PARAMETERS</span></span>

### <span data-ttu-id="3950c-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="3950c-113">-AsJob</span></span>
<span data-ttu-id="3950c-114">작업으로 명령 실행</span><span class="sxs-lookup"><span data-stu-id="3950c-114">Run the command as a job</span></span>

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

### <span data-ttu-id="3950c-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3950c-115">-DefaultProfile</span></span>
<span data-ttu-id="3950c-116">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="3950c-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3950c-117">-Location</span><span class="sxs-lookup"><span data-stu-id="3950c-117">-Location</span></span>
<span data-ttu-id="3950c-118">전용 HSM을 만들어야 하는 지원되는 Azure 위치입니다.</span><span class="sxs-lookup"><span data-stu-id="3950c-118">The supported Azure location where the dedicated HSM should be created.</span></span>

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

### <span data-ttu-id="3950c-119">-Name</span><span class="sxs-lookup"><span data-stu-id="3950c-119">-Name</span></span>
<span data-ttu-id="3950c-120">전용 Hsm의 이름</span><span class="sxs-lookup"><span data-stu-id="3950c-120">Name of the dedicated Hsm</span></span>

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

### <span data-ttu-id="3950c-121">-NetworkInterface</span><span class="sxs-lookup"><span data-stu-id="3950c-121">-NetworkInterface</span></span>
<span data-ttu-id="3950c-122">전용 HSM과 연결된 네트워크 인터페이스에 대한 리소스 ID 목록을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="3950c-122">Specifies the list of resource Ids for the network interfaces associated with the dedicated HSM.</span></span>
<span data-ttu-id="3950c-123">생성을 위해 NETWORKINTERFACE 속성에 대한 NOTES 섹션을 참조하고 해시 테이블을 만드십시오.</span><span class="sxs-lookup"><span data-stu-id="3950c-123">To construct, see NOTES section for NETWORKINTERFACE properties and create a hash table.</span></span>

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

### <span data-ttu-id="3950c-124">-NoWait</span><span class="sxs-lookup"><span data-stu-id="3950c-124">-NoWait</span></span>
<span data-ttu-id="3950c-125">명령을 비동기적으로 실행</span><span class="sxs-lookup"><span data-stu-id="3950c-125">Run the command asynchronously</span></span>

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

### <span data-ttu-id="3950c-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3950c-126">-ResourceGroupName</span></span>
<span data-ttu-id="3950c-127">리소스가 속한 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="3950c-127">The name of the Resource Group to which the resource belongs.</span></span>

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

### <span data-ttu-id="3950c-128">-Sku</span><span class="sxs-lookup"><span data-stu-id="3950c-128">-Sku</span></span>
<span data-ttu-id="3950c-129">전용 HSM의 SKU</span><span class="sxs-lookup"><span data-stu-id="3950c-129">SKU of the dedicated HSM</span></span>

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

### <span data-ttu-id="3950c-130">-StampId</span><span class="sxs-lookup"><span data-stu-id="3950c-130">-StampId</span></span>
<span data-ttu-id="3950c-131">이 필드는 RP가 가용성 영역이 지원되지 않는 경우에 사용됩니다.</span><span class="sxs-lookup"><span data-stu-id="3950c-131">This field will be used when RP does not support Availability zones.</span></span>

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

### <span data-ttu-id="3950c-132">-SubnetId</span><span class="sxs-lookup"><span data-stu-id="3950c-132">-SubnetId</span></span>
<span data-ttu-id="3950c-133">리소스 ARM /subscriptions/{SubscriptionId}/resourceGroups/{ResourceGroupName}/...</span><span class="sxs-lookup"><span data-stu-id="3950c-133">The ARM resource id in the form of /subscriptions/{SubscriptionId}/resourceGroups/{ResourceGroupName}/...</span></span>

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

### <span data-ttu-id="3950c-134">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="3950c-134">-SubscriptionId</span></span>
<span data-ttu-id="3950c-135">Microsoft Azure 구독을 고유하게 식별하는 구독 자격 증명입니다.</span><span class="sxs-lookup"><span data-stu-id="3950c-135">Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="3950c-136">구독 ID는 모든 서비스 호출에 대한 URI의 일부를 형성합니다.</span><span class="sxs-lookup"><span data-stu-id="3950c-136">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="3950c-137">-Tag</span><span class="sxs-lookup"><span data-stu-id="3950c-137">-Tag</span></span>
<span data-ttu-id="3950c-138">리소스 태그</span><span class="sxs-lookup"><span data-stu-id="3950c-138">Resource tags</span></span>

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

### <span data-ttu-id="3950c-139">-Zone</span><span class="sxs-lookup"><span data-stu-id="3950c-139">-Zone</span></span>
<span data-ttu-id="3950c-140">전용 Hsm 영역.</span><span class="sxs-lookup"><span data-stu-id="3950c-140">The Dedicated Hsm zones.</span></span>

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

### <span data-ttu-id="3950c-141">-Confirm</span><span class="sxs-lookup"><span data-stu-id="3950c-141">-Confirm</span></span>
<span data-ttu-id="3950c-142">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="3950c-142">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3950c-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3950c-143">-WhatIf</span></span>
<span data-ttu-id="3950c-144">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="3950c-144">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3950c-145">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="3950c-145">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3950c-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3950c-146">CommonParameters</span></span>
<span data-ttu-id="3950c-147">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="3950c-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3950c-148">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="3950c-148">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3950c-149">입력</span><span class="sxs-lookup"><span data-stu-id="3950c-149">INPUTS</span></span>

## <span data-ttu-id="3950c-150">출력</span><span class="sxs-lookup"><span data-stu-id="3950c-150">OUTPUTS</span></span>

### <span data-ttu-id="3950c-151">Microsoft.Azure.PowerShell.Cmdlets.DedicatedHsm.Models.Api20181031.IDedicatedHsm</span><span class="sxs-lookup"><span data-stu-id="3950c-151">Microsoft.Azure.PowerShell.Cmdlets.DedicatedHsm.Models.Api20181031.IDedicatedHsm</span></span>

## <span data-ttu-id="3950c-152">참고 사항</span><span class="sxs-lookup"><span data-stu-id="3950c-152">NOTES</span></span>

<span data-ttu-id="3950c-153">별칭</span><span class="sxs-lookup"><span data-stu-id="3950c-153">ALIASES</span></span>

<span data-ttu-id="3950c-154">복합 매개 변수 속성</span><span class="sxs-lookup"><span data-stu-id="3950c-154">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="3950c-155">아래에 설명된 매개 변수를 만들 수 있도록 적절한 속성을 포함하는 해시 테이블을 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="3950c-155">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="3950c-156">해시 테이블에 대한 자세한 내용은 다음 Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="3950c-156">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="3950c-157">NETWORKINTERFACE <INetworkInterface[]>: 전용 HSM과 연결된 네트워크 인터페이스에 대한 리소스 ID 목록을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="3950c-157">NETWORKINTERFACE <INetworkInterface[]>: Specifies the list of resource Ids for the network interfaces associated with the dedicated HSM.</span></span>
  - <span data-ttu-id="3950c-158">`[PrivateIPAddress <String>]`: 인터페이스의 개인 IP 주소</span><span class="sxs-lookup"><span data-stu-id="3950c-158">`[PrivateIPAddress <String>]`: Private Ip address of the interface</span></span>

## <span data-ttu-id="3950c-159">관련 링크</span><span class="sxs-lookup"><span data-stu-id="3950c-159">RELATED LINKS</span></span>

