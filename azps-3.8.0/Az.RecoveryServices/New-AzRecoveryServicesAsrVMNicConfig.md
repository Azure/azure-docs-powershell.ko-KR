---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/new-azrecoveryservicesasrvmnicconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/New-AzRecoveryServicesAsrVMNicConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/New-AzRecoveryServicesAsrVMNicConfig.md
ms.openlocfilehash: f7b6cd7171b6f50ed0f239e733ca98f0ecd5c05a
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94042686"
---
# <span data-ttu-id="26c32-101">New-AzRecoveryServicesAsrVMNicConfig</span><span class="sxs-lookup"><span data-stu-id="26c32-101">New-AzRecoveryServicesAsrVMNicConfig</span></span>

## <span data-ttu-id="26c32-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="26c32-102">SYNOPSIS</span></span>
<span data-ttu-id="26c32-103">장애 조치 및 테스트 장애 조치 관련 구성 세부 정보를 포함 하는 ASR NIC 구성을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="26c32-103">Creates an ASR NIC config that contains the failover and test failover related configuration details.</span></span>

## <span data-ttu-id="26c32-104">구문과</span><span class="sxs-lookup"><span data-stu-id="26c32-104">SYNTAX</span></span>

```
New-AzRecoveryServicesAsrVMNicConfig -NicId <String> -ReplicationProtectedItem <ASRReplicationProtectedItem>
 [-RecoveryVMNetworkId <String>] [-RecoveryVMSubnetName <String>] [-RecoveryNetworkSecurityGroupId <String>]
 [-EnableAcceleratedNetworkingOnRecovery] [-RecoveryNicStaticIPAddress <String>]
 [-RecoveryPublicIPAddressId <String>] [-RecoveryLBBackendAddressPoolId <String[]>] [-TfoVMNetworkId <String>]
 [-TfoVMSubnetName <String>] [-TfoNetworkSecurityGroupId <String>] [-EnableAcceleratedNetworkingOnTfo]
 [-TfoNicStaticIPAddress <String>] [-TfoPublicIPAddressId <String>] [-TfoLBBackendAddressPoolId <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="26c32-105">설명은</span><span class="sxs-lookup"><span data-stu-id="26c32-105">DESCRIPTION</span></span>
<span data-ttu-id="26c32-106">**AzRecoveryServicesAsrVMNicConfig** cmdlet은 장애 조치 및 테스트 장애 조치 관련 세부 정보를 포함 하는 ASR NIC config 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="26c32-106">The **New-AzRecoveryServicesAsrVMNicConfig** cmdlet creates an ASR NIC config object that contains the failover and test failover related details.</span></span> <span data-ttu-id="26c32-107">어떠한 정보도 전달 되지 않을 경우 복제 보호 항목에서 해당 값을 선택 하 여 이러한 값이 null로 업데이트 되지 않도록 합니다.</span><span class="sxs-lookup"><span data-stu-id="26c32-107">In case any information is not passed, the corresponding values are picked from the replication protected item to avoid these values being updated to null.</span></span>

## <span data-ttu-id="26c32-108">예제의</span><span class="sxs-lookup"><span data-stu-id="26c32-108">EXAMPLES</span></span>

### <span data-ttu-id="26c32-109">예제 1</span><span class="sxs-lookup"><span data-stu-id="26c32-109">Example 1</span></span>
```powershell
PS C:\> $nicConfig = New-AzRecoveryServicesAsrVMNicConfig -NicId $AsrNicGuid -ReplicationProtectedItem $Rpi -RecoveryVMNetworkId $recoveryNetworkId -RecoveryVMSubnetName $recoverySubnetName -RecoveryNicStaticIPAddress "10.0.0.1" `
    -TfoVMNetworkId $tfoNetworkId -TfoVMSubnetName $tfoSubnetName -TfoNicStaticIPAddress "10.0.1.1"
```

