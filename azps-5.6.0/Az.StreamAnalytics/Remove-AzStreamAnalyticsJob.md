---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StreamAnalytics.dll-Help.xml
Module Name: Az.StreamAnalytics
ms.assetid: 2F3BDDFE-7585-4802-BFA5-D110F846A33E
online version: https://docs.microsoft.com/powershell/module/az.streamanalytics/remove-azstreamanalyticsjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/Remove-AzStreamAnalyticsJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/Remove-AzStreamAnalyticsJob.md
ms.openlocfilehash: 183aa9dd5cc7da6e0d86c1fa1018bcfe405c0f7e
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101973760"
---
# <span data-ttu-id="e101b-101">Remove-AzStreamAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="e101b-101">Remove-AzStreamAnalyticsJob</span></span>

## <span data-ttu-id="e101b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e101b-102">SYNOPSIS</span></span>
<span data-ttu-id="e101b-103">Stream Analytics 작업을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="e101b-103">Removes a Stream Analytics job.</span></span>

## <span data-ttu-id="e101b-104">구문</span><span class="sxs-lookup"><span data-stu-id="e101b-104">SYNTAX</span></span>

```
Remove-AzStreamAnalyticsJob [-Name] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e101b-105">설명</span><span class="sxs-lookup"><span data-stu-id="e101b-105">DESCRIPTION</span></span>
<span data-ttu-id="e101b-106">**Remove-AzStreamAnalyticsJob** cmdlet은 Azure에서 특정 Stream Analytics 작업을 비동기적으로 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="e101b-106">The **Remove-AzStreamAnalyticsJob** cmdlet asynchronously deletes a specific Stream Analytics job in Azure.</span></span>

## <span data-ttu-id="e101b-107">예제</span><span class="sxs-lookup"><span data-stu-id="e101b-107">EXAMPLES</span></span>

### <span data-ttu-id="e101b-108">예제 1: 작업 제거</span><span class="sxs-lookup"><span data-stu-id="e101b-108">EXAMPLE 1: Remove a job</span></span>
```
PS C:\>Remove-AzStreamAnalyticsJob -ResourceGroupName "StreamAnalytics-Default-West-US" -Name "StreamingJob"
```

<span data-ttu-id="e101b-109">이 명령은 StreamingJob 작업을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="e101b-109">This command removes the job StreamingJob.</span></span>

## <span data-ttu-id="e101b-110">매개 변수</span><span class="sxs-lookup"><span data-stu-id="e101b-110">PARAMETERS</span></span>

### <span data-ttu-id="e101b-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e101b-111">-DefaultProfile</span></span>
<span data-ttu-id="e101b-112">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="e101b-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e101b-113">-Name</span><span class="sxs-lookup"><span data-stu-id="e101b-113">-Name</span></span>
<span data-ttu-id="e101b-114">제거할 Azure Stream Analytics 작업의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="e101b-114">Specifies the name of the Azure Stream Analytics job to remove.</span></span>

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

### <span data-ttu-id="e101b-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e101b-115">-ResourceGroupName</span></span>
<span data-ttu-id="e101b-116">Azure Stream Analytics 작업이 속한 리소스 그룹의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="e101b-116">Specifies the name of the resource group to which the Azure Stream Analytics job belongs.</span></span>

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

### <span data-ttu-id="e101b-117">-확인</span><span class="sxs-lookup"><span data-stu-id="e101b-117">-Confirm</span></span>
<span data-ttu-id="e101b-118">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="e101b-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e101b-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e101b-119">-WhatIf</span></span>
<span data-ttu-id="e101b-120">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="e101b-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e101b-121">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="e101b-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e101b-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e101b-122">CommonParameters</span></span>
<span data-ttu-id="e101b-123">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="e101b-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e101b-124">자세한 내용은 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="e101b-124">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e101b-125">입력</span><span class="sxs-lookup"><span data-stu-id="e101b-125">INPUTS</span></span>

### <span data-ttu-id="e101b-126">System.String</span><span class="sxs-lookup"><span data-stu-id="e101b-126">System.String</span></span>

## <span data-ttu-id="e101b-127">출력</span><span class="sxs-lookup"><span data-stu-id="e101b-127">OUTPUTS</span></span>

### <span data-ttu-id="e101b-128">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="e101b-128">System.Boolean</span></span>

## <span data-ttu-id="e101b-129">참고 사항</span><span class="sxs-lookup"><span data-stu-id="e101b-129">NOTES</span></span>

## <span data-ttu-id="e101b-130">관련 링크</span><span class="sxs-lookup"><span data-stu-id="e101b-130">RELATED LINKS</span></span>

[<span data-ttu-id="e101b-131">Get-AzStreamAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="e101b-131">Get-AzStreamAnalyticsJob</span></span>](./Get-AzStreamAnalyticsJob.md)

[<span data-ttu-id="e101b-132">New-AzStreamAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="e101b-132">New-AzStreamAnalyticsJob</span></span>](./New-AzStreamAnalyticsJob.md)

[<span data-ttu-id="e101b-133">Start-AzStreamAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="e101b-133">Start-AzStreamAnalyticsJob</span></span>](./Start-AzStreamAnalyticsJob.md)

[<span data-ttu-id="e101b-134">Stop-AzStreamAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="e101b-134">Stop-AzStreamAnalyticsJob</span></span>](./Stop-AzStreamAnalyticsJob.md)


