---
external help file: Microsoft.Azure.Commands.StreamAnalytics.dll-Help.xml
Module Name: AzureRM.StreamAnalytics
ms.assetid: 75B0776E-32D5-4EE4-B35C-73E13185A4F1
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/StreamAnalytics/Commands.StreamAnalytics/help/Remove-AzureRmStreamAnalyticsFunction.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/StreamAnalytics/Commands.StreamAnalytics/help/Remove-AzureRmStreamAnalyticsFunction.md
ms.openlocfilehash: 10687094bcbbc6cc9a52e648d830d46eac089c4d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93535380"
---
# <span data-ttu-id="07b81-101">Remove-AzureRmStreamAnalyticsFunction</span><span class="sxs-lookup"><span data-stu-id="07b81-101">Remove-AzureRmStreamAnalyticsFunction</span></span>

## <span data-ttu-id="07b81-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="07b81-102">SYNOPSIS</span></span>
<span data-ttu-id="07b81-103">Stream Analytics 작업에서 함수를 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="07b81-103">Deletes a function from a Stream Analytics job.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="07b81-104">구문과</span><span class="sxs-lookup"><span data-stu-id="07b81-104">SYNTAX</span></span>

```
Remove-AzureRmStreamAnalyticsFunction [-JobName] <String> [-Name] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="07b81-105">설명은</span><span class="sxs-lookup"><span data-stu-id="07b81-105">DESCRIPTION</span></span>
<span data-ttu-id="07b81-106">**AzureRmStreamAnalyticsFunction** Cmdlet은 Azure Stream Analytics 작업에서 비동기적으로 함수를 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="07b81-106">The **Remove-AzureRmStreamAnalyticsFunction** cmdlet deletes a function asynchronously from an Azure Stream Analytics job.</span></span>

## <span data-ttu-id="07b81-107">예제의</span><span class="sxs-lookup"><span data-stu-id="07b81-107">EXAMPLES</span></span>

### <span data-ttu-id="07b81-108">예제 1: Stream Analytics 함수 제거</span><span class="sxs-lookup"><span data-stu-id="07b81-108">Example 1: Remove a Stream Analytics function</span></span>
```
PS C:\>Remove-AzureRmStreamAnalyticsFunction -ResourceGroupName "StreamAnalytics-Default-West-US" -JobName "StreamJob22" -Name "ScoreTweet"
```

<span data-ttu-id="07b81-109">이 명령은 StreamJob22 이라는 작업에서 ScoreTweet 이라는 함수를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="07b81-109">This command removes the function named ScoreTweet from the job named StreamJob22.</span></span>

## <span data-ttu-id="07b81-110">변수</span><span class="sxs-lookup"><span data-stu-id="07b81-110">PARAMETERS</span></span>

### <span data-ttu-id="07b81-111">-JobName</span><span class="sxs-lookup"><span data-stu-id="07b81-111">-JobName</span></span>
<span data-ttu-id="07b81-112">함수가 속한 Stream Analytics 작업의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="07b81-112">Specifies the name of the Stream Analytics job to which a function belongs.</span></span>
<span data-ttu-id="07b81-113">이 cmdlet은이 매개 변수에서 지정 하는 작업에서 함수를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="07b81-113">This cmdlet removes a function from the job that this parameter specifies.</span></span>

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

### <span data-ttu-id="07b81-114">-이름</span><span class="sxs-lookup"><span data-stu-id="07b81-114">-Name</span></span>
<span data-ttu-id="07b81-115">이 cmdlet이 제거 하는 Stream Analytics 함수의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="07b81-115">Specifies the name of the Stream Analytics function that this cmdlet removes.</span></span>

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

### <span data-ttu-id="07b81-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="07b81-116">-ResourceGroupName</span></span>
<span data-ttu-id="07b81-117">Stream Analytics 함수가 속한 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="07b81-117">Specifies the name of the resource group to which a Stream Analytics function belongs.</span></span>
<span data-ttu-id="07b81-118">이 cmdlet은이 매개 변수에서 지정 하는 리소스 그룹의 함수를 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="07b81-118">This cmdlet deletes a function in the resource group that this parameter specifies.</span></span>

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

### <span data-ttu-id="07b81-119">-확인</span><span class="sxs-lookup"><span data-stu-id="07b81-119">-Confirm</span></span>
<span data-ttu-id="07b81-120">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="07b81-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="07b81-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="07b81-121">-WhatIf</span></span>
<span data-ttu-id="07b81-122">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="07b81-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="07b81-123">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="07b81-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="07b81-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="07b81-124">-DefaultProfile</span></span>
<span data-ttu-id="07b81-125">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="07b81-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="07b81-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="07b81-126">CommonParameters</span></span>
<span data-ttu-id="07b81-127">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="07b81-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="07b81-128">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="07b81-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="07b81-129">입력</span><span class="sxs-lookup"><span data-stu-id="07b81-129">INPUTS</span></span>

## <span data-ttu-id="07b81-130">출력</span><span class="sxs-lookup"><span data-stu-id="07b81-130">OUTPUTS</span></span>

### <span data-ttu-id="07b81-131">System. 개체</span><span class="sxs-lookup"><span data-stu-id="07b81-131">System.Object</span></span>

## <span data-ttu-id="07b81-132">상속자</span><span class="sxs-lookup"><span data-stu-id="07b81-132">NOTES</span></span>

## <span data-ttu-id="07b81-133">관련 링크</span><span class="sxs-lookup"><span data-stu-id="07b81-133">RELATED LINKS</span></span>

[<span data-ttu-id="07b81-134">Get-AzureRmStreamAnalyticsFunction</span><span class="sxs-lookup"><span data-stu-id="07b81-134">Get-AzureRmStreamAnalyticsFunction</span></span>](./Get-AzureRmStreamAnalyticsFunction.md)

[<span data-ttu-id="07b81-135">새로운 AzureRmStreamAnalyticsFunction</span><span class="sxs-lookup"><span data-stu-id="07b81-135">New-AzureRmStreamAnalyticsFunction</span></span>](./New-AzureRmStreamAnalyticsFunction.md)

[<span data-ttu-id="07b81-136">테스트-AzureRmStreamAnalyticsFunction</span><span class="sxs-lookup"><span data-stu-id="07b81-136">Test-AzureRmStreamAnalyticsFunction</span></span>](./Test-AzureRmStreamAnalyticsFunction.md)


