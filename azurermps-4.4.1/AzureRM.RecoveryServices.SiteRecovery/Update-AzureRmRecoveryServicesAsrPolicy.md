---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Update-AzureRmRecoveryServicesAsrPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Update-AzureRmRecoveryServicesAsrPolicy.md
ms.openlocfilehash: 302b781ee6af68cb960ab01668147edc56e04284
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93533899"
---
# <span data-ttu-id="5599f-101">Update-AzureRmRecoveryServicesAsrPolicy</span><span class="sxs-lookup"><span data-stu-id="5599f-101">Update-AzureRmRecoveryServicesAsrPolicy</span></span>

## <span data-ttu-id="5599f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5599f-102">SYNOPSIS</span></span>
<span data-ttu-id="5599f-103">Azure Site Recovery 복제 정책을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="5599f-103">Updates an Azure Site Recovery replication policy.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5599f-104">구문과</span><span class="sxs-lookup"><span data-stu-id="5599f-104">SYNTAX</span></span>

```
Update-AzureRmRecoveryServicesAsrPolicy -InputObject <ASRPolicy> [-ReplicationMethod <String>]
 [-ReplicationFrequencyInSeconds <String>] [-NumberOfRecoveryPointsToRetain <Int32>]
 [-ApplicationConsistentSnapshotFrequencyInHours <Int32>] [-Compression <String>] [-ReplicationPort <UInt16>]
 [-Authentication <String>] [-ReplicationStartTime <TimeSpan>] [-ReplicaDeletion <String>]
 [-RecoveryAzureStorageAccountId <String>] [-Encryption <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5599f-105">설명은</span><span class="sxs-lookup"><span data-stu-id="5599f-105">DESCRIPTION</span></span>
<span data-ttu-id="5599f-106">**업데이트 AzureRmRecoveryServicesAsrPolicy** cmdlet은 지정 된 Azure Site Recovery 복제 정책을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="5599f-106">The **Update-AzureRmRecoveryServicesAsrPolicy** cmdlet updates the specified Azure Site Recovery replication policy.</span></span>

## <span data-ttu-id="5599f-107">예제의</span><span class="sxs-lookup"><span data-stu-id="5599f-107">EXAMPLES</span></span>

### <span data-ttu-id="5599f-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="5599f-108">Example 1</span></span>
```
PS C:\> $currentJob = Update-AzureRmRecoveryServicesAsrPolicy -Policy $Policy -ReplicationFrequencyInSeconds 900
```

<span data-ttu-id="5599f-109">지정 된 매개 변수를 사용 하 여 복제 정책 업데이트 작업을 시작 하 고 작업을 추적 하는 데 사용 되는 ASR 작업을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="5599f-109">Starts the update replication policy operation using the specified parameters and returns the ASR job used to track the operation.</span></span>

## <span data-ttu-id="5599f-110">변수</span><span class="sxs-lookup"><span data-stu-id="5599f-110">PARAMETERS</span></span>

### <span data-ttu-id="5599f-111">-ApplicationConsistentSnapshotFrequencyInHours</span><span class="sxs-lookup"><span data-stu-id="5599f-111">-ApplicationConsistentSnapshotFrequencyInHours</span></span>
<span data-ttu-id="5599f-112">응용 프로그램 일치 복구 지점을 만들 빈도 (시간)를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="5599f-112">Specifies the frequency(in hours) at which to create application consistent recovery points.</span></span>

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

### <span data-ttu-id="5599f-113">-인증</span><span class="sxs-lookup"><span data-stu-id="5599f-113">-Authentication</span></span>
<span data-ttu-id="5599f-114">사용 되는 인증 유형을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="5599f-114">Specifies the type of authentication used.</span></span>
<span data-ttu-id="5599f-115">유효한 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="5599f-115">Valid values are:</span></span>

- <span data-ttu-id="5599f-116">인증</span><span class="sxs-lookup"><span data-stu-id="5599f-116">Certificate</span></span>
-  <span data-ttu-id="5599f-117">커버로스</span><span class="sxs-lookup"><span data-stu-id="5599f-117">Kerberos</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: Certificate, Kerberos

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5599f-118">-압축</span><span class="sxs-lookup"><span data-stu-id="5599f-118">-Compression</span></span>
<span data-ttu-id="5599f-119">압축을 사용할 수 있는지 여부를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="5599f-119">Specifies if compression should be enabled.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: Enable, Disable

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5599f-120">-암호화</span><span class="sxs-lookup"><span data-stu-id="5599f-120">-Encryption</span></span>
<span data-ttu-id="5599f-121">암호화를 사용 하거나 사용 하지 않도록 설정할지 여부를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="5599f-121">Specifies if encryption should be enabled or disabled.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: Enable, Disable

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5599f-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="5599f-122">-InputObject</span></span>
<span data-ttu-id="5599f-123">Cmdlet에 대 한 Input 개체: 업데이트할 복제 정책에 해당 하는 ASR 복제 정책 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="5599f-123">Input object for the cmdlet: Specifies the ASR replication policy object corresponding to the replication policy to be updated.</span></span>

```yaml
Type: ASRPolicy
Parameter Sets: (All)
Aliases: Policy

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="5599f-124">-NumberOfRecoveryPointsToRetain</span><span class="sxs-lookup"><span data-stu-id="5599f-124">-NumberOfRecoveryPointsToRetain</span></span>
<span data-ttu-id="5599f-125">유지할 번호 복구 지점을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="5599f-125">Specifies the number recovery points to retain.</span></span>

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

