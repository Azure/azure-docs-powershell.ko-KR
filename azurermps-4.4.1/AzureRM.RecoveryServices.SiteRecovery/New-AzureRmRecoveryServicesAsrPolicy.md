---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/New-AzureRmRecoveryServicesAsrPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/New-AzureRmRecoveryServicesAsrPolicy.md
ms.openlocfilehash: a0a55ad071a21f7924eb5a4115a7699fc6690060
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93529208"
---
# <span data-ttu-id="395f1-101">New-AzureRmRecoveryServicesAsrPolicy</span><span class="sxs-lookup"><span data-stu-id="395f1-101">New-AzureRmRecoveryServicesAsrPolicy</span></span>

## <span data-ttu-id="395f1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="395f1-102">SYNOPSIS</span></span>
<span data-ttu-id="395f1-103">Azure Site Recovery 복제 정책을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="395f1-103">Creates an Azure Site Recovery replication policy.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="395f1-104">구문과</span><span class="sxs-lookup"><span data-stu-id="395f1-104">SYNTAX</span></span>

### <span data-ttu-id="395f1-105">EnterpriseToAzure (기본값)</span><span class="sxs-lookup"><span data-stu-id="395f1-105">EnterpriseToAzure (Default)</span></span>
```
New-AzureRmRecoveryServicesAsrPolicy -Name <String> -ReplicationProvider <String>
 -ReplicationFrequencyInSeconds <String> [-NumberOfRecoveryPointsToRetain <Int32>]
 [-ApplicationConsistentSnapshotFrequencyInHours <Int32>] [-ReplicationStartTime <TimeSpan>]
 [-RecoveryAzureStorageAccountId <String>] [-Encryption <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="395f1-106">Enterprise엔터프라이즈</span><span class="sxs-lookup"><span data-stu-id="395f1-106">EnterpriseToEnterprise</span></span>
```
New-AzureRmRecoveryServicesAsrPolicy -Name <String> -ReplicationProvider <String> [-ReplicationMethod <String>]
 -ReplicationFrequencyInSeconds <String> [-NumberOfRecoveryPointsToRetain <Int32>]
 [-ApplicationConsistentSnapshotFrequencyInHours <Int32>] [-Compression <String>] -ReplicationPort <UInt16>
 [-Authentication <String>] [-ReplicationStartTime <TimeSpan>] [-ReplicaDeletion <String>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="395f1-107">설명은</span><span class="sxs-lookup"><span data-stu-id="395f1-107">DESCRIPTION</span></span>
<span data-ttu-id="395f1-108">**새 AzureRmRecoveryServicesAsrPolicy** Cmdlet은 Azure Site Recovery 복제 정책을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="395f1-108">The **New-AzureRmRecoveryServicesAsrPolicy** cmdlet creates an Azure Site Recovery replication policy.</span></span>
<span data-ttu-id="395f1-109">복제 정책은 복제 빈도 및 복구 지점 수와 같은 복제 설정을 지정 하는 데 사용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="395f1-109">The replication policy is used to specify replication settings such as the replication frequency and number of recovery points.</span></span>

## <span data-ttu-id="395f1-110">예제의</span><span class="sxs-lookup"><span data-stu-id="395f1-110">EXAMPLES</span></span>

### <span data-ttu-id="395f1-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="395f1-111">Example 1</span></span>
```
PS C:\> $currentJob = New-AzureRmRecoveryServicesAsrProtectionContainerMapping -Name $PolicyName -Policy $ProtectionProfile -PrimaryProtectionContainer $PrimaryContainer -RecoveryProtectionContainer $RecoveryContainer
```

<span data-ttu-id="395f1-112">지정 된 매개 변수를 사용 하 여 복제 정책 만들기 작업을 시작 하 고 작업을 추적 하는 데 사용 되는 ASR 작업을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="395f1-112">Starts the replication policy creation operation using the specified parameters and returns the ASR job used to track the operation.</span></span>

## <span data-ttu-id="395f1-113">변수</span><span class="sxs-lookup"><span data-stu-id="395f1-113">PARAMETERS</span></span>

### <span data-ttu-id="395f1-114">-ApplicationConsistentSnapshotFrequencyInHours</span><span class="sxs-lookup"><span data-stu-id="395f1-114">-ApplicationConsistentSnapshotFrequencyInHours</span></span>
<span data-ttu-id="395f1-115">응용 프로그램 일치 복구 지점을 만들 빈도 (시간)를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="395f1-115">Specifies the frequency(in hours) at which to create application consistent recovery points.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="395f1-116">-인증</span><span class="sxs-lookup"><span data-stu-id="395f1-116">-Authentication</span></span>
<span data-ttu-id="395f1-117">사용 되는 인증 유형을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="395f1-117">Specifies the type of authentication used.</span></span>
<span data-ttu-id="395f1-118">유효한 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="395f1-118">Valid values are:</span></span>

- <span data-ttu-id="395f1-119">인증</span><span class="sxs-lookup"><span data-stu-id="395f1-119">Certificate</span></span>
-  <span data-ttu-id="395f1-120">커버로스</span><span class="sxs-lookup"><span data-stu-id="395f1-120">Kerberos</span></span>

```yaml
Type: String
Parameter Sets: EnterpriseToEnterprise
Aliases: 
Accepted values: Certificate, Kerberos

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="395f1-121">-압축</span><span class="sxs-lookup"><span data-stu-id="395f1-121">-Compression</span></span>
<span data-ttu-id="395f1-122">압축을 사용할 수 있는지 여부를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="395f1-122">Specifies if compression should be enabled.</span></span>

```yaml
Type: String
Parameter Sets: EnterpriseToEnterprise
Aliases: 
Accepted values: Enable, Disable

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="395f1-123">-암호화</span><span class="sxs-lookup"><span data-stu-id="395f1-123">-Encryption</span></span>
<span data-ttu-id="395f1-124">암호화를 사용 하거나 사용 하지 않도록 설정할지 여부를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="395f1-124">Specifies if encryption should be enabled or disabled.</span></span>

```yaml
Type: String
Parameter Sets: EnterpriseToAzure
Aliases: 
Accepted values: Enable, Disable

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="395f1-125">-이름</span><span class="sxs-lookup"><span data-stu-id="395f1-125">-Name</span></span>
<span data-ttu-id="395f1-126">ASR 복제 정책의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="395f1-126">Specifies the name of the ASR replication policy.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="395f1-127">-NumberOfRecoveryPointsToRetain</span><span class="sxs-lookup"><span data-stu-id="395f1-127">-NumberOfRecoveryPointsToRetain</span></span>
<span data-ttu-id="395f1-128">유지할 번호 복구 지점을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="395f1-128">Specifies the number recovery points to retain.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: RecoveryPoints

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="395f1-129">-RecoveryAzureStorageAccountId</span><span class="sxs-lookup"><span data-stu-id="395f1-129">-RecoveryAzureStorageAccountId</span></span>
<span data-ttu-id="395f1-130">복제 대상의 Azure storage 계정 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="395f1-130">Specifies the Azure storage account ID of the replication target.</span></span> <span data-ttu-id="395f1-131">New-AzureRmRecoveryServicesASRReplicationProtectedItem cmdlet을 사용 하 여 복제를 사용 하도록 설정 하는 동안 대체가 제공 되지 않은 경우 복제 대상 저장소 계정으로 사용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="395f1-131">Used as the target storage account for replication if an alternate is not provided while enabling replication using the New-AzureRmRecoveryServicesASRReplicationProtectedItem cmdlet.</span></span>

```yaml
Type: String
Parameter Sets: EnterpriseToAzure
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="395f1-132">-ReplicaDeletion</span><span class="sxs-lookup"><span data-stu-id="395f1-132">-ReplicaDeletion</span></span>
<span data-ttu-id="395f1-133">VMM 관리 사이트에서 다른 복제를 사용 하지 않도록 설정할 때 복제 가상 컴퓨터를 삭제할 것인지 여부를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="395f1-133">Specifies if the replica virtual machine should be deleted on disabling replication from a VMM managed site to another.</span></span>

```yaml
Type: String
Parameter Sets: EnterpriseToEnterprise
Aliases: 
Accepted values: Required, NotRequired

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="395f1-134">-ReplicationFrequencyInSeconds</span><span class="sxs-lookup"><span data-stu-id="395f1-134">-ReplicationFrequencyInSeconds</span></span>
<span data-ttu-id="395f1-135">복제 빈도 간격 (초)을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="395f1-135">Specifies the replication frequency interval in seconds.</span></span>
<span data-ttu-id="395f1-136">유효한 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="395f1-136">Valid values are:</span></span>

- <span data-ttu-id="395f1-137">30</span><span class="sxs-lookup"><span data-stu-id="395f1-137">30</span></span>
- <span data-ttu-id="395f1-138">300</span><span class="sxs-lookup"><span data-stu-id="395f1-138">300</span></span>
- <span data-ttu-id="395f1-139">900</span><span class="sxs-lookup"><span data-stu-id="395f1-139">900</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: 30, 300, 900

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="395f1-140">-ReplicationMethod</span><span class="sxs-lookup"><span data-stu-id="395f1-140">-ReplicationMethod</span></span>
<span data-ttu-id="395f1-141">복제 방법을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="395f1-141">Specifies the replication method.</span></span>
<span data-ttu-id="395f1-142">유효한 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="395f1-142">Valid values are:</span></span>

- <span data-ttu-id="395f1-143">온라인</span><span class="sxs-lookup"><span data-stu-id="395f1-143">Online</span></span>
- <span data-ttu-id="395f1-144">이거나</span><span class="sxs-lookup"><span data-stu-id="395f1-144">Offline</span></span>

```yaml
Type: String
Parameter Sets: EnterpriseToEnterprise
Aliases: 
Accepted values: Online, Offline

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="395f1-145">-ReplicationPort</span><span class="sxs-lookup"><span data-stu-id="395f1-145">-ReplicationPort</span></span>
<span data-ttu-id="395f1-146">복제에 사용 되는 포트를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="395f1-146">Specifies the port used for replication.</span></span>

```yaml
Type: UInt16
Parameter Sets: EnterpriseToEnterprise
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="395f1-147">-ReplicationProvider</span><span class="sxs-lookup"><span data-stu-id="395f1-147">-ReplicationProvider</span></span>
<span data-ttu-id="395f1-148">복제 공급자를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="395f1-148">Specifies the replication provider.</span></span>
<span data-ttu-id="395f1-149">유효한 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="395f1-149">Valid values are:</span></span>

- <span data-ttu-id="395f1-150">HyperVReplica2012R2</span><span class="sxs-lookup"><span data-stu-id="395f1-150">HyperVReplica2012R2</span></span>
- <span data-ttu-id="395f1-151">HyperVReplica2012</span><span class="sxs-lookup"><span data-stu-id="395f1-151">HyperVReplica2012</span></span>
- <span data-ttu-id="395f1-152">HyperVReplicaAzure</span><span class="sxs-lookup"><span data-stu-id="395f1-152">HyperVReplicaAzure</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: HyperVReplica2012R2, HyperVReplica2012, HyperVReplicaAzure

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="395f1-153">-ReplicationStartTime</span><span class="sxs-lookup"><span data-stu-id="395f1-153">-ReplicationStartTime</span></span>
<span data-ttu-id="395f1-154">복제 시작 시간을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="395f1-154">Specifies the replication start time.</span></span>
<span data-ttu-id="395f1-155">작업의 시작 부분에서 24 시간 이상 이어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="395f1-155">It must be no later than 24-hours from the start of the job.</span></span>

```yaml
Type: TimeSpan
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="395f1-156">-확인</span><span class="sxs-lookup"><span data-stu-id="395f1-156">-Confirm</span></span>
<span data-ttu-id="395f1-157">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="395f1-157">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="395f1-158">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="395f1-158">-WhatIf</span></span>
<span data-ttu-id="395f1-159">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="395f1-159">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="395f1-160">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="395f1-160">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="395f1-161">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="395f1-161">CommonParameters</span></span>
<span data-ttu-id="395f1-162">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="395f1-162">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="395f1-163">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="395f1-163">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="395f1-164">입력</span><span class="sxs-lookup"><span data-stu-id="395f1-164">INPUTS</span></span>

### <span data-ttu-id="395f1-165">않아야</span><span class="sxs-lookup"><span data-stu-id="395f1-165">None</span></span>

## <span data-ttu-id="395f1-166">출력</span><span class="sxs-lookup"><span data-stu-id="395f1-166">OUTPUTS</span></span>

### <span data-ttu-id="395f1-167">System. 개체</span><span class="sxs-lookup"><span data-stu-id="395f1-167">System.Object</span></span>

## <span data-ttu-id="395f1-168">상속자</span><span class="sxs-lookup"><span data-stu-id="395f1-168">NOTES</span></span>

## <span data-ttu-id="395f1-169">관련 링크</span><span class="sxs-lookup"><span data-stu-id="395f1-169">RELATED LINKS</span></span>

[<span data-ttu-id="395f1-170">Get-AzureRmRecoveryServicesAsrPolicy</span><span class="sxs-lookup"><span data-stu-id="395f1-170">Get-AzureRmRecoveryServicesAsrPolicy</span></span>](./Get-AzureRmRecoveryServicesAsrPolicy.md)

[<span data-ttu-id="395f1-171">제거-AzureRmRecoveryServicesAsrPolicy</span><span class="sxs-lookup"><span data-stu-id="395f1-171">Remove-AzureRmRecoveryServicesAsrPolicy</span></span>](./Remove-AzureRmRecoveryServicesAsrPolicy.md)
