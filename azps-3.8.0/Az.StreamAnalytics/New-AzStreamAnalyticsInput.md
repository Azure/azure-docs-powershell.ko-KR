---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StreamAnalytics.dll-Help.xml
Module Name: Az.StreamAnalytics
ms.assetid: 35CE5C5F-F8D4-426F-A33A-4F9EA50E9B83
online version: https://docs.microsoft.com/en-us/powershell/module/az.streamanalytics/new-azstreamanalyticsinput
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/New-AzStreamAnalyticsInput.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/New-AzStreamAnalyticsInput.md
ms.openlocfilehash: 6b9fb63bfeba8d7708389a8730ec4bcdfab55f6d
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93878009"
---
# <span data-ttu-id="027b2-101">New-AzStreamAnalyticsInput</span><span class="sxs-lookup"><span data-stu-id="027b2-101">New-AzStreamAnalyticsInput</span></span>

## <span data-ttu-id="027b2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="027b2-102">SYNOPSIS</span></span>
<span data-ttu-id="027b2-103">작업 입력을 만들거나 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="027b2-103">Creates or updates a job input.</span></span>

## <span data-ttu-id="027b2-104">구문과</span><span class="sxs-lookup"><span data-stu-id="027b2-104">SYNTAX</span></span>

```
New-AzStreamAnalyticsInput [-JobName] <String> [[-Name] <String>] [-File] <String> [-Force]
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="027b2-105">설명은</span><span class="sxs-lookup"><span data-stu-id="027b2-105">DESCRIPTION</span></span>
<span data-ttu-id="027b2-106">**AzStreamAnalyticsInput** Cmdlet은 Stream Analytics 작업 내에 입력을 만들거나 기존 입력을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="027b2-106">The **New-AzStreamAnalyticsInput** cmdlet creates an input within a Stream Analytics job or updates an existing input.</span></span>
<span data-ttu-id="027b2-107">입력 이름은 JSON 파일 또는 명령줄에서 지정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="027b2-107">The name of the input can be specified in the JSON file or on the command line.</span></span>
<span data-ttu-id="027b2-108">둘 다 지정 된 경우 명령줄의 name 명령은 파일의 이름과 일치 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="027b2-108">If both are specified, the name on command line must match the name in the file.</span></span>
<span data-ttu-id="027b2-109">이미 존재 하 고 *Force* 매개 변수를 지정 하지 않은 입력을 지정 하는 경우 cmdlet은 기존 입력을 바꿀지 여부를 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="027b2-109">If you specify an input that already exists and do not specify the *Force* parameter, the cmdlet will ask whether or not to replace the existing input.</span></span>
<span data-ttu-id="027b2-110">*Force* 매개 변수를 지정 하 고 기존 입력 이름을 지정 하면 입력이 확인 없이 바뀝니다.</span><span class="sxs-lookup"><span data-stu-id="027b2-110">If you specify the *Force* parameter and specify an existing input name, the input will be replaced without confirmation.</span></span>

## <span data-ttu-id="027b2-111">예제의</span><span class="sxs-lookup"><span data-stu-id="027b2-111">EXAMPLES</span></span>

### <span data-ttu-id="027b2-112">예제 1: 파일의 정의를 사용 하 여 작업 입력 만들기</span><span class="sxs-lookup"><span data-stu-id="027b2-112">EXAMPLE 1: Create a job input with a definition from a file</span></span>
```
PS C:\>New-AzStreamAnalyticsInput -ResourceGroupName "StreamAnalytics-Default-West-US" -JobName "StreamingJob" -File "C:\Input.json"
```

<span data-ttu-id="027b2-113">이 명령은 파일 Input.js에 대 한 입력을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="027b2-113">This command creates an input from the file Input.json.</span></span>
<span data-ttu-id="027b2-114">입력 정의 파일에 지정 된 이름을 사용 하는 기존 입력이 이미 정의 되어 있는 경우 cmdlet은이를 바꿀 것인지 여부를 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="027b2-114">If an existing input with the name specified in the input definition file is already defined, the cmdlet will ask whether or not to replace it.</span></span>

### <span data-ttu-id="027b2-115">예제 2: 작업 입력 만들기</span><span class="sxs-lookup"><span data-stu-id="027b2-115">EXAMPLE 2: Create a job input</span></span>
```
PS C:\>New-AzStreamAnalyticsInput -ResourceGroupName "StreamAnalytics-Default-West-US" -JobName "StreamingJob" -File "C:\Input.json" -Name "EntryStream"
```

<span data-ttu-id="027b2-116">이 명령은 EntryStream 이라는 작업에 새 입력을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="027b2-116">This command creates a new input on the job called EntryStream.</span></span>
<span data-ttu-id="027b2-117">이 이름을 사용 하는 기존 입력이 이미 정의 되어 있는 경우 cmdlet은이를 바꿀 것인지 여부를 묻는 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="027b2-117">If an existing input with this name is already defined, the cmdlet will ask whether or not to replace it.</span></span>

### <span data-ttu-id="027b2-118">예제 3: 작업 입력을 파일의 정의로 바꾸기</span><span class="sxs-lookup"><span data-stu-id="027b2-118">EXAMPLE 3: Replace a job input with a definition from a file</span></span>
```
PS C:\>New-AzStreamAnalyticsInput -ResourceGroupName "StreamAnalytics-Default-West-US" -JobName "StreamingJob" -File "C:\Input.json" -Name "EntryStream" -Force
```

<span data-ttu-id="027b2-119">이 명령은 확인 하지 않고 파일의 정의를 사용 하 여 EntryStream 이라는 기존 입력 원본의 정의를 바꿉니다.</span><span class="sxs-lookup"><span data-stu-id="027b2-119">This command replaces the definition of the existing input source called EntryStream with the definition from file without confirmation.</span></span>

## <span data-ttu-id="027b2-120">변수</span><span class="sxs-lookup"><span data-stu-id="027b2-120">PARAMETERS</span></span>

### <span data-ttu-id="027b2-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="027b2-121">-DefaultProfile</span></span>
<span data-ttu-id="027b2-122">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="027b2-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="027b2-123">-파일</span><span class="sxs-lookup"><span data-stu-id="027b2-123">-File</span></span>
<span data-ttu-id="027b2-124">만들 Azure Stream Analytics 입력의 JSON 표현을 포함 하는 JSON 파일의 경로를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="027b2-124">Specifies the path to a JSON file that contains the JSON representation of the Azure Stream Analytics input to create.</span></span>

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

### <span data-ttu-id="027b2-125">-Force</span><span class="sxs-lookup"><span data-stu-id="027b2-125">-Force</span></span>
<span data-ttu-id="027b2-126">사용자 확인을 요청 하지 않고 명령을 강제로 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="027b2-126">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="027b2-127">-JobName</span><span class="sxs-lookup"><span data-stu-id="027b2-127">-JobName</span></span>
<span data-ttu-id="027b2-128">Azure Stream Analytics 입력을 만들 Azure Stream Analytics 작업의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="027b2-128">Specifies the name of the Azure Stream Analytics job under which to create the Azure Stream Analytics input.</span></span>

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

### <span data-ttu-id="027b2-129">-이름</span><span class="sxs-lookup"><span data-stu-id="027b2-129">-Name</span></span>
<span data-ttu-id="027b2-130">만들 Azure Stream Analytics 입력의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="027b2-130">Specifies the name of the Azure Stream Analytics input to create.</span></span>

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

### <span data-ttu-id="027b2-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="027b2-131">-ResourceGroupName</span></span>
<span data-ttu-id="027b2-132">Azure 스트리밍 입력을 만들 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="027b2-132">Specifies the name of the resource group under which to create the Azure Streaming input.</span></span>

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

### <span data-ttu-id="027b2-133">-확인</span><span class="sxs-lookup"><span data-stu-id="027b2-133">-Confirm</span></span>
<span data-ttu-id="027b2-134">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="027b2-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="027b2-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="027b2-135">-WhatIf</span></span>
<span data-ttu-id="027b2-136">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="027b2-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="027b2-137">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="027b2-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="027b2-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="027b2-138">CommonParameters</span></span>
<span data-ttu-id="027b2-139">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="027b2-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="027b2-140">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="027b2-140">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="027b2-141">입력</span><span class="sxs-lookup"><span data-stu-id="027b2-141">INPUTS</span></span>

### <span data-ttu-id="027b2-142">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="027b2-142">System.String</span></span>

## <span data-ttu-id="027b2-143">출력</span><span class="sxs-lookup"><span data-stu-id="027b2-143">OUTPUTS</span></span>

### <span data-ttu-id="027b2-144">Microsoft. StreamAnalytics. PSInput</span><span class="sxs-lookup"><span data-stu-id="027b2-144">Microsoft.Azure.Commands.StreamAnalytics.Models.PSInput</span></span>

## <span data-ttu-id="027b2-145">상속자</span><span class="sxs-lookup"><span data-stu-id="027b2-145">NOTES</span></span>

## <span data-ttu-id="027b2-146">관련 링크</span><span class="sxs-lookup"><span data-stu-id="027b2-146">RELATED LINKS</span></span>

[<span data-ttu-id="027b2-147">Get-AzStreamAnalyticsInput</span><span class="sxs-lookup"><span data-stu-id="027b2-147">Get-AzStreamAnalyticsInput</span></span>](./Get-AzStreamAnalyticsInput.md)

[<span data-ttu-id="027b2-148">제거-AzStreamAnalyticsInput</span><span class="sxs-lookup"><span data-stu-id="027b2-148">Remove-AzStreamAnalyticsInput</span></span>](./Remove-AzStreamAnalyticsInput.md)

[<span data-ttu-id="027b2-149">테스트-AzStreamAnalyticsInput</span><span class="sxs-lookup"><span data-stu-id="027b2-149">Test-AzStreamAnalyticsInput</span></span>](./Test-AzStreamAnalyticsInput.md)


