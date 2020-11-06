---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: AzureRM.RecoveryServices.SiteRecovery
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.siterecovery/remove-azurermrecoveryservicesasrrecoveryplan
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Remove-AzureRmRecoveryServicesAsrRecoveryPlan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Remove-AzureRmRecoveryServicesAsrRecoveryPlan.md
ms.openlocfilehash: 5f4298c2a4bfdc081447e6a8b15bac565b20b2db
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93529777"
---
# <span data-ttu-id="a76cf-101">Remove-AzureRmRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="a76cf-101">Remove-AzureRmRecoveryServicesAsrRecoveryPlan</span></span>

## <span data-ttu-id="a76cf-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a76cf-102">SYNOPSIS</span></span>
<span data-ttu-id="a76cf-103">복구 서비스 자격 증명 모음에서 지정 된 ASR 복구 계획을 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="a76cf-103">Deletes the specified ASR recovery plan from Recovery Services vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a76cf-104">구문과</span><span class="sxs-lookup"><span data-stu-id="a76cf-104">SYNTAX</span></span>

### <span data-ttu-id="a76cf-105">ByObject (기본값)</span><span class="sxs-lookup"><span data-stu-id="a76cf-105">ByObject (Default)</span></span>
```
Remove-AzureRmRecoveryServicesAsrRecoveryPlan -InputObject <ASRRecoveryPlan>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a76cf-106">ByName</span><span class="sxs-lookup"><span data-stu-id="a76cf-106">ByName</span></span>
```
Remove-AzureRmRecoveryServicesAsrRecoveryPlan -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a76cf-107">설명은</span><span class="sxs-lookup"><span data-stu-id="a76cf-107">DESCRIPTION</span></span>
<span data-ttu-id="a76cf-108">**AzureRmRecoveryServicesAsrRecoveryPlan** Cmdlet은 복구 서비스 자격 증명 모음에서 지정 된 복구 계획을 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="a76cf-108">The **Remove-AzureRmRecoveryServicesAsrRecoveryPlan** cmdlet deletes the specified recovery plan from the Recovery Services vault.</span></span>

## <span data-ttu-id="a76cf-109">예제의</span><span class="sxs-lookup"><span data-stu-id="a76cf-109">EXAMPLES</span></span>

### <span data-ttu-id="a76cf-110">예제 1</span><span class="sxs-lookup"><span data-stu-id="a76cf-110">Example 1</span></span>
```
PS C:\> $currentJob = Remove-AzureRmRecoveryServicesAsrRecoveryPlan -RecoveryPlan $RP
```

<span data-ttu-id="a76cf-111">지정 된 복구 계획의 삭제를 시작 하 고 작업을 추적 하는 데 사용 되는 ASR 작업을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="a76cf-111">Starts the deletion of specified recovery plan and returns the ASR job used to track the operation.</span></span>

## <span data-ttu-id="a76cf-112">변수</span><span class="sxs-lookup"><span data-stu-id="a76cf-112">PARAMETERS</span></span>

### <span data-ttu-id="a76cf-113">-확인</span><span class="sxs-lookup"><span data-stu-id="a76cf-113">-Confirm</span></span>
<span data-ttu-id="a76cf-114">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="a76cf-114">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a76cf-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a76cf-115">-DefaultProfile</span></span>
<span data-ttu-id="a76cf-116">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="a76cf-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>
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

### <span data-ttu-id="a76cf-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a76cf-117">-InputObject</span></span>
<span data-ttu-id="a76cf-118">Cmdlet에 대 한 입력 개체: 삭제할 복구 계획에 해당 하는 ASR 복구 계획 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="a76cf-118">The input object to the cmdlet: The ASR recovery plan object corresponding to the recovery plan to be deleted.</span></span>

```yaml
Type: ASRRecoveryPlan
Parameter Sets: ByObject
Aliases: RecoveryPlan

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a76cf-119">-이름</span><span class="sxs-lookup"><span data-stu-id="a76cf-119">-Name</span></span>
<span data-ttu-id="a76cf-120">삭제할 복구 계획의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a76cf-120">Specifies the name of the recovery plan to be deleted.</span></span>

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

### <span data-ttu-id="a76cf-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a76cf-121">-WhatIf</span></span>
<span data-ttu-id="a76cf-122">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="a76cf-122">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="a76cf-123">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="a76cf-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a76cf-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a76cf-124">CommonParameters</span></span>
<span data-ttu-id="a76cf-125">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="a76cf-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a76cf-126">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a76cf-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a76cf-127">입력</span><span class="sxs-lookup"><span data-stu-id="a76cf-127">INPUTS</span></span>

### <span data-ttu-id="a76cf-128">SiteRecovery를 통한 Recoveryrrecoveryplan 계획</span><span class="sxs-lookup"><span data-stu-id="a76cf-128">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRRecoveryPlan</span></span>

## <span data-ttu-id="a76cf-129">출력</span><span class="sxs-lookup"><span data-stu-id="a76cf-129">OUTPUTS</span></span>

### <span data-ttu-id="a76cf-130">System. 개체</span><span class="sxs-lookup"><span data-stu-id="a76cf-130">System.Object</span></span>

## <span data-ttu-id="a76cf-131">상속자</span><span class="sxs-lookup"><span data-stu-id="a76cf-131">NOTES</span></span>

## <span data-ttu-id="a76cf-132">관련 링크</span><span class="sxs-lookup"><span data-stu-id="a76cf-132">RELATED LINKS</span></span>

[<span data-ttu-id="a76cf-133">Get-AzureRmRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="a76cf-133">Get-AzureRmRecoveryServicesAsrRecoveryPlan</span></span>](./Get-AzureRmRecoveryServicesAsrRecoveryPlan.md)

[<span data-ttu-id="a76cf-134">새로운 AzureRmRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="a76cf-134">New-AzureRmRecoveryServicesAsrRecoveryPlan</span></span>](./New-AzureRmRecoveryServicesAsrRecoveryPlan.md)

[<span data-ttu-id="a76cf-135">업데이트-AzureRmRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="a76cf-135">Update-AzureRmRecoveryServicesAsrRecoveryPlan</span></span>](./Update-AzureRmRecoveryServicesAsrRecoveryPlan.md)


