---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Resume-AzureRmRecoveryServicesAsrJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Resume-AzureRmRecoveryServicesAsrJob.md
ms.openlocfilehash: ac3f3c843f13fd500156cf148b5c80436e2e2649
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93533907"
---
# <span data-ttu-id="3633b-101">Resume-AzureRmRecoveryServicesAsrJob</span><span class="sxs-lookup"><span data-stu-id="3633b-101">Resume-AzureRmRecoveryServicesAsrJob</span></span>

## <span data-ttu-id="3633b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3633b-102">SYNOPSIS</span></span>
<span data-ttu-id="3633b-103">일시 중단 된 Azure Site Recovery 작업을 다시 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="3633b-103">Resumes a suspended Azure Site Recovery job.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3633b-104">구문과</span><span class="sxs-lookup"><span data-stu-id="3633b-104">SYNTAX</span></span>

### <span data-ttu-id="3633b-105">ByObject (기본값)</span><span class="sxs-lookup"><span data-stu-id="3633b-105">ByObject (Default)</span></span>
```
Resume-AzureRmRecoveryServicesAsrJob -InputObject <ASRJob> [-Comment <String>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="3633b-106">ByName</span><span class="sxs-lookup"><span data-stu-id="3633b-106">ByName</span></span>
```
Resume-AzureRmRecoveryServicesAsrJob -Name <String> [-Comment <String>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="3633b-107">설명은</span><span class="sxs-lookup"><span data-stu-id="3633b-107">DESCRIPTION</span></span>
<span data-ttu-id="3633b-108">**AzureRmRecoveryServicesAsrJob** cmdlet은 일시 중단 된 Azure Site Recovery 작업을 다시 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="3633b-108">The **Resume-AzureRmRecoveryServicesAsrJob** cmdlet resumes a suspended Azure Site Recovery job.</span></span>

## <span data-ttu-id="3633b-109">예제의</span><span class="sxs-lookup"><span data-stu-id="3633b-109">EXAMPLES</span></span>

### <span data-ttu-id="3633b-110">예제 1</span><span class="sxs-lookup"><span data-stu-id="3633b-110">Example 1</span></span>
```
PS C:\> $currentJob = Resume-AzureRmRecoveryServicesAsrJob -Job $Job
```

<span data-ttu-id="3633b-111">대기 또는 일시 중단 상태에 있는 경우 지정 된 작업을 다시 시작 하 고 ASR 작업에 해당 하는 업데이트 된 ASR 작업 개체를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="3633b-111">Resume the specified job if it is in a waiting or suspended state and return the updated ASR job object corresponding to the ASR job.</span></span>

## <span data-ttu-id="3633b-112">변수</span><span class="sxs-lookup"><span data-stu-id="3633b-112">PARAMETERS</span></span>

### <span data-ttu-id="3633b-113">-메모</span><span class="sxs-lookup"><span data-stu-id="3633b-113">-Comment</span></span>
<span data-ttu-id="3633b-114">작업 로그에 대 한 설명입니다.</span><span class="sxs-lookup"><span data-stu-id="3633b-114">Comments for the job log.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Comments

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3633b-115">-InputObject</span><span class="sxs-lookup"><span data-stu-id="3633b-115">-InputObject</span></span>
<span data-ttu-id="3633b-116">Cmdlet에 대 한 입력 개체: 다시 시작할 작업에 해당 하는 ASR 작업 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="3633b-116">The input object to the cmdlet: The ASR Job object corresponding to the job to be resumed.</span></span>

```yaml
Type: ASRJob
Parameter Sets: ByObject
Aliases: Job

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="3633b-117">-이름</span><span class="sxs-lookup"><span data-stu-id="3633b-117">-Name</span></span>
<span data-ttu-id="3633b-118">이름으로 ASR 작업을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="3633b-118">Specify the ASR job by name.</span></span>

```yaml
Type: String
Parameter Sets: ByName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3633b-119">-확인</span><span class="sxs-lookup"><span data-stu-id="3633b-119">-Confirm</span></span>
<span data-ttu-id="3633b-120">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="3633b-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3633b-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3633b-121">-WhatIf</span></span>
<span data-ttu-id="3633b-122">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="3633b-122">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="3633b-123">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="3633b-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3633b-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3633b-124">CommonParameters</span></span>
<span data-ttu-id="3633b-125">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="3633b-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3633b-126">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3633b-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3633b-127">입력</span><span class="sxs-lookup"><span data-stu-id="3633b-127">INPUTS</span></span>

### <span data-ttu-id="3633b-128">SiteRecovery. r i m m 작업</span><span class="sxs-lookup"><span data-stu-id="3633b-128">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="3633b-129">출력</span><span class="sxs-lookup"><span data-stu-id="3633b-129">OUTPUTS</span></span>

### <span data-ttu-id="3633b-130">SiteRecovery. r i m m 작업</span><span class="sxs-lookup"><span data-stu-id="3633b-130">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="3633b-131">상속자</span><span class="sxs-lookup"><span data-stu-id="3633b-131">NOTES</span></span>

## <span data-ttu-id="3633b-132">관련 링크</span><span class="sxs-lookup"><span data-stu-id="3633b-132">RELATED LINKS</span></span>

[<span data-ttu-id="3633b-133">Get-AzureRmRecoveryServicesAsrJob</span><span class="sxs-lookup"><span data-stu-id="3633b-133">Get-AzureRmRecoveryServicesAsrJob</span></span>](./Get-AzureRmRecoveryServicesAsrJob.md)

[<span data-ttu-id="3633b-134">다시 시작-AzureRmRecoveryServicesAsrJob</span><span class="sxs-lookup"><span data-stu-id="3633b-134">Restart-AzureRmRecoveryServicesAsrJob</span></span>](./Restart-AzureRmRecoveryServicesAsrJob.md)

[<span data-ttu-id="3633b-135">중지-AzureRmRecoveryServicesAsrJob</span><span class="sxs-lookup"><span data-stu-id="3633b-135">Stop-AzureRmRecoveryServicesAsrJob</span></span>](./Stop-AzureRmRecoveryServicesAsrJob.md)
