---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: AzureRM.RecoveryServices.SiteRecovery
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.siterecovery/set-azurermrecoveryservicesasrreplicationprotecteditem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices.SiteRecovery/help/Set-AzureRmRecoveryServicesAsrReplicationProtectedItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices.SiteRecovery/help/Set-AzureRmRecoveryServicesAsrReplicationProtectedItem.md
ms.openlocfilehash: d387774ebf5f269474df959de981568141f90fbe
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93528435"
---
# <span data-ttu-id="6eb43-101">Set-AzureRmRecoveryServicesAsrReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="6eb43-101">Set-AzureRmRecoveryServicesAsrReplicationProtectedItem</span></span>

## <span data-ttu-id="6eb43-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6eb43-102">SYNOPSIS</span></span>
<span data-ttu-id="6eb43-103">지정 된 복제 보호 항목에 대 한 대상 네트워크 및 가상 컴퓨터 크기와 같은 복구 속성을 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="6eb43-103">Sets recovery properties such as target network and virtual machine size for the specified replication protected item.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6eb43-104">구문과</span><span class="sxs-lookup"><span data-stu-id="6eb43-104">SYNTAX</span></span>

```
Set-AzureRmRecoveryServicesAsrReplicationProtectedItem -InputObject <ASRReplicationProtectedItem>
 [-Name <String>] [-Size <String>] [-PrimaryNic <String>] [-RecoveryNetworkId <String>]
 [-RecoveryCloudServiceId <String>] [-RecoveryNicSubnetName <String>] [-RecoveryNicStaticIPAddress <String>]
 [-NicSelectionType <String>] [-RecoveryResourceGroupId <String>] [-LicenseType <String>]
 [-RecoveryAvailabilitySet <String>] [-RecoveryBootDiagStorageAccountId <String>]
 [-AzureToAzureUpdateReplicationConfiguration <ASRAzuretoAzureDiskReplicationConfig[]>]
 [-UseManagedDisk <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="6eb43-105">설명은</span><span class="sxs-lookup"><span data-stu-id="6eb43-105">DESCRIPTION</span></span>
<span data-ttu-id="6eb43-106">**AzureRmRecoveryServicesAsrReplicationProtectedItem** Cmdlet은 복제 보호 항목에 대 한 복구 속성을 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="6eb43-106">The **Set-AzureRmRecoveryServicesAsrReplicationProtectedItem** cmdlet sets the recovery properties for a Replication Protected Item.</span></span>

## <span data-ttu-id="6eb43-107">예제의</span><span class="sxs-lookup"><span data-stu-id="6eb43-107">EXAMPLES</span></span>

### <span data-ttu-id="6eb43-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="6eb43-108">Example 1</span></span>
```
PS C:\> $currentJob = Set-AzureRmRecoveryServicesAsrReplicationProtectedItem -ReplicationProtectedItem $RPI -PrimaryNic $NicId -RecoveryNetworkId $AzureNetworkID -RecoveryNicSubnetName $subnetName
```

<span data-ttu-id="6eb43-109">지정 된 매개 변수를 사용 하 여 복제 보호 항목 설정의 업데이트 작업을 시작 하 고 작업을 추적 하는 데 사용 되는 ASR 작업을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="6eb43-109">Starts the operation of updating the replication protect item settings using the specified parameters and returns the ASR job used to track the operation.</span></span>

## <span data-ttu-id="6eb43-110">변수</span><span class="sxs-lookup"><span data-stu-id="6eb43-110">PARAMETERS</span></span>

### <span data-ttu-id="6eb43-111">-AzureToAzureUpdateReplicationConfiguration</span><span class="sxs-lookup"><span data-stu-id="6eb43-111">-AzureToAzureUpdateReplicationConfiguration</span></span>
<span data-ttu-id="6eb43-112">방법 업데이트를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="6eb43-112">Specifies the update relication configration.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRAzuretoAzureDiskReplicationConfig[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6eb43-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6eb43-113">-DefaultProfile</span></span>
<span data-ttu-id="6eb43-114">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="6eb43-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6eb43-115">-InputObject</span><span class="sxs-lookup"><span data-stu-id="6eb43-115">-InputObject</span></span>
<span data-ttu-id="6eb43-116">Cmdlet에 대 한 입력 개체: 업데이트할 복제 보호 항목에 해당 하는 ASR 복제 보호 항목 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="6eb43-116">The input object to the cmdlet: The ASR replication protected item object corresponding to the replication protected item to update.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRReplicationProtectedItem
Parameter Sets: (All)
Aliases: ReplicationProtectedItem

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="6eb43-117">-LicenseType</span><span class="sxs-lookup"><span data-stu-id="6eb43-117">-LicenseType</span></span>
<span data-ttu-id="6eb43-118">Windows Server 가상 컴퓨터에 사용할 라이선스 유형 선택 항목을 입력 합니다.</span><span class="sxs-lookup"><span data-stu-id="6eb43-118">Specifiy the license type selection to be used for Windows Server virtual machines.</span></span> <span data-ttu-id="6eb43-119">마이그레이션에 대 한 Azure 하이브리드 사용 혜택 (허브)을 사용할 자격이 있는 경우이 보호 항목을 장애 조치 하는 동안 허브 설정을 사용 하도록 지정 하는 경우 라이선스 유형을 WindowsServer로 설정 하는 것이 좋습니다.</span><span class="sxs-lookup"><span data-stu-id="6eb43-119">If you are entitled to use the Azure Hybrid Use Benefit (HUB) for migrations and would like to specify that the HUB setting be used while failing over this protected item set the license type to be WindowsServer.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: NoLicenseType, WindowsServer

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6eb43-120">-이름</span><span class="sxs-lookup"><span data-stu-id="6eb43-120">-Name</span></span>
<span data-ttu-id="6eb43-121">장애 조치에 생성 되는 복구 가상 컴퓨터의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="6eb43-121">Specifies the name of the recovery virtual machine that will be created on failover.</span></span>

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

### <span data-ttu-id="6eb43-122">-NicSelectionType</span><span class="sxs-lookup"><span data-stu-id="6eb43-122">-NicSelectionType</span></span>
<span data-ttu-id="6eb43-123">사용자가 설정 하거나 기본적으로 설정 되는 NIC (네트워크 인터페이스 카드) 속성을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="6eb43-123">Specifies the network interface card (NIC) properties set by user or set by default.</span></span>
<span data-ttu-id="6eb43-124">NotSelected를 지정 하 여 기본 값으로 돌아갈 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="6eb43-124">You can specify NotSelected to go back to the default values.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: NotSelected, SelectedByUser

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6eb43-125">-PrimaryNic</span><span class="sxs-lookup"><span data-stu-id="6eb43-125">-PrimaryNic</span></span>
<span data-ttu-id="6eb43-126">이 cmdlet이 복구 네트워크 속성을 설정 하는 가상 컴퓨터의 NIC를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="6eb43-126">Specifies the NIC of the virtual machine for which this cmdlet sets the recovery network property.</span></span>

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

### <span data-ttu-id="6eb43-127">-RecoveryAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="6eb43-127">-RecoveryAvailabilitySet</span></span>
<span data-ttu-id="6eb43-128">장애 조치 (failover) 후 복제 보호 항목에 대 한 가용성 집합입니다.</span><span class="sxs-lookup"><span data-stu-id="6eb43-128">Availability set for replication protected item after failover.</span></span>

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

### <span data-ttu-id="6eb43-129">-RecoveryBootDiagStorageAccountId</span><span class="sxs-lookup"><span data-stu-id="6eb43-129">-RecoveryBootDiagStorageAccountId</span></span>
<span data-ttu-id="6eb43-130">복구 azure VM에 대 한 부팅 진단의 저장소 계정을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="6eb43-130">Specifies the storage account for boot diagnostics for recovery azure VM.</span></span>

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

### <span data-ttu-id="6eb43-131">-RecoveryCloudServiceId</span><span class="sxs-lookup"><span data-stu-id="6eb43-131">-RecoveryCloudServiceId</span></span>
<span data-ttu-id="6eb43-132">이 가상 컴퓨터를 장애 조치 (failover) 할 복구 클라우드 서비스의 리소스 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="6eb43-132">The resource ID of the recovery cloud service to failover this virtual machine to.</span></span>

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

### <span data-ttu-id="6eb43-133">-RecoveryNetworkId</span><span class="sxs-lookup"><span data-stu-id="6eb43-133">-RecoveryNetworkId</span></span>
<span data-ttu-id="6eb43-134">보호 된 항목을 장애 조치 해야 하는 Azure 가상 네트워크의 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="6eb43-134">Specifies the ID of the Azure virtual network to which the protected item should be failed over.</span></span>

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

### <span data-ttu-id="6eb43-135">-RecoveryNicStaticIPAddress</span><span class="sxs-lookup"><span data-stu-id="6eb43-135">-RecoveryNicStaticIPAddress</span></span>
<span data-ttu-id="6eb43-136">복구 시 기본 NIC에 할당 해야 하는 고정 IP 주소를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="6eb43-136">Specifies the static IP address that should be assigned to primary NIC on recovery.</span></span>

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

### <span data-ttu-id="6eb43-137">-RecoveryNicSubnetName</span><span class="sxs-lookup"><span data-stu-id="6eb43-137">-RecoveryNicSubnetName</span></span>
<span data-ttu-id="6eb43-138">보호 된 항목의이 NIC가 장애 조치 (failover)에 연결 되어야 하는 복구 Azure 가상 네트워크의 서브넷 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="6eb43-138">Specifies the name of the subnet on the recovery Azure virtual network to which this NIC of the protected item should be connected to on failover.</span></span>

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

### <span data-ttu-id="6eb43-139">-RecoveryResourceGroupId</span><span class="sxs-lookup"><span data-stu-id="6eb43-139">-RecoveryResourceGroupId</span></span>
<span data-ttu-id="6eb43-140">장애 조치 시 보호 되는 항목이 복구 되는 복구 영역에 있는 Azure 리소스 그룹의 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="6eb43-140">The ID of the Azure resource group in the recovery region in which the protected item will be recovered on failover.</span></span>

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

### <span data-ttu-id="6eb43-141">-크기</span><span class="sxs-lookup"><span data-stu-id="6eb43-141">-Size</span></span>
<span data-ttu-id="6eb43-142">복구 가상 컴퓨터 크기를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="6eb43-142">Specifies the recovery virtual machine size.</span></span>
<span data-ttu-id="6eb43-143">값은 Azure 가상 머신에서 지원 되는 크기 집합에서 지정 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="6eb43-143">The value should be from the set of sizes supported by Azure virtual machines.</span></span>

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

### <span data-ttu-id="6eb43-144">-UseManagedDisk</span><span class="sxs-lookup"><span data-stu-id="6eb43-144">-UseManagedDisk</span></span>
<span data-ttu-id="6eb43-145">장애 조치에 만든 Azure 가상 컴퓨터에서 관리 디스크를 사용 해야 하는지 여부를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="6eb43-145">Specifies if the Azure virtual machine that is created on failover should use managed disks.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: True, False

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6eb43-146">-확인</span><span class="sxs-lookup"><span data-stu-id="6eb43-146">-Confirm</span></span>
<span data-ttu-id="6eb43-147">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="6eb43-147">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6eb43-148">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6eb43-148">-WhatIf</span></span>
<span data-ttu-id="6eb43-149">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="6eb43-149">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="6eb43-150">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="6eb43-150">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6eb43-151">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6eb43-151">CommonParameters</span></span>
<span data-ttu-id="6eb43-152">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="6eb43-152">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6eb43-153">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6eb43-153">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6eb43-154">입력</span><span class="sxs-lookup"><span data-stu-id="6eb43-154">INPUTS</span></span>

### <span data-ttu-id="6eb43-155">SiteRecovery. ASRReplicationProtectedItem에 대 한 서비스</span><span class="sxs-lookup"><span data-stu-id="6eb43-155">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRReplicationProtectedItem</span></span>

## <span data-ttu-id="6eb43-156">출력</span><span class="sxs-lookup"><span data-stu-id="6eb43-156">OUTPUTS</span></span>

### <span data-ttu-id="6eb43-157">SiteRecovery. r i m m 작업</span><span class="sxs-lookup"><span data-stu-id="6eb43-157">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="6eb43-158">상속자</span><span class="sxs-lookup"><span data-stu-id="6eb43-158">NOTES</span></span>

## <span data-ttu-id="6eb43-159">관련 링크</span><span class="sxs-lookup"><span data-stu-id="6eb43-159">RELATED LINKS</span></span>

[<span data-ttu-id="6eb43-160">Get-AzureRmRecoveryServicesAsrReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="6eb43-160">Get-AzureRmRecoveryServicesAsrReplicationProtectedItem</span></span>](./Get-AzureRmRecoveryServicesAsrReplicationProtectedItem.md)

[<span data-ttu-id="6eb43-161">새로운 AzureRmRecoveryServicesAsrReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="6eb43-161">New-AzureRmRecoveryServicesAsrReplicationProtectedItem</span></span>](./New-AzureRmRecoveryServicesAsrReplicationProtectedItem.md)

[<span data-ttu-id="6eb43-162">제거-AzureRmRecoveryServicesAsrReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="6eb43-162">Remove-AzureRmRecoveryServicesAsrReplicationProtectedItem</span></span>](./Remove-AzureRmRecoveryServicesAsrReplicationProtectedItem.md)