<span data-ttu-id="26c32-110">NIC에 대해 구성 된 장애 조치 및 테스트 faiover 네트워킹 설정을 사용 하 여 ASRVmNicConfig 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="26c32-110">Creates an ASRVmNicConfig object with the failover and test faiover networking settings configured for the NIC.</span></span> <span data-ttu-id="26c32-111">위에서 전달 되지 않은 속성은 전달 된 보호 된 항목에서 반입 됩니다.</span><span class="sxs-lookup"><span data-stu-id="26c32-111">Any property that's not passed above is fetched from the protected item passed.</span></span>

## <span data-ttu-id="26c32-112">변수</span><span class="sxs-lookup"><span data-stu-id="26c32-112">PARAMETERS</span></span>

### <span data-ttu-id="26c32-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="26c32-113">-DefaultProfile</span></span>
<span data-ttu-id="26c32-114">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="26c32-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="26c32-115">-EnableAcceleratedNetworkingOnRecovery</span><span class="sxs-lookup"><span data-stu-id="26c32-115">-EnableAcceleratedNetworkingOnRecovery</span></span>
<span data-ttu-id="26c32-116">복구 NIC에서 가속 네트워킹을 사용할 수 있는지 여부를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="26c32-116">Specifies whether accelerated networking is enabled on recovery NIC.</span></span>

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

### <span data-ttu-id="26c32-117">-EnableAcceleratedNetworkingOnTfo</span><span class="sxs-lookup"><span data-stu-id="26c32-117">-EnableAcceleratedNetworkingOnTfo</span></span>
<span data-ttu-id="26c32-118">테스트 장애 조치 NIC에서 가속 네트워킹을 사용할 수 있는지 여부를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="26c32-118">Specifies whether accelerated networking is enabled on test failover NIC.</span></span>

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

### <span data-ttu-id="26c32-119">-NicId</span><span class="sxs-lookup"><span data-stu-id="26c32-119">-NicId</span></span>
<span data-ttu-id="26c32-120">ASR NIC GUID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="26c32-120">Specify the ASR NIC GUID.</span></span>

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

### <span data-ttu-id="26c32-121">-RecoveryLBBackendAddressPoolId</span><span class="sxs-lookup"><span data-stu-id="26c32-121">-RecoveryLBBackendAddressPoolId</span></span>
<span data-ttu-id="26c32-122">복구 NIC에 대 한 백 엔드 주소 풀의 Id를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="26c32-122">Specifies the IDs of backend address pools for the recovery NIC.</span></span>

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

### <span data-ttu-id="26c32-123">-RecoveryNetworkSecurityGroupId</span><span class="sxs-lookup"><span data-stu-id="26c32-123">-RecoveryNetworkSecurityGroupId</span></span>
<span data-ttu-id="26c32-124">복구 NIC와 연결 된 NSG의 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="26c32-124">Specifies the ID of the NSG associated with recovery NIC.</span></span>

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

### <span data-ttu-id="26c32-125">-RecoveryNicStaticIPAddress</span><span class="sxs-lookup"><span data-stu-id="26c32-125">-RecoveryNicStaticIPAddress</span></span>
<span data-ttu-id="26c32-126">복구 NIC의 IP 주소를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="26c32-126">Specifies the IP address of the recovery NIC.</span></span>

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

### <span data-ttu-id="26c32-127">-RecoveryPublicIPAddressId</span><span class="sxs-lookup"><span data-stu-id="26c32-127">-RecoveryPublicIPAddressId</span></span>
<span data-ttu-id="26c32-128">복구 NIC에 연결 된 공용 IP 주소의 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="26c32-128">Specifies the ID of the public IP address associated with recovery NIC.</span></span>

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

### <span data-ttu-id="26c32-129">-RecoveryVMNetworkId</span><span class="sxs-lookup"><span data-stu-id="26c32-129">-RecoveryVMNetworkId</span></span>
<span data-ttu-id="26c32-130">복구 가상 네트워크의 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="26c32-130">Specifies the ID of the recovery virtual network.</span></span>

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

