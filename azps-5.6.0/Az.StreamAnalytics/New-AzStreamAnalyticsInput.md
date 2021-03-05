---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StreamAnalytics.dll-Help.xml
Module Name: Az.StreamAnalytics
ms.assetid: 35CE5C5F-F8D4-426F-A33A-4F9EA50E9B83
online version: https://docs.microsoft.com/powershell/module/az.streamanalytics/new-azstreamanalyticsinput
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/New-AzStreamAnalyticsInput.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/New-AzStreamAnalyticsInput.md
ms.openlocfilehash: 6dfb659987178b4bfe65855552e1018d085de360
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101973824"
---
# <span data-ttu-id="363e9-101">New-AzStreamAnalyticsInput</span><span class="sxs-lookup"><span data-stu-id="363e9-101">New-AzStreamAnalyticsInput</span></span>

## <span data-ttu-id="363e9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="363e9-102">SYNOPSIS</span></span>
<span data-ttu-id="363e9-103">작업 입력을 생성하거나 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="363e9-103">Creates or updates a job input.</span></span>

## <span data-ttu-id="363e9-104">구문</span><span class="sxs-lookup"><span data-stu-id="363e9-104">SYNTAX</span></span>

```
New-AzStreamAnalyticsInput [-JobName] <String> [[-Name] <String>] [-File] <String> [-Force]
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="363e9-105">설명</span><span class="sxs-lookup"><span data-stu-id="363e9-105">DESCRIPTION</span></span>
<span data-ttu-id="363e9-106">**New-AzStreamAnalyticsInput** cmdlet은 Stream Analytics 작업 내에서 입력을 생성하거나 기존 입력을 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="363e9-106">The **New-AzStreamAnalyticsInput** cmdlet creates an input within a Stream Analytics job or updates an existing input.</span></span>
<span data-ttu-id="363e9-107">입력의 이름은 JSON 파일 또는 명령줄에 지정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="363e9-107">The name of the input can be specified in the JSON file or on the command line.</span></span>
<span data-ttu-id="363e9-108">둘 다 지정되어 있는 경우 명령줄의 이름은 파일의 이름과 일치해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="363e9-108">If both are specified, the name on command line must match the name in the file.</span></span>
<span data-ttu-id="363e9-109">이미 존재하는 입력을 지정하고 *Force* 매개 변수를 지정하지 않으면 cmdlet에서 기존 입력을 바꿀지 여부를 묻습니다.</span><span class="sxs-lookup"><span data-stu-id="363e9-109">If you specify an input that already exists and do not specify the *Force* parameter, the cmdlet will ask whether or not to replace the existing input.</span></span>
<span data-ttu-id="363e9-110">Force 매개  변수를 지정하고 기존 입력 이름을 지정하면 입력이 확인 없이 대체됩니다.</span><span class="sxs-lookup"><span data-stu-id="363e9-110">If you specify the *Force* parameter and specify an existing input name, the input will be replaced without confirmation.</span></span>

## <span data-ttu-id="363e9-111">예제</span><span class="sxs-lookup"><span data-stu-id="363e9-111">EXAMPLES</span></span>

### <span data-ttu-id="363e9-112">예제 1: 파일에서 정의를 사용하여 작업 입력 만들기</span><span class="sxs-lookup"><span data-stu-id="363e9-112">Example 1: Create a job input with a definition from a file</span></span>
```powershell
PS C:\>New-AzStreamAnalyticsInput -ResourceGroupName "StreamAnalytics-Default-West-US" -JobName "StreamingJob" -File "C:\Input.json"
```

<span data-ttu-id="363e9-113">이 명령은 설정한 파일에서 Input.js만듭니다.</span><span class="sxs-lookup"><span data-stu-id="363e9-113">This command creates an input from the file Input.json.</span></span>
<span data-ttu-id="363e9-114">입력 정의 파일에 지정된 이름이 있는 기존 입력이 이미 정의되어 있는 경우 cmdlet은 이를 바꿀지 여부를 묻습니다.</span><span class="sxs-lookup"><span data-stu-id="363e9-114">If an existing input with the name specified in the input definition file is already defined, the cmdlet will ask whether or not to replace it.</span></span>

### <span data-ttu-id="363e9-115">예제 2: 작업 입력 만들기</span><span class="sxs-lookup"><span data-stu-id="363e9-115">Example 2: Create a job input</span></span>
```powershell
PS C:\>New-AzStreamAnalyticsInput -ResourceGroupName "StreamAnalytics-Default-West-US" -JobName "StreamingJob" -File "C:\Input.json" -Name "EntryStream"
```

<span data-ttu-id="363e9-116">이 명령은 EntryStream이라는 작업에서 새 입력을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="363e9-116">This command creates a new input on the job called EntryStream.</span></span>
<span data-ttu-id="363e9-117">이 이름이 있는 기존 입력이 이미 정의되어 있는 경우 cmdlet은 이 입력을 바꿀지 여부를 묻습니다.</span><span class="sxs-lookup"><span data-stu-id="363e9-117">If an existing input with this name is already defined, the cmdlet will ask whether or not to replace it.</span></span>

### <span data-ttu-id="363e9-118">예제 3: 작업 입력을 파일에서 정의로 바꾸기</span><span class="sxs-lookup"><span data-stu-id="363e9-118">Example 3: Replace a job input with a definition from a file</span></span>
```powershell
PS C:\>New-AzStreamAnalyticsInput -ResourceGroupName "StreamAnalytics-Default-West-US" -JobName "StreamingJob" -File "C:\Input.json" -Name "EntryStream" -Force
```

<span data-ttu-id="363e9-119">이 명령은 EntryStream이라는 기존 입력 원본의 정의를 확인 없이 파일에서 정의로 바 대체합니다.</span><span class="sxs-lookup"><span data-stu-id="363e9-119">This command replaces the definition of the existing input source called EntryStream with the definition from file without confirmation.</span></span>

## <span data-ttu-id="363e9-120">매개 변수</span><span class="sxs-lookup"><span data-stu-id="363e9-120">PARAMETERS</span></span>

### <span data-ttu-id="363e9-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="363e9-121">-DefaultProfile</span></span>
<span data-ttu-id="363e9-122">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="363e9-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="363e9-123">-File</span><span class="sxs-lookup"><span data-stu-id="363e9-123">-File</span></span>
<span data-ttu-id="363e9-124">만들 Azure Stream Analytics 입력의 JSON 표현을 포함하는 JSON 파일의 경로를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="363e9-124">Specifies the path to a JSON file that contains the JSON representation of the Azure Stream Analytics input to create.</span></span>

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

### <span data-ttu-id="363e9-125">-Force</span><span class="sxs-lookup"><span data-stu-id="363e9-125">-Force</span></span>
<span data-ttu-id="363e9-126">사용자 확인을 요청하지 않고 명령을 강제로 실행합니다.</span><span class="sxs-lookup"><span data-stu-id="363e9-126">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="363e9-127">-JobName</span><span class="sxs-lookup"><span data-stu-id="363e9-127">-JobName</span></span>
<span data-ttu-id="363e9-128">Azure Stream Analytics 입력을 만들 Azure Stream Analytics 작업의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="363e9-128">Specifies the name of the Azure Stream Analytics job under which to create the Azure Stream Analytics input.</span></span>

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

### <span data-ttu-id="363e9-129">-Name</span><span class="sxs-lookup"><span data-stu-id="363e9-129">-Name</span></span>
<span data-ttu-id="363e9-130">만들 Azure Stream Analytics 입력의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="363e9-130">Specifies the name of the Azure Stream Analytics input to create.</span></span>

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

### <span data-ttu-id="363e9-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="363e9-131">-ResourceGroupName</span></span>
<span data-ttu-id="363e9-132">Azure Streaming 입력을 만들 리소스 그룹의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="363e9-132">Specifies the name of the resource group under which to create the Azure Streaming input.</span></span>

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

### <span data-ttu-id="363e9-133">-확인</span><span class="sxs-lookup"><span data-stu-id="363e9-133">-Confirm</span></span>
<span data-ttu-id="363e9-134">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="363e9-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="363e9-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="363e9-135">-WhatIf</span></span>
<span data-ttu-id="363e9-136">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="363e9-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="363e9-137">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="363e9-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="363e9-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="363e9-138">CommonParameters</span></span>
<span data-ttu-id="363e9-139">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="363e9-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="363e9-140">자세한 내용은 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="363e9-140">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="363e9-141">입력</span><span class="sxs-lookup"><span data-stu-id="363e9-141">INPUTS</span></span>

### <span data-ttu-id="363e9-142">System.String</span><span class="sxs-lookup"><span data-stu-id="363e9-142">System.String</span></span>

## <span data-ttu-id="363e9-143">출력</span><span class="sxs-lookup"><span data-stu-id="363e9-143">OUTPUTS</span></span>

### <span data-ttu-id="363e9-144">Microsoft.Azure.Commands.StreamAnalytics.Models.PSInput</span><span class="sxs-lookup"><span data-stu-id="363e9-144">Microsoft.Azure.Commands.StreamAnalytics.Models.PSInput</span></span>

## <span data-ttu-id="363e9-145">참고 사항</span><span class="sxs-lookup"><span data-stu-id="363e9-145">NOTES</span></span>

## <span data-ttu-id="363e9-146">관련 링크</span><span class="sxs-lookup"><span data-stu-id="363e9-146">RELATED LINKS</span></span>

[<span data-ttu-id="363e9-147">Get-AzStreamAnalyticsInput</span><span class="sxs-lookup"><span data-stu-id="363e9-147">Get-AzStreamAnalyticsInput</span></span>](./Get-AzStreamAnalyticsInput.md)

[<span data-ttu-id="363e9-148">Remove-AzStreamAnalyticsInput</span><span class="sxs-lookup"><span data-stu-id="363e9-148">Remove-AzStreamAnalyticsInput</span></span>](./Remove-AzStreamAnalyticsInput.md)

[<span data-ttu-id="363e9-149">Test-AzStreamAnalyticsInput</span><span class="sxs-lookup"><span data-stu-id="363e9-149">Test-AzStreamAnalyticsInput</span></span>](./Test-AzStreamAnalyticsInput.md)


