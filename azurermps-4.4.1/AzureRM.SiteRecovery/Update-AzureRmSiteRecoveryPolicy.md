---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM.SiteRecovery
ms.assetid: 313E7444-2EB4-4B91-9E56-5730CB006046
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Update-AzureRmSiteRecoveryPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Update-AzureRmSiteRecoveryPolicy.md
ms.openlocfilehash: 5279ca9664c827bdb85b42519f6776c10ab37e31
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93529097"
---
# <span data-ttu-id="381cc-101">Update-AzureRmSiteRecoveryPolicy</span><span class="sxs-lookup"><span data-stu-id="381cc-101">Update-AzureRmSiteRecoveryPolicy</span></span>

## <span data-ttu-id="381cc-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="381cc-102">SYNOPSIS</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="381cc-103">구문과</span><span class="sxs-lookup"><span data-stu-id="381cc-103">SYNTAX</span></span>

```
Update-AzureRmSiteRecoveryPolicy -Policy <ASRPolicy> [-ReplicationMethod <String>]
 [-ReplicationFrequencyInSeconds <String>] [-RecoveryPoints <Int32>]
 [-ApplicationConsistentSnapshotFrequencyInHours <Int32>] [-Compression <String>] [-ReplicationPort <UInt16>]
 [-Authentication <String>] [-ReplicationStartTime <TimeSpan>] [-ReplicaDeletion <String>]
 [-RecoveryAzureStorageAccountId <String>] [-Encryption <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="381cc-104">설명은</span><span class="sxs-lookup"><span data-stu-id="381cc-104">DESCRIPTION</span></span>

## <span data-ttu-id="381cc-105">예제의</span><span class="sxs-lookup"><span data-stu-id="381cc-105">EXAMPLES</span></span>

## <span data-ttu-id="381cc-106">변수</span><span class="sxs-lookup"><span data-stu-id="381cc-106">PARAMETERS</span></span>

### <span data-ttu-id="381cc-107">-ApplicationConsistentSnapshotFrequencyInHours</span><span class="sxs-lookup"><span data-stu-id="381cc-107">-ApplicationConsistentSnapshotFrequencyInHours</span></span>
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

### <span data-ttu-id="381cc-108">-인증</span><span class="sxs-lookup"><span data-stu-id="381cc-108">-Authentication</span></span>
```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 
Accepted values: Certificate, Kerberos

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="381cc-109">-압축</span><span class="sxs-lookup"><span data-stu-id="381cc-109">-Compression</span></span>
```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 
Accepted values: Enable, Disable

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="381cc-110">-암호화</span><span class="sxs-lookup"><span data-stu-id="381cc-110">-Encryption</span></span>
```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 
Accepted values: Enable, Disable

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="381cc-111">-정책</span><span class="sxs-lookup"><span data-stu-id="381cc-111">-Policy</span></span>
```yaml
Type: Microsoft.Azure.Commands.SiteRecovery.ASRPolicy
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="381cc-112">-RecoveryAzureStorageAccountId</span><span class="sxs-lookup"><span data-stu-id="381cc-112">-RecoveryAzureStorageAccountId</span></span>
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

### <span data-ttu-id="381cc-113">-RecoveryPoints</span><span class="sxs-lookup"><span data-stu-id="381cc-113">-RecoveryPoints</span></span>
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

### <span data-ttu-id="381cc-114">-ReplicaDeletion</span><span class="sxs-lookup"><span data-stu-id="381cc-114">-ReplicaDeletion</span></span>
```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 
Accepted values: Required, NotRequired

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="381cc-115">-ReplicationFrequencyInSeconds</span><span class="sxs-lookup"><span data-stu-id="381cc-115">-ReplicationFrequencyInSeconds</span></span>
```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 
Accepted values: 30, 300, 900

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="381cc-116">-ReplicationMethod</span><span class="sxs-lookup"><span data-stu-id="381cc-116">-ReplicationMethod</span></span>
```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 
Accepted values: Online, Offline

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="381cc-117">-ReplicationPort</span><span class="sxs-lookup"><span data-stu-id="381cc-117">-ReplicationPort</span></span>
```yaml
Type: System.UInt16
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="381cc-118">-ReplicationStartTime</span><span class="sxs-lookup"><span data-stu-id="381cc-118">-ReplicationStartTime</span></span>
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

### <span data-ttu-id="381cc-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="381cc-119">-DefaultProfile</span></span>
<span data-ttu-id="381cc-120">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="381cc-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="381cc-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="381cc-121">CommonParameters</span></span>
<span data-ttu-id="381cc-122">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="381cc-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="381cc-123">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="381cc-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="381cc-124">입력</span><span class="sxs-lookup"><span data-stu-id="381cc-124">INPUTS</span></span>

### <span data-ttu-id="381cc-125">ASRPolicy</span><span class="sxs-lookup"><span data-stu-id="381cc-125">ASRPolicy</span></span>
<span data-ttu-id="381cc-126">' Policy ' 매개 변수는 파이프라인에서 ' ASRPolicy ' 형식의 값을 허용 합니다.</span><span class="sxs-lookup"><span data-stu-id="381cc-126">Parameter 'Policy' accepts value of type 'ASRPolicy' from the pipeline</span></span>

## <span data-ttu-id="381cc-127">출력</span><span class="sxs-lookup"><span data-stu-id="381cc-127">OUTPUTS</span></span>

## <span data-ttu-id="381cc-128">상속자</span><span class="sxs-lookup"><span data-stu-id="381cc-128">NOTES</span></span>

## <span data-ttu-id="381cc-129">관련 링크</span><span class="sxs-lookup"><span data-stu-id="381cc-129">RELATED LINKS</span></span>

