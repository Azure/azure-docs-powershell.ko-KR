---
external help file: Microsoft.Azure.Commands.RecoveryServicesRdfe.dll-Help.xml
ms.assetid: 853D5585-2A92-4B65-BA8C-EC06BEE8C237
online version: ''
schema: 2.0.0
ms.openlocfilehash: 63274c772c6085fc8c491557851673a38056aa77
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94045891"
---
# <span data-ttu-id="0ef4c-101">New-AzureSiteRecoveryProtectionProfileObject</span><span class="sxs-lookup"><span data-stu-id="0ef4c-101">New-AzureSiteRecoveryProtectionProfileObject</span></span>

## <span data-ttu-id="0ef4c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0ef4c-102">SYNOPSIS</span></span>
<span data-ttu-id="0ef4c-103">사이트 복구 보호 프로필 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="0ef4c-103">Creates a Site Recovery protection profile object.</span></span>

## <span data-ttu-id="0ef4c-104">구문과</span><span class="sxs-lookup"><span data-stu-id="0ef4c-104">SYNTAX</span></span>

### <span data-ttu-id="0ef4c-105">EnterpriseToAzure (기본값)</span><span class="sxs-lookup"><span data-stu-id="0ef4c-105">EnterpriseToAzure (Default)</span></span>
```
New-AzureSiteRecoveryProtectionProfileObject [-Name <String>] -ReplicationProvider <String>
 -RecoveryAzureSubscription <String> -RecoveryAzureStorageAccount <String>
 -ReplicationFrequencyInSeconds <String> [-RecoveryPoints <Int32>]
 [-ApplicationConsistentSnapshotFrequencyInHours <Int32>] [-ReplicationStartTime <TimeSpan>] [-Force]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="0ef4c-106">Enterprise엔터프라이즈</span><span class="sxs-lookup"><span data-stu-id="0ef4c-106">EnterpriseToEnterprise</span></span>
```
New-AzureSiteRecoveryProtectionProfileObject [-Name <String>] -ReplicationProvider <String>
 [-ReplicationMethod <String>] -ReplicationFrequencyInSeconds <String> [-RecoveryPoints <Int32>]
 [-ApplicationConsistentSnapshotFrequencyInHours <Int32>] [-CompressionEnabled] -ReplicationPort <UInt16>
 [-Authentication <String>] [-ReplicationStartTime <TimeSpan>] [-AllowReplicaDeletion] [-Force]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="0ef4c-107">설명은</span><span class="sxs-lookup"><span data-stu-id="0ef4c-107">DESCRIPTION</span></span>
<span data-ttu-id="0ef4c-108">**AzureSiteRecoveryProtectionProfileObject** Cmdlet은 Azure Site Recovery 보호 프로필 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="0ef4c-108">The **New-AzureSiteRecoveryProtectionProfileObject** cmdlet creates an Azure Site Recovery protection profile object.</span></span>
<span data-ttu-id="0ef4c-109">이 cmdlet은 다른 cmdlet에 사용할 **ASRProtectionProfile** 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="0ef4c-109">This cmdlet creates an **ASRProtectionProfile** object to use with other cmdlets.</span></span>

## <span data-ttu-id="0ef4c-110">예제의</span><span class="sxs-lookup"><span data-stu-id="0ef4c-110">EXAMPLES</span></span>

### <span data-ttu-id="0ef4c-111">예제 1: 보호 프로필 만들기</span><span class="sxs-lookup"><span data-stu-id="0ef4c-111">Example 1: Create a protection profile</span></span>
```
PS C:\> New-AzureSiteRecoveryProtectionProfileObject -ReplicationProvider "HyperVReplica" -AllowReplicaDeletion -ApplicationConsistentSnapshotFrequencyInHours 1 -CompressionEnabled -RecoveryPoints 2 -ReplicationFrequencyInSeconds 30 -ReplicationMethod "Online" -ReplicationPort 8085 -ReplicationStartTime 1
Name                                     : 
ID                                       : 
ReplicationProvider                      : HyperVReplica
HyperVReplicaProviderSettingsObject      : Microsoft.Azure.Portal.RecoveryServices.Models.Common.HyperVReplicaProviderSettings
HyperVReplicaAzureProviderSettingsObject :
```

<span data-ttu-id="0ef4c-112">이 명령은 보호 프로필 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="0ef4c-112">This command creates a protection profile object.</span></span>

### <span data-ttu-id="0ef4c-113">예제 2: HyperVReplicaAzure 공급자에 대 한 보호 프로필 만들기</span><span class="sxs-lookup"><span data-stu-id="0ef4c-113">Example 2: Create a protection profile for HyperVReplicaAzure provider</span></span>
```
PS C:\> New-AzureSiteRecoveryProtectionProfileObject -Name "ProtectionProfile" -ReplicationProvider "HyperVReplicaAzure" -RecoveryAzureSubscription "cb53d0c3-bd59-4721-89bc-06916a9147ef" -RecoveryAzureStorageAccount "Contoso01" -ReplicationFrequencyInSeconds 30 -RecoveryPoints 1 -Force
Name                                     : ProtectionProfile
ID                                       : 
ReplicationProvider                      : HyperVReplicaAzure
HyperVReplicaProviderSettingsObject      : 
HyperVReplicaAzureProviderSettingsObject : Microsoft.Azure.Portal.RecoveryServices.Models.Common.HyperVReplicaAzureProviderSettings
```

