---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/update-azrecoveryservicesasrrecoveryplan
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Update-AzRecoveryServicesAsrRecoveryPlan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Update-AzRecoveryServicesAsrRecoveryPlan.md
ms.openlocfilehash: 99c91f24bcc81ee6d6971b74779dfd116b90fdef
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94219169"
---
# <span data-ttu-id="28d05-101">Update-AzRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="28d05-101">Update-AzRecoveryServicesAsrRecoveryPlan</span></span>

## <span data-ttu-id="28d05-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="28d05-102">SYNOPSIS</span></span>
<span data-ttu-id="28d05-103">Azure Site recovery 계획의 콘텐츠를 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="28d05-103">Updates the contents of an Azure Site recovery plan.</span></span>

## <span data-ttu-id="28d05-104">구문과</span><span class="sxs-lookup"><span data-stu-id="28d05-104">SYNTAX</span></span>

### <span data-ttu-id="28d05-105">ByRPObject (기본값)</span><span class="sxs-lookup"><span data-stu-id="28d05-105">ByRPObject (Default)</span></span>
```
Update-AzRecoveryServicesAsrRecoveryPlan -InputObject <ASRRecoveryPlan>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="28d05-106">ByRPFile</span><span class="sxs-lookup"><span data-stu-id="28d05-106">ByRPFile</span></span>
```
Update-AzRecoveryServicesAsrRecoveryPlan -Path <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="28d05-107">설명은</span><span class="sxs-lookup"><span data-stu-id="28d05-107">DESCRIPTION</span></span>
<span data-ttu-id="28d05-108">**AzRecoveryServicesAsrRecoveryPlan** cmdlet은 지정 된 asr 복구 계획 개체 또는 asr 복구 계획 정의 json 파일의 콘텐츠를 사용 하 여 복구 계획의 콘텐츠를 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="28d05-108">The **Update-AzRecoveryServicesAsrRecoveryPlan** cmdlet updates the contents of a recovery plan using the contents of the specified ASR recovery plan object or ASR recovery plan definition json file.</span></span>

## <span data-ttu-id="28d05-109">예제의</span><span class="sxs-lookup"><span data-stu-id="28d05-109">EXAMPLES</span></span>

### <span data-ttu-id="28d05-110">예제 1: 복구 계획 업데이트</span><span class="sxs-lookup"><span data-stu-id="28d05-110">Example 1: Update a recovery plan</span></span>
```
PS C:\> $currentJob = Update-AzRecoveryServicesAsrRecoveryPlan -RecoveryPlan $RP
```

<span data-ttu-id="28d05-111">지정 된 ASR 복구 계획 개체의 콘텐츠를 사용 하 여 복구 계획을 업데이트 하는 작업을 시작 하 고 작업을 추적 하는 데 사용 되는 ASR 작업을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="28d05-111">Start the operation of updating a recovery plan using the contents of the specified ASR recovery plan object and returns the ASR job used to track the operation.</span></span>

## <span data-ttu-id="28d05-112">변수</span><span class="sxs-lookup"><span data-stu-id="28d05-112">PARAMETERS</span></span>

### <span data-ttu-id="28d05-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="28d05-113">-DefaultProfile</span></span>
<span data-ttu-id="28d05-114">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="28d05-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="28d05-115">-InputObject</span><span class="sxs-lookup"><span data-stu-id="28d05-115">-InputObject</span></span>
<span data-ttu-id="28d05-116">Cmdlet에 대 한 Input 개체: 개체에서 참조 하는 복구 계획을 업데이트 하는 데 사용 되는 콘텐츠 인 ASR 복구 계획 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="28d05-116">Input Object to the cmdlet: Specifies an ASR recovery plan object, the contents of which are used to update the recovery plan referred to by the object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRRecoveryPlan
Parameter Sets: ByRPObject
Aliases: RecoveryPlan

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="28d05-117">-Path</span><span class="sxs-lookup"><span data-stu-id="28d05-117">-Path</span></span>
<span data-ttu-id="28d05-118">복구 계획을 업데이트 하는 데 사용 되는 복구 계획 정의 json 파일의 경로를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="28d05-118">Specifies the path of the recovery plan definition json file used to update the recovery plan.</span></span>

```yaml
Type: System.String
Parameter Sets: ByRPFile
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="28d05-119">-확인</span><span class="sxs-lookup"><span data-stu-id="28d05-119">-Confirm</span></span>
<span data-ttu-id="28d05-120">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="28d05-120">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="28d05-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="28d05-121">-WhatIf</span></span>
<span data-ttu-id="28d05-122">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="28d05-122">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="28d05-123">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="28d05-123">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="28d05-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="28d05-124">CommonParameters</span></span>
<span data-ttu-id="28d05-125">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="28d05-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="28d05-126">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="28d05-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="28d05-127">입력</span><span class="sxs-lookup"><span data-stu-id="28d05-127">INPUTS</span></span>

### <span data-ttu-id="28d05-128">SiteRecovery를 통한 Recoveryrrecoveryplan 계획</span><span class="sxs-lookup"><span data-stu-id="28d05-128">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRRecoveryPlan</span></span>

## <span data-ttu-id="28d05-129">출력</span><span class="sxs-lookup"><span data-stu-id="28d05-129">OUTPUTS</span></span>

### <span data-ttu-id="28d05-130">SiteRecovery. r i m m 작업</span><span class="sxs-lookup"><span data-stu-id="28d05-130">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="28d05-131">상속자</span><span class="sxs-lookup"><span data-stu-id="28d05-131">NOTES</span></span>

## <span data-ttu-id="28d05-132">관련 링크</span><span class="sxs-lookup"><span data-stu-id="28d05-132">RELATED LINKS</span></span>

[<span data-ttu-id="28d05-133">Get-AzRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="28d05-133">Get-AzRecoveryServicesAsrRecoveryPlan</span></span>](./Get-AzRecoveryServicesAsrRecoveryPlan.md)

[<span data-ttu-id="28d05-134">새로운 AzRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="28d05-134">New-AzRecoveryServicesAsrRecoveryPlan</span></span>](./New-AzRecoveryServicesAsrRecoveryPlan.md)

[<span data-ttu-id="28d05-135">제거-AzRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="28d05-135">Remove-AzRecoveryServicesAsrRecoveryPlan</span></span>](./Remove-AzRecoveryServicesAsrRecoveryPlan.md)
