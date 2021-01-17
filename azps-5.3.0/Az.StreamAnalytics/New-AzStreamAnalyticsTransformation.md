---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StreamAnalytics.dll-Help.xml
Module Name: Az.StreamAnalytics
ms.assetid: 8FF53426-D4AE-455E-A182-D7FBC7262FE1
online version: https://docs.microsoft.com/en-us/powershell/module/az.streamanalytics/new-azstreamanalyticstransformation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/New-AzStreamAnalyticsTransformation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/New-AzStreamAnalyticsTransformation.md
ms.openlocfilehash: 017c084e98d8983343ae1f8c19464cc254b26e2e
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98384294"
---
# <span data-ttu-id="3741f-101">New-AzStreamAnalyticsTransformation</span><span class="sxs-lookup"><span data-stu-id="3741f-101">New-AzStreamAnalyticsTransformation</span></span>

## <span data-ttu-id="3741f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3741f-102">SYNOPSIS</span></span>
<span data-ttu-id="3741f-103">작업 내에서 변환을 생성하거나 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="3741f-103">Creates or updates a transformation within a job.</span></span>

## <span data-ttu-id="3741f-104">구문</span><span class="sxs-lookup"><span data-stu-id="3741f-104">SYNTAX</span></span>

```
New-AzStreamAnalyticsTransformation [-JobName] <String> [[-Name] <String>] [-File] <String> [-Force]
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="3741f-105">설명</span><span class="sxs-lookup"><span data-stu-id="3741f-105">DESCRIPTION</span></span>
<span data-ttu-id="3741f-106">**New-AzStreamAnalyticsTransformation** cmdlet은 Stream Analytics 작업 내에서 변환을 생성하거나 기존 변환을 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="3741f-106">The **New-AzStreamAnalyticsTransformation** cmdlet creates a transformation within a Stream Analytics job or updates the existing transformation.</span></span>
<span data-ttu-id="3741f-107">.에서 변환의 이름을 지정할 수 있습니다. JSON 파일 또는 명령줄에 있습니다.</span><span class="sxs-lookup"><span data-stu-id="3741f-107">The name of the transformation can be specified in the .JSON file or on the command line.</span></span>
<span data-ttu-id="3741f-108">둘 다 지정된 경우 명령줄의 이름이 파일의 이름과 일치해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="3741f-108">If both are specified, the name on command line must match the name in the file.</span></span>
<span data-ttu-id="3741f-109">이미 존재하는 변환을 지정하고 Force 매개 변수를 지정하지 않으면 cmdlet에서 기존 변환을 바꿀지 여부를 묻습니다.</span><span class="sxs-lookup"><span data-stu-id="3741f-109">If you specify a transformation that already exists and do not specify the Force parameter, the cmdlet will ask whether or not to replace the existing transformation.</span></span>
<span data-ttu-id="3741f-110">Force 매개 변수를 *지정하고* 기존 변환 이름을 지정하면 변환이 확인 없이 대체됩니다.</span><span class="sxs-lookup"><span data-stu-id="3741f-110">If you specify the *Force* parameter and specify an existing transformation name, the transformation will be replaced without confirmation.</span></span>

## <span data-ttu-id="3741f-111">예제</span><span class="sxs-lookup"><span data-stu-id="3741f-111">EXAMPLES</span></span>

### <span data-ttu-id="3741f-112">예제 1: 작업에서 변환 만들기 또는 바꾸기</span><span class="sxs-lookup"><span data-stu-id="3741f-112">Example 1: Create or replace a transformation in a job</span></span>
```powershell
PS C:\>New-AzStreamAnalyticsTransformation -ResourceGroupName "StreamAnalytics-Default-West-US" -File "C:\Transformation.json" -JobName "StreamingJob" -Name "StreamingJobTransform"
```

<span data-ttu-id="3741f-113">이 명령은 StreamingJob이라는 작업에서 StreamingJobTransform이라는 변환을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="3741f-113">This command creates a transformation called StreamingJobTransform in the job called StreamingJob.</span></span>
<span data-ttu-id="3741f-114">기존 변환이 해당 이름으로 이미 정의되어 있는 경우 cmdlet에서 해당 변환을 바꿀지 여부를 묻습니다.</span><span class="sxs-lookup"><span data-stu-id="3741f-114">If an existing transformation is already defined with that name, the cmdlet will ask whether or not to replace it.</span></span>

### <span data-ttu-id="3741f-115">예제 2: 작업의 변환 바꾸기</span><span class="sxs-lookup"><span data-stu-id="3741f-115">Example 2: Replace a transformation in a job</span></span>
```powershell
PS C:\>New-AzStreamAnalyticsTransformation -ResourceGroupName "StreamAnalytics-Default-West-US" -File "C:\Transformation.json" -JobName "StreamingJob" -Name "StreamingJobTransform" -Force
```

<span data-ttu-id="3741f-116">이 명령은 확인 없이 StreamingJob 작업에서 StreamingJobTransform의 정의를 대체합니다.</span><span class="sxs-lookup"><span data-stu-id="3741f-116">This command replaces the definition of StreamingJobTransform in the job StreamingJob without confirmation.</span></span>

## <span data-ttu-id="3741f-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="3741f-117">PARAMETERS</span></span>

### <span data-ttu-id="3741f-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3741f-118">-DefaultProfile</span></span>
<span data-ttu-id="3741f-119">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="3741f-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3741f-120">-File</span><span class="sxs-lookup"><span data-stu-id="3741f-120">-File</span></span>
<span data-ttu-id="3741f-121">만들 Azure Stream Analytics 변환의 JSON 표현을 포함하는 JSON 파일의 경로를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="3741f-121">Specifies the path to a JSON file that contains the JSON representation of the Azure Stream Analytics transformation to create.</span></span>

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

### <span data-ttu-id="3741f-122">-Force</span><span class="sxs-lookup"><span data-stu-id="3741f-122">-Force</span></span>
<span data-ttu-id="3741f-123">사용자 확인을 요청하지 않고 명령을 강제로 실행합니다.</span><span class="sxs-lookup"><span data-stu-id="3741f-123">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="3741f-124">-JobName</span><span class="sxs-lookup"><span data-stu-id="3741f-124">-JobName</span></span>
<span data-ttu-id="3741f-125">Azure Stream Analytics 변환을 만들 Azure Stream Analytics 작업의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="3741f-125">Specifies the name of the Azure Stream Analytics job under which to create the Azure Stream Analytics transformation.</span></span>

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

### <span data-ttu-id="3741f-126">-Name</span><span class="sxs-lookup"><span data-stu-id="3741f-126">-Name</span></span>
<span data-ttu-id="3741f-127">만들 Azure Stream Analytics 변환의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="3741f-127">Specifies the name of the Azure Stream Analytics transformation to create.</span></span>

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

### <span data-ttu-id="3741f-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3741f-128">-ResourceGroupName</span></span>
<span data-ttu-id="3741f-129">Azure Stream Analytics 변환을 만들 리소스 그룹의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="3741f-129">Specifies the name of the resource group under which to create the Azure Stream Analytics transformation.</span></span>

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

### <span data-ttu-id="3741f-130">-Confirm</span><span class="sxs-lookup"><span data-stu-id="3741f-130">-Confirm</span></span>
<span data-ttu-id="3741f-131">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="3741f-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3741f-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3741f-132">-WhatIf</span></span>
<span data-ttu-id="3741f-133">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="3741f-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3741f-134">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="3741f-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3741f-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3741f-135">CommonParameters</span></span>
<span data-ttu-id="3741f-136">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="3741f-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3741f-137">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="3741f-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3741f-138">입력</span><span class="sxs-lookup"><span data-stu-id="3741f-138">INPUTS</span></span>

### <span data-ttu-id="3741f-139">System.String</span><span class="sxs-lookup"><span data-stu-id="3741f-139">System.String</span></span>

## <span data-ttu-id="3741f-140">출력</span><span class="sxs-lookup"><span data-stu-id="3741f-140">OUTPUTS</span></span>

### <span data-ttu-id="3741f-141">Microsoft.Azure.Commands.StreamAnalytics.Models.PSTransformation</span><span class="sxs-lookup"><span data-stu-id="3741f-141">Microsoft.Azure.Commands.StreamAnalytics.Models.PSTransformation</span></span>

## <span data-ttu-id="3741f-142">참고 사항</span><span class="sxs-lookup"><span data-stu-id="3741f-142">NOTES</span></span>

## <span data-ttu-id="3741f-143">관련 링크</span><span class="sxs-lookup"><span data-stu-id="3741f-143">RELATED LINKS</span></span>

[<span data-ttu-id="3741f-144">Get-AzStreamAnalyticsTransformation</span><span class="sxs-lookup"><span data-stu-id="3741f-144">Get-AzStreamAnalyticsTransformation</span></span>](./Get-AzStreamAnalyticsTransformation.md)


