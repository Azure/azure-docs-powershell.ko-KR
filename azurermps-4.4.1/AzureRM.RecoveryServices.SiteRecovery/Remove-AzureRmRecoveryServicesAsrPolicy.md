---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Remove-AzureRmRecoveryServicesAsrPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Remove-AzureRmRecoveryServicesAsrPolicy.md
ms.openlocfilehash: 7263601a3f719ce48a43e26ad76f9ba388a058ae
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93529195"
---
# <span data-ttu-id="06c80-101">Remove-AzureRmRecoveryServicesAsrPolicy</span><span class="sxs-lookup"><span data-stu-id="06c80-101">Remove-AzureRmRecoveryServicesAsrPolicy</span></span>

## <span data-ttu-id="06c80-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="06c80-102">SYNOPSIS</span></span>
<span data-ttu-id="06c80-103">복구 서비스 자격 증명 모음에서 지정 된 ASR 복제 정책을 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="06c80-103">Deletes the specified ASR replication policy from the Recovery Services vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="06c80-104">구문과</span><span class="sxs-lookup"><span data-stu-id="06c80-104">SYNTAX</span></span>

```
Remove-AzureRmRecoveryServicesAsrPolicy -InputObject <ASRPolicy> [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="06c80-105">설명은</span><span class="sxs-lookup"><span data-stu-id="06c80-105">DESCRIPTION</span></span>
<span data-ttu-id="06c80-106">**AzureRmRecoveryServicesAsrPolicy** Cmdlet이 복구 서비스 자격 증명 모음에서 지정 된 복제 정책을 삭제 했습니다.</span><span class="sxs-lookup"><span data-stu-id="06c80-106">The **Remove-AzureRmRecoveryServicesAsrPolicy** cmdlet deleted the specified replication policy from the Recovery Services vault.</span></span>

## <span data-ttu-id="06c80-107">예제의</span><span class="sxs-lookup"><span data-stu-id="06c80-107">EXAMPLES</span></span>

### <span data-ttu-id="06c80-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="06c80-108">Example 1</span></span>
```
PS C:\> $currentJob = Remove-AzureRmRecoveryServicesAsrPolicy -Policy $Policy
```

<span data-ttu-id="06c80-109">지정 된 복제 정책의 삭제를 시작 하 고 작업을 추적 하는 데 사용 되는 ASR 작업을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="06c80-109">Starts the deletion of the specified replication policy and returns the ASR job used to track the operation.</span></span>

## <span data-ttu-id="06c80-110">변수</span><span class="sxs-lookup"><span data-stu-id="06c80-110">PARAMETERS</span></span>

### <span data-ttu-id="06c80-111">-InputObject</span><span class="sxs-lookup"><span data-stu-id="06c80-111">-InputObject</span></span>
<span data-ttu-id="06c80-112">Cmdlet에 대 한 입력 개체: 삭제할 복제 정책에 해당 하는 ASR 복제 정책 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="06c80-112">The input object to the cmdlet: The ASR replication policy object corresponding to the replication policy to be deleted.</span></span>

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

### <span data-ttu-id="06c80-113">-확인</span><span class="sxs-lookup"><span data-stu-id="06c80-113">-Confirm</span></span>
<span data-ttu-id="06c80-114">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="06c80-114">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="06c80-115">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="06c80-115">-WhatIf</span></span>
<span data-ttu-id="06c80-116">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="06c80-116">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="06c80-117">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="06c80-117">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="06c80-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="06c80-118">CommonParameters</span></span>
<span data-ttu-id="06c80-119">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="06c80-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="06c80-120">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="06c80-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="06c80-121">입력</span><span class="sxs-lookup"><span data-stu-id="06c80-121">INPUTS</span></span>

### <span data-ttu-id="06c80-122">SiteRecovery. r i m g 정책</span><span class="sxs-lookup"><span data-stu-id="06c80-122">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRPolicy</span></span>

## <span data-ttu-id="06c80-123">출력</span><span class="sxs-lookup"><span data-stu-id="06c80-123">OUTPUTS</span></span>

### <span data-ttu-id="06c80-124">System. 개체</span><span class="sxs-lookup"><span data-stu-id="06c80-124">System.Object</span></span>

## <span data-ttu-id="06c80-125">상속자</span><span class="sxs-lookup"><span data-stu-id="06c80-125">NOTES</span></span>

## <span data-ttu-id="06c80-126">관련 링크</span><span class="sxs-lookup"><span data-stu-id="06c80-126">RELATED LINKS</span></span>

[<span data-ttu-id="06c80-127">Get-AzureRmRecoveryServicesAsrPolicy</span><span class="sxs-lookup"><span data-stu-id="06c80-127">Get-AzureRmRecoveryServicesAsrPolicy</span></span>](./Get-AzureRmRecoveryServicesAsrPolicy.md)

[<span data-ttu-id="06c80-128">새로운 AzureRmRecoveryServicesAsrPolicy</span><span class="sxs-lookup"><span data-stu-id="06c80-128">New-AzureRmRecoveryServicesAsrPolicy</span></span>](./New-AzureRmRecoveryServicesAsrPolicy.md)