### <span data-ttu-id="26c32-131">-RecoveryVMSubnetName</span><span class="sxs-lookup"><span data-stu-id="26c32-131">-RecoveryVMSubnetName</span></span>
<span data-ttu-id="26c32-132">복구 서브넷의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="26c32-132">Specifies the name of the recovery subnet.</span></span>

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

### <span data-ttu-id="26c32-133">-ReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="26c32-133">-ReplicationProtectedItem</span></span>
<span data-ttu-id="26c32-134">ASR 복제 보호 항목을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="26c32-134">Specify the ASR Replication Protected Item.</span></span>

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

### <span data-ttu-id="26c32-135">-TfoLBBackendAddressPoolId</span><span class="sxs-lookup"><span data-stu-id="26c32-135">-TfoLBBackendAddressPoolId</span></span>
<span data-ttu-id="26c32-136">복구 NIC에 대 한 백 엔드 주소 풀의 Id를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="26c32-136">Specifies the IDs of backend address pools for the recovery NIC.</span></span>

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

### <span data-ttu-id="26c32-137">-TfoNetworkSecurityGroupId</span><span class="sxs-lookup"><span data-stu-id="26c32-137">-TfoNetworkSecurityGroupId</span></span>
<span data-ttu-id="26c32-138">테스트 장애 조치 NIC와 연결 된 NSG의 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="26c32-138">Specifies the ID of the NSG associated with test failover NIC.</span></span>

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

### <span data-ttu-id="26c32-139">-TfoNicStaticIPAddress</span><span class="sxs-lookup"><span data-stu-id="26c32-139">-TfoNicStaticIPAddress</span></span>
<span data-ttu-id="26c32-140">테스트 장애 조치 NIC의 IP 주소를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="26c32-140">Specifies the IP address of the test failover NIC.</span></span>

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

### <span data-ttu-id="26c32-141">-TfoPublicIPAddressId</span><span class="sxs-lookup"><span data-stu-id="26c32-141">-TfoPublicIPAddressId</span></span>
<span data-ttu-id="26c32-142">테스트 장애 조치 NIC와 연결 된 공용 IP 주소의 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="26c32-142">Specifies the ID of the public IP address associated with test failover NIC.</span></span>

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

### <span data-ttu-id="26c32-143">-TfoVMNetworkId</span><span class="sxs-lookup"><span data-stu-id="26c32-143">-TfoVMNetworkId</span></span>
<span data-ttu-id="26c32-144">테스트 장애 조치 가상 네트워크의 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="26c32-144">Specifies the ID of the test failover virtual network.</span></span>

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

### <span data-ttu-id="26c32-145">-TfoVMSubnetName</span><span class="sxs-lookup"><span data-stu-id="26c32-145">-TfoVMSubnetName</span></span>
<span data-ttu-id="26c32-146">테스트 장애 조치 (failover) 서브넷의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="26c32-146">Specifies the name of the test failover subnet.</span></span>

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

### <span data-ttu-id="26c32-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="26c32-147">CommonParameters</span></span>
<span data-ttu-id="26c32-148">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="26c32-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="26c32-149">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="26c32-149">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="26c32-150">입력</span><span class="sxs-lookup"><span data-stu-id="26c32-150">INPUTS</span></span>

### <span data-ttu-id="26c32-151">않아야</span><span class="sxs-lookup"><span data-stu-id="26c32-151">None</span></span>

## <span data-ttu-id="26c32-152">출력</span><span class="sxs-lookup"><span data-stu-id="26c32-152">OUTPUTS</span></span>

### <span data-ttu-id="26c32-153">SiteRecovery. ASRVMNicConfig에 대 한 서비스</span><span class="sxs-lookup"><span data-stu-id="26c32-153">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRVMNicConfig</span></span>

## <span data-ttu-id="26c32-154">상속자</span><span class="sxs-lookup"><span data-stu-id="26c32-154">NOTES</span></span>

## <span data-ttu-id="26c32-155">관련 링크</span><span class="sxs-lookup"><span data-stu-id="26c32-155">RELATED LINKS</span></span>
