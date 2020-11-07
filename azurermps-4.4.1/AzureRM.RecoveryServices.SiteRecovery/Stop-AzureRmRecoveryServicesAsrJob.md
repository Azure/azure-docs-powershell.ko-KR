---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Stop-AzureRmRecoveryServicesAsrJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Stop-AzureRmRecoveryServicesAsrJob.md
ms.openlocfilehash: e639e6fc42e440b5088a34ee29e21d324ed7d235
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93703650"
---
# <span data-ttu-id="29b64-101">Stop-AzureRmRecoveryServicesAsrJob</span><span class="sxs-lookup"><span data-stu-id="29b64-101">Stop-AzureRmRecoveryServicesAsrJob</span></span>

## <span data-ttu-id="29b64-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="29b64-102">SYNOPSIS</span></span>
<span data-ttu-id="29b64-103">Azure Site Recovery 작업을 중지 합니다.</span><span class="sxs-lookup"><span data-stu-id="29b64-103">Stops an Azure Site Recovery job.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="29b64-104">구문과</span><span class="sxs-lookup"><span data-stu-id="29b64-104">SYNTAX</span></span>

### <span data-ttu-id="29b64-105">ByObject (기본값)</span><span class="sxs-lookup"><span data-stu-id="29b64-105">ByObject (Default)</span></span>
```
Stop-AzureRmRecoveryServicesAsrJob -InputObject <ASRJob> [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="29b64-106">ByName</span><span class="sxs-lookup"><span data-stu-id="29b64-106">ByName</span></span>
```
Stop-AzureRmRecoveryServicesAsrJob -Name <String> [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="29b64-107">설명은</span><span class="sxs-lookup"><span data-stu-id="29b64-107">DESCRIPTION</span></span>
<span data-ttu-id="29b64-108">**AzureRmRecoveryServicesAsrJob** cmdlet은 지정 된 Azure Site Recovery 작업을 중지 합니다.</span><span class="sxs-lookup"><span data-stu-id="29b64-108">The **Stop-AzureRmRecoveryServicesAsrJob** cmdlet stops the specified Azure Site Recovery job.</span></span>

## <span data-ttu-id="29b64-109">예제의</span><span class="sxs-lookup"><span data-stu-id="29b64-109">EXAMPLES</span></span>

### <span data-ttu-id="29b64-110">예제 1</span><span class="sxs-lookup"><span data-stu-id="29b64-110">Example 1</span></span>
```
PS C:\> $currentJob = Stop-AzureRmRecoveryServicesAsrJob -Job $Job
```

<span data-ttu-id="29b64-111">지정 된 작업을 중지 하려고 시도 하 고 업데이트 된 ASR 작업 개체를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="29b64-111">Attempts to stop the specified job and returns an updated ASR job object.</span></span>

## <span data-ttu-id="29b64-112">변수</span><span class="sxs-lookup"><span data-stu-id="29b64-112">PARAMETERS</span></span>

### <span data-ttu-id="29b64-113">-InputObject</span><span class="sxs-lookup"><span data-stu-id="29b64-113">-InputObject</span></span>
<span data-ttu-id="29b64-114">Input 개체: 중지 될 ASR 작업에 해당 하는 ASR 작업 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="29b64-114">Input Object: Specify the ASR job object corresponding to the ASR job to be stopped</span></span>

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

### <span data-ttu-id="29b64-115">-이름</span><span class="sxs-lookup"><span data-stu-id="29b64-115">-Name</span></span>
<span data-ttu-id="29b64-116">ASR 작업 이름으로 중지할 ASR 작업을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="29b64-116">Specify the ASR Job to be stopped by the ASR job name.</span></span>

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

### <span data-ttu-id="29b64-117">-확인</span><span class="sxs-lookup"><span data-stu-id="29b64-117">-Confirm</span></span>
<span data-ttu-id="29b64-118">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="29b64-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="29b64-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="29b64-119">-WhatIf</span></span>
<span data-ttu-id="29b64-120">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="29b64-120">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="29b64-121">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="29b64-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="29b64-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="29b64-122">CommonParameters</span></span>
<span data-ttu-id="29b64-123">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="29b64-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="29b64-124">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="29b64-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="29b64-125">입력</span><span class="sxs-lookup"><span data-stu-id="29b64-125">INPUTS</span></span>

### <span data-ttu-id="29b64-126">SiteRecovery. r i m m 작업</span><span class="sxs-lookup"><span data-stu-id="29b64-126">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="29b64-127">출력</span><span class="sxs-lookup"><span data-stu-id="29b64-127">OUTPUTS</span></span>

### <span data-ttu-id="29b64-128">SiteRecovery. r i m m 작업</span><span class="sxs-lookup"><span data-stu-id="29b64-128">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="29b64-129">상속자</span><span class="sxs-lookup"><span data-stu-id="29b64-129">NOTES</span></span>

## <span data-ttu-id="29b64-130">관련 링크</span><span class="sxs-lookup"><span data-stu-id="29b64-130">RELATED LINKS</span></span>

[<span data-ttu-id="29b64-131">Get-AzureRmRecoveryServicesAsrJob</span><span class="sxs-lookup"><span data-stu-id="29b64-131">Get-AzureRmRecoveryServicesAsrJob</span></span>](./Get-AzureRmRecoveryServicesAsrJob.md)

[<span data-ttu-id="29b64-132">다시 시작-AzureRmRecoveryServicesAsrJob</span><span class="sxs-lookup"><span data-stu-id="29b64-132">Restart-AzureRmRecoveryServicesAsrJob</span></span>](./Restart-AzureRmRecoveryServicesAsrJob.md)

[<span data-ttu-id="29b64-133">이력서-AzureRmRecoveryServicesAsrJob</span><span class="sxs-lookup"><span data-stu-id="29b64-133">Resume-AzureRmRecoveryServicesAsrJob</span></span>](./Resume-AzureRmRecoveryServicesAsrJob.md)
