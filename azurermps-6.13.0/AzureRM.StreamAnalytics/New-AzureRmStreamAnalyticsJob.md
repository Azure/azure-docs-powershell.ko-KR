---
external help file: Microsoft.Azure.Commands.StreamAnalytics.dll-Help.xml
Module Name: AzureRM.StreamAnalytics
ms.assetid: F281B351-F7C7-47D1-9745-FFE4BAA840FD
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.streamanalytics/new-azurermstreamanalyticsjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/StreamAnalytics/Commands.StreamAnalytics/help/New-AzureRmStreamAnalyticsJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/StreamAnalytics/Commands.StreamAnalytics/help/New-AzureRmStreamAnalyticsJob.md
ms.openlocfilehash: 540ea984d165a841288d1928192ad0ce035f7eb2
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93530849"
---
# <span data-ttu-id="ac028-101">New-AzureRmStreamAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="ac028-101">New-AzureRmStreamAnalyticsJob</span></span>

## <span data-ttu-id="ac028-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ac028-102">SYNOPSIS</span></span>
<span data-ttu-id="ac028-103">Stream Analytics 작업을 만들거나 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="ac028-103">Creates or updates a Stream Analytics job.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ac028-104">구문과</span><span class="sxs-lookup"><span data-stu-id="ac028-104">SYNTAX</span></span>

