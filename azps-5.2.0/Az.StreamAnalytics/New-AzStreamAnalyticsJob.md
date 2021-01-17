---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StreamAnalytics.dll-Help.xml
Module Name: Az.StreamAnalytics
ms.assetid: F281B351-F7C7-47D1-9745-FFE4BAA840FD
online version: https://docs.microsoft.com/en-us/powershell/module/az.streamanalytics/new-azstreamanalyticsjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/New-AzStreamAnalyticsJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/New-AzStreamAnalyticsJob.md
ms.openlocfilehash: ed5b11684fdb8701343c9390962e95942f4075e9
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98366360"
---
# <span data-ttu-id="2939d-101">New-AzStreamAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="2939d-101">New-AzStreamAnalyticsJob</span></span>

## <span data-ttu-id="2939d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2939d-102">SYNOPSIS</span></span>
<span data-ttu-id="2939d-103">Stream Analytics 작업을 생성하거나 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="2939d-103">Creates or updates a Stream Analytics job.</span></span>

## <span data-ttu-id="2939d-104">구문</span><span class="sxs-lookup"><span data-stu-id="2939d-104">SYNTAX</span></span>

```
New-AzStreamAnalyticsJob [[-Name] <String>] [-File] <String> [-Force] [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2939d-105">설명</span><span class="sxs-lookup"><span data-stu-id="2939d-105">DESCRIPTION</span></span>
<span data-ttu-id="2939d-106">**New-AzStreamAnalyticsJob** cmdlet은 Azure에서 새 Stream Analytics 작업을 만들거나 기존 지정된 작업의 정의를 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="2939d-106">The **New-AzStreamAnalyticsJob** cmdlet creates a new Stream Analytics job in Azure or updates the definition of an existing specified job.</span></span>
<span data-ttu-id="2939d-107">작업의 이름은 .에서 지정할 수 있습니다. JSON 파일 또는 명령줄에 있습니다.</span><span class="sxs-lookup"><span data-stu-id="2939d-107">The name of the job can be specified in the .JSON file or on the command line.</span></span>
<span data-ttu-id="2939d-108">둘 다 지정된 경우 명령줄의 이름이 파일의 이름과 일치해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="2939d-108">If both are specified, the name on command line must match the name in the file.</span></span>
<span data-ttu-id="2939d-109">이미 존재하는 작업 이름을 지정하고 *Force* 매개 변수를 지정하지 않으면 cmdlet에서 기존 작업을 바꿀지 여부를 묻습니다.</span><span class="sxs-lookup"><span data-stu-id="2939d-109">If you specify a job name that already exists and do not specify the *Force* parameter, the cmdlet will ask whether or not to replace the existing job.</span></span>
<span data-ttu-id="2939d-110">*Force* 매개 변수를 지정하고 기존 작업 이름을 지정하면 작업 정의가 확인 없이 대체됩니다.</span><span class="sxs-lookup"><span data-stu-id="2939d-110">If you specify the *Force* parameter and specify an existing job name, the job definition will be replaced without confirmation.</span></span>

## <span data-ttu-id="2939d-111">예제</span><span class="sxs-lookup"><span data-stu-id="2939d-111">EXAMPLES</span></span>

### <span data-ttu-id="2939d-112">예제 1: 작업 만들기</span><span class="sxs-lookup"><span data-stu-id="2939d-112">EXAMPLE 1: Create a job</span></span>
```
PS C:\>New-AzStreamAnalyticsJob -ResourceGroupName "StreamAnalytics-Default-West-US" -File "C:\JobDefinition.json"
```

<span data-ttu-id="2939d-113">이 명령은 JobDefinition.js정의에서 작업을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="2939d-113">This command creates a job from the definition in JobDefinition.json.</span></span>
<span data-ttu-id="2939d-114">작업 정의 파일에 지정된 이름의 기존 작업이 이미 정의되어 있는 경우 cmdlet은 이를 바꿀지 여부를 묻습니다.</span><span class="sxs-lookup"><span data-stu-id="2939d-114">If an existing job with the specified name in the job definition file is already defined, the cmdlet will ask whether or not to replace it.</span></span>

### <span data-ttu-id="2939d-115">예제 2: 작업 정의 바꾸기</span><span class="sxs-lookup"><span data-stu-id="2939d-115">EXAMPLE 2: Replace a job definition</span></span>
```
PS C:\>New-AzStreamAnalyticsJob -ResourceGroupName "StreamAnalytics-Default-West-US" -File "C:\JobDefinition.json" -Name "StreamingJob" -Force
```

<span data-ttu-id="2939d-116">이 명령은 확인 없이 StreamingJob에 대한 작업 정의를 대체합니다.</span><span class="sxs-lookup"><span data-stu-id="2939d-116">This command replaces the job definition for StreamingJob without confirmation.</span></span>

## <span data-ttu-id="2939d-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="2939d-117">PARAMETERS</span></span>

### <span data-ttu-id="2939d-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2939d-118">-DefaultProfile</span></span>
<span data-ttu-id="2939d-119">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="2939d-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2939d-120">-File</span><span class="sxs-lookup"><span data-stu-id="2939d-120">-File</span></span>
<span data-ttu-id="2939d-121">만들 Azure Stream Analytics 작업의 JSON 표현을 포함하는 JSON 파일의 경로를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="2939d-121">Specifies the path to a JSON file that contains the JSON representation of the Azure Stream Analytics job to create.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2939d-122">-Force</span><span class="sxs-lookup"><span data-stu-id="2939d-122">-Force</span></span>
<span data-ttu-id="2939d-123">사용자 확인을 요청하지 않고 명령을 강제로 실행합니다.</span><span class="sxs-lookup"><span data-stu-id="2939d-123">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="2939d-124">-Name</span><span class="sxs-lookup"><span data-stu-id="2939d-124">-Name</span></span>
<span data-ttu-id="2939d-125">만들 Azure Stream Analytics 작업의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="2939d-125">Specifies the name of the Azure Stream Analytics job to create.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2939d-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2939d-126">-ResourceGroupName</span></span>
<span data-ttu-id="2939d-127">Azure Stream Analytics 작업이 속해야 하는 리소스 그룹의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="2939d-127">Specifies the name of the resource group to which the Azure Stream Analytics job should belong.</span></span>

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

### <span data-ttu-id="2939d-128">-Confirm</span><span class="sxs-lookup"><span data-stu-id="2939d-128">-Confirm</span></span>
<span data-ttu-id="2939d-129">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="2939d-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2939d-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2939d-130">-WhatIf</span></span>
<span data-ttu-id="2939d-131">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="2939d-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2939d-132">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="2939d-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2939d-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2939d-133">CommonParameters</span></span>
<span data-ttu-id="2939d-134">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="2939d-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2939d-135">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="2939d-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2939d-136">입력</span><span class="sxs-lookup"><span data-stu-id="2939d-136">INPUTS</span></span>

### <span data-ttu-id="2939d-137">System.String</span><span class="sxs-lookup"><span data-stu-id="2939d-137">System.String</span></span>

## <span data-ttu-id="2939d-138">출력</span><span class="sxs-lookup"><span data-stu-id="2939d-138">OUTPUTS</span></span>

### <span data-ttu-id="2939d-139">Microsoft.Azure.Commands.StreamAnalytics.Models.PSJob</span><span class="sxs-lookup"><span data-stu-id="2939d-139">Microsoft.Azure.Commands.StreamAnalytics.Models.PSJob</span></span>

## <span data-ttu-id="2939d-140">참고 사항</span><span class="sxs-lookup"><span data-stu-id="2939d-140">NOTES</span></span>

## <span data-ttu-id="2939d-141">관련 링크</span><span class="sxs-lookup"><span data-stu-id="2939d-141">RELATED LINKS</span></span>

[<span data-ttu-id="2939d-142">Get-AzStreamAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="2939d-142">Get-AzStreamAnalyticsJob</span></span>](./Get-AzStreamAnalyticsJob.md)

[<span data-ttu-id="2939d-143">Remove-AzStreamAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="2939d-143">Remove-AzStreamAnalyticsJob</span></span>](./Remove-AzStreamAnalyticsJob.md)

[<span data-ttu-id="2939d-144">Start-AzStreamAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="2939d-144">Start-AzStreamAnalyticsJob</span></span>](./Start-AzStreamAnalyticsJob.md)

[<span data-ttu-id="2939d-145">Stop-AzStreamAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="2939d-145">Stop-AzStreamAnalyticsJob</span></span>](./Stop-AzStreamAnalyticsJob.md)

[<span data-ttu-id="2939d-146">Stop-AzStreamAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="2939d-146">Stop-AzStreamAnalyticsJob</span></span>](./Stop-AzStreamAnalyticsJob.md)


