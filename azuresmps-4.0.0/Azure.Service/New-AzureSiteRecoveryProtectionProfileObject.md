---
external help file: Microsoft.Azure.Commands.RecoveryServicesRdfe.dll-Help.xml
ms.assetid: 853D5585-2A92-4B65-BA8C-EC06BEE8C237
online version: ''
schema: 2.0.0
ms.openlocfilehash: d7681631d98f80def1076a04ab57f1774bad245c
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/14/2021
ms.locfileid: "100403649"
---
# <span data-ttu-id="c909e-101">New-AzureSiteRecoveryProtectionProfileObject</span><span class="sxs-lookup"><span data-stu-id="c909e-101">New-AzureSiteRecoveryProtectionProfileObject</span></span>

## <span data-ttu-id="c909e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c909e-102">SYNOPSIS</span></span>
<span data-ttu-id="c909e-103">Site Recovery 보호 프로필 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="c909e-103">Creates a Site Recovery protection profile object.</span></span>

## <span data-ttu-id="c909e-104">구문</span><span class="sxs-lookup"><span data-stu-id="c909e-104">SYNTAX</span></span>

### <span data-ttu-id="c909e-105">EnterpriseToAzure(기본값)</span><span class="sxs-lookup"><span data-stu-id="c909e-105">EnterpriseToAzure (Default)</span></span>
```
New-AzureSiteRecoveryProtectionProfileObject [-Name <String>] -ReplicationProvider <String>
 -RecoveryAzureSubscription <String> -RecoveryAzureStorageAccount <String>
 -ReplicationFrequencyInSeconds <String> [-RecoveryPoints <Int32>]
 [-ApplicationConsistentSnapshotFrequencyInHours <Int32>] [-ReplicationStartTime <TimeSpan>] [-Force]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="c909e-106">EnterpriseToEnterprise</span><span class="sxs-lookup"><span data-stu-id="c909e-106">EnterpriseToEnterprise</span></span>
```
New-AzureSiteRecoveryProtectionProfileObject [-Name <String>] -ReplicationProvider <String>
 [-ReplicationMethod <String>] -ReplicationFrequencyInSeconds <String> [-RecoveryPoints <Int32>]
 [-ApplicationConsistentSnapshotFrequencyInHours <Int32>] [-CompressionEnabled] -ReplicationPort <UInt16>
 [-Authentication <String>] [-ReplicationStartTime <TimeSpan>] [-AllowReplicaDeletion] [-Force]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="c909e-107">설명</span><span class="sxs-lookup"><span data-stu-id="c909e-107">DESCRIPTION</span></span>
<span data-ttu-id="c909e-108">**New-AzureSiteRecoveryProtectionProfileObject** cmdlet은 Azure Site Recovery 보호 프로필 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="c909e-108">The **New-AzureSiteRecoveryProtectionProfileObject** cmdlet creates an Azure Site Recovery protection profile object.</span></span>
<span data-ttu-id="c909e-109">이 cmdlet은 다른 cmdlet과 함께 사용할 **ASRProtectionProfile** 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="c909e-109">This cmdlet creates an **ASRProtectionProfile** object to use with other cmdlets.</span></span>

## <span data-ttu-id="c909e-110">예제</span><span class="sxs-lookup"><span data-stu-id="c909e-110">EXAMPLES</span></span>

### <span data-ttu-id="c909e-111">예제 1: 보호 프로필 만들기</span><span class="sxs-lookup"><span data-stu-id="c909e-111">Example 1: Create a protection profile</span></span>
```
PS C:\> New-AzureSiteRecoveryProtectionProfileObject -ReplicationProvider "HyperVReplica" -AllowReplicaDeletion -ApplicationConsistentSnapshotFrequencyInHours 1 -CompressionEnabled -RecoveryPoints 2 -ReplicationFrequencyInSeconds 30 -ReplicationMethod "Online" -ReplicationPort 8085 -ReplicationStartTime 1
Name                                     : 
ID                                       : 
ReplicationProvider                      : HyperVReplica
HyperVReplicaProviderSettingsObject      : Microsoft.Azure.Portal.RecoveryServices.Models.Common.HyperVReplicaProviderSettings
HyperVReplicaAzureProviderSettingsObject :
```

<span data-ttu-id="c909e-112">이 명령은 보호 프로필 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="c909e-112">This command creates a protection profile object.</span></span>

