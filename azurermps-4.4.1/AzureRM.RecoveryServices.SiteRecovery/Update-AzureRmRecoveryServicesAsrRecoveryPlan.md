---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Update-AzureRmRecoveryServicesAsrRecoveryPlan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Update-AzureRmRecoveryServicesAsrRecoveryPlan.md
ms.openlocfilehash: 21a46346c681a6f184033d4f50d65e6c9a019844
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93703643"
---
# <span data-ttu-id="c0b89-101">Update-AzureRmRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="c0b89-101">Update-AzureRmRecoveryServicesAsrRecoveryPlan</span></span>

## <span data-ttu-id="c0b89-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c0b89-102">SYNOPSIS</span></span>
<span data-ttu-id="c0b89-103">Azure Site recovery 계획의 콘텐츠를 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="c0b89-103">Updates the contents of an Azure Site recovery plan.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c0b89-104">구문과</span><span class="sxs-lookup"><span data-stu-id="c0b89-104">SYNTAX</span></span>

### <span data-ttu-id="c0b89-105">ByRPObject (기본값)</span><span class="sxs-lookup"><span data-stu-id="c0b89-105">ByRPObject (Default)</span></span>
```
Update-AzureRmRecoveryServicesAsrRecoveryPlan -InputObject <ASRRecoveryPlan> [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="c0b89-106">ByRPFile</span><span class="sxs-lookup"><span data-stu-id="c0b89-106">ByRPFile</span></span>
```
Update-AzureRmRecoveryServicesAsrRecoveryPlan -Path <String> [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c0b89-107">설명은</span><span class="sxs-lookup"><span data-stu-id="c0b89-107">DESCRIPTION</span></span>
<span data-ttu-id="c0b89-108">**AzureRmRecoveryServicesAsrRecoveryPlan** cmdlet은 지정 된 asr 복구 계획 개체 또는 asr 복구 계획 정의 json 파일의 콘텐츠를 사용 하 여 복구 계획의 콘텐츠를 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="c0b89-108">The **Update-AzureRmRecoveryServicesAsrRecoveryPlan** cmdlet updates the contents of a recovery plan using the contents of the specified ASR recovery plan object or ASR recovery plan definition json file.</span></span>

## <span data-ttu-id="c0b89-109">예제의</span><span class="sxs-lookup"><span data-stu-id="c0b89-109">EXAMPLES</span></span>

### <span data-ttu-id="c0b89-110">예제 1: 복구 계획 업데이트</span><span class="sxs-lookup"><span data-stu-id="c0b89-110">Example 1: Update a recovery plan</span></span>
```
PS C:\> $currentJob = Update-AzureRmRecoveryServicesAsrRecoveryPlan -RecoveryPlan $RP
```

<span data-ttu-id="c0b89-111">지정 된 ASR 복구 계획 개체의 콘텐츠를 사용 하 여 복구 계획을 업데이트 하는 작업을 시작 하 고 작업을 추적 하는 데 사용 되는 ASR 작업을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="c0b89-111">Start the operation of updating a recovery plan using the contents of the specified ASR recovery plan object and returns the ASR job used to track the operation.</span></span>

## <span data-ttu-id="c0b89-112">변수</span><span class="sxs-lookup"><span data-stu-id="c0b89-112">PARAMETERS</span></span>

### <span data-ttu-id="c0b89-113">-InputObject</span><span class="sxs-lookup"><span data-stu-id="c0b89-113">-InputObject</span></span>
<span data-ttu-id="c0b89-114">Cmdlet에 대 한 Input 개체: 개체에서 참조 하는 복구 계획을 업데이트 하는 데 사용 되는 콘텐츠 인 ASR 복구 계획 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="c0b89-114">Input Object to the cmdlet: Specifies an ASR recovery plan object, the contents of which are used to update the recovery plan referred to by the object.</span></span>

```yaml
Type: ASRRecoveryPlan
Parameter Sets: ByRPObject
Aliases: RecoveryPlan

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c0b89-115">-Path</span><span class="sxs-lookup"><span data-stu-id="c0b89-115">-Path</span></span>
<span data-ttu-id="c0b89-116">복구 계획을 업데이트 하는 데 사용 되는 복구 계획 정의 json 파일의 경로를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="c0b89-116">Specifies the path of the recovery plan definition json file used to update the recovery plan.</span></span>

```yaml
Type: String
Parameter Sets: ByRPFile
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c0b89-117">-확인</span><span class="sxs-lookup"><span data-stu-id="c0b89-117">-Confirm</span></span>
<span data-ttu-id="c0b89-118">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="c0b89-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c0b89-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c0b89-119">-WhatIf</span></span>
<span data-ttu-id="c0b89-120">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="c0b89-120">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="c0b89-121">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="c0b89-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c0b89-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c0b89-122">CommonParameters</span></span>
<span data-ttu-id="c0b89-123">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="c0b89-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c0b89-124">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c0b89-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c0b89-125">입력</span><span class="sxs-lookup"><span data-stu-id="c0b89-125">INPUTS</span></span>

### <span data-ttu-id="c0b89-126">SiteRecovery를 통한 Recoveryrrecoveryplan 계획</span><span class="sxs-lookup"><span data-stu-id="c0b89-126">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRRecoveryPlan</span></span>

## <span data-ttu-id="c0b89-127">출력</span><span class="sxs-lookup"><span data-stu-id="c0b89-127">OUTPUTS</span></span>

### <span data-ttu-id="c0b89-128">System. 개체</span><span class="sxs-lookup"><span data-stu-id="c0b89-128">System.Object</span></span>

## <span data-ttu-id="c0b89-129">상속자</span><span class="sxs-lookup"><span data-stu-id="c0b89-129">NOTES</span></span>

## <span data-ttu-id="c0b89-130">관련 링크</span><span class="sxs-lookup"><span data-stu-id="c0b89-130">RELATED LINKS</span></span>

[<span data-ttu-id="c0b89-131">Get-AzureRmRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="c0b89-131">Get-AzureRmRecoveryServicesAsrRecoveryPlan</span></span>](./Get-AzureRmRecoveryServicesAsrRecoveryPlan.md)

[<span data-ttu-id="c0b89-132">새로운 AzureRmRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="c0b89-132">New-AzureRmRecoveryServicesAsrRecoveryPlan</span></span>](./New-AzureRmRecoveryServicesAsrRecoveryPlan.md)

[<span data-ttu-id="c0b89-133">제거-AzureRmRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="c0b89-133">Remove-AzureRmRecoveryServicesAsrRecoveryPlan</span></span>](./Remove-AzureRmRecoveryServicesAsrRecoveryPlan.md)


