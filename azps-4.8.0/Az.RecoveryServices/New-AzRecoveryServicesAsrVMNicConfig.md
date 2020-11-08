---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/new-azrecoveryservicesasrvmnicconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/New-AzRecoveryServicesAsrVMNicConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/New-AzRecoveryServicesAsrVMNicConfig.md
ms.openlocfilehash: 658a0cfa66abd71a63edc67ab2615713ac815bcd
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94214263"
---
# <span data-ttu-id="d1e32-101">New-AzRecoveryServicesAsrVMNicConfig</span><span class="sxs-lookup"><span data-stu-id="d1e32-101">New-AzRecoveryServicesAsrVMNicConfig</span></span>

## <span data-ttu-id="d1e32-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d1e32-102">SYNOPSIS</span></span>
<span data-ttu-id="d1e32-103">장애 조치 및 테스트 장애 조치 관련 구성 세부 정보를 포함 하는 ASR NIC 구성을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="d1e32-103">Creates an ASR NIC config that contains the failover and test failover related configuration details.</span></span>

## <span data-ttu-id="d1e32-104">구문과</span><span class="sxs-lookup"><span data-stu-id="d1e32-104">SYNTAX</span></span>

```
New-AzRecoveryServicesAsrVMNicConfig -NicId <String> -ReplicationProtectedItem <ASRReplicationProtectedItem>
 [-RecoveryVMNetworkId <String>] [-RecoveryNicName <String>] [-RecoveryNicResourceGroupName <String>]
 [-ReuseExistingNic] [-RecoveryVMSubnetName <String>] [-RecoveryNetworkSecurityGroupId <String>]
 [-EnableAcceleratedNetworkingOnRecovery] [-RecoveryNicStaticIPAddress <String>]
 [-RecoveryPublicIPAddressId <String>] [-RecoveryLBBackendAddressPoolId <String[]>] [-TfoVMNetworkId <String>]
 [-TfoNicName <String>] [-TfoNicResourceGroupName <String>] [-TfoReuseExistingNic] [-TfoVMSubnetName <String>]
 [-TfoNetworkSecurityGroupId <String>] [-EnableAcceleratedNetworkingOnTfo] [-TfoNicStaticIPAddress <String>]
 [-TfoPublicIPAddressId <String>] [-TfoLBBackendAddressPoolId <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d1e32-105">설명은</span><span class="sxs-lookup"><span data-stu-id="d1e32-105">DESCRIPTION</span></span>
<span data-ttu-id="d1e32-106">**AzRecoveryServicesAsrVMNicConfig** cmdlet은 장애 조치 및 테스트 장애 조치 관련 세부 정보를 포함 하는 ASR NIC config 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="d1e32-106">The **New-AzRecoveryServicesAsrVMNicConfig** cmdlet creates an ASR NIC config object that contains the failover and test failover related details.</span></span> <span data-ttu-id="d1e32-107">어떠한 정보도 전달 되지 않을 경우 복제 보호 항목에서 해당 값을 선택 하 여 이러한 값이 null로 업데이트 되지 않도록 합니다.</span><span class="sxs-lookup"><span data-stu-id="d1e32-107">In case any information is not passed, the corresponding values are picked from the replication protected item to avoid these values being updated to null.</span></span>

## <span data-ttu-id="d1e32-108">예제의</span><span class="sxs-lookup"><span data-stu-id="d1e32-108">EXAMPLES</span></span>

### <span data-ttu-id="d1e32-109">예제 1</span><span class="sxs-lookup"><span data-stu-id="d1e32-109">Example 1</span></span>
```powershell
PS C:\> $nicConfig = New-AzRecoveryServicesAsrVMNicConfig -NicId $AsrNicGuid -ReplicationProtectedItem $Rpi -RecoveryVMNetworkId $recoveryNetworkId -RecoveryVMSubnetName $recoverySubnetName -RecoveryNicStaticIPAddress "10.0.0.1" `
    -TfoVMNetworkId $tfoNetworkId -TfoVMSubnetName $tfoSubnetName -TfoNicStaticIPAddress "10.0.1.1"
```

