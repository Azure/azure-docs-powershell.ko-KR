---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: AzureRM.RecoveryServices.SiteRecovery
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.siterecovery/set-azurermrecoveryservicesasrreplicationprotecteditem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Set-AzureRmRecoveryServicesAsrReplicationProtectedItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Set-AzureRmRecoveryServicesAsrReplicationProtectedItem.md
ms.openlocfilehash: a3ae73e9831202418d35481270a1d04b1cb09a59
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93529761"
---
# <span data-ttu-id="72de4-101">Set-AzureRmRecoveryServicesAsrReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="72de4-101">Set-AzureRmRecoveryServicesAsrReplicationProtectedItem</span></span>

## <span data-ttu-id="72de4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="72de4-102">SYNOPSIS</span></span>
<span data-ttu-id="72de4-103">지정 된 복제 보호 항목에 대 한 대상 네트워크 및 가상 컴퓨터 크기와 같은 복구 속성을 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="72de4-103">Sets recovery properties such as target network and virtual machine size for the specified replication protected item.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="72de4-104">구문과</span><span class="sxs-lookup"><span data-stu-id="72de4-104">SYNTAX</span></span>

```
Set-AzureRmRecoveryServicesAsrReplicationProtectedItem -InputObject <ASRReplicationProtectedItem>
 [-Name <String>] [-Size <String>] [-PrimaryNic <String>] [-RecoveryNetworkId <String>]
 [-RecoveryCloudServiceId <String>] [-RecoveryNicSubnetName <String>] [-RecoveryNicStaticIPAddress <String>]
 [-NicSelectionType <String>] [-RecoveryResourceGroupId <String>] [-LicenseType <String>]
 [-RecoveryAvailabilitySet <String>] [-UseManagedDisk <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="72de4-105">설명은</span><span class="sxs-lookup"><span data-stu-id="72de4-105">DESCRIPTION</span></span>
<span data-ttu-id="72de4-106">**AzureRmRecoveryServicesAsrReplicationProtectedItem** Cmdlet은 복제 보호 항목에 대 한 복구 속성을 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="72de4-106">The **Set-AzureRmRecoveryServicesAsrReplicationProtectedItem** cmdlet sets the recovery properties for a Replication Protected Item.</span></span>

## <span data-ttu-id="72de4-107">예제의</span><span class="sxs-lookup"><span data-stu-id="72de4-107">EXAMPLES</span></span>

### <span data-ttu-id="72de4-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="72de4-108">Example 1</span></span>
```
PS C:\> $currentJob = Set-AzureRmRecoveryServicesAsrReplicationProtectedItem -ReplicationProtectedItem $RPI -PrimaryNic $NicId -RecoveryNetworkId $AzureNetworkID -RecoveryNicSubnetName $subnetName
```

<span data-ttu-id="72de4-109">지정 된 매개 변수를 사용 하 여 복제 보호 항목 설정의 업데이트 작업을 시작 하 고 작업을 추적 하는 데 사용 되는 ASR 작업을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="72de4-109">Starts the operation of updating the replication protect item settings using the specified parameters and returns the ASR job used to track the operation.</span></span>

## <span data-ttu-id="72de4-110">변수</span><span class="sxs-lookup"><span data-stu-id="72de4-110">PARAMETERS</span></span>

### <span data-ttu-id="72de4-111">-확인</span><span class="sxs-lookup"><span data-stu-id="72de4-111">-Confirm</span></span>
<span data-ttu-id="72de4-112">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="72de4-112">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="72de4-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="72de4-113">-DefaultProfile</span></span>
<span data-ttu-id="72de4-114">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="72de4-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>
```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="72de4-115">-InputObject</span><span class="sxs-lookup"><span data-stu-id="72de4-115">-InputObject</span></span>
<span data-ttu-id="72de4-116">Cmdlet에 대 한 입력 개체: 업데이트할 복제 보호 항목에 해당 하는 ASR 복제 보호 항목 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="72de4-116">The input object to the cmdlet: The ASR replication protected item object corresponding to the replication protected item to update.</span></span>

