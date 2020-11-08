---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StreamAnalytics.dll-Help.xml
Module Name: Az.StreamAnalytics
ms.assetid: 79EB2AD9-BFE1-49BE-870F-7DFC99D6FE17
online version: https://docs.microsoft.com/en-us/powershell/module/az.streamanalytics/new-azstreamanalyticsfunction
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/New-AzStreamAnalyticsFunction.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/New-AzStreamAnalyticsFunction.md
ms.openlocfilehash: 71a6267b06ce47ee36f220033ec598af3680deeb
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94047487"
---
# <span data-ttu-id="17218-101">New-AzStreamAnalyticsFunction</span><span class="sxs-lookup"><span data-stu-id="17218-101">New-AzStreamAnalyticsFunction</span></span>

## <span data-ttu-id="17218-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="17218-102">SYNOPSIS</span></span>
<span data-ttu-id="17218-103">Stream Analytics 작업에서 함수를 만들거나 바꿉니다.</span><span class="sxs-lookup"><span data-stu-id="17218-103">Creates or replaces a function in a Stream Analytics job.</span></span>

## <span data-ttu-id="17218-104">구문과</span><span class="sxs-lookup"><span data-stu-id="17218-104">SYNTAX</span></span>

```
New-AzStreamAnalyticsFunction [-JobName] <String> [[-Name] <String>] [-File] <String> [-Force]
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="17218-105">설명은</span><span class="sxs-lookup"><span data-stu-id="17218-105">DESCRIPTION</span></span>
<span data-ttu-id="17218-106">**AzStreamAnalyticsFunction** Cmdlet은 Azure Stream Analytics 작업에서 함수를 만들거나 기존 함수를 대체 합니다.</span><span class="sxs-lookup"><span data-stu-id="17218-106">The **New-AzStreamAnalyticsFunction** cmdlet creates a function in an Azure Stream Analytics job or replaces an existing function.</span></span>
<span data-ttu-id="17218-107">JSON (JavaScript Object Notation) 파일에서 함수를 정의 합니다.</span><span class="sxs-lookup"><span data-stu-id="17218-107">Define the function in a JavaScript Object Notation (JSON) file.</span></span>
<span data-ttu-id="17218-108">*Name* 매개 변수 또는 json 파일을 사용 하 여 함수의 이름을 지정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="17218-108">You can specify the name of the function by using the *Name* parameter or in the .json file.</span></span>
<span data-ttu-id="17218-109">이름을 두 가지 방법으로 모두 지정 하는 경우에는 이름이 일치 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="17218-109">If you specify the name in both ways, the names must match.</span></span>
<span data-ttu-id="17218-110">기존 함수를 바꾸려면 기존 함수의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="17218-110">To replace an existing function, specify the name of the existing function.</span></span>

## <span data-ttu-id="17218-111">예제의</span><span class="sxs-lookup"><span data-stu-id="17218-111">EXAMPLES</span></span>

### <span data-ttu-id="17218-112">예제 1: Stream Analytics 함수 만들기</span><span class="sxs-lookup"><span data-stu-id="17218-112">Example 1: Create a Stream Analytics function</span></span>
```
PS C:\>New-AzStreamAnalyticsFunction -ResourceGroupName "StreamAnalytics-Default-West-US" -JobName "StreamJob07" -File "C:\Function07.json"
```

<span data-ttu-id="17218-113">이 명령은 파일 Function07.js에 있는 함수를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="17218-113">This command creates a function from the file Function07.json.</span></span>
<span data-ttu-id="17218-114">함수의 이름은 json 파일에 저장 됩니다.</span><span class="sxs-lookup"><span data-stu-id="17218-114">The name of the function is stored in the .json file.</span></span>

### <span data-ttu-id="17218-115">예제 2: ScoreTweet 라는 Stream Analytics 함수 만들기</span><span class="sxs-lookup"><span data-stu-id="17218-115">Example 2: Create a Stream Analytics function named ScoreTweet</span></span>
```
PS C:\>New-AzStreamAnalyticsFunction -ResourceGroupName "StreamAnalytics-Default-West-US" -JobName "StreamJob22" -File "C:\Function22.json" -Name "ScoreTweet"
```

<span data-ttu-id="17218-116">이 명령은 ScoreTweet 이라는 작업에 함수를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="17218-116">This command creates a function on the job named ScoreTweet.</span></span>

### <span data-ttu-id="17218-117">예제 3: Stream Analytics 함수 바꾸기</span><span class="sxs-lookup"><span data-stu-id="17218-117">Example 3: Replace a Stream Analytics function</span></span>
```
PS C:\>New-AzStreamAnalyticsFunction -ResourceGroupName "StreamAnalytics-Default-West-US" -JobName "StreamJob22" -File "C:\Function22.json" -Name "ScoreTweet" -Force
```

<span data-ttu-id="17218-118">이 명령은 ScoreTweet 이라는 기존 함수의 정의를 Function22.js의 정의로 바꿉니다.</span><span class="sxs-lookup"><span data-stu-id="17218-118">This command replaces the definition of the existing function named ScoreTweet with the definition in Function22.json.</span></span>

## <span data-ttu-id="17218-119">변수</span><span class="sxs-lookup"><span data-stu-id="17218-119">PARAMETERS</span></span>

### <span data-ttu-id="17218-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="17218-120">-DefaultProfile</span></span>
<span data-ttu-id="17218-121">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="17218-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="17218-122">-파일</span><span class="sxs-lookup"><span data-stu-id="17218-122">-File</span></span>
<span data-ttu-id="17218-123">Stream Analytics 함수의 JSON 표현을 포함 하는 json 파일의 경로를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="17218-123">Specifies the path of a .json file that contains the JSON representation of the Stream Analytics function.</span></span>

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

### <span data-ttu-id="17218-124">-Force</span><span class="sxs-lookup"><span data-stu-id="17218-124">-Force</span></span>
<span data-ttu-id="17218-125">이 cmdlet이 확인 메시지를 표시 하지 않고 기존 Stream Analytics 함수를 대체 합니다.</span><span class="sxs-lookup"><span data-stu-id="17218-125">Indicates that this cmdlet replaces an existing Stream Analytics function without prompting you for confirmation.</span></span>

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

### <span data-ttu-id="17218-126">-JobName</span><span class="sxs-lookup"><span data-stu-id="17218-126">-JobName</span></span>
<span data-ttu-id="17218-127">이 cmdlet이 Stream Analytics 함수를 만드는 스트림 분석 작업의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="17218-127">Specifies the name of the Stream Analytics job under which this cmdlet creates a Stream Analytics function.</span></span>

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

### <span data-ttu-id="17218-128">-이름</span><span class="sxs-lookup"><span data-stu-id="17218-128">-Name</span></span>
<span data-ttu-id="17218-129">이 cmdlet이 만드는 Stream Analytics 함수의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="17218-129">Specifies the name of the Stream Analytics function that this cmdlet creates.</span></span>

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

### <span data-ttu-id="17218-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="17218-130">-ResourceGroupName</span></span>
<span data-ttu-id="17218-131">이 cmdlet이 Stream Analytics 함수를 만드는 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="17218-131">Specifies the name of the resource group under which this cmdlet creates a Stream Analytics function.</span></span>

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

### <span data-ttu-id="17218-132">-확인</span><span class="sxs-lookup"><span data-stu-id="17218-132">-Confirm</span></span>
<span data-ttu-id="17218-133">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="17218-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="17218-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="17218-134">-WhatIf</span></span>
<span data-ttu-id="17218-135">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="17218-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="17218-136">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="17218-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="17218-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="17218-137">CommonParameters</span></span>
<span data-ttu-id="17218-138">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="17218-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="17218-139">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="17218-139">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="17218-140">입력</span><span class="sxs-lookup"><span data-stu-id="17218-140">INPUTS</span></span>

### <span data-ttu-id="17218-141">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="17218-141">System.String</span></span>

## <span data-ttu-id="17218-142">출력</span><span class="sxs-lookup"><span data-stu-id="17218-142">OUTPUTS</span></span>

### <span data-ttu-id="17218-143">Microsoft. i. a i m/. a i m/. i m a 함수</span><span class="sxs-lookup"><span data-stu-id="17218-143">Microsoft.Azure.Commands.StreamAnalytics.Models.PSFunction</span></span>

## <span data-ttu-id="17218-144">상속자</span><span class="sxs-lookup"><span data-stu-id="17218-144">NOTES</span></span>

## <span data-ttu-id="17218-145">관련 링크</span><span class="sxs-lookup"><span data-stu-id="17218-145">RELATED LINKS</span></span>

[<span data-ttu-id="17218-146">Get-AzStreamAnalyticsFunction</span><span class="sxs-lookup"><span data-stu-id="17218-146">Get-AzStreamAnalyticsFunction</span></span>](./Get-AzStreamAnalyticsFunction.md)

[<span data-ttu-id="17218-147">제거-AzStreamAnalyticsFunction</span><span class="sxs-lookup"><span data-stu-id="17218-147">Remove-AzStreamAnalyticsFunction</span></span>](./Remove-AzStreamAnalyticsFunction.md)

[<span data-ttu-id="17218-148">테스트-AzStreamAnalyticsFunction</span><span class="sxs-lookup"><span data-stu-id="17218-148">Test-AzStreamAnalyticsFunction</span></span>](./Test-AzStreamAnalyticsFunction.md)


