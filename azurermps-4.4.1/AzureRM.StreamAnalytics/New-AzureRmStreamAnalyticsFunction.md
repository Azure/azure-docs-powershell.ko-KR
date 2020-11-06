---
external help file: Microsoft.Azure.Commands.StreamAnalytics.dll-Help.xml
Module Name: AzureRM.StreamAnalytics
ms.assetid: 79EB2AD9-BFE1-49BE-870F-7DFC99D6FE17
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/StreamAnalytics/Commands.StreamAnalytics/help/New-AzureRmStreamAnalyticsFunction.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/StreamAnalytics/Commands.StreamAnalytics/help/New-AzureRmStreamAnalyticsFunction.md
ms.openlocfilehash: 6b05bb1d379a5d9072cc286505a507d3718aa33e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93529974"
---
# <span data-ttu-id="57d44-101">New-AzureRmStreamAnalyticsFunction</span><span class="sxs-lookup"><span data-stu-id="57d44-101">New-AzureRmStreamAnalyticsFunction</span></span>

## <span data-ttu-id="57d44-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="57d44-102">SYNOPSIS</span></span>
<span data-ttu-id="57d44-103">Stream Analytics 작업에서 함수를 만들거나 바꿉니다.</span><span class="sxs-lookup"><span data-stu-id="57d44-103">Creates or replaces a function in a Stream Analytics job.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="57d44-104">구문과</span><span class="sxs-lookup"><span data-stu-id="57d44-104">SYNTAX</span></span>