```yaml
Type: ASRReplicationProtectedItem
Parameter Sets: (All)
Aliases: ReplicationProtectedItem

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="72de4-117">-LicenseType</span><span class="sxs-lookup"><span data-stu-id="72de4-117">-LicenseType</span></span>
<span data-ttu-id="72de4-118">Windows Server 가상 컴퓨터에 사용할 라이선스 유형 선택 항목을 입력 합니다.</span><span class="sxs-lookup"><span data-stu-id="72de4-118">Specifiy the license type selection to be used for Windows Server virtual machines.</span></span> <span data-ttu-id="72de4-119">마이그레이션에 대 한 Azure 하이브리드 사용 혜택 (허브)을 사용할 자격이 있는 경우이 보호 항목을 장애 조치 하는 동안 허브 설정을 사용 하도록 지정 하는 경우 라이선스 유형을 WindowsServer로 설정 하는 것이 좋습니다.</span><span class="sxs-lookup"><span data-stu-id="72de4-119">If you are entitled to use the Azure Hybrid Use Benefit (HUB) for migrations and would like to specify that the HUB setting be used while failing over this protected item set the license type to be WindowsServer.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:
Accepted values: NoLicenseType, WindowsServer

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="72de4-120">-이름</span><span class="sxs-lookup"><span data-stu-id="72de4-120">-Name</span></span>
<span data-ttu-id="72de4-121">장애 조치에 생성 되는 복구 가상 컴퓨터의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="72de4-121">Specifies the name of the recovery virtual machine that will be created on failover.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="72de4-122">-NicSelectionType</span><span class="sxs-lookup"><span data-stu-id="72de4-122">-NicSelectionType</span></span>
<span data-ttu-id="72de4-123">사용자가 설정 하거나 기본적으로 설정 되는 NIC (네트워크 인터페이스 카드) 속성을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="72de4-123">Specifies the network interface card (NIC) properties set by user or set by default.</span></span>
<span data-ttu-id="72de4-124">NotSelected를 지정 하 여 기본 값으로 돌아갈 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="72de4-124">You can specify NotSelected to go back to the default values.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:
Accepted values: NotSelected, SelectedByUser

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="72de4-125">-PrimaryNic</span><span class="sxs-lookup"><span data-stu-id="72de4-125">-PrimaryNic</span></span>
<span data-ttu-id="72de4-126">이 cmdlet이 복구 네트워크 속성을 설정 하는 가상 컴퓨터의 NIC를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="72de4-126">Specifies the NIC of the virtual machine for which this cmdlet sets the recovery network property.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="72de4-127">-RecoveryAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="72de4-127">-RecoveryAvailabilitySet</span></span>
<span data-ttu-id="72de4-128">장애 조치 (failover) 후 복제 보호 항목에 대 한 가용성 집합입니다.</span><span class="sxs-lookup"><span data-stu-id="72de4-128">Availability set for replication protected item after failover.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="72de4-129">-RecoveryCloudServiceId</span><span class="sxs-lookup"><span data-stu-id="72de4-129">-RecoveryCloudServiceId</span></span>
<span data-ttu-id="72de4-130">이 가상 컴퓨터를 장애 조치 (failover) 할 복구 클라우드 서비스의 리소스 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="72de4-130">The resource ID of the recovery cloud service to failover this virtual machine to.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="72de4-131">-RecoveryNetworkId</span><span class="sxs-lookup"><span data-stu-id="72de4-131">-RecoveryNetworkId</span></span>
<span data-ttu-id="72de4-132">보호 된 항목을 장애 조치 해야 하는 Azure 가상 네트워크의 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="72de4-132">Specifies the ID of the Azure virtual network to which the protected item should be failed over.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="72de4-133">-RecoveryNicStaticIPAddress</span><span class="sxs-lookup"><span data-stu-id="72de4-133">-RecoveryNicStaticIPAddress</span></span>
<span data-ttu-id="72de4-134">복구 시 기본 NIC에 할당 해야 하는 고정 IP 주소를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="72de4-134">Specifies the static IP address that should be assigned to primary NIC on recovery.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="72de4-135">-RecoveryNicSubnetName</span><span class="sxs-lookup"><span data-stu-id="72de4-135">-RecoveryNicSubnetName</span></span>
<span data-ttu-id="72de4-136">보호 된 항목의이 NIC가 장애 조치 (failover)에 연결 되어야 하는 복구 Azure 가상 네트워크의 서브넷 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="72de4-136">Specifies the name of the subnet on the recovery Azure virtual network to which this NIC of the protected item should be connected to on failover.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="72de4-137">-RecoveryResourceGroupId</span><span class="sxs-lookup"><span data-stu-id="72de4-137">-RecoveryResourceGroupId</span></span>
<span data-ttu-id="72de4-138">장애 조치 시 보호 되는 항목이 복구 되는 복구 영역에 있는 Azure 리소스 그룹의 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="72de4-138">The ID of the Azure resource group in the recovery region in which the protected item will be recovered on failover.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="72de4-139">-크기</span><span class="sxs-lookup"><span data-stu-id="72de4-139">-Size</span></span>
<span data-ttu-id="72de4-140">복구 가상 컴퓨터 크기를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="72de4-140">Specifies the recovery virtual machine size.</span></span>
<span data-ttu-id="72de4-141">값은 Azure 가상 머신에서 지원 되는 크기 집합에서 지정 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="72de4-141">The value should be from the set of sizes supported by Azure virtual machines.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="72de4-142">-UseManagedDisk</span><span class="sxs-lookup"><span data-stu-id="72de4-142">-UseManagedDisk</span></span>
<span data-ttu-id="72de4-143">장애 조치에 만든 Azure 가상 컴퓨터에서 관리 디스크를 사용 해야 하는지 여부를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="72de4-143">Specifies if the Azure virtual machine that is created on failover should use managed disks.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:
Accepted values: True, False

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="72de4-144">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="72de4-144">-WhatIf</span></span>
<span data-ttu-id="72de4-145">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="72de4-145">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="72de4-146">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="72de4-146">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="72de4-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="72de4-147">CommonParameters</span></span>
<span data-ttu-id="72de4-148">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="72de4-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="72de4-149">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="72de4-149">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="72de4-150">입력</span><span class="sxs-lookup"><span data-stu-id="72de4-150">INPUTS</span></span>

### <span data-ttu-id="72de4-151">SiteRecovery. ASRReplicationProtectedItem에 대 한 서비스</span><span class="sxs-lookup"><span data-stu-id="72de4-151">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRReplicationProtectedItem</span></span>

## <span data-ttu-id="72de4-152">출력</span><span class="sxs-lookup"><span data-stu-id="72de4-152">OUTPUTS</span></span>

### <span data-ttu-id="72de4-153">SiteRecovery. r i m m 작업</span><span class="sxs-lookup"><span data-stu-id="72de4-153">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="72de4-154">상속자</span><span class="sxs-lookup"><span data-stu-id="72de4-154">NOTES</span></span>

## <span data-ttu-id="72de4-155">관련 링크</span><span class="sxs-lookup"><span data-stu-id="72de4-155">RELATED LINKS</span></span>

[<span data-ttu-id="72de4-156">Get-AzureRmRecoveryServicesAsrReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="72de4-156">Get-AzureRmRecoveryServicesAsrReplicationProtectedItem</span></span>](./Get-AzureRmRecoveryServicesAsrReplicationProtectedItem.md)

[<span data-ttu-id="72de4-157">새로운 AzureRmRecoveryServicesAsrReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="72de4-157">New-AzureRmRecoveryServicesAsrReplicationProtectedItem</span></span>](./New-AzureRmRecoveryServicesAsrReplicationProtectedItem.md)

[<span data-ttu-id="72de4-158">제거-AzureRmRecoveryServicesAsrReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="72de4-158">Remove-AzureRmRecoveryServicesAsrReplicationProtectedItem</span></span>](./Remove-AzureRmRecoveryServicesAsrReplicationProtectedItem.md)
