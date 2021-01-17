---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StreamAnalytics.dll-Help.xml
Module Name: Az.StreamAnalytics
ms.assetid: 43B2A4FD-DA74-403A-89D0-40FE9A3E5A7E
online version: https://docs.microsoft.com/en-us/powershell/module/az.streamanalytics/new-azstreamanalyticsoutput
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/New-AzStreamAnalyticsOutput.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/New-AzStreamAnalyticsOutput.md
ms.openlocfilehash: b0e32d58d416fce869995595c3e2a2ff69e8f349
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98366311"
---
# <span data-ttu-id="c36ce-101">New-AzStreamAnalyticsOutput</span><span class="sxs-lookup"><span data-stu-id="c36ce-101">New-AzStreamAnalyticsOutput</span></span>

## <span data-ttu-id="c36ce-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c36ce-102">SYNOPSIS</span></span>
<span data-ttu-id="c36ce-103">Stream Analytics 작업의 출력을 생성하거나 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="c36ce-103">Creates or updates outputs for a Stream Analytics job.</span></span>

## <span data-ttu-id="c36ce-104">구문</span><span class="sxs-lookup"><span data-stu-id="c36ce-104">SYNTAX</span></span>

```
New-AzStreamAnalyticsOutput [-JobName] <String> [[-Name] <String>] [-File] <String> [-Force]
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="c36ce-105">설명</span><span class="sxs-lookup"><span data-stu-id="c36ce-105">DESCRIPTION</span></span>
<span data-ttu-id="c36ce-106">**New-AzStreamAnalyticsOutput** cmdlet은 Stream Analytics 작업 내에서 출력을 생성하거나 기존 출력을 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="c36ce-106">The **New-AzStreamAnalyticsOutput** cmdlet creates an output within a Stream Analytics job or updates an existing output.</span></span>
<span data-ttu-id="c36ce-107">출력의 이름은 .에서 지정할 수 있습니다. JSON 파일 또는 명령줄에 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c36ce-107">The name of the output can be specified in the .JSON file or on the command line.</span></span>
<span data-ttu-id="c36ce-108">둘 다 지정된 경우 명령줄의 이름이 파일의 이름과 일치해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="c36ce-108">If both are specified, the name on command line must match the name in the file.</span></span>
<span data-ttu-id="c36ce-109">이미 존재하는 출력을 지정하고 *Force* 매개 변수를 지정하지 않으면 cmdlet에서 기존 출력을 바꿀지 여부를 묻습니다.</span><span class="sxs-lookup"><span data-stu-id="c36ce-109">If you specify an output that already exists and do not specify the *Force* parameter, the cmdlet will ask whether or not to replace the existing output.</span></span>
<span data-ttu-id="c36ce-110">Force 매개 변수를 *지정하고* 기존 출력 이름을 지정하면 확인 없이 출력이 대체됩니다.</span><span class="sxs-lookup"><span data-stu-id="c36ce-110">If you specify the *Force* parameter and specify an existing output name, the output will be replaced without confirmation.</span></span>

## <span data-ttu-id="c36ce-111">예제</span><span class="sxs-lookup"><span data-stu-id="c36ce-111">EXAMPLES</span></span>

### <span data-ttu-id="c36ce-112">예제 1: 작업 출력 추가</span><span class="sxs-lookup"><span data-stu-id="c36ce-112">Example 1: Add an output to a job</span></span>
```powershell
PS C:\>New-AzStreamAnalyticsOutput -ResourceGroupName "StreamAnalytics-Default-West-US" -File "C:\Output.json" -JobName "StreamingJob" -Name "Output"
```

<span data-ttu-id="c36ce-113">이 명령은 StreamingJob이라는 작업에서 Output이라는 새 출력을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="c36ce-113">This command creates a new output called Output in the job called StreamingJob.</span></span>
<span data-ttu-id="c36ce-114">이 이름의 기존 출력이 이미 정의되어 있는 경우 cmdlet은 이를 바꿀지 여부를 묻습니다.</span><span class="sxs-lookup"><span data-stu-id="c36ce-114">If an existing output with this name is already defined, the cmdlet will ask whether or not to replace it.</span></span>

### <span data-ttu-id="c36ce-115">예제 2: 작업 출력 정의 바꾸기</span><span class="sxs-lookup"><span data-stu-id="c36ce-115">Example 2: Replace a job output definition</span></span>
```powershell
PS C:\>New-AzStreamAnalyticsOutput -ResourceGroupName "StreamAnalytics-Default-West-US" -File "C:\Output.json" -JobName "StreamingJob" -Name "Output" -Force
```

<span data-ttu-id="c36ce-116">이 명령은 확인 없이 StreamingJob이라는 작업의 출력에 대한 정의를 대체합니다.</span><span class="sxs-lookup"><span data-stu-id="c36ce-116">This command replaces the definition for Output in the job called StreamingJob without confirmation.</span></span>

## <span data-ttu-id="c36ce-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c36ce-117">PARAMETERS</span></span>

### <span data-ttu-id="c36ce-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c36ce-118">-DefaultProfile</span></span>
<span data-ttu-id="c36ce-119">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="c36ce-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c36ce-120">-File</span><span class="sxs-lookup"><span data-stu-id="c36ce-120">-File</span></span>
<span data-ttu-id="c36ce-121">만들 Azure Stream Analytics 출력의 JSON 표현을 포함하는 JSON 파일의 경로를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="c36ce-121">Specifies the path to a JSON file that contains the JSON representation of the Azure Stream Analytics output to create.</span></span>

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

### <span data-ttu-id="c36ce-122">-Force</span><span class="sxs-lookup"><span data-stu-id="c36ce-122">-Force</span></span>
<span data-ttu-id="c36ce-123">사용자 확인을 요청하지 않고 명령을 강제로 실행합니다.</span><span class="sxs-lookup"><span data-stu-id="c36ce-123">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="c36ce-124">-JobName</span><span class="sxs-lookup"><span data-stu-id="c36ce-124">-JobName</span></span>
<span data-ttu-id="c36ce-125">Azure Stream Analytics 출력을 만들 Azure Stream Analytics 작업의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="c36ce-125">Specifies the name of the Azure Stream Analytics job under which to create the Azure Stream Analytics output.</span></span>

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

### <span data-ttu-id="c36ce-126">-Name</span><span class="sxs-lookup"><span data-stu-id="c36ce-126">-Name</span></span>
<span data-ttu-id="c36ce-127">만들 Azure Stream Analytics 출력의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="c36ce-127">Specifies the name of the Azure Stream Analytics output to create.</span></span>

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

### <span data-ttu-id="c36ce-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c36ce-128">-ResourceGroupName</span></span>
<span data-ttu-id="c36ce-129">Azure Stream Analytics 출력을 만들 리소스 그룹의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="c36ce-129">Specifies the name of the resource group under which to create the Azure Stream Analytics output.</span></span>

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

### <span data-ttu-id="c36ce-130">-Confirm</span><span class="sxs-lookup"><span data-stu-id="c36ce-130">-Confirm</span></span>
<span data-ttu-id="c36ce-131">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="c36ce-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c36ce-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c36ce-132">-WhatIf</span></span>
<span data-ttu-id="c36ce-133">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="c36ce-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c36ce-134">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="c36ce-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c36ce-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c36ce-135">CommonParameters</span></span>
<span data-ttu-id="c36ce-136">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="c36ce-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c36ce-137">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="c36ce-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c36ce-138">입력</span><span class="sxs-lookup"><span data-stu-id="c36ce-138">INPUTS</span></span>

### <span data-ttu-id="c36ce-139">System.String</span><span class="sxs-lookup"><span data-stu-id="c36ce-139">System.String</span></span>

## <span data-ttu-id="c36ce-140">출력</span><span class="sxs-lookup"><span data-stu-id="c36ce-140">OUTPUTS</span></span>

### <span data-ttu-id="c36ce-141">Microsoft.Azure.Commands.StreamAnalytics.Models.PSOutput</span><span class="sxs-lookup"><span data-stu-id="c36ce-141">Microsoft.Azure.Commands.StreamAnalytics.Models.PSOutput</span></span>

## <span data-ttu-id="c36ce-142">참고 사항</span><span class="sxs-lookup"><span data-stu-id="c36ce-142">NOTES</span></span>

## <span data-ttu-id="c36ce-143">관련 링크</span><span class="sxs-lookup"><span data-stu-id="c36ce-143">RELATED LINKS</span></span>

[<span data-ttu-id="c36ce-144">Get-AzStreamAnalyticsOutput</span><span class="sxs-lookup"><span data-stu-id="c36ce-144">Get-AzStreamAnalyticsOutput</span></span>](./Get-AzStreamAnalyticsOutput.md)

[<span data-ttu-id="c36ce-145">Remove-AzStreamAnalyticsOutput</span><span class="sxs-lookup"><span data-stu-id="c36ce-145">Remove-AzStreamAnalyticsOutput</span></span>](./Remove-AzStreamAnalyticsOutput.md)

[<span data-ttu-id="c36ce-146">Test-AzStreamAnalyticsOutput</span><span class="sxs-lookup"><span data-stu-id="c36ce-146">Test-AzStreamAnalyticsOutput</span></span>](./Test-AzStreamAnalyticsOutput.md)