<span data-ttu-id="d1e32-110">NIC에 대해 구성 된 장애 조치 및 테스트 faiover 네트워킹 설정을 사용 하 여 ASRVmNicConfig 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="d1e32-110">Creates an ASRVmNicConfig object with the failover and test faiover networking settings configured for the NIC.</span></span> <span data-ttu-id="d1e32-111">위에서 전달 되지 않은 속성은 전달 된 보호 된 항목에서 반입 됩니다.</span><span class="sxs-lookup"><span data-stu-id="d1e32-111">Any property that's not passed above is fetched from the protected item passed.</span></span>

### <span data-ttu-id="d1e32-112">예제 2</span><span class="sxs-lookup"><span data-stu-id="d1e32-112">Example 2</span></span>
```powershell
PS C:\> $nicConfig = New-AzRecoveryServicesAsrVMNicConfig -NicId $AsrNicGuid -ReplicationProtectedItem $Rpi -TfoNicName $TfoNicName -TfoNicResourceGroupName $TfoNicRgName -TfoReuseExistingNic
```

<span data-ttu-id="d1e32-113">NIC 이름 바꾸기에 대해 구성 된 테스트 faiover 네트워킹 설정을 사용 하 여 ASRVmNicConfig 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="d1e32-113">Creates an ASRVmNicConfig object with the test faiover networking settings configured for the NIC renaming.</span></span> <span data-ttu-id="d1e32-114">위에서 전달 되지 않은 속성은 전달 된 보호 된 항목에서 반입 됩니다.</span><span class="sxs-lookup"><span data-stu-id="d1e32-114">Any property that's not passed above is fetched from the protected item passed.</span></span>


### <span data-ttu-id="d1e32-115">예제 3</span><span class="sxs-lookup"><span data-stu-id="d1e32-115">Example 3</span></span>

<span data-ttu-id="d1e32-116">장애 조치 및 테스트 장애 조치 관련 구성 세부 정보를 포함 하는 ASR NIC 구성을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="d1e32-116">Creates an ASR NIC config that contains the failover and test failover related configuration details.</span></span> <span data-ttu-id="d1e32-117">생성</span><span class="sxs-lookup"><span data-stu-id="d1e32-117">(autogenerated)</span></span>

```powershell
<!-- Aladdin Generated Example --> 
New-AzRecoveryServicesAsrVMNicConfig -NicId $AsrNicGuid -RecoveryNetworkSecurityGroupId <String> -RecoveryNicStaticIPAddress '10.0.0.1' -RecoveryVMNetworkId $recoveryNetworkId -RecoveryVMSubnetName $recoverySubnetName -ReplicationProtectedItem $Rpi -TfoNetworkSecurityGroupId <String> -TfoNicStaticIPAddress <String> -TfoVMNetworkId <String> -TfoVMSubnetName <String>
```

## <span data-ttu-id="d1e32-118">변수</span><span class="sxs-lookup"><span data-stu-id="d1e32-118">PARAMETERS</span></span>

### <span data-ttu-id="d1e32-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d1e32-119">-DefaultProfile</span></span>
<span data-ttu-id="d1e32-120">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="d1e32-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d1e32-121">-EnableAcceleratedNetworkingOnRecovery</span><span class="sxs-lookup"><span data-stu-id="d1e32-121">-EnableAcceleratedNetworkingOnRecovery</span></span>
<span data-ttu-id="d1e32-122">복구 NIC에서 가속 네트워킹을 사용할 수 있는지 여부를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d1e32-122">Specifies whether accelerated networking is enabled on recovery NIC.</span></span>

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

### <span data-ttu-id="d1e32-123">-EnableAcceleratedNetworkingOnTfo</span><span class="sxs-lookup"><span data-stu-id="d1e32-123">-EnableAcceleratedNetworkingOnTfo</span></span>
<span data-ttu-id="d1e32-124">테스트 장애 조치 NIC에서 가속 네트워킹을 사용할 수 있는지 여부를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d1e32-124">Specifies whether accelerated networking is enabled on test failover NIC.</span></span>

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

### <span data-ttu-id="d1e32-125">-NicId</span><span class="sxs-lookup"><span data-stu-id="d1e32-125">-NicId</span></span>
<span data-ttu-id="d1e32-126">ASR NIC GUID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d1e32-126">Specify the ASR NIC GUID.</span></span>

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