<span data-ttu-id="0ef4c-114">이 명령은 HyperVReplicaAzure 공급자에 대 한 보호 프로필을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="0ef4c-114">This command creates a protection profile for a HyperVReplicaAzure provider.</span></span>

## <span data-ttu-id="0ef4c-115">변수</span><span class="sxs-lookup"><span data-stu-id="0ef4c-115">PARAMETERS</span></span>

### <span data-ttu-id="0ef4c-116">-AllowReplicaDeletion</span><span class="sxs-lookup"><span data-stu-id="0ef4c-116">-AllowReplicaDeletion</span></span>
<span data-ttu-id="0ef4c-117">보호 프로필에서 복제본 엔터티를 삭제할 수 있음을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="0ef4c-117">Indicates that the protection profile enables deletion of replica entities.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: EnterpriseToEnterprise
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0ef4c-118">-ApplicationConsistentSnapshotFrequencyInHours</span><span class="sxs-lookup"><span data-stu-id="0ef4c-118">-ApplicationConsistentSnapshotFrequencyInHours</span></span>
<span data-ttu-id="0ef4c-119">응용 프로그램 일관성 스냅숏에 대 한 빈도 (시간)를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="0ef4c-119">Specifies the frequency, in hours, for application consistent snapshots.</span></span>

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

### <span data-ttu-id="0ef4c-120">-인증</span><span class="sxs-lookup"><span data-stu-id="0ef4c-120">-Authentication</span></span>
<span data-ttu-id="0ef4c-121">사용할 인증 유형을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="0ef4c-121">Specifies the type of authentication to use.</span></span>
<span data-ttu-id="0ef4c-122">이 매개 변수에 허용 되는 값은 인증서 및 Kerberos입니다.</span><span class="sxs-lookup"><span data-stu-id="0ef4c-122">The acceptable values for this parameter are: Certificate and Kerberos.</span></span>

```yaml
Type: String
Parameter Sets: EnterpriseToEnterprise
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0ef4c-123">-CompressionEnabled</span><span class="sxs-lookup"><span data-stu-id="0ef4c-123">-CompressionEnabled</span></span>
<span data-ttu-id="0ef4c-124">보호 프로필에서 압축을 사용할 수 있음을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="0ef4c-124">Indicates that the protection profile enables compression.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: EnterpriseToEnterprise
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0ef4c-125">-Force</span><span class="sxs-lookup"><span data-stu-id="0ef4c-125">-Force</span></span>
<span data-ttu-id="0ef4c-126">사용자 확인을 요청 하지 않고 명령을 강제로 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="0ef4c-126">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0ef4c-127">-이름</span><span class="sxs-lookup"><span data-stu-id="0ef4c-127">-Name</span></span>
<span data-ttu-id="0ef4c-128">보호 프로필의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="0ef4c-128">Specifies a name for the protection profile.</span></span>

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

### <span data-ttu-id="0ef4c-129">-프로필</span><span class="sxs-lookup"><span data-stu-id="0ef4c-129">-Profile</span></span>
<span data-ttu-id="0ef4c-130">이 cmdlet이 읽는 Azure 프로필을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="0ef4c-130">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="0ef4c-131">프로필을 지정 하지 않으면이 cmdlet은 로컬 기본 프로필을 읽습니다.</span><span class="sxs-lookup"><span data-stu-id="0ef4c-131">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0ef4c-132">-RecoveryAzureStorageAccount</span><span class="sxs-lookup"><span data-stu-id="0ef4c-132">-RecoveryAzureStorageAccount</span></span>
<span data-ttu-id="0ef4c-133">Azure 복제본 엔터티를 저장할 Azure Storage 계정의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="0ef4c-133">Specifies the name of an Azure Storage account on which to store the Azure replica entity.</span></span>

```yaml
Type: String
Parameter Sets: EnterpriseToAzure
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0ef4c-134">-RecoveryAzureSubscription</span><span class="sxs-lookup"><span data-stu-id="0ef4c-134">-RecoveryAzureSubscription</span></span>
<span data-ttu-id="0ef4c-135">저장소 계정에 대 한 Azure 구독에 대 한 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="0ef4c-135">Specifies the ID for an Azure Subscription for a storage account.</span></span>
<span data-ttu-id="0ef4c-136">이 매개 변수는 Azure 복제본 엔터티를 저장할 계정을 참조 합니다.</span><span class="sxs-lookup"><span data-stu-id="0ef4c-136">This parameter refers to the account on which to store the Azure replica entity.</span></span>