### <span data-ttu-id="c909e-113">예제 2: HyperVReplicaAzure 공급자에 대한 보호 프로필 만들기</span><span class="sxs-lookup"><span data-stu-id="c909e-113">Example 2: Create a protection profile for HyperVReplicaAzure provider</span></span>
```
PS C:\> New-AzureSiteRecoveryProtectionProfileObject -Name "ProtectionProfile" -ReplicationProvider "HyperVReplicaAzure" -RecoveryAzureSubscription "cb53d0c3-bd59-4721-89bc-06916a9147ef" -RecoveryAzureStorageAccount "Contoso01" -ReplicationFrequencyInSeconds 30 -RecoveryPoints 1 -Force
Name                                     : ProtectionProfile
ID                                       : 
ReplicationProvider                      : HyperVReplicaAzure
HyperVReplicaProviderSettingsObject      : 
HyperVReplicaAzureProviderSettingsObject : Microsoft.Azure.Portal.RecoveryServices.Models.Common.HyperVReplicaAzureProviderSettings
```

<span data-ttu-id="c909e-114">이 명령은 HyperVReplicaAzure 공급자에 대한 보호 프로필을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="c909e-114">This command creates a protection profile for a HyperVReplicaAzure provider.</span></span>

## <span data-ttu-id="c909e-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c909e-115">PARAMETERS</span></span>

### <span data-ttu-id="c909e-116">-AllowReplicaDeletion</span><span class="sxs-lookup"><span data-stu-id="c909e-116">-AllowReplicaDeletion</span></span>
<span data-ttu-id="c909e-117">보호 프로필을 통해 복제본 엔터티를 삭제할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c909e-117">Indicates that the protection profile enables deletion of replica entities.</span></span>

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

### <span data-ttu-id="c909e-118">-ApplicationConsistentSnapshotFrequencyInHours</span><span class="sxs-lookup"><span data-stu-id="c909e-118">-ApplicationConsistentSnapshotFrequencyInHours</span></span>
<span data-ttu-id="c909e-119">애플리케이션 일치 스냅숏의 빈도(시간)를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="c909e-119">Specifies the frequency, in hours, for application consistent snapshots.</span></span>

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

### <span data-ttu-id="c909e-120">-Authentication</span><span class="sxs-lookup"><span data-stu-id="c909e-120">-Authentication</span></span>
<span data-ttu-id="c909e-121">사용할 인증 유형을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="c909e-121">Specifies the type of authentication to use.</span></span>
<span data-ttu-id="c909e-122">이 매개 변수에 허용되는 값은 인증서 및 Kerberos입니다.</span><span class="sxs-lookup"><span data-stu-id="c909e-122">The acceptable values for this parameter are: Certificate and Kerberos.</span></span>

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

### <span data-ttu-id="c909e-123">-CompressionEnabled</span><span class="sxs-lookup"><span data-stu-id="c909e-123">-CompressionEnabled</span></span>
<span data-ttu-id="c909e-124">보호 프로필이 압축을 사용할 수 있도록 하여 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="c909e-124">Indicates that the protection profile enables compression.</span></span>

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

### <span data-ttu-id="c909e-125">-Force</span><span class="sxs-lookup"><span data-stu-id="c909e-125">-Force</span></span>
<span data-ttu-id="c909e-126">사용자 확인을 요청하지 않고 명령을 강제로 실행합니다.</span><span class="sxs-lookup"><span data-stu-id="c909e-126">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="c909e-127">-Name</span><span class="sxs-lookup"><span data-stu-id="c909e-127">-Name</span></span>
<span data-ttu-id="c909e-128">보호 프로필의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="c909e-128">Specifies a name for the protection profile.</span></span>

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

### <span data-ttu-id="c909e-129">-Profile</span><span class="sxs-lookup"><span data-stu-id="c909e-129">-Profile</span></span>
<span data-ttu-id="c909e-130">이 cmdlet이 읽을 Azure 프로필을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="c909e-130">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="c909e-131">프로필을 지정하지 않으면 이 cmdlet은 로컬 기본 프로필에서 읽습니다.</span><span class="sxs-lookup"><span data-stu-id="c909e-131">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="c909e-132">-RecoveryAzureStorageAccount</span><span class="sxs-lookup"><span data-stu-id="c909e-132">-RecoveryAzureStorageAccount</span></span>
<span data-ttu-id="c909e-133">Azure 복제본 엔터티를 저장할 Azure Storage 계정의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="c909e-133">Specifies the name of an Azure Storage account on which to store the Azure replica entity.</span></span>

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

### <span data-ttu-id="c909e-134">-RecoveryAzureSubscription</span><span class="sxs-lookup"><span data-stu-id="c909e-134">-RecoveryAzureSubscription</span></span>
<span data-ttu-id="c909e-135">저장소 계정에 대한 Azure 구독의 ID를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="c909e-135">Specifies the ID for an Azure Subscription for a storage account.</span></span>
<span data-ttu-id="c909e-136">이 매개 변수는 Azure 복제본 엔터티를 저장할 계정을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="c909e-136">This parameter refers to the account on which to store the Azure replica entity.</span></span>

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