### <span data-ttu-id="d1e32-127">-RecoveryLBBackendAddressPoolId</span><span class="sxs-lookup"><span data-stu-id="d1e32-127">-RecoveryLBBackendAddressPoolId</span></span>
<span data-ttu-id="d1e32-128">복구 NIC에 대 한 백 엔드 주소 풀의 Id를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d1e32-128">Specifies the IDs of backend address pools for the recovery NIC.</span></span>

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

### <span data-ttu-id="d1e32-129">-RecoveryNetworkSecurityGroupId</span><span class="sxs-lookup"><span data-stu-id="d1e32-129">-RecoveryNetworkSecurityGroupId</span></span>
<span data-ttu-id="d1e32-130">복구 NIC와 연결 된 NSG의 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d1e32-130">Specifies the ID of the NSG associated with recovery NIC.</span></span>

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

### <span data-ttu-id="d1e32-131">-RecoveryNicName</span><span class="sxs-lookup"><span data-stu-id="d1e32-131">-RecoveryNicName</span></span>
<span data-ttu-id="d1e32-132">복구 NIC의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d1e32-132">Specifies the name of the recovery NIC.</span></span>

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

### <span data-ttu-id="d1e32-133">-RecoveryNicResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d1e32-133">-RecoveryNicResourceGroupName</span></span>
<span data-ttu-id="d1e32-134">복구 NIC 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d1e32-134">Specifies the name of the recovery NIC resource group.</span></span>

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

### <span data-ttu-id="d1e32-135">-RecoveryNicStaticIPAddress</span><span class="sxs-lookup"><span data-stu-id="d1e32-135">-RecoveryNicStaticIPAddress</span></span>
<span data-ttu-id="d1e32-136">복구 NIC의 IP 주소를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d1e32-136">Specifies the IP address of the recovery NIC.</span></span>

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

### <span data-ttu-id="d1e32-137">-RecoveryPublicIPAddressId</span><span class="sxs-lookup"><span data-stu-id="d1e32-137">-RecoveryPublicIPAddressId</span></span>
<span data-ttu-id="d1e32-138">복구 NIC에 연결 된 공용 IP 주소의 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d1e32-138">Specifies the ID of the public IP address associated with recovery NIC.</span></span>

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

### <span data-ttu-id="d1e32-139">-RecoveryVMNetworkId</span><span class="sxs-lookup"><span data-stu-id="d1e32-139">-RecoveryVMNetworkId</span></span>
<span data-ttu-id="d1e32-140">복구 가상 네트워크의 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d1e32-140">Specifies the ID of the recovery virtual network.</span></span>

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

### <span data-ttu-id="d1e32-141">-RecoveryVMSubnetName</span><span class="sxs-lookup"><span data-stu-id="d1e32-141">-RecoveryVMSubnetName</span></span>
<span data-ttu-id="d1e32-142">복구 서브넷의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d1e32-142">Specifies the name of the recovery subnet.</span></span>

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

### <span data-ttu-id="d1e32-143">-ReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="d1e32-143">-ReplicationProtectedItem</span></span>
<span data-ttu-id="d1e32-144">ASR 복제 보호 항목을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d1e32-144">Specify the ASR Replication Protected Item.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRReplicationProtectedItem
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d1e32-145">-ReuseExistingNic</span><span class="sxs-lookup"><span data-stu-id="d1e32-145">-ReuseExistingNic</span></span>
<span data-ttu-id="d1e32-146">장애 조치 중 기존 NIC를 사용할 수 있는지 여부를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d1e32-146">Specifies whether an existing NIC can be used during failover.</span></span>

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

### <span data-ttu-id="d1e32-147">-TfoLBBackendAddressPoolId</span><span class="sxs-lookup"><span data-stu-id="d1e32-147">-TfoLBBackendAddressPoolId</span></span>
<span data-ttu-id="d1e32-148">복구 NIC에 대 한 백 엔드 주소 풀의 Id를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d1e32-148">Specifies the IDs of backend address pools for the recovery NIC.</span></span>

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

### <span data-ttu-id="d1e32-149">-TfoNetworkSecurityGroupId</span><span class="sxs-lookup"><span data-stu-id="d1e32-149">-TfoNetworkSecurityGroupId</span></span>
<span data-ttu-id="d1e32-150">테스트 장애 조치 NIC와 연결 된 NSG의 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d1e32-150">Specifies the ID of the NSG associated with test failover NIC.</span></span>

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