```
New-AzureRmStreamAnalyticsJob [[-Name] <String>] [-File] <String> [-Force] [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ac028-105">설명은</span><span class="sxs-lookup"><span data-stu-id="ac028-105">DESCRIPTION</span></span>
<span data-ttu-id="ac028-106">**AzureRmStreamAnalyticsJob** Cmdlet은 Azure에서 새 Stream Analytics 작업을 만들거나 지정 된 기존 작업의 정의를 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="ac028-106">The **New-AzureRmStreamAnalyticsJob** cmdlet creates a new Stream Analytics job in Azure or updates the definition of an existing specified job.</span></span>
<span data-ttu-id="ac028-107">작업 이름은에 지정 될 수 있습니다. JSON 파일 또는 명령줄</span><span class="sxs-lookup"><span data-stu-id="ac028-107">The name of the job can be specified in the .JSON file or on the command line.</span></span>
<span data-ttu-id="ac028-108">둘 다 지정 된 경우 명령줄의 name 명령은 파일의 이름과 일치 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="ac028-108">If both are specified, the name on command line must match the name in the file.</span></span>
<span data-ttu-id="ac028-109">이미 존재 하 고 *Force* 매개 변수를 지정 하지 않은 작업 이름을 지정 하면 cmdlet은 기존 작업을 바꿀지 여부를 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="ac028-109">If you specify a job name that already exists and do not specify the *Force* parameter, the cmdlet will ask whether or not to replace the existing job.</span></span>
<span data-ttu-id="ac028-110">*Force* 매개 변수를 지정 하 고 기존 작업 이름을 지정 하면 작업 정의가 확인 되지 않고 대체 됩니다.</span><span class="sxs-lookup"><span data-stu-id="ac028-110">If you specify the *Force* parameter and specify an existing job name, the job definition will be replaced without confirmation.</span></span>

## <span data-ttu-id="ac028-111">예제의</span><span class="sxs-lookup"><span data-stu-id="ac028-111">EXAMPLES</span></span>

### <span data-ttu-id="ac028-112">예제 1: 작업 만들기</span><span class="sxs-lookup"><span data-stu-id="ac028-112">EXAMPLE 1: Create a job</span></span>
```
PS C:\>New-AzureRmStreamAnalyticsJob -ResourceGroupName "StreamAnalytics-Default-West-US" -File "C:\JobDefinition.json"
```

<span data-ttu-id="ac028-113">이 명령은 JobDefinition.js에 대 한 정의에서 작업을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="ac028-113">This command creates a job from the definition in JobDefinition.json.</span></span>
<span data-ttu-id="ac028-114">작업 정의 파일에서 지정 된 이름의 기존 작업이 이미 정의 되어 있으면 cmdlet에서 해당 작업을 바꿀지 여부를 묻는 메시지가 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="ac028-114">If an existing job with the specified name in the job definition file is already defined, the cmdlet will ask whether or not to replace it.</span></span>

### <span data-ttu-id="ac028-115">예제 2: 작업 정의 바꾸기</span><span class="sxs-lookup"><span data-stu-id="ac028-115">EXAMPLE 2: Replace a job definition</span></span>
```
PS C:\>New-AzureRmStreamAnalyticsJob -ResourceGroupName "StreamAnalytics-Default-West-US" -File "C:\JobDefinition.json" -Name "StreamingJob" -Force
```

<span data-ttu-id="ac028-116">이 명령은 확인 없이 StreamingJob에 대 한 작업 정의를 바꿉니다.</span><span class="sxs-lookup"><span data-stu-id="ac028-116">This command replaces the job definition for StreamingJob without confirmation.</span></span>

## <span data-ttu-id="ac028-117">변수</span><span class="sxs-lookup"><span data-stu-id="ac028-117">PARAMETERS</span></span>

### <span data-ttu-id="ac028-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ac028-118">-DefaultProfile</span></span>
<span data-ttu-id="ac028-119">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="ac028-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ac028-120">-파일</span><span class="sxs-lookup"><span data-stu-id="ac028-120">-File</span></span>
<span data-ttu-id="ac028-121">만들 Azure Stream Analytics 작업의 JSON 표현을 포함 하는 JSON 파일에 대 한 경로를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ac028-121">Specifies the path to a JSON file that contains the JSON representation of the Azure Stream Analytics job to create.</span></span>

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

### <span data-ttu-id="ac028-122">-Force</span><span class="sxs-lookup"><span data-stu-id="ac028-122">-Force</span></span>
<span data-ttu-id="ac028-123">사용자 확인을 요청 하지 않고 명령을 강제로 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="ac028-123">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="ac028-124">-이름</span><span class="sxs-lookup"><span data-stu-id="ac028-124">-Name</span></span>
<span data-ttu-id="ac028-125">만들 Azure Stream Analytics 작업의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ac028-125">Specifies the name of the Azure Stream Analytics job to create.</span></span>

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

### <span data-ttu-id="ac028-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ac028-126">-ResourceGroupName</span></span>
<span data-ttu-id="ac028-127">Azure Stream Analytics 작업을 속해야 하는 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ac028-127">Specifies the name of the resource group to which the Azure Stream Analytics job should belong.</span></span>

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

### <span data-ttu-id="ac028-128">-확인</span><span class="sxs-lookup"><span data-stu-id="ac028-128">-Confirm</span></span>
<span data-ttu-id="ac028-129">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="ac028-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ac028-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ac028-130">-WhatIf</span></span>
<span data-ttu-id="ac028-131">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="ac028-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ac028-132">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="ac028-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ac028-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ac028-133">CommonParameters</span></span>
<span data-ttu-id="ac028-134">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="ac028-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ac028-135">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ac028-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ac028-136">입력</span><span class="sxs-lookup"><span data-stu-id="ac028-136">INPUTS</span></span>

### <span data-ttu-id="ac028-137">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="ac028-137">System.String</span></span>

## <span data-ttu-id="ac028-138">출력</span><span class="sxs-lookup"><span data-stu-id="ac028-138">OUTPUTS</span></span>

### <span data-ttu-id="ac028-139">Microsoft. Azure. PSJob.</span><span class="sxs-lookup"><span data-stu-id="ac028-139">Microsoft.Azure.Commands.StreamAnalytics.Models.PSJob</span></span>

## <span data-ttu-id="ac028-140">상속자</span><span class="sxs-lookup"><span data-stu-id="ac028-140">NOTES</span></span>

## <span data-ttu-id="ac028-141">관련 링크</span><span class="sxs-lookup"><span data-stu-id="ac028-141">RELATED LINKS</span></span>

[<span data-ttu-id="ac028-142">Get-AzureRmStreamAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="ac028-142">Get-AzureRmStreamAnalyticsJob</span></span>](./Get-AzureRmStreamAnalyticsJob.md)

[<span data-ttu-id="ac028-143">제거-AzureRmStreamAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="ac028-143">Remove-AzureRmStreamAnalyticsJob</span></span>](./Remove-AzureRmStreamAnalyticsJob.md)

[<span data-ttu-id="ac028-144">시작-AzureRmStreamAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="ac028-144">Start-AzureRmStreamAnalyticsJob</span></span>](./Start-AzureRmStreamAnalyticsJob.md)

[<span data-ttu-id="ac028-145">중지-AzureRmStreamAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="ac028-145">Stop-AzureRmStreamAnalyticsJob</span></span>](./Stop-AzureRmStreamAnalyticsJob.md)

[<span data-ttu-id="ac028-146">중지-AzureRmStreamAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="ac028-146">Stop-AzureRmStreamAnalyticsJob</span></span>](./Stop-AzureRmStreamAnalyticsJob.md)


