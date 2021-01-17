---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StreamAnalytics.dll-Help.xml
Module Name: Az.StreamAnalytics
ms.assetid: 75B0776E-32D5-4EE4-B35C-73E13185A4F1
online version: https://docs.microsoft.com/en-us/powershell/module/az.streamanalytics/remove-azstreamanalyticsfunction
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/Remove-AzStreamAnalyticsFunction.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/Remove-AzStreamAnalyticsFunction.md
ms.openlocfilehash: d481cf5ba28a87e098691d4b3fa5c179670d881d
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98366304"
---
# <span data-ttu-id="e3e76-101">Remove-AzStreamAnalyticsFunction</span><span class="sxs-lookup"><span data-stu-id="e3e76-101">Remove-AzStreamAnalyticsFunction</span></span>

## <span data-ttu-id="e3e76-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e3e76-102">SYNOPSIS</span></span>
<span data-ttu-id="e3e76-103">Stream Analytics 작업에서 함수를 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="e3e76-103">Deletes a function from a Stream Analytics job.</span></span>

## <span data-ttu-id="e3e76-104">구문</span><span class="sxs-lookup"><span data-stu-id="e3e76-104">SYNTAX</span></span>

```
Remove-AzStreamAnalyticsFunction [-JobName] <String> [-Name] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e3e76-105">설명</span><span class="sxs-lookup"><span data-stu-id="e3e76-105">DESCRIPTION</span></span>
<span data-ttu-id="e3e76-106">**Remove-AzStreamAnalyticsFunction** cmdlet은 Azure Stream Analytics 작업에서 함수를 비동기적으로 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="e3e76-106">The **Remove-AzStreamAnalyticsFunction** cmdlet deletes a function asynchronously from an Azure Stream Analytics job.</span></span>

## <span data-ttu-id="e3e76-107">예제</span><span class="sxs-lookup"><span data-stu-id="e3e76-107">EXAMPLES</span></span>

### <span data-ttu-id="e3e76-108">예제 1: Stream Analytics 함수 제거</span><span class="sxs-lookup"><span data-stu-id="e3e76-108">Example 1: Remove a Stream Analytics function</span></span>
```
PS C:\>Remove-AzStreamAnalyticsFunction -ResourceGroupName "StreamAnalytics-Default-West-US" -JobName "StreamJob22" -Name "ScoreTweet"
```

<span data-ttu-id="e3e76-109">이 명령은 StreamJob22라는 작업에서 ScoreTweet이라는 함수를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="e3e76-109">This command removes the function named ScoreTweet from the job named StreamJob22.</span></span>

## <span data-ttu-id="e3e76-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e3e76-110">PARAMETERS</span></span>

### <span data-ttu-id="e3e76-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e3e76-111">-DefaultProfile</span></span>
<span data-ttu-id="e3e76-112">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="e3e76-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e3e76-113">-JobName</span><span class="sxs-lookup"><span data-stu-id="e3e76-113">-JobName</span></span>
<span data-ttu-id="e3e76-114">함수가 속한 Stream Analytics 작업의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="e3e76-114">Specifies the name of the Stream Analytics job to which a function belongs.</span></span>
<span data-ttu-id="e3e76-115">이 cmdlet은 이 매개 변수가 지정하는 작업에서 함수를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="e3e76-115">This cmdlet removes a function from the job that this parameter specifies.</span></span>

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

### <span data-ttu-id="e3e76-116">-Name</span><span class="sxs-lookup"><span data-stu-id="e3e76-116">-Name</span></span>
<span data-ttu-id="e3e76-117">이 cmdlet이 제거하는 Stream Analytics 함수의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="e3e76-117">Specifies the name of the Stream Analytics function that this cmdlet removes.</span></span>

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

### <span data-ttu-id="e3e76-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e3e76-118">-ResourceGroupName</span></span>
<span data-ttu-id="e3e76-119">Stream Analytics 함수가 속한 리소스 그룹의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="e3e76-119">Specifies the name of the resource group to which a Stream Analytics function belongs.</span></span>
<span data-ttu-id="e3e76-120">이 cmdlet은 이 매개 변수가 지정하는 리소스 그룹에서 함수를 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="e3e76-120">This cmdlet deletes a function in the resource group that this parameter specifies.</span></span>

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

### <span data-ttu-id="e3e76-121">-Confirm</span><span class="sxs-lookup"><span data-stu-id="e3e76-121">-Confirm</span></span>
<span data-ttu-id="e3e76-122">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="e3e76-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e3e76-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e3e76-123">-WhatIf</span></span>
<span data-ttu-id="e3e76-124">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="e3e76-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e3e76-125">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="e3e76-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e3e76-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e3e76-126">CommonParameters</span></span>
<span data-ttu-id="e3e76-127">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="e3e76-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e3e76-128">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="e3e76-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e3e76-129">입력</span><span class="sxs-lookup"><span data-stu-id="e3e76-129">INPUTS</span></span>

### <span data-ttu-id="e3e76-130">System.String</span><span class="sxs-lookup"><span data-stu-id="e3e76-130">System.String</span></span>

## <span data-ttu-id="e3e76-131">출력</span><span class="sxs-lookup"><span data-stu-id="e3e76-131">OUTPUTS</span></span>

### <span data-ttu-id="e3e76-132">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="e3e76-132">System.Boolean</span></span>

## <span data-ttu-id="e3e76-133">참고 사항</span><span class="sxs-lookup"><span data-stu-id="e3e76-133">NOTES</span></span>

## <span data-ttu-id="e3e76-134">관련 링크</span><span class="sxs-lookup"><span data-stu-id="e3e76-134">RELATED LINKS</span></span>

[<span data-ttu-id="e3e76-135">Get-AzStreamAnalyticsFunction</span><span class="sxs-lookup"><span data-stu-id="e3e76-135">Get-AzStreamAnalyticsFunction</span></span>](./Get-AzStreamAnalyticsFunction.md)

[<span data-ttu-id="e3e76-136">New-AzStreamAnalyticsFunction</span><span class="sxs-lookup"><span data-stu-id="e3e76-136">New-AzStreamAnalyticsFunction</span></span>](./New-AzStreamAnalyticsFunction.md)

[<span data-ttu-id="e3e76-137">Test-AzStreamAnalyticsFunction</span><span class="sxs-lookup"><span data-stu-id="e3e76-137">Test-AzStreamAnalyticsFunction</span></span>](./Test-AzStreamAnalyticsFunction.md)


