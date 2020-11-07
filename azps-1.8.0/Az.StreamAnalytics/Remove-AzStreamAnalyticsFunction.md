---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StreamAnalytics.dll-Help.xml
Module Name: Az.StreamAnalytics
ms.assetid: 75B0776E-32D5-4EE4-B35C-73E13185A4F1
online version: https://docs.microsoft.com/en-us/powershell/module/az.streamanalytics/remove-azstreamanalyticsfunction
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/Remove-AzStreamAnalyticsFunction.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/Remove-AzStreamAnalyticsFunction.md
ms.openlocfilehash: bf5c869e8831fd37a10f9923d415a91f88fd0960
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93698444"
---
# <span data-ttu-id="c7ad5-101">Remove-AzStreamAnalyticsFunction</span><span class="sxs-lookup"><span data-stu-id="c7ad5-101">Remove-AzStreamAnalyticsFunction</span></span>

## <span data-ttu-id="c7ad5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c7ad5-102">SYNOPSIS</span></span>
<span data-ttu-id="c7ad5-103">Stream Analytics 작업에서 함수를 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="c7ad5-103">Deletes a function from a Stream Analytics job.</span></span>

## <span data-ttu-id="c7ad5-104">구문과</span><span class="sxs-lookup"><span data-stu-id="c7ad5-104">SYNTAX</span></span>

```
Remove-AzStreamAnalyticsFunction [-JobName] <String> [-Name] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c7ad5-105">설명은</span><span class="sxs-lookup"><span data-stu-id="c7ad5-105">DESCRIPTION</span></span>
<span data-ttu-id="c7ad5-106">**AzStreamAnalyticsFunction** Cmdlet은 Azure Stream Analytics 작업에서 비동기적으로 함수를 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="c7ad5-106">The **Remove-AzStreamAnalyticsFunction** cmdlet deletes a function asynchronously from an Azure Stream Analytics job.</span></span>

## <span data-ttu-id="c7ad5-107">예제의</span><span class="sxs-lookup"><span data-stu-id="c7ad5-107">EXAMPLES</span></span>

### <span data-ttu-id="c7ad5-108">예제 1: Stream Analytics 함수 제거</span><span class="sxs-lookup"><span data-stu-id="c7ad5-108">Example 1: Remove a Stream Analytics function</span></span>
```
PS C:\>Remove-AzStreamAnalyticsFunction -ResourceGroupName "StreamAnalytics-Default-West-US" -JobName "StreamJob22" -Name "ScoreTweet"
```

<span data-ttu-id="c7ad5-109">이 명령은 StreamJob22 이라는 작업에서 ScoreTweet 이라는 함수를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="c7ad5-109">This command removes the function named ScoreTweet from the job named StreamJob22.</span></span>

## <span data-ttu-id="c7ad5-110">변수</span><span class="sxs-lookup"><span data-stu-id="c7ad5-110">PARAMETERS</span></span>

### <span data-ttu-id="c7ad5-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c7ad5-111">-DefaultProfile</span></span>
<span data-ttu-id="c7ad5-112">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="c7ad5-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c7ad5-113">-JobName</span><span class="sxs-lookup"><span data-stu-id="c7ad5-113">-JobName</span></span>
<span data-ttu-id="c7ad5-114">함수가 속한 Stream Analytics 작업의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="c7ad5-114">Specifies the name of the Stream Analytics job to which a function belongs.</span></span>
<span data-ttu-id="c7ad5-115">이 cmdlet은이 매개 변수에서 지정 하는 작업에서 함수를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="c7ad5-115">This cmdlet removes a function from the job that this parameter specifies.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c7ad5-116">-이름</span><span class="sxs-lookup"><span data-stu-id="c7ad5-116">-Name</span></span>
<span data-ttu-id="c7ad5-117">이 cmdlet이 제거 하는 Stream Analytics 함수의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="c7ad5-117">Specifies the name of the Stream Analytics function that this cmdlet removes.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c7ad5-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c7ad5-118">-ResourceGroupName</span></span>
<span data-ttu-id="c7ad5-119">Stream Analytics 함수가 속한 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="c7ad5-119">Specifies the name of the resource group to which a Stream Analytics function belongs.</span></span>
<span data-ttu-id="c7ad5-120">이 cmdlet은이 매개 변수에서 지정 하는 리소스 그룹의 함수를 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="c7ad5-120">This cmdlet deletes a function in the resource group that this parameter specifies.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c7ad5-121">-확인</span><span class="sxs-lookup"><span data-stu-id="c7ad5-121">-Confirm</span></span>
<span data-ttu-id="c7ad5-122">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="c7ad5-122">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c7ad5-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c7ad5-123">-WhatIf</span></span>
<span data-ttu-id="c7ad5-124">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="c7ad5-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c7ad5-125">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="c7ad5-125">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c7ad5-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c7ad5-126">CommonParameters</span></span>
<span data-ttu-id="c7ad5-127">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="c7ad5-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c7ad5-128">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c7ad5-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c7ad5-129">입력</span><span class="sxs-lookup"><span data-stu-id="c7ad5-129">INPUTS</span></span>

### <span data-ttu-id="c7ad5-130">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="c7ad5-130">System.String</span></span>

## <span data-ttu-id="c7ad5-131">출력</span><span class="sxs-lookup"><span data-stu-id="c7ad5-131">OUTPUTS</span></span>

### <span data-ttu-id="c7ad5-132">시스템 부울</span><span class="sxs-lookup"><span data-stu-id="c7ad5-132">System.Boolean</span></span>

## <span data-ttu-id="c7ad5-133">상속자</span><span class="sxs-lookup"><span data-stu-id="c7ad5-133">NOTES</span></span>

## <span data-ttu-id="c7ad5-134">관련 링크</span><span class="sxs-lookup"><span data-stu-id="c7ad5-134">RELATED LINKS</span></span>

[<span data-ttu-id="c7ad5-135">Get-AzStreamAnalyticsFunction</span><span class="sxs-lookup"><span data-stu-id="c7ad5-135">Get-AzStreamAnalyticsFunction</span></span>](./Get-AzStreamAnalyticsFunction.md)

[<span data-ttu-id="c7ad5-136">새로운 AzStreamAnalyticsFunction</span><span class="sxs-lookup"><span data-stu-id="c7ad5-136">New-AzStreamAnalyticsFunction</span></span>](./New-AzStreamAnalyticsFunction.md)

[<span data-ttu-id="c7ad5-137">테스트-AzStreamAnalyticsFunction</span><span class="sxs-lookup"><span data-stu-id="c7ad5-137">Test-AzStreamAnalyticsFunction</span></span>](./Test-AzStreamAnalyticsFunction.md)