### <span data-ttu-id="d1e32-151">-TfoNicName</span><span class="sxs-lookup"><span data-stu-id="d1e32-151">-TfoNicName</span></span>
<span data-ttu-id="d1e32-152">테스트 장애 조치 NIC의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d1e32-152">Specifies the name of the test failover NIC.</span></span>

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

### <span data-ttu-id="d1e32-153">-TfoNicResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d1e32-153">-TfoNicResourceGroupName</span></span>
<span data-ttu-id="d1e32-154">테스트 장애 조치 NIC 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d1e32-154">Specifies the name of the test failover NIC resource group.</span></span>

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

### <span data-ttu-id="d1e32-155">-TfoNicStaticIPAddress</span><span class="sxs-lookup"><span data-stu-id="d1e32-155">-TfoNicStaticIPAddress</span></span>
<span data-ttu-id="d1e32-156">테스트 장애 조치 NIC의 IP 주소를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d1e32-156">Specifies the IP address of the test failover NIC.</span></span>

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

### <span data-ttu-id="d1e32-157">-TfoPublicIPAddressId</span><span class="sxs-lookup"><span data-stu-id="d1e32-157">-TfoPublicIPAddressId</span></span>
<span data-ttu-id="d1e32-158">테스트 장애 조치 NIC와 연결 된 공용 IP 주소의 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d1e32-158">Specifies the ID of the public IP address associated with test failover NIC.</span></span>

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

### <span data-ttu-id="d1e32-159">-TfoReuseExistingNic</span><span class="sxs-lookup"><span data-stu-id="d1e32-159">-TfoReuseExistingNic</span></span>
<span data-ttu-id="d1e32-160">테스트 장애 조치 (failover) 중 기존 NIC를 사용할 수 있는지 여부를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d1e32-160">Specifies whether an existing NIC can be used during test failover.</span></span>

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

### <span data-ttu-id="d1e32-161">-TfoVMNetworkId</span><span class="sxs-lookup"><span data-stu-id="d1e32-161">-TfoVMNetworkId</span></span>
<span data-ttu-id="d1e32-162">테스트 장애 조치 가상 네트워크의 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d1e32-162">Specifies the ID of the test failover virtual network.</span></span>

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

### <span data-ttu-id="d1e32-163">-TfoVMSubnetName</span><span class="sxs-lookup"><span data-stu-id="d1e32-163">-TfoVMSubnetName</span></span>
<span data-ttu-id="d1e32-164">테스트 장애 조치 (failover) 서브넷의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d1e32-164">Specifies the name of the test failover subnet.</span></span>

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

### <span data-ttu-id="d1e32-165">-확인</span><span class="sxs-lookup"><span data-stu-id="d1e32-165">-Confirm</span></span>
<span data-ttu-id="d1e32-166">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="d1e32-166">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d1e32-167">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d1e32-167">-WhatIf</span></span>
<span data-ttu-id="d1e32-168">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="d1e32-168">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="d1e32-169">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="d1e32-169">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d1e32-170">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d1e32-170">CommonParameters</span></span>
<span data-ttu-id="d1e32-171">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="d1e32-171">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d1e32-172">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="d1e32-172">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d1e32-173">입력</span><span class="sxs-lookup"><span data-stu-id="d1e32-173">INPUTS</span></span>

### <span data-ttu-id="d1e32-174">않아야</span><span class="sxs-lookup"><span data-stu-id="d1e32-174">None</span></span>

## <span data-ttu-id="d1e32-175">출력</span><span class="sxs-lookup"><span data-stu-id="d1e32-175">OUTPUTS</span></span>

### <span data-ttu-id="d1e32-176">SiteRecovery. ASRVMNicConfig에 대 한 서비스</span><span class="sxs-lookup"><span data-stu-id="d1e32-176">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRVMNicConfig</span></span>

## <span data-ttu-id="d1e32-177">상속자</span><span class="sxs-lookup"><span data-stu-id="d1e32-177">NOTES</span></span>

## <span data-ttu-id="d1e32-178">관련 링크</span><span class="sxs-lookup"><span data-stu-id="d1e32-178">RELATED LINKS</span></span>
