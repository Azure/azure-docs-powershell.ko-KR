---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/new-azrecoveryservicesasrvmnicconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/New-AzRecoveryServicesAsrVMNicConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/New-AzRecoveryServicesAsrVMNicConfig.md
ms.openlocfilehash: 658a0cfa66abd71a63edc67ab2615713ac815bcd
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98492451"
---
# <span data-ttu-id="3c14c-101">New-AzRecoveryServicesAsrVMNicConfig</span><span class="sxs-lookup"><span data-stu-id="3c14c-101">New-AzRecoveryServicesAsrVMNicConfig</span></span>

## <span data-ttu-id="3c14c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3c14c-102">SYNOPSIS</span></span>
<span data-ttu-id="3c14c-103">장애 조치(failover) 및 테스트 장애 조치(failover) 관련 구성 세부 정보를 포함하는 ASR NIC 구성을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="3c14c-103">Creates an ASR NIC config that contains the failover and test failover related configuration details.</span></span>

## <span data-ttu-id="3c14c-104">구문</span><span class="sxs-lookup"><span data-stu-id="3c14c-104">SYNTAX</span></span>

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

## <span data-ttu-id="3c14c-105">설명</span><span class="sxs-lookup"><span data-stu-id="3c14c-105">DESCRIPTION</span></span>
<span data-ttu-id="3c14c-106">**New-AzRecoveryServicesAsrVMNicConfig** cmdlet은 장애 조치(failover) 및 테스트 장애 조치 관련 세부 정보를 포함하는 ASR NIC 구성 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="3c14c-106">The **New-AzRecoveryServicesAsrVMNicConfig** cmdlet creates an ASR NIC config object that contains the failover and test failover related details.</span></span> <span data-ttu-id="3c14c-107">정보가 전달되지 않은 경우 이러한 값이 null로 업데이트되지 않도록 복제 보호 항목에서 해당 값을 선택해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="3c14c-107">In case any information is not passed, the corresponding values are picked from the replication protected item to avoid these values being updated to null.</span></span>

## <span data-ttu-id="3c14c-108">예제</span><span class="sxs-lookup"><span data-stu-id="3c14c-108">EXAMPLES</span></span>

### <span data-ttu-id="3c14c-109">예제 1</span><span class="sxs-lookup"><span data-stu-id="3c14c-109">Example 1</span></span>
```powershell
PS C:\> $nicConfig = New-AzRecoveryServicesAsrVMNicConfig -NicId $AsrNicGuid -ReplicationProtectedItem $Rpi -RecoveryVMNetworkId $recoveryNetworkId -RecoveryVMSubnetName $recoverySubnetName -RecoveryNicStaticIPAddress "10.0.0.1" `
    -TfoVMNetworkId $tfoNetworkId -TfoVMSubnetName $tfoSubnetName -TfoNicStaticIPAddress "10.0.1.1"