### <span data-ttu-id="c909e-137">-RecoveryPoints</span><span class="sxs-lookup"><span data-stu-id="c909e-137">-RecoveryPoints</span></span>
<span data-ttu-id="c909e-138">복구 지점을 유지할 시간을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="c909e-138">Specifies the number of hours to retain recovery points.</span></span>

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

### <span data-ttu-id="c909e-139">-ReplicationFrequencyInSeconds</span><span class="sxs-lookup"><span data-stu-id="c909e-139">-ReplicationFrequencyInSeconds</span></span>
<span data-ttu-id="c909e-140">복제에 대한 빈도 간격(초)을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="c909e-140">Specifies the frequency interval, in seconds, for replication.</span></span> <span data-ttu-id="c909e-141">이 매개 변수에 허용되는 값은</span><span class="sxs-lookup"><span data-stu-id="c909e-141">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="c909e-142">30</span><span class="sxs-lookup"><span data-stu-id="c909e-142">30</span></span> 
- <span data-ttu-id="c909e-143">300</span><span class="sxs-lookup"><span data-stu-id="c909e-143">300</span></span> 
- <span data-ttu-id="c909e-144">900</span><span class="sxs-lookup"><span data-stu-id="c909e-144">900</span></span>

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

### <span data-ttu-id="c909e-145">-ReplicationMethod</span><span class="sxs-lookup"><span data-stu-id="c909e-145">-ReplicationMethod</span></span>
<span data-ttu-id="c909e-146">복제 방법을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="c909e-146">Specifies the replication method.</span></span> <span data-ttu-id="c909e-147">이 매개 변수에 허용되는 값은</span><span class="sxs-lookup"><span data-stu-id="c909e-147">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="c909e-148">온라인.</span><span class="sxs-lookup"><span data-stu-id="c909e-148">Online.</span></span>
<span data-ttu-id="c909e-149">네트워크를 통해 복제합니다.</span><span class="sxs-lookup"><span data-stu-id="c909e-149">Replication over the network.</span></span>
- <span data-ttu-id="c909e-150">오프라인.</span><span class="sxs-lookup"><span data-stu-id="c909e-150">Offline.</span></span>

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

### <span data-ttu-id="c909e-151">-ReplicationPort</span><span class="sxs-lookup"><span data-stu-id="c909e-151">-ReplicationPort</span></span>
<span data-ttu-id="c909e-152">복제가 발생하는 포트의 수를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="c909e-152">Specifies the number of the port on which the replication occurs.</span></span>

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

### <span data-ttu-id="c909e-153">-ReplicationProvider</span><span class="sxs-lookup"><span data-stu-id="c909e-153">-ReplicationProvider</span></span>
<span data-ttu-id="c909e-154">복제 공급자의 유형을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="c909e-154">Specifies the type of replication provider.</span></span> <span data-ttu-id="c909e-155">이 매개 변수에 허용되는 값은 HyperVReplica 및 HyperVReplicaAzure입니다.</span><span class="sxs-lookup"><span data-stu-id="c909e-155">The acceptable values for this parameter are: HyperVReplica and HyperVReplicaAzure.</span></span>

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

### <span data-ttu-id="c909e-156">-ReplicationStartTime</span><span class="sxs-lookup"><span data-stu-id="c909e-156">-ReplicationStartTime</span></span>
<span data-ttu-id="c909e-157">복제의 시작 시간을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="c909e-157">Specifies the start time of the replication.</span></span>
<span data-ttu-id="c909e-158">작업을 시작한 후 24시간 이내에 시간을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="c909e-158">Specify a time within 24 hours after you start the job.</span></span>

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

### <span data-ttu-id="c909e-159">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c909e-159">CommonParameters</span></span>
<span data-ttu-id="c909e-160">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="c909e-160">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c909e-161">자세한 내용은 다음 about_CommonParameters https://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="c909e-161">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c909e-162">입력</span><span class="sxs-lookup"><span data-stu-id="c909e-162">INPUTS</span></span>

## <span data-ttu-id="c909e-163">출력</span><span class="sxs-lookup"><span data-stu-id="c909e-163">OUTPUTS</span></span>

## <span data-ttu-id="c909e-164">참고 사항</span><span class="sxs-lookup"><span data-stu-id="c909e-164">NOTES</span></span>

## <span data-ttu-id="c909e-165">관련 링크</span><span class="sxs-lookup"><span data-stu-id="c909e-165">RELATED LINKS</span></span>




