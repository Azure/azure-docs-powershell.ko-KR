---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Restart-AzureRmRecoveryServicesAsrJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Restart-AzureRmRecoveryServicesAsrJob.md
ms.openlocfilehash: 2f219882199010b2765ebd4386691451d74a182d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93703654"
---
# <span data-ttu-id="1a00e-101">Restart-AzureRmRecoveryServicesAsrJob</span><span class="sxs-lookup"><span data-stu-id="1a00e-101">Restart-AzureRmRecoveryServicesAsrJob</span></span>

## <span data-ttu-id="1a00e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1a00e-102">SYNOPSIS</span></span>
<span data-ttu-id="1a00e-103">Azure Site Recovery 작업을 다시 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="1a00e-103">Restarts an Azure Site Recovery job.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1a00e-104">구문과</span><span class="sxs-lookup"><span data-stu-id="1a00e-104">SYNTAX</span></span>

### <span data-ttu-id="1a00e-105">ByObject (기본값)</span><span class="sxs-lookup"><span data-stu-id="1a00e-105">ByObject (Default)</span></span>
```
Restart-AzureRmRecoveryServicesAsrJob -InputObject <ASRJob> [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1a00e-106">ByName</span><span class="sxs-lookup"><span data-stu-id="1a00e-106">ByName</span></span>
```
Restart-AzureRmRecoveryServicesAsrJob -Name <String> [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1a00e-107">설명은</span><span class="sxs-lookup"><span data-stu-id="1a00e-107">DESCRIPTION</span></span>
<span data-ttu-id="1a00e-108">**AzureRmRecoveryServicesAsrJob** Cmdlet은 Azure Site Recovery 작업을 다시 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="1a00e-108">The **Restart-AzureRmRecoveryServicesAsrJob** cmdlet restarts an Azure Site Recovery job.</span></span>

## <span data-ttu-id="1a00e-109">예제의</span><span class="sxs-lookup"><span data-stu-id="1a00e-109">EXAMPLES</span></span>

### <span data-ttu-id="1a00e-110">예제 1</span><span class="sxs-lookup"><span data-stu-id="1a00e-110">Example 1</span></span>
```
PS C:\> $currentJob = Restart-AzureRmRecoveryServicesAsrJob -Job $Job
```

<span data-ttu-id="1a00e-111">지정 된 ASR 작업을 다시 시작 하 고 ASR 작업의 업데이트 된 ASR 작업 개체를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="1a00e-111">Restarts the specified ASR job and returns the updated ASR job object of the ASR job.</span></span>

## <span data-ttu-id="1a00e-112">변수</span><span class="sxs-lookup"><span data-stu-id="1a00e-112">PARAMETERS</span></span>

### <span data-ttu-id="1a00e-113">-InputObject</span><span class="sxs-lookup"><span data-stu-id="1a00e-113">-InputObject</span></span>
<span data-ttu-id="1a00e-114">Cmdlet에 대 한 입력 개체: 다시 시작할 ASR 작업에 해당 하는 ASR 작업 개체</span><span class="sxs-lookup"><span data-stu-id="1a00e-114">The input object to the cmdlet: The ASR job object corresponding to the ASR job to be restarted</span></span>
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

### <span data-ttu-id="1a00e-115">-이름</span><span class="sxs-lookup"><span data-stu-id="1a00e-115">-Name</span></span>
<span data-ttu-id="1a00e-116">이름을 기준으로 작업을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="1a00e-116">Specify the job by name.</span></span>

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

### <span data-ttu-id="1a00e-117">-확인</span><span class="sxs-lookup"><span data-stu-id="1a00e-117">-Confirm</span></span>
<span data-ttu-id="1a00e-118">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="1a00e-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1a00e-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1a00e-119">-WhatIf</span></span>
<span data-ttu-id="1a00e-120">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="1a00e-120">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="1a00e-121">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="1a00e-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1a00e-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1a00e-122">CommonParameters</span></span>
<span data-ttu-id="1a00e-123">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="1a00e-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1a00e-124">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1a00e-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1a00e-125">입력</span><span class="sxs-lookup"><span data-stu-id="1a00e-125">INPUTS</span></span>

### <span data-ttu-id="1a00e-126">SiteRecovery. r i m m 작업</span><span class="sxs-lookup"><span data-stu-id="1a00e-126">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="1a00e-127">출력</span><span class="sxs-lookup"><span data-stu-id="1a00e-127">OUTPUTS</span></span>

### <span data-ttu-id="1a00e-128">SiteRecovery. r i m m 작업</span><span class="sxs-lookup"><span data-stu-id="1a00e-128">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="1a00e-129">상속자</span><span class="sxs-lookup"><span data-stu-id="1a00e-129">NOTES</span></span>

## <span data-ttu-id="1a00e-130">관련 링크</span><span class="sxs-lookup"><span data-stu-id="1a00e-130">RELATED LINKS</span></span>

[<span data-ttu-id="1a00e-131">Get-AzureRmRecoveryServicesAsrJob</span><span class="sxs-lookup"><span data-stu-id="1a00e-131">Get-AzureRmRecoveryServicesAsrJob</span></span>](./Get-AzureRmRecoveryServicesAsrJob.md)

[<span data-ttu-id="1a00e-132">이력서-AzureRmRecoveryServicesAsrJob</span><span class="sxs-lookup"><span data-stu-id="1a00e-132">Resume-AzureRmRecoveryServicesAsrJob</span></span>](./Resume-AzureRmRecoveryServicesAsrJob.md)

[<span data-ttu-id="1a00e-133">중지-AzureRmRecoveryServicesAsrJob</span><span class="sxs-lookup"><span data-stu-id="1a00e-133">Stop-AzureRmRecoveryServicesAsrJob</span></span>](./Stop-AzureRmRecoveryServicesAsrJob.md)