```

<span data-ttu-id="3c14c-110">NIC에 대해 구성된 장애 조치(failover) 및 테스트 페이오버 네트워킹 설정을 사용하여 ASRVmNicConfig 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="3c14c-110">Creates an ASRVmNicConfig object with the failover and test faiover networking settings configured for the NIC.</span></span> <span data-ttu-id="3c14c-111">위에서 전달되지 않은 속성은 전달된 보호된 항목에서 페치됩니다.</span><span class="sxs-lookup"><span data-stu-id="3c14c-111">Any property that's not passed above is fetched from the protected item passed.</span></span>

### <span data-ttu-id="3c14c-112">예제 2</span><span class="sxs-lookup"><span data-stu-id="3c14c-112">Example 2</span></span>
```powershell
PS C:\> $nicConfig = New-AzRecoveryServicesAsrVMNicConfig -NicId $AsrNicGuid -ReplicationProtectedItem $Rpi -TfoNicName $TfoNicName -TfoNicResourceGroupName $TfoNicRgName -TfoReuseExistingNic
```

<span data-ttu-id="3c14c-113">NIC 이름 변경에 대해 구성된 테스트 페이오버 네트워킹 설정을 사용하여 ASRVmNicConfig 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="3c14c-113">Creates an ASRVmNicConfig object with the test faiover networking settings configured for the NIC renaming.</span></span> <span data-ttu-id="3c14c-114">위에서 전달되지 않은 속성은 전달된 보호된 항목에서 페치됩니다.</span><span class="sxs-lookup"><span data-stu-id="3c14c-114">Any property that's not passed above is fetched from the protected item passed.</span></span>


### <span data-ttu-id="3c14c-115">예제 3</span><span class="sxs-lookup"><span data-stu-id="3c14c-115">Example 3</span></span>

<span data-ttu-id="3c14c-116">장애 조치(failover) 및 테스트 장애 조치(failover) 관련 구성 세부 정보를 포함하는 ASR NIC 구성을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="3c14c-116">Creates an ASR NIC config that contains the failover and test failover related configuration details.</span></span> <span data-ttu-id="3c14c-117">(자동Generated)</span><span class="sxs-lookup"><span data-stu-id="3c14c-117">(autogenerated)</span></span>

```powershell
<!-- Aladdin Generated Example --> 
New-AzRecoveryServicesAsrVMNicConfig -NicId $AsrNicGuid -RecoveryNetworkSecurityGroupId <String> -RecoveryNicStaticIPAddress '10.0.0.1' -RecoveryVMNetworkId $recoveryNetworkId -RecoveryVMSubnetName $recoverySubnetName -ReplicationProtectedItem $Rpi -TfoNetworkSecurityGroupId <String> -TfoNicStaticIPAddress <String> -TfoVMNetworkId <String> -TfoVMSubnetName <String>
```

## <span data-ttu-id="3c14c-118">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="3c14c-118">PARAMETERS</span></span>

### <span data-ttu-id="3c14c-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3c14c-119">-DefaultProfile</span></span>
<span data-ttu-id="3c14c-120">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="3c14c-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3c14c-121">-EnableAcceleratedNetworkingOnRecovery</span><span class="sxs-lookup"><span data-stu-id="3c14c-121">-EnableAcceleratedNetworkingOnRecovery</span></span>
<span data-ttu-id="3c14c-122">복구 NIC에서 가속 네트워킹을 사용할지 여부를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="3c14c-122">Specifies whether accelerated networking is enabled on recovery NIC.</span></span>

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

### <span data-ttu-id="3c14c-123">-EnableAcceleratedNetworkingOnTfo</span><span class="sxs-lookup"><span data-stu-id="3c14c-123">-EnableAcceleratedNetworkingOnTfo</span></span>
<span data-ttu-id="3c14c-124">테스트 장애 조치(failover) NIC에서 가속화된 네트워킹을 사용할지 여부를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="3c14c-124">Specifies whether accelerated networking is enabled on test failover NIC.</span></span>

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

### <span data-ttu-id="3c14c-125">-NicId</span><span class="sxs-lookup"><span data-stu-id="3c14c-125">-NicId</span></span>
<span data-ttu-id="3c14c-126">ASR NIC GUID를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="3c14c-126">Specify the ASR NIC GUID.</span></span>

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

### <span data-ttu-id="3c14c-127">-RecoveryLBBackendAddressPoolId</span><span class="sxs-lookup"><span data-stu-id="3c14c-127">-RecoveryLBBackendAddressPoolId</span></span>
<span data-ttu-id="3c14c-128">복구 NIC에 대한 백드 주소 풀의 ID를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="3c14c-128">Specifies the IDs of backend address pools for the recovery NIC.</span></span>

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

### <span data-ttu-id="3c14c-129">-RecoveryNetworkSecurityGroupId</span><span class="sxs-lookup"><span data-stu-id="3c14c-129">-RecoveryNetworkSecurityGroupId</span></span>
<span data-ttu-id="3c14c-130">복구 NIC와 연결된 NSG의 ID를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="3c14c-130">Specifies the ID of the NSG associated with recovery NIC.</span></span>

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

### <span data-ttu-id="3c14c-131">-RecoveryNicName</span><span class="sxs-lookup"><span data-stu-id="3c14c-131">-RecoveryNicName</span></span>
<span data-ttu-id="3c14c-132">복구 NIC의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="3c14c-132">Specifies the name of the recovery NIC.</span></span>

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

### <span data-ttu-id="3c14c-133">-RecoveryNicResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3c14c-133">-RecoveryNicResourceGroupName</span></span>
<span data-ttu-id="3c14c-134">복구 NIC 리소스 그룹의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="3c14c-134">Specifies the name of the recovery NIC resource group.</span></span>

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

### <span data-ttu-id="3c14c-135">-RecoveryNicStaticIPAddress</span><span class="sxs-lookup"><span data-stu-id="3c14c-135">-RecoveryNicStaticIPAddress</span></span>
<span data-ttu-id="3c14c-136">복구 NIC의 IP 주소를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="3c14c-136">Specifies the IP address of the recovery NIC.</span></span>

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

### <span data-ttu-id="3c14c-137">-RecoveryPublicIPAddressId</span><span class="sxs-lookup"><span data-stu-id="3c14c-137">-RecoveryPublicIPAddressId</span></span>
<span data-ttu-id="3c14c-138">복구 NIC와 연결된 공용 IP 주소의 ID를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="3c14c-138">Specifies the ID of the public IP address associated with recovery NIC.</span></span>

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

### <span data-ttu-id="3c14c-139">-RecoveryVMNetworkId</span><span class="sxs-lookup"><span data-stu-id="3c14c-139">-RecoveryVMNetworkId</span></span>
<span data-ttu-id="3c14c-140">복구 가상 네트워크의 ID를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="3c14c-140">Specifies the ID of the recovery virtual network.</span></span>

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

### <span data-ttu-id="3c14c-141">-RecoveryVMSubnetName</span><span class="sxs-lookup"><span data-stu-id="3c14c-141">-RecoveryVMSubnetName</span></span>
<span data-ttu-id="3c14c-142">복구 서브넷의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="3c14c-142">Specifies the name of the recovery subnet.</span></span>

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

### <span data-ttu-id="3c14c-143">-ReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="3c14c-143">-ReplicationProtectedItem</span></span>
<span data-ttu-id="3c14c-144">ASR 복제 보호 항목을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="3c14c-144">Specify the ASR Replication Protected Item.</span></span>

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

### <span data-ttu-id="3c14c-145">-ReuseExistingNic</span><span class="sxs-lookup"><span data-stu-id="3c14c-145">-ReuseExistingNic</span></span>
<span data-ttu-id="3c14c-146">장애 조치(failover) 중에 기존 NIC를 사용할 수 있는지 여부를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="3c14c-146">Specifies whether an existing NIC can be used during failover.</span></span>

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

### <span data-ttu-id="3c14c-147">-TfoLBBackendAddressPoolId</span><span class="sxs-lookup"><span data-stu-id="3c14c-147">-TfoLBBackendAddressPoolId</span></span>
<span data-ttu-id="3c14c-148">복구 NIC에 대한 백드 주소 풀의 ID를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="3c14c-148">Specifies the IDs of backend address pools for the recovery NIC.</span></span>

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

### <span data-ttu-id="3c14c-149">-TfoNetworkSecurityGroupId</span><span class="sxs-lookup"><span data-stu-id="3c14c-149">-TfoNetworkSecurityGroupId</span></span>
<span data-ttu-id="3c14c-150">테스트 장애 조치(failover) NIC와 연결된 NSG의 ID를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="3c14c-150">Specifies the ID of the NSG associated with test failover NIC.</span></span>

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

### <span data-ttu-id="3c14c-151">-TfoNicName</span><span class="sxs-lookup"><span data-stu-id="3c14c-151">-TfoNicName</span></span>
<span data-ttu-id="3c14c-152">테스트 장애 조치(failover) NIC의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="3c14c-152">Specifies the name of the test failover NIC.</span></span>

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

### <span data-ttu-id="3c14c-153">-TfoNicResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3c14c-153">-TfoNicResourceGroupName</span></span>
<span data-ttu-id="3c14c-154">테스트 장애 조치(failover) NIC 리소스 그룹의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="3c14c-154">Specifies the name of the test failover NIC resource group.</span></span>

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

### <span data-ttu-id="3c14c-155">-TfoNicStaticIPAddress</span><span class="sxs-lookup"><span data-stu-id="3c14c-155">-TfoNicStaticIPAddress</span></span>
<span data-ttu-id="3c14c-156">테스트 장애 조치(failover) NIC의 IP 주소를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="3c14c-156">Specifies the IP address of the test failover NIC.</span></span>

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

### <span data-ttu-id="3c14c-157">-TfoPublicIPAddressId</span><span class="sxs-lookup"><span data-stu-id="3c14c-157">-TfoPublicIPAddressId</span></span>
<span data-ttu-id="3c14c-158">테스트 장애 조치(failover) NIC와 연결된 공용 IP 주소의 ID를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="3c14c-158">Specifies the ID of the public IP address associated with test failover NIC.</span></span>

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

### <span data-ttu-id="3c14c-159">-TfoReuseExistingNic</span><span class="sxs-lookup"><span data-stu-id="3c14c-159">-TfoReuseExistingNic</span></span>
<span data-ttu-id="3c14c-160">테스트 장애 조치(failover) 중에 기존 NIC를 사용할 수 있는지 여부를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="3c14c-160">Specifies whether an existing NIC can be used during test failover.</span></span>

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

### <span data-ttu-id="3c14c-161">-TfoVMNetworkId</span><span class="sxs-lookup"><span data-stu-id="3c14c-161">-TfoVMNetworkId</span></span>
<span data-ttu-id="3c14c-162">테스트 장애 조치(failover) 가상 네트워크의 ID를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="3c14c-162">Specifies the ID of the test failover virtual network.</span></span>

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

### <span data-ttu-id="3c14c-163">-TfoVMSubnetName</span><span class="sxs-lookup"><span data-stu-id="3c14c-163">-TfoVMSubnetName</span></span>
<span data-ttu-id="3c14c-164">테스트 장애 조치 서브넷의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="3c14c-164">Specifies the name of the test failover subnet.</span></span>

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

### <span data-ttu-id="3c14c-165">-Confirm</span><span class="sxs-lookup"><span data-stu-id="3c14c-165">-Confirm</span></span>
<span data-ttu-id="3c14c-166">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="3c14c-166">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3c14c-167">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3c14c-167">-WhatIf</span></span>
<span data-ttu-id="3c14c-168">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="3c14c-168">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="3c14c-169">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="3c14c-169">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3c14c-170">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3c14c-170">CommonParameters</span></span>
<span data-ttu-id="3c14c-171">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="3c14c-171">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3c14c-172">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="3c14c-172">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3c14c-173">입력</span><span class="sxs-lookup"><span data-stu-id="3c14c-173">INPUTS</span></span>

### <span data-ttu-id="3c14c-174">없음</span><span class="sxs-lookup"><span data-stu-id="3c14c-174">None</span></span>

## <span data-ttu-id="3c14c-175">출력</span><span class="sxs-lookup"><span data-stu-id="3c14c-175">OUTPUTS</span></span>

### <span data-ttu-id="3c14c-176">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRVMNicConfig</span><span class="sxs-lookup"><span data-stu-id="3c14c-176">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRVMNicConfig</span></span>

## <span data-ttu-id="3c14c-177">참고 사항</span><span class="sxs-lookup"><span data-stu-id="3c14c-177">NOTES</span></span>

## <span data-ttu-id="3c14c-178">관련 링크</span><span class="sxs-lookup"><span data-stu-id="3c14c-178">RELATED LINKS</span></span>
