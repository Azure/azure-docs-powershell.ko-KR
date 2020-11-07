---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM.SiteRecovery
ms.assetid: 85C543FE-BBC1-4A1B-9974-1D3BF520085C
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/New-AzureRmSiteRecoveryPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/New-AzureRmSiteRecoveryPolicy.md
ms.openlocfilehash: e876e1a7beeee19cd68ac629eb08d48356f98da8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93711223"
---
# <span data-ttu-id="f1d24-101">New-AzureRmSiteRecoveryPolicy</span><span class="sxs-lookup"><span data-stu-id="f1d24-101">New-AzureRmSiteRecoveryPolicy</span></span>

## <span data-ttu-id="f1d24-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f1d24-102">SYNOPSIS</span></span>
<span data-ttu-id="f1d24-103">사이트 복구 복제 정책을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="f1d24-103">Creates a Site Recovery replication policy.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f1d24-104">구문과</span><span class="sxs-lookup"><span data-stu-id="f1d24-104">SYNTAX</span></span>

### <span data-ttu-id="f1d24-105">EnterpriseToAzure (기본값)</span><span class="sxs-lookup"><span data-stu-id="f1d24-105">EnterpriseToAzure (Default)</span></span>
```
New-AzureRmSiteRecoveryPolicy -Name <String> -ReplicationProvider <String>
 -ReplicationFrequencyInSeconds <String> [-RecoveryPoints <Int32>]
 [-ApplicationConsistentSnapshotFrequencyInHours <Int32>] [-ReplicationStartTime <TimeSpan>]
 [-RecoveryAzureStorageAccountId <String>] [-Encryption <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="f1d24-106">Enterprise엔터프라이즈</span><span class="sxs-lookup"><span data-stu-id="f1d24-106">EnterpriseToEnterprise</span></span>
```
New-AzureRmSiteRecoveryPolicy -Name <String> -ReplicationProvider <String> [-ReplicationMethod <String>]
 -ReplicationFrequencyInSeconds <String> [-RecoveryPoints <Int32>]
 [-ApplicationConsistentSnapshotFrequencyInHours <Int32>] [-Compression <String>] -ReplicationPort <UInt16>
 [-Authentication <String>] [-ReplicationStartTime <TimeSpan>] [-ReplicaDeletion <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f1d24-107">설명은</span><span class="sxs-lookup"><span data-stu-id="f1d24-107">DESCRIPTION</span></span>
<span data-ttu-id="f1d24-108">**새 AzureRmSiteRecoveryPolicy** Cmdlet은 Azure Site Recovery 복제 정책을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="f1d24-108">The **New-AzureRmSiteRecoveryPolicy** cmdlet creates an Azure Site Recovery replication policy.</span></span>
<span data-ttu-id="f1d24-109">복제 정책은 복제 빈도 및 복구 지점 수와 같은 복제 설정을 지정 하는 데 사용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="f1d24-109">The replication policy is used to specify replication settings such as the replication frequency and number of recovery points.</span></span>

## <span data-ttu-id="f1d24-110">예제의</span><span class="sxs-lookup"><span data-stu-id="f1d24-110">EXAMPLES</span></span>

## <span data-ttu-id="f1d24-111">변수</span><span class="sxs-lookup"><span data-stu-id="f1d24-111">PARAMETERS</span></span>

### <span data-ttu-id="f1d24-112">-ApplicationConsistentSnapshotFrequencyInHours</span><span class="sxs-lookup"><span data-stu-id="f1d24-112">-ApplicationConsistentSnapshotFrequencyInHours</span></span>
<span data-ttu-id="f1d24-113">응용 프로그램의 일관 된 스냅숏 빈도 (시간)를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="f1d24-113">Specifies the frequency of the application consistent snapshot in hours.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f1d24-114">-인증</span><span class="sxs-lookup"><span data-stu-id="f1d24-114">-Authentication</span></span>
<span data-ttu-id="f1d24-115">사용 되는 인증 유형을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="f1d24-115">Specifies the type of authentication used.</span></span>
<span data-ttu-id="f1d24-116">유효한 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="f1d24-116">Valid values are:</span></span>

- <span data-ttu-id="f1d24-117">인증</span><span class="sxs-lookup"><span data-stu-id="f1d24-117">Certificate</span></span>
-  <span data-ttu-id="f1d24-118">커버로스</span><span class="sxs-lookup"><span data-stu-id="f1d24-118">Kerberos</span></span>

```yaml
Type: System.String
Parameter Sets: EnterpriseToEnterprise
Aliases: 
Accepted values: Certificate, Kerberos

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f1d24-119">-압축</span><span class="sxs-lookup"><span data-stu-id="f1d24-119">-Compression</span></span>
```yaml
Type: System.String
Parameter Sets: EnterpriseToEnterprise
Aliases: 
Accepted values: Enable, Disable

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f1d24-120">-암호화</span><span class="sxs-lookup"><span data-stu-id="f1d24-120">-Encryption</span></span>
```yaml
Type: System.String
Parameter Sets: EnterpriseToAzure
Aliases: 
Accepted values: Enable, Disable

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f1d24-121">-이름</span><span class="sxs-lookup"><span data-stu-id="f1d24-121">-Name</span></span>
<span data-ttu-id="f1d24-122">사이트 복구 복제 정책을 식별 하는 친근 한 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="f1d24-122">Specifies a friendly name which identifies the Site Recovery replication policy.</span></span>

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

### <span data-ttu-id="f1d24-123">-RecoveryAzureStorageAccountId</span><span class="sxs-lookup"><span data-stu-id="f1d24-123">-RecoveryAzureStorageAccountId</span></span>
<span data-ttu-id="f1d24-124">복제 대상의 Azure storage 계정 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="f1d24-124">Specifies the Azure storage account ID of the replication target.</span></span>

```yaml
Type: System.String
Parameter Sets: EnterpriseToAzure
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f1d24-125">-RecoveryPoints</span><span class="sxs-lookup"><span data-stu-id="f1d24-125">-RecoveryPoints</span></span>
<span data-ttu-id="f1d24-126">복구 지점을 유지 하는 데 소요 되는 시간 (초)을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="f1d24-126">Specifies the number of hours to retain recovery points.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f1d24-127">-ReplicaDeletion</span><span class="sxs-lookup"><span data-stu-id="f1d24-127">-ReplicaDeletion</span></span>
```yaml
Type: System.String
Parameter Sets: EnterpriseToEnterprise
Aliases: 
Accepted values: Required, NotRequired

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f1d24-128">-ReplicationFrequencyInSeconds</span><span class="sxs-lookup"><span data-stu-id="f1d24-128">-ReplicationFrequencyInSeconds</span></span>
<span data-ttu-id="f1d24-129">복제 빈도 간격 (초)을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="f1d24-129">Specifies the replication frequency interval in seconds.</span></span>
<span data-ttu-id="f1d24-130">유효한 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="f1d24-130">Valid values are:</span></span>

- <span data-ttu-id="f1d24-131">30</span><span class="sxs-lookup"><span data-stu-id="f1d24-131">30</span></span>
- <span data-ttu-id="f1d24-132">300</span><span class="sxs-lookup"><span data-stu-id="f1d24-132">300</span></span>
- <span data-ttu-id="f1d24-133">900</span><span class="sxs-lookup"><span data-stu-id="f1d24-133">900</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 
Accepted values: 30, 300, 900

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f1d24-134">-ReplicationMethod</span><span class="sxs-lookup"><span data-stu-id="f1d24-134">-ReplicationMethod</span></span>
<span data-ttu-id="f1d24-135">복제 방법을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="f1d24-135">Specifies the replication method.</span></span>
<span data-ttu-id="f1d24-136">유효한 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="f1d24-136">Valid values are:</span></span>

- <span data-ttu-id="f1d24-137">온라인</span><span class="sxs-lookup"><span data-stu-id="f1d24-137">Online</span></span>
- <span data-ttu-id="f1d24-138">이거나</span><span class="sxs-lookup"><span data-stu-id="f1d24-138">Offline</span></span>

```yaml
Type: System.String
Parameter Sets: EnterpriseToEnterprise
Aliases: 
Accepted values: Online, Offline

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f1d24-139">-ReplicationPort</span><span class="sxs-lookup"><span data-stu-id="f1d24-139">-ReplicationPort</span></span>
<span data-ttu-id="f1d24-140">복제에 사용 되는 포트를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="f1d24-140">Specifies the port used for replication.</span></span>

```yaml
Type: System.UInt16
Parameter Sets: EnterpriseToEnterprise
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f1d24-141">-ReplicationProvider</span><span class="sxs-lookup"><span data-stu-id="f1d24-141">-ReplicationProvider</span></span>
<span data-ttu-id="f1d24-142">복제 공급자를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="f1d24-142">Specifies the replication provider.</span></span>
<span data-ttu-id="f1d24-143">유효한 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="f1d24-143">Valid values are:</span></span>

- <span data-ttu-id="f1d24-144">HyperVReplica2012R2</span><span class="sxs-lookup"><span data-stu-id="f1d24-144">HyperVReplica2012R2</span></span>
- <span data-ttu-id="f1d24-145">HyperVReplica2012</span><span class="sxs-lookup"><span data-stu-id="f1d24-145">HyperVReplica2012</span></span>
- <span data-ttu-id="f1d24-146">HyperVReplicaAzure</span><span class="sxs-lookup"><span data-stu-id="f1d24-146">HyperVReplicaAzure</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 
Accepted values: HyperVReplica2012R2, HyperVReplica2012, HyperVReplicaAzure

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f1d24-147">-ReplicationStartTime</span><span class="sxs-lookup"><span data-stu-id="f1d24-147">-ReplicationStartTime</span></span>
<span data-ttu-id="f1d24-148">복제 시작 시간을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="f1d24-148">Specifies the replication start time.</span></span>
<span data-ttu-id="f1d24-149">작업의 시작 부분에서 24 시간 이상 이어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="f1d24-149">It must be no later than 24-hours from the start of the job.</span></span>

```yaml
Type: System.Nullable`1[System.TimeSpan]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f1d24-150">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f1d24-150">-DefaultProfile</span></span>
<span data-ttu-id="f1d24-151">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="f1d24-151">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f1d24-152">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f1d24-152">CommonParameters</span></span>
<span data-ttu-id="f1d24-153">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="f1d24-153">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f1d24-154">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f1d24-154">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f1d24-155">입력</span><span class="sxs-lookup"><span data-stu-id="f1d24-155">INPUTS</span></span>

## <span data-ttu-id="f1d24-156">출력</span><span class="sxs-lookup"><span data-stu-id="f1d24-156">OUTPUTS</span></span>

## <span data-ttu-id="f1d24-157">상속자</span><span class="sxs-lookup"><span data-stu-id="f1d24-157">NOTES</span></span>

## <span data-ttu-id="f1d24-158">관련 링크</span><span class="sxs-lookup"><span data-stu-id="f1d24-158">RELATED LINKS</span></span>

[<span data-ttu-id="f1d24-159">Get-AzureRmSiteRecoveryPolicy</span><span class="sxs-lookup"><span data-stu-id="f1d24-159">Get-AzureRmSiteRecoveryPolicy</span></span>](./Get-AzureRmSiteRecoveryPolicy.md)

[<span data-ttu-id="f1d24-160">제거-AzureRmSiteRecoveryPolicy</span><span class="sxs-lookup"><span data-stu-id="f1d24-160">Remove-AzureRmSiteRecoveryPolicy</span></span>](./Remove-AzureRmSiteRecoveryPolicy.md)
