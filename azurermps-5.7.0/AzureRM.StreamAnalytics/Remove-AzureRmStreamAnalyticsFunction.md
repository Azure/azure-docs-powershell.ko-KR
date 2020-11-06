---
external help file: Microsoft.Azure.Commands.StreamAnalytics.dll-Help.xml
Module Name: AzureRM
ms.assetid: 75B0776E-32D5-4EE4-B35C-73E13185A4F1
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.streamanalytics/remove-azurermstreamanalyticsfunction
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/StreamAnalytics/Commands.StreamAnalytics/help/Remove-AzureRmStreamAnalyticsFunction.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/StreamAnalytics/Commands.StreamAnalytics/help/Remove-AzureRmStreamAnalyticsFunction.md
ms.openlocfilehash: d76b1139955490189aeb9c2269cc4e9ede8197be
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93531567"
---
# <span data-ttu-id="aea00-101">Remove-AzureRmStreamAnalyticsFunction</span><span class="sxs-lookup"><span data-stu-id="aea00-101">Remove-AzureRmStreamAnalyticsFunction</span></span>

## <span data-ttu-id="aea00-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="aea00-102">SYNOPSIS</span></span>
<span data-ttu-id="aea00-103">Stream Analytics 작업에서 함수를 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="aea00-103">Deletes a function from a Stream Analytics job.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="aea00-104">구문과</span><span class="sxs-lookup"><span data-stu-id="aea00-104">SYNTAX</span></span>

```
Remove-AzureRmStreamAnalyticsFunction [-JobName] <String> [-Name] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="aea00-105">설명은</span><span class="sxs-lookup"><span data-stu-id="aea00-105">DESCRIPTION</span></span>
<span data-ttu-id="aea00-106">**AzureRmStreamAnalyticsFunction** Cmdlet은 Azure Stream Analytics 작업에서 비동기적으로 함수를 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="aea00-106">The **Remove-AzureRmStreamAnalyticsFunction** cmdlet deletes a function asynchronously from an Azure Stream Analytics job.</span></span>

## <span data-ttu-id="aea00-107">예제의</span><span class="sxs-lookup"><span data-stu-id="aea00-107">EXAMPLES</span></span>

### <span data-ttu-id="aea00-108">예제 1: Stream Analytics 함수 제거</span><span class="sxs-lookup"><span data-stu-id="aea00-108">Example 1: Remove a Stream Analytics function</span></span>
```
PS C:\>Remove-AzureRmStreamAnalyticsFunction -ResourceGroupName "StreamAnalytics-Default-West-US" -JobName "StreamJob22" -Name "ScoreTweet"
```

<span data-ttu-id="aea00-109">이 명령은 StreamJob22 이라는 작업에서 ScoreTweet 이라는 함수를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="aea00-109">This command removes the function named ScoreTweet from the job named StreamJob22.</span></span>

## <span data-ttu-id="aea00-110">변수</span><span class="sxs-lookup"><span data-stu-id="aea00-110">PARAMETERS</span></span>

### <span data-ttu-id="aea00-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="aea00-111">-DefaultProfile</span></span>
<span data-ttu-id="aea00-112">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="aea00-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="aea00-113">-JobName</span><span class="sxs-lookup"><span data-stu-id="aea00-113">-JobName</span></span>
<span data-ttu-id="aea00-114">함수가 속한 Stream Analytics 작업의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="aea00-114">Specifies the name of the Stream Analytics job to which a function belongs.</span></span>
<span data-ttu-id="aea00-115">이 cmdlet은이 매개 변수에서 지정 하는 작업에서 함수를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="aea00-115">This cmdlet removes a function from the job that this parameter specifies.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="aea00-116">-이름</span><span class="sxs-lookup"><span data-stu-id="aea00-116">-Name</span></span>
<span data-ttu-id="aea00-117">이 cmdlet이 제거 하는 Stream Analytics 함수의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="aea00-117">Specifies the name of the Stream Analytics function that this cmdlet removes.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="aea00-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="aea00-118">-ResourceGroupName</span></span>
<span data-ttu-id="aea00-119">Stream Analytics 함수가 속한 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="aea00-119">Specifies the name of the resource group to which a Stream Analytics function belongs.</span></span>
<span data-ttu-id="aea00-120">이 cmdlet은이 매개 변수에서 지정 하는 리소스 그룹의 함수를 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="aea00-120">This cmdlet deletes a function in the resource group that this parameter specifies.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="aea00-121">-확인</span><span class="sxs-lookup"><span data-stu-id="aea00-121">-Confirm</span></span>
<span data-ttu-id="aea00-122">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="aea00-122">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="aea00-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="aea00-123">-WhatIf</span></span>
<span data-ttu-id="aea00-124">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="aea00-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="aea00-125">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="aea00-125">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="aea00-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="aea00-126">CommonParameters</span></span>
<span data-ttu-id="aea00-127">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="aea00-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="aea00-128">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="aea00-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="aea00-129">입력</span><span class="sxs-lookup"><span data-stu-id="aea00-129">INPUTS</span></span>

### <span data-ttu-id="aea00-130">않아야</span><span class="sxs-lookup"><span data-stu-id="aea00-130">None</span></span>
<span data-ttu-id="aea00-131">이 cmdlet은 입력을 허용 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="aea00-131">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="aea00-132">출력</span><span class="sxs-lookup"><span data-stu-id="aea00-132">OUTPUTS</span></span>

### <span data-ttu-id="aea00-133">System. 개체</span><span class="sxs-lookup"><span data-stu-id="aea00-133">System.Object</span></span>

## <span data-ttu-id="aea00-134">상속자</span><span class="sxs-lookup"><span data-stu-id="aea00-134">NOTES</span></span>

## <span data-ttu-id="aea00-135">관련 링크</span><span class="sxs-lookup"><span data-stu-id="aea00-135">RELATED LINKS</span></span>

[<span data-ttu-id="aea00-136">Get-AzureRmStreamAnalyticsFunction</span><span class="sxs-lookup"><span data-stu-id="aea00-136">Get-AzureRmStreamAnalyticsFunction</span></span>](./Get-AzureRmStreamAnalyticsFunction.md)

[<span data-ttu-id="aea00-137">새로운 AzureRmStreamAnalyticsFunction</span><span class="sxs-lookup"><span data-stu-id="aea00-137">New-AzureRmStreamAnalyticsFunction</span></span>](./New-AzureRmStreamAnalyticsFunction.md)

[<span data-ttu-id="aea00-138">테스트-AzureRmStreamAnalyticsFunction</span><span class="sxs-lookup"><span data-stu-id="aea00-138">Test-AzureRmStreamAnalyticsFunction</span></span>](./Test-AzureRmStreamAnalyticsFunction.md)


