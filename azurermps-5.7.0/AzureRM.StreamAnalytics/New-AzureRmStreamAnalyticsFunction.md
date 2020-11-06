---
external help file: Microsoft.Azure.Commands.StreamAnalytics.dll-Help.xml
Module Name: AzureRM
ms.assetid: 79EB2AD9-BFE1-49BE-870F-7DFC99D6FE17
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.streamanalytics/new-azurermstreamanalyticsfunction
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/StreamAnalytics/Commands.StreamAnalytics/help/New-AzureRmStreamAnalyticsFunction.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/StreamAnalytics/Commands.StreamAnalytics/help/New-AzureRmStreamAnalyticsFunction.md
ms.openlocfilehash: 0351a7b139b8bf68f8d7154b65949c1cdda4bbdd
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93531577"
---
# <span data-ttu-id="05363-101">New-AzureRmStreamAnalyticsFunction</span><span class="sxs-lookup"><span data-stu-id="05363-101">New-AzureRmStreamAnalyticsFunction</span></span>

## <span data-ttu-id="05363-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="05363-102">SYNOPSIS</span></span>
<span data-ttu-id="05363-103">Stream Analytics 작업에서 함수를 만들거나 바꿉니다.</span><span class="sxs-lookup"><span data-stu-id="05363-103">Creates or replaces a function in a Stream Analytics job.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="05363-104">구문과</span><span class="sxs-lookup"><span data-stu-id="05363-104">SYNTAX</span></span>

