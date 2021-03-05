---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StreamAnalytics.dll-Help.xml
Module Name: Az.StreamAnalytics
ms.assetid: 8FF53426-D4AE-455E-A182-D7FBC7262FE1
online version: https://docs.microsoft.com/powershell/module/az.streamanalytics/new-azstreamanalyticstransformation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/New-AzStreamAnalyticsTransformation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/New-AzStreamAnalyticsTransformation.md
ms.openlocfilehash: d9529d31ab53c16b3d8be10c2d92761a2c8a5fee
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "102007520"
---
# <span data-ttu-id="19d4b-101">New-AzStreamAnalyticsTransformation</span><span class="sxs-lookup"><span data-stu-id="19d4b-101">New-AzStreamAnalyticsTransformation</span></span>

## <span data-ttu-id="19d4b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="19d4b-102">SYNOPSIS</span></span>
<span data-ttu-id="19d4b-103">작업 내에서 변환을 생성하거나 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="19d4b-103">Creates or updates a transformation within a job.</span></span>

## <span data-ttu-id="19d4b-104">구문</span><span class="sxs-lookup"><span data-stu-id="19d4b-104">SYNTAX</span></span>

```
New-AzStreamAnalyticsTransformation [-JobName] <String> [[-Name] <String>] [-File] <String> [-Force]
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="19d4b-105">설명</span><span class="sxs-lookup"><span data-stu-id="19d4b-105">DESCRIPTION</span></span>
<span data-ttu-id="19d4b-106">**New-AzStreamAnalyticsTransformation** cmdlet은 Stream Analytics 작업 내에서 변환을 생성하거나 기존 변환을 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="19d4b-106">The **New-AzStreamAnalyticsTransformation** cmdlet creates a transformation within a Stream Analytics job or updates the existing transformation.</span></span>
<span data-ttu-id="19d4b-107">변환의 이름은 에서 지정할 수 있습니다. JSON 파일 또는 명령줄에 있습니다.</span><span class="sxs-lookup"><span data-stu-id="19d4b-107">The name of the transformation can be specified in the .JSON file or on the command line.</span></span>
<span data-ttu-id="19d4b-108">둘 다 지정되어 있는 경우 명령줄의 이름은 파일의 이름과 일치해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="19d4b-108">If both are specified, the name on command line must match the name in the file.</span></span>
<span data-ttu-id="19d4b-109">이미 있는 변환을 지정하고 Force 매개 변수를 지정하지 않으면 cmdlet에서 기존 변환을 바꿀지 여부를 묻습니다.</span><span class="sxs-lookup"><span data-stu-id="19d4b-109">If you specify a transformation that already exists and do not specify the Force parameter, the cmdlet will ask whether or not to replace the existing transformation.</span></span>
<span data-ttu-id="19d4b-110">Force 매개 변수를 *지정하고* 기존 변환 이름을 지정하면 확인 없이 변환이 대체됩니다.</span><span class="sxs-lookup"><span data-stu-id="19d4b-110">If you specify the *Force* parameter and specify an existing transformation name, the transformation will be replaced without confirmation.</span></span>

## <span data-ttu-id="19d4b-111">예제</span><span class="sxs-lookup"><span data-stu-id="19d4b-111">EXAMPLES</span></span>

### <span data-ttu-id="19d4b-112">예제 1: 작업에서 변환 만들기 또는 바꾸기</span><span class="sxs-lookup"><span data-stu-id="19d4b-112">Example 1: Create or replace a transformation in a job</span></span>
```powershell
PS C:\>New-AzStreamAnalyticsTransformation -ResourceGroupName "StreamAnalytics-Default-West-US" -File "C:\Transformation.json" -JobName "StreamingJob" -Name "StreamingJobTransform"
```

<span data-ttu-id="19d4b-113">이 명령은 StreamingJob이라는 작업에서 StreamingJobTransform이라는 변환을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="19d4b-113">This command creates a transformation called StreamingJobTransform in the job called StreamingJob.</span></span>
<span data-ttu-id="19d4b-114">기존 변환이 해당 이름으로 이미 정의되어 있는 경우 cmdlet은 해당 변환을 바꿀지 여부를 묻습니다.</span><span class="sxs-lookup"><span data-stu-id="19d4b-114">If an existing transformation is already defined with that name, the cmdlet will ask whether or not to replace it.</span></span>

### <span data-ttu-id="19d4b-115">예제 2: 작업의 변환 바꾸기</span><span class="sxs-lookup"><span data-stu-id="19d4b-115">Example 2: Replace a transformation in a job</span></span>
```powershell
PS C:\>New-AzStreamAnalyticsTransformation -ResourceGroupName "StreamAnalytics-Default-West-US" -File "C:\Transformation.json" -JobName "StreamingJob" -Name "StreamingJobTransform" -Force
```

<span data-ttu-id="19d4b-116">이 명령은 확인 없이 StreamingJob 작업에서 StreamingJobTransform의 정의를 대체합니다.</span><span class="sxs-lookup"><span data-stu-id="19d4b-116">This command replaces the definition of StreamingJobTransform in the job StreamingJob without confirmation.</span></span>

## <span data-ttu-id="19d4b-117">매개 변수</span><span class="sxs-lookup"><span data-stu-id="19d4b-117">PARAMETERS</span></span>

### <span data-ttu-id="19d4b-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="19d4b-118">-DefaultProfile</span></span>
<span data-ttu-id="19d4b-119">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="19d4b-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="19d4b-120">-File</span><span class="sxs-lookup"><span data-stu-id="19d4b-120">-File</span></span>
<span data-ttu-id="19d4b-121">만들 Azure Stream Analytics 변환의 JSON 표현이 포함된 JSON 파일의 경로를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="19d4b-121">Specifies the path to a JSON file that contains the JSON representation of the Azure Stream Analytics transformation to create.</span></span>

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

### <span data-ttu-id="19d4b-122">-Force</span><span class="sxs-lookup"><span data-stu-id="19d4b-122">-Force</span></span>
<span data-ttu-id="19d4b-123">사용자 확인을 요청하지 않고 명령을 강제로 실행합니다.</span><span class="sxs-lookup"><span data-stu-id="19d4b-123">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="19d4b-124">-JobName</span><span class="sxs-lookup"><span data-stu-id="19d4b-124">-JobName</span></span>
<span data-ttu-id="19d4b-125">Azure Stream Analytics 변환을 만들 Azure Stream Analytics 작업의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="19d4b-125">Specifies the name of the Azure Stream Analytics job under which to create the Azure Stream Analytics transformation.</span></span>

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

### <span data-ttu-id="19d4b-126">-Name</span><span class="sxs-lookup"><span data-stu-id="19d4b-126">-Name</span></span>
<span data-ttu-id="19d4b-127">만들 Azure Stream Analytics 변환의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="19d4b-127">Specifies the name of the Azure Stream Analytics transformation to create.</span></span>

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

### <span data-ttu-id="19d4b-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="19d4b-128">-ResourceGroupName</span></span>
<span data-ttu-id="19d4b-129">Azure Stream Analytics 변환을 만들 리소스 그룹의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="19d4b-129">Specifies the name of the resource group under which to create the Azure Stream Analytics transformation.</span></span>

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

### <span data-ttu-id="19d4b-130">-확인</span><span class="sxs-lookup"><span data-stu-id="19d4b-130">-Confirm</span></span>
<span data-ttu-id="19d4b-131">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="19d4b-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="19d4b-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="19d4b-132">-WhatIf</span></span>
<span data-ttu-id="19d4b-133">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="19d4b-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="19d4b-134">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="19d4b-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="19d4b-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="19d4b-135">CommonParameters</span></span>
<span data-ttu-id="19d4b-136">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="19d4b-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="19d4b-137">자세한 내용은 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="19d4b-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="19d4b-138">입력</span><span class="sxs-lookup"><span data-stu-id="19d4b-138">INPUTS</span></span>

### <span data-ttu-id="19d4b-139">System.String</span><span class="sxs-lookup"><span data-stu-id="19d4b-139">System.String</span></span>

## <span data-ttu-id="19d4b-140">출력</span><span class="sxs-lookup"><span data-stu-id="19d4b-140">OUTPUTS</span></span>

### <span data-ttu-id="19d4b-141">Microsoft.Azure.Commands.StreamAnalytics.Models.PSTransformation</span><span class="sxs-lookup"><span data-stu-id="19d4b-141">Microsoft.Azure.Commands.StreamAnalytics.Models.PSTransformation</span></span>

## <span data-ttu-id="19d4b-142">참고 사항</span><span class="sxs-lookup"><span data-stu-id="19d4b-142">NOTES</span></span>

## <span data-ttu-id="19d4b-143">관련 링크</span><span class="sxs-lookup"><span data-stu-id="19d4b-143">RELATED LINKS</span></span>

[<span data-ttu-id="19d4b-144">Get-AzStreamAnalyticsTransformation</span><span class="sxs-lookup"><span data-stu-id="19d4b-144">Get-AzStreamAnalyticsTransformation</span></span>](./Get-AzStreamAnalyticsTransformation.md)