```yaml
Type: String
Parameter Sets: EnterpriseToAzure
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0ef4c-137">-RecoveryPoints</span><span class="sxs-lookup"><span data-stu-id="0ef4c-137">-RecoveryPoints</span></span>
<span data-ttu-id="0ef4c-138">복구 지점을 유지 하는 데 소요 되는 시간 (초)을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="0ef4c-138">Specifies the number of hours to retain recovery points.</span></span>

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

### <span data-ttu-id="0ef4c-139">-ReplicationFrequencyInSeconds</span><span class="sxs-lookup"><span data-stu-id="0ef4c-139">-ReplicationFrequencyInSeconds</span></span>
<span data-ttu-id="0ef4c-140">복제 빈도 간격 (초)을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="0ef4c-140">Specifies the frequency interval, in seconds, for replication.</span></span> <span data-ttu-id="0ef4c-141">이 매개 변수에 허용 되는 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="0ef4c-141">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="0ef4c-142">30</span><span class="sxs-lookup"><span data-stu-id="0ef4c-142">30</span></span> 
- <span data-ttu-id="0ef4c-143">300</span><span class="sxs-lookup"><span data-stu-id="0ef4c-143">300</span></span> 
- <span data-ttu-id="0ef4c-144">900</span><span class="sxs-lookup"><span data-stu-id="0ef4c-144">900</span></span>

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

### <span data-ttu-id="0ef4c-145">-ReplicationMethod</span><span class="sxs-lookup"><span data-stu-id="0ef4c-145">-ReplicationMethod</span></span>
<span data-ttu-id="0ef4c-146">복제 방법을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="0ef4c-146">Specifies the replication method.</span></span> <span data-ttu-id="0ef4c-147">이 매개 변수에 허용 되는 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="0ef4c-147">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="0ef4c-148">온라인.</span><span class="sxs-lookup"><span data-stu-id="0ef4c-148">Online.</span></span>
<span data-ttu-id="0ef4c-149">네트워크를 통해 복제.</span><span class="sxs-lookup"><span data-stu-id="0ef4c-149">Replication over the network.</span></span>
- <span data-ttu-id="0ef4c-150">이거나.</span><span class="sxs-lookup"><span data-stu-id="0ef4c-150">Offline.</span></span>

```yaml
Type: String
Parameter Sets: EnterpriseToEnterprise
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0ef4c-151">-ReplicationPort</span><span class="sxs-lookup"><span data-stu-id="0ef4c-151">-ReplicationPort</span></span>
<span data-ttu-id="0ef4c-152">복제를 수행 하는 포트 번호를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="0ef4c-152">Specifies the number of the port on which the replication occurs.</span></span>

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

### <span data-ttu-id="0ef4c-153">-ReplicationProvider</span><span class="sxs-lookup"><span data-stu-id="0ef4c-153">-ReplicationProvider</span></span>
<span data-ttu-id="0ef4c-154">복제 공급자 유형을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="0ef4c-154">Specifies the type of replication provider.</span></span> <span data-ttu-id="0ef4c-155">이 매개 변수에 허용 되는 값은 HyperVReplica 및 HyperVReplicaAzure입니다.</span><span class="sxs-lookup"><span data-stu-id="0ef4c-155">The acceptable values for this parameter are: HyperVReplica and HyperVReplicaAzure.</span></span>

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

### <span data-ttu-id="0ef4c-156">-ReplicationStartTime</span><span class="sxs-lookup"><span data-stu-id="0ef4c-156">-ReplicationStartTime</span></span>
<span data-ttu-id="0ef4c-157">복제 시작 시간을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="0ef4c-157">Specifies the start time of the replication.</span></span>
<span data-ttu-id="0ef4c-158">작업을 시작한 후 24 시간 이내에 시간을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="0ef4c-158">Specify a time within 24 hours after you start the job.</span></span>

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

### <span data-ttu-id="0ef4c-159">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0ef4c-159">CommonParameters</span></span>
<span data-ttu-id="0ef4c-160">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="0ef4c-160">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0ef4c-161">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0ef4c-161">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0ef4c-162">입력</span><span class="sxs-lookup"><span data-stu-id="0ef4c-162">INPUTS</span></span>

## <span data-ttu-id="0ef4c-163">출력</span><span class="sxs-lookup"><span data-stu-id="0ef4c-163">OUTPUTS</span></span>

## <span data-ttu-id="0ef4c-164">상속자</span><span class="sxs-lookup"><span data-stu-id="0ef4c-164">NOTES</span></span>

## <span data-ttu-id="0ef4c-165">관련 링크</span><span class="sxs-lookup"><span data-stu-id="0ef4c-165">RELATED LINKS</span></span>

[<span data-ttu-id="0ef4c-166">Azure Site Recovery 서비스 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="0ef4c-166">Azure Site Recovery Services Cmdlets</span></span>](./Azure.SiteRecoveryServices.md)