```
New-AzureRmStreamAnalyticsFunction [-JobName] <String> [[-Name] <String>] [-File] <String> [-Force]
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="05363-105">설명은</span><span class="sxs-lookup"><span data-stu-id="05363-105">DESCRIPTION</span></span>
<span data-ttu-id="05363-106">**AzureRmStreamAnalyticsFunction** Cmdlet은 Azure Stream Analytics 작업에서 함수를 만들거나 기존 함수를 대체 합니다.</span><span class="sxs-lookup"><span data-stu-id="05363-106">The **New-AzureRmStreamAnalyticsFunction** cmdlet creates a function in an Azure Stream Analytics job or replaces an existing function.</span></span>
<span data-ttu-id="05363-107">JSON (JavaScript Object Notation) 파일에서 함수를 정의 합니다.</span><span class="sxs-lookup"><span data-stu-id="05363-107">Define the function in a JavaScript Object Notation (JSON) file.</span></span>

<span data-ttu-id="05363-108">*Name* 매개 변수 또는 json 파일을 사용 하 여 함수의 이름을 지정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="05363-108">You can specify the name of the function by using the *Name* parameter or in the .json file.</span></span>
<span data-ttu-id="05363-109">이름을 두 가지 방법으로 모두 지정 하는 경우에는 이름이 일치 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="05363-109">If you specify the name in both ways, the names must match.</span></span>

<span data-ttu-id="05363-110">기존 함수를 바꾸려면 기존 함수의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="05363-110">To replace an existing function, specify the name of the existing function.</span></span>

## <span data-ttu-id="05363-111">예제의</span><span class="sxs-lookup"><span data-stu-id="05363-111">EXAMPLES</span></span>

### <span data-ttu-id="05363-112">예제 1: Stream Analytics 함수 만들기</span><span class="sxs-lookup"><span data-stu-id="05363-112">Example 1: Create a Stream Analytics function</span></span>
```
PS C:\>New-AzureRmStreamAnalyticsFunction -ResourceGroupName "StreamAnalytics-Default-West-US" -JobName "StreamJob07" -File "C:\Function07.json"
```

<span data-ttu-id="05363-113">이 명령은 파일 Function07.js에 있는 함수를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="05363-113">This command creates a function from the file Function07.json.</span></span>
<span data-ttu-id="05363-114">함수의 이름은 json 파일에 저장 됩니다.</span><span class="sxs-lookup"><span data-stu-id="05363-114">The name of the function is stored in the .json file.</span></span>

### <span data-ttu-id="05363-115">예제 2: ScoreTweet 라는 Stream Analytics 함수 만들기</span><span class="sxs-lookup"><span data-stu-id="05363-115">Example 2: Create a Stream Analytics function named ScoreTweet</span></span>
```
PS C:\>New-AzureRmStreamAnalyticsFunction -ResourceGroupName "StreamAnalytics-Default-West-US" -JobName "StreamJob22" -File "C:\Function22.json" -Name "ScoreTweet"
```

<span data-ttu-id="05363-116">이 명령은 ScoreTweet 이라는 작업에 함수를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="05363-116">This command creates a function on the job named ScoreTweet.</span></span>

### <span data-ttu-id="05363-117">예제 3: Stream Analytics 함수 바꾸기</span><span class="sxs-lookup"><span data-stu-id="05363-117">Example 3: Replace a Stream Analytics function</span></span>
```
PS C:\>New-AzureRmStreamAnalyticsFunction -ResourceGroupName "StreamAnalytics-Default-West-US" -JobName "StreamJob22" -File "C:\Function22.json" -Name "ScoreTweet" -Force
```

<span data-ttu-id="05363-118">이 명령은 ScoreTweet 이라는 기존 함수의 정의를 Function22.js의 정의로 바꿉니다.</span><span class="sxs-lookup"><span data-stu-id="05363-118">This command replaces the definition of the existing function named ScoreTweet with the definition in Function22.json.</span></span>

## <span data-ttu-id="05363-119">변수</span><span class="sxs-lookup"><span data-stu-id="05363-119">PARAMETERS</span></span>

### <span data-ttu-id="05363-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="05363-120">-DefaultProfile</span></span>
<span data-ttu-id="05363-121">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="05363-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="05363-122">-파일</span><span class="sxs-lookup"><span data-stu-id="05363-122">-File</span></span>
<span data-ttu-id="05363-123">Stream Analytics 함수의 JSON 표현을 포함 하는 json 파일의 경로를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="05363-123">Specifies the path of a .json file that contains the JSON representation of the Stream Analytics function.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="05363-124">-Force</span><span class="sxs-lookup"><span data-stu-id="05363-124">-Force</span></span>
<span data-ttu-id="05363-125">이 cmdlet이 확인 메시지를 표시 하지 않고 기존 Stream Analytics 함수를 대체 합니다.</span><span class="sxs-lookup"><span data-stu-id="05363-125">Indicates that this cmdlet replaces an existing Stream Analytics function without prompting you for confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="05363-126">-JobName</span><span class="sxs-lookup"><span data-stu-id="05363-126">-JobName</span></span>
<span data-ttu-id="05363-127">이 cmdlet이 Stream Analytics 함수를 만드는 스트림 분석 작업의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="05363-127">Specifies the name of the Stream Analytics job under which this cmdlet creates a Stream Analytics function.</span></span>

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

### <span data-ttu-id="05363-128">-이름</span><span class="sxs-lookup"><span data-stu-id="05363-128">-Name</span></span>
<span data-ttu-id="05363-129">이 cmdlet이 만드는 Stream Analytics 함수의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="05363-129">Specifies the name of the Stream Analytics function that this cmdlet creates.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="05363-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="05363-130">-ResourceGroupName</span></span>
<span data-ttu-id="05363-131">이 cmdlet이 Stream Analytics 함수를 만드는 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="05363-131">Specifies the name of the resource group under which this cmdlet creates a Stream Analytics function.</span></span>

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

### <span data-ttu-id="05363-132">-확인</span><span class="sxs-lookup"><span data-stu-id="05363-132">-Confirm</span></span>
<span data-ttu-id="05363-133">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="05363-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="05363-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="05363-134">-WhatIf</span></span>
<span data-ttu-id="05363-135">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="05363-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="05363-136">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="05363-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="05363-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="05363-137">CommonParameters</span></span>
<span data-ttu-id="05363-138">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="05363-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="05363-139">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="05363-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="05363-140">입력</span><span class="sxs-lookup"><span data-stu-id="05363-140">INPUTS</span></span>

### <span data-ttu-id="05363-141">않아야</span><span class="sxs-lookup"><span data-stu-id="05363-141">None</span></span>
<span data-ttu-id="05363-142">이 cmdlet은 입력을 허용 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="05363-142">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="05363-143">출력</span><span class="sxs-lookup"><span data-stu-id="05363-143">OUTPUTS</span></span>

### <span data-ttu-id="05363-144">Microsoft. i. a i m/. a i m/. i m a 함수</span><span class="sxs-lookup"><span data-stu-id="05363-144">Microsoft.Azure.Commands.StreamAnalytics.Models.PSFunction</span></span>

## <span data-ttu-id="05363-145">상속자</span><span class="sxs-lookup"><span data-stu-id="05363-145">NOTES</span></span>

## <span data-ttu-id="05363-146">관련 링크</span><span class="sxs-lookup"><span data-stu-id="05363-146">RELATED LINKS</span></span>

[<span data-ttu-id="05363-147">Get-AzureRmStreamAnalyticsFunction</span><span class="sxs-lookup"><span data-stu-id="05363-147">Get-AzureRmStreamAnalyticsFunction</span></span>](./Get-AzureRmStreamAnalyticsFunction.md)

[<span data-ttu-id="05363-148">제거-AzureRmStreamAnalyticsFunction</span><span class="sxs-lookup"><span data-stu-id="05363-148">Remove-AzureRmStreamAnalyticsFunction</span></span>](./Remove-AzureRmStreamAnalyticsFunction.md)

[<span data-ttu-id="05363-149">테스트-AzureRmStreamAnalyticsFunction</span><span class="sxs-lookup"><span data-stu-id="05363-149">Test-AzureRmStreamAnalyticsFunction</span></span>](./Test-AzureRmStreamAnalyticsFunction.md)