```
New-AzureRmStreamAnalyticsFunction [-JobName] <String> [[-Name] <String>] [-File] <String> [-Force]
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="57d44-105">설명은</span><span class="sxs-lookup"><span data-stu-id="57d44-105">DESCRIPTION</span></span>
<span data-ttu-id="57d44-106">**AzureRmStreamAnalyticsFunction** Cmdlet은 Azure Stream Analytics 작업에서 함수를 만들거나 기존 함수를 대체 합니다.</span><span class="sxs-lookup"><span data-stu-id="57d44-106">The **New-AzureRmStreamAnalyticsFunction** cmdlet creates a function in an Azure Stream Analytics job or replaces an existing function.</span></span>
<span data-ttu-id="57d44-107">JSON (JavaScript Object Notation) 파일에서 함수를 정의 합니다.</span><span class="sxs-lookup"><span data-stu-id="57d44-107">Define the function in a JavaScript Object Notation (JSON) file.</span></span>

<span data-ttu-id="57d44-108">*Name* 매개 변수 또는 json 파일을 사용 하 여 함수의 이름을 지정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="57d44-108">You can specify the name of the function by using the *Name* parameter or in the .json file.</span></span>
<span data-ttu-id="57d44-109">이름을 두 가지 방법으로 모두 지정 하는 경우에는 이름이 일치 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="57d44-109">If you specify the name in both ways, the names must match.</span></span>

<span data-ttu-id="57d44-110">기존 함수를 바꾸려면 기존 함수의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="57d44-110">To replace an existing function, specify the name of the existing function.</span></span>

## <span data-ttu-id="57d44-111">예제의</span><span class="sxs-lookup"><span data-stu-id="57d44-111">EXAMPLES</span></span>

### <span data-ttu-id="57d44-112">예제 1: Stream Analytics 함수 만들기</span><span class="sxs-lookup"><span data-stu-id="57d44-112">Example 1: Create a Stream Analytics function</span></span>
```
PS C:\>New-AzureRmStreamAnalyticsFunction -ResourceGroupName "StreamAnalytics-Default-West-US" -JobName "StreamJob07" -File "C:\Function07.json"
```

<span data-ttu-id="57d44-113">이 명령은 파일 Function07.js에 있는 함수를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="57d44-113">This command creates a function from the file Function07.json.</span></span>
<span data-ttu-id="57d44-114">함수의 이름은 json 파일에 저장 됩니다.</span><span class="sxs-lookup"><span data-stu-id="57d44-114">The name of the function is stored in the .json file.</span></span>

### <span data-ttu-id="57d44-115">예제 2: ScoreTweet 라는 Stream Analytics 함수 만들기</span><span class="sxs-lookup"><span data-stu-id="57d44-115">Example 2: Create a Stream Analytics function named ScoreTweet</span></span>
```
PS C:\>New-AzureRmStreamAnalyticsFunction -ResourceGroupName "StreamAnalytics-Default-West-US" -JobName "StreamJob22" -File "C:\Function22.json" -Name "ScoreTweet"
```

<span data-ttu-id="57d44-116">이 명령은 ScoreTweet 이라는 작업에 함수를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="57d44-116">This command creates a function on the job named ScoreTweet.</span></span>

### <span data-ttu-id="57d44-117">예제 3: Stream Analytics 함수 바꾸기</span><span class="sxs-lookup"><span data-stu-id="57d44-117">Example 3: Replace a Stream Analytics function</span></span>
```
PS C:\>New-AzureRmStreamAnalyticsFunction -ResourceGroupName "StreamAnalytics-Default-West-US" -JobName "StreamJob22" -File "C:\Function22.json" -Name "ScoreTweet" -Force
```

<span data-ttu-id="57d44-118">이 명령은 ScoreTweet 이라는 기존 함수의 정의를 Function22.js의 정의로 바꿉니다.</span><span class="sxs-lookup"><span data-stu-id="57d44-118">This command replaces the definition of the existing function named ScoreTweet with the definition in Function22.json.</span></span>

## <span data-ttu-id="57d44-119">변수</span><span class="sxs-lookup"><span data-stu-id="57d44-119">PARAMETERS</span></span>

### <span data-ttu-id="57d44-120">-파일</span><span class="sxs-lookup"><span data-stu-id="57d44-120">-File</span></span>
<span data-ttu-id="57d44-121">Stream Analytics 함수의 JSON 표현을 포함 하는 json 파일의 경로를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="57d44-121">Specifies the path of a .json file that contains the JSON representation of the Stream Analytics function.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="57d44-122">-Force</span><span class="sxs-lookup"><span data-stu-id="57d44-122">-Force</span></span>
<span data-ttu-id="57d44-123">이 cmdlet이 확인 메시지를 표시 하지 않고 기존 Stream Analytics 함수를 대체 합니다.</span><span class="sxs-lookup"><span data-stu-id="57d44-123">Indicates that this cmdlet replaces an existing Stream Analytics function without prompting you for confirmation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="57d44-124">-JobName</span><span class="sxs-lookup"><span data-stu-id="57d44-124">-JobName</span></span>
<span data-ttu-id="57d44-125">이 cmdlet이 Stream Analytics 함수를 만드는 스트림 분석 작업의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="57d44-125">Specifies the name of the Stream Analytics job under which this cmdlet creates a Stream Analytics function.</span></span>

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

### <span data-ttu-id="57d44-126">-이름</span><span class="sxs-lookup"><span data-stu-id="57d44-126">-Name</span></span>
<span data-ttu-id="57d44-127">이 cmdlet이 만드는 Stream Analytics 함수의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="57d44-127">Specifies the name of the Stream Analytics function that this cmdlet creates.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="57d44-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="57d44-128">-ResourceGroupName</span></span>
<span data-ttu-id="57d44-129">이 cmdlet이 Stream Analytics 함수를 만드는 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="57d44-129">Specifies the name of the resource group under which this cmdlet creates a Stream Analytics function.</span></span>

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

### <span data-ttu-id="57d44-130">-확인</span><span class="sxs-lookup"><span data-stu-id="57d44-130">-Confirm</span></span>
<span data-ttu-id="57d44-131">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="57d44-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="57d44-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="57d44-132">-WhatIf</span></span>
<span data-ttu-id="57d44-133">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="57d44-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="57d44-134">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="57d44-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="57d44-135">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="57d44-135">-DefaultProfile</span></span>
<span data-ttu-id="57d44-136">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="57d44-136">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="57d44-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="57d44-137">CommonParameters</span></span>
<span data-ttu-id="57d44-138">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="57d44-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="57d44-139">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="57d44-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="57d44-140">입력</span><span class="sxs-lookup"><span data-stu-id="57d44-140">INPUTS</span></span>

## <span data-ttu-id="57d44-141">출력</span><span class="sxs-lookup"><span data-stu-id="57d44-141">OUTPUTS</span></span>

### <span data-ttu-id="57d44-142">Microsoft. i. a i m/. a i m/. i m a 함수</span><span class="sxs-lookup"><span data-stu-id="57d44-142">Microsoft.Azure.Commands.StreamAnalytics.Models.PSFunction</span></span>

## <span data-ttu-id="57d44-143">상속자</span><span class="sxs-lookup"><span data-stu-id="57d44-143">NOTES</span></span>

## <span data-ttu-id="57d44-144">관련 링크</span><span class="sxs-lookup"><span data-stu-id="57d44-144">RELATED LINKS</span></span>

[<span data-ttu-id="57d44-145">Get-AzureRmStreamAnalyticsFunction</span><span class="sxs-lookup"><span data-stu-id="57d44-145">Get-AzureRmStreamAnalyticsFunction</span></span>](./Get-AzureRmStreamAnalyticsFunction.md)

[<span data-ttu-id="57d44-146">제거-AzureRmStreamAnalyticsFunction</span><span class="sxs-lookup"><span data-stu-id="57d44-146">Remove-AzureRmStreamAnalyticsFunction</span></span>](./Remove-AzureRmStreamAnalyticsFunction.md)

[<span data-ttu-id="57d44-147">테스트-AzureRmStreamAnalyticsFunction</span><span class="sxs-lookup"><span data-stu-id="57d44-147">Test-AzureRmStreamAnalyticsFunction</span></span>](./Test-AzureRmStreamAnalyticsFunction.md)


