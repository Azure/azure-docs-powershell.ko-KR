---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM
ms.assetid: 85C543FE-BBC1-4A1B-9974-1D3BF520085C
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.siterecovery/new-azurermsiterecoverypolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/New-AzureRmSiteRecoveryPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/New-AzureRmSiteRecoveryPolicy.md
ms.openlocfilehash: 65e5e507259198cdacc69ff0764b4f4f18bf9077
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93703967"
---
# <span data-ttu-id="1f703-101">New-AzureRmSiteRecoveryPolicy</span><span class="sxs-lookup"><span data-stu-id="1f703-101">New-AzureRmSiteRecoveryPolicy</span></span>

## <span data-ttu-id="1f703-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1f703-102">SYNOPSIS</span></span>
<span data-ttu-id="1f703-103">사이트 복구 복제 정책을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="1f703-103">Creates a Site Recovery replication policy.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1f703-104">구문과</span><span class="sxs-lookup"><span data-stu-id="1f703-104">SYNTAX</span></span>

### <span data-ttu-id="1f703-105">EnterpriseToAzure (기본값)</span><span class="sxs-lookup"><span data-stu-id="1f703-105">EnterpriseToAzure (Default)</span></span>
```
New-AzureRmSiteRecoveryPolicy -Name <String> -ReplicationProvider <String>
 -ReplicationFrequencyInSeconds <String> [-RecoveryPoints <Int32>]
 [-ApplicationConsistentSnapshotFrequencyInHours <Int32>] [-ReplicationStartTime <TimeSpan>]
 [-RecoveryAzureStorageAccountId <String>] [-Encryption <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="1f703-106">Enterprise엔터프라이즈</span><span class="sxs-lookup"><span data-stu-id="1f703-106">EnterpriseToEnterprise</span></span>
```
New-AzureRmSiteRecoveryPolicy -Name <String> -ReplicationProvider <String> [-ReplicationMethod <String>]
 -ReplicationFrequencyInSeconds <String> [-RecoveryPoints <Int32>]
 [-ApplicationConsistentSnapshotFrequencyInHours <Int32>] [-Compression <String>] -ReplicationPort <UInt16>
 [-Authentication <String>] [-ReplicationStartTime <TimeSpan>] [-ReplicaDeletion <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1f703-107">설명은</span><span class="sxs-lookup"><span data-stu-id="1f703-107">DESCRIPTION</span></span>
<span data-ttu-id="1f703-108">**새 AzureRmSiteRecoveryPolicy** Cmdlet은 Azure Site Recovery 복제 정책을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="1f703-108">The **New-AzureRmSiteRecoveryPolicy** cmdlet creates an Azure Site Recovery replication policy.</span></span>
<span data-ttu-id="1f703-109">복제 정책은 복제 빈도 및 복구 지점 수와 같은 복제 설정을 지정 하는 데 사용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="1f703-109">The replication policy is used to specify replication settings such as the replication frequency and number of recovery points.</span></span>

## <span data-ttu-id="1f703-110">예제의</span><span class="sxs-lookup"><span data-stu-id="1f703-110">EXAMPLES</span></span>

## <span data-ttu-id="1f703-111">변수</span><span class="sxs-lookup"><span data-stu-id="1f703-111">PARAMETERS</span></span>

### <span data-ttu-id="1f703-112">-ApplicationConsistentSnapshotFrequencyInHours</span><span class="sxs-lookup"><span data-stu-id="1f703-112">-ApplicationConsistentSnapshotFrequencyInHours</span></span>
<span data-ttu-id="1f703-113">응용 프로그램의 일관 된 스냅숏 빈도 (시간)를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="1f703-113">Specifies the frequency of the application consistent snapshot in hours.</span></span>

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

### <span data-ttu-id="1f703-114">-인증</span><span class="sxs-lookup"><span data-stu-id="1f703-114">-Authentication</span></span>
<span data-ttu-id="1f703-115">사용 되는 인증 유형을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="1f703-115">Specifies the type of authentication used.</span></span>
<span data-ttu-id="1f703-116">유효한 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="1f703-116">Valid values are:</span></span>

- <span data-ttu-id="1f703-117">인증</span><span class="sxs-lookup"><span data-stu-id="1f703-117">Certificate</span></span>
-  <span data-ttu-id="1f703-118">커버로스</span><span class="sxs-lookup"><span data-stu-id="1f703-118">Kerberos</span></span>

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

### <span data-ttu-id="1f703-119">-압축</span><span class="sxs-lookup"><span data-stu-id="1f703-119">-Compression</span></span>
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

### <span data-ttu-id="1f703-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1f703-120">-DefaultProfile</span></span>
<span data-ttu-id="1f703-121">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="1f703-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1f703-122">-암호화</span><span class="sxs-lookup"><span data-stu-id="1f703-122">-Encryption</span></span>
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

### <span data-ttu-id="1f703-123">-이름</span><span class="sxs-lookup"><span data-stu-id="1f703-123">-Name</span></span>
<span data-ttu-id="1f703-124">사이트 복구 복제 정책을 식별 하는 친근 한 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="1f703-124">Specifies a friendly name which identifies the Site Recovery replication policy.</span></span>

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

### <span data-ttu-id="1f703-125">-RecoveryAzureStorageAccountId</span><span class="sxs-lookup"><span data-stu-id="1f703-125">-RecoveryAzureStorageAccountId</span></span>
<span data-ttu-id="1f703-126">복제 대상의 Azure storage 계정 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="1f703-126">Specifies the Azure storage account ID of the replication target.</span></span>

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

### <span data-ttu-id="1f703-127">-RecoveryPoints</span><span class="sxs-lookup"><span data-stu-id="1f703-127">-RecoveryPoints</span></span>
<span data-ttu-id="1f703-128">복구 지점을 유지 하는 데 소요 되는 시간 (초)을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="1f703-128">Specifies the number of hours to retain recovery points.</span></span>

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

### <span data-ttu-id="1f703-129">-ReplicaDeletion</span><span class="sxs-lookup"><span data-stu-id="1f703-129">-ReplicaDeletion</span></span>
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

### <span data-ttu-id="1f703-130">-ReplicationFrequencyInSeconds</span><span class="sxs-lookup"><span data-stu-id="1f703-130">-ReplicationFrequencyInSeconds</span></span>
<span data-ttu-id="1f703-131">복제 빈도 간격 (초)을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="1f703-131">Specifies the replication frequency interval in seconds.</span></span>
<span data-ttu-id="1f703-132">유효한 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="1f703-132">Valid values are:</span></span>

- <span data-ttu-id="1f703-133">30</span><span class="sxs-lookup"><span data-stu-id="1f703-133">30</span></span>
- <span data-ttu-id="1f703-134">300</span><span class="sxs-lookup"><span data-stu-id="1f703-134">300</span></span>
- <span data-ttu-id="1f703-135">900</span><span class="sxs-lookup"><span data-stu-id="1f703-135">900</span></span>

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

### <span data-ttu-id="1f703-136">-ReplicationMethod</span><span class="sxs-lookup"><span data-stu-id="1f703-136">-ReplicationMethod</span></span>
<span data-ttu-id="1f703-137">복제 방법을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="1f703-137">Specifies the replication method.</span></span>
<span data-ttu-id="1f703-138">유효한 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="1f703-138">Valid values are:</span></span>

- <span data-ttu-id="1f703-139">온라인</span><span class="sxs-lookup"><span data-stu-id="1f703-139">Online</span></span>
- <span data-ttu-id="1f703-140">이거나</span><span class="sxs-lookup"><span data-stu-id="1f703-140">Offline</span></span>

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

### <span data-ttu-id="1f703-141">-ReplicationPort</span><span class="sxs-lookup"><span data-stu-id="1f703-141">-ReplicationPort</span></span>
<span data-ttu-id="1f703-142">복제에 사용 되는 포트를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="1f703-142">Specifies the port used for replication.</span></span>

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

### <span data-ttu-id="1f703-143">-ReplicationProvider</span><span class="sxs-lookup"><span data-stu-id="1f703-143">-ReplicationProvider</span></span>
<span data-ttu-id="1f703-144">복제 공급자를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="1f703-144">Specifies the replication provider.</span></span>
<span data-ttu-id="1f703-145">유효한 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="1f703-145">Valid values are:</span></span>

- <span data-ttu-id="1f703-146">HyperVReplica2012R2</span><span class="sxs-lookup"><span data-stu-id="1f703-146">HyperVReplica2012R2</span></span>
- <span data-ttu-id="1f703-147">HyperVReplica2012</span><span class="sxs-lookup"><span data-stu-id="1f703-147">HyperVReplica2012</span></span>
- <span data-ttu-id="1f703-148">HyperVReplicaAzure</span><span class="sxs-lookup"><span data-stu-id="1f703-148">HyperVReplicaAzure</span></span>

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

### <span data-ttu-id="1f703-149">-ReplicationStartTime</span><span class="sxs-lookup"><span data-stu-id="1f703-149">-ReplicationStartTime</span></span>
<span data-ttu-id="1f703-150">복제 시작 시간을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="1f703-150">Specifies the replication start time.</span></span>
<span data-ttu-id="1f703-151">작업의 시작 부분에서 24 시간 이상 이어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="1f703-151">It must be no later than 24-hours from the start of the job.</span></span>

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

### <span data-ttu-id="1f703-152">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1f703-152">CommonParameters</span></span>
<span data-ttu-id="1f703-153">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="1f703-153">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1f703-154">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1f703-154">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1f703-155">입력</span><span class="sxs-lookup"><span data-stu-id="1f703-155">INPUTS</span></span>

### <span data-ttu-id="1f703-156">않아야</span><span class="sxs-lookup"><span data-stu-id="1f703-156">None</span></span>
<span data-ttu-id="1f703-157">이 cmdlet은 입력을 허용 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="1f703-157">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="1f703-158">출력</span><span class="sxs-lookup"><span data-stu-id="1f703-158">OUTPUTS</span></span>

## <span data-ttu-id="1f703-159">상속자</span><span class="sxs-lookup"><span data-stu-id="1f703-159">NOTES</span></span>

## <span data-ttu-id="1f703-160">관련 링크</span><span class="sxs-lookup"><span data-stu-id="1f703-160">RELATED LINKS</span></span>

[<span data-ttu-id="1f703-161">Get-AzureRmSiteRecoveryPolicy</span><span class="sxs-lookup"><span data-stu-id="1f703-161">Get-AzureRmSiteRecoveryPolicy</span></span>](./Get-AzureRmSiteRecoveryPolicy.md)

[<span data-ttu-id="1f703-162">제거-AzureRmSiteRecoveryPolicy</span><span class="sxs-lookup"><span data-stu-id="1f703-162">Remove-AzureRmSiteRecoveryPolicy</span></span>](./Remove-AzureRmSiteRecoveryPolicy.md)