### <span data-ttu-id="5599f-126">-RecoveryAzureStorageAccountId</span><span class="sxs-lookup"><span data-stu-id="5599f-126">-RecoveryAzureStorageAccountId</span></span>
<span data-ttu-id="5599f-127">복제 대상의 Azure storage 계정 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="5599f-127">Specifies the Azure storage account ID of the replication target.</span></span> <span data-ttu-id="5599f-128">New-AzureRmRecoveryServicesASRReplicationProtectedItem cmdlet을 사용 하 여 복제를 사용 하도록 설정 하는 동안 대체가 제공 되지 않은 경우 복제 대상 저장소 계정으로 사용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="5599f-128">Used as the target storage account for replication if an alternate is not provided while enabling replication using the New-AzureRmRecoveryServicesASRReplicationProtectedItem cmdlet.</span></span>

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

### <span data-ttu-id="5599f-129">-ReplicaDeletion</span><span class="sxs-lookup"><span data-stu-id="5599f-129">-ReplicaDeletion</span></span>
<span data-ttu-id="5599f-130">VMM 관리 사이트에서 다른 복제를 사용 하지 않도록 설정할 때 복제 가상 컴퓨터를 삭제할 것인지 여부를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="5599f-130">Specifies if the replica virtual machine should be deleted on disabling replication from a VMM managed site to another.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: Required, NotRequired

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5599f-131">-ReplicationFrequencyInSeconds</span><span class="sxs-lookup"><span data-stu-id="5599f-131">-ReplicationFrequencyInSeconds</span></span>
<span data-ttu-id="5599f-132">복제 빈도 간격 (초)을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="5599f-132">Specifies the replication frequency interval in seconds.</span></span>
<span data-ttu-id="5599f-133">유효한 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="5599f-133">Valid values are:</span></span>

- <span data-ttu-id="5599f-134">30</span><span class="sxs-lookup"><span data-stu-id="5599f-134">30</span></span>
- <span data-ttu-id="5599f-135">300</span><span class="sxs-lookup"><span data-stu-id="5599f-135">300</span></span>
- <span data-ttu-id="5599f-136">900</span><span class="sxs-lookup"><span data-stu-id="5599f-136">900</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: 30, 300, 900

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5599f-137">-ReplicationMethod</span><span class="sxs-lookup"><span data-stu-id="5599f-137">-ReplicationMethod</span></span>
<span data-ttu-id="5599f-138">복제 방법을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="5599f-138">Specifies the replication method.</span></span>
<span data-ttu-id="5599f-139">유효한 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="5599f-139">Valid values are:</span></span>

- <span data-ttu-id="5599f-140">온라인</span><span class="sxs-lookup"><span data-stu-id="5599f-140">Online</span></span>
- <span data-ttu-id="5599f-141">이거나</span><span class="sxs-lookup"><span data-stu-id="5599f-141">Offline</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: Online, Offline

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5599f-142">-ReplicationPort</span><span class="sxs-lookup"><span data-stu-id="5599f-142">-ReplicationPort</span></span>
<span data-ttu-id="5599f-143">복제에 사용 되는 포트를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="5599f-143">Specifies the port used for replication.</span></span>

```yaml
Type: UInt16
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5599f-144">-ReplicationStartTime</span><span class="sxs-lookup"><span data-stu-id="5599f-144">-ReplicationStartTime</span></span>
<span data-ttu-id="5599f-145">복제 시작 시간을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="5599f-145">Specifies the replication start time.</span></span>
<span data-ttu-id="5599f-146">작업의 시작 부분에서 24 시간 이상 이어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="5599f-146">It must be no later than 24-hours from the start of the job.</span></span>

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

### <span data-ttu-id="5599f-147">-확인</span><span class="sxs-lookup"><span data-stu-id="5599f-147">-Confirm</span></span>
<span data-ttu-id="5599f-148">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="5599f-148">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5599f-149">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5599f-149">-WhatIf</span></span>
<span data-ttu-id="5599f-150">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="5599f-150">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="5599f-151">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="5599f-151">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5599f-152">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5599f-152">CommonParameters</span></span>
<span data-ttu-id="5599f-153">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="5599f-153">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5599f-154">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5599f-154">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5599f-155">입력</span><span class="sxs-lookup"><span data-stu-id="5599f-155">INPUTS</span></span>

### <span data-ttu-id="5599f-156">SiteRecovery. r i m g 정책</span><span class="sxs-lookup"><span data-stu-id="5599f-156">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRPolicy</span></span>

## <span data-ttu-id="5599f-157">출력</span><span class="sxs-lookup"><span data-stu-id="5599f-157">OUTPUTS</span></span>

### <span data-ttu-id="5599f-158">System. 개체</span><span class="sxs-lookup"><span data-stu-id="5599f-158">System.Object</span></span>

## <span data-ttu-id="5599f-159">상속자</span><span class="sxs-lookup"><span data-stu-id="5599f-159">NOTES</span></span>

## <span data-ttu-id="5599f-160">관련 링크</span><span class="sxs-lookup"><span data-stu-id="5599f-160">RELATED LINKS</span></span>

