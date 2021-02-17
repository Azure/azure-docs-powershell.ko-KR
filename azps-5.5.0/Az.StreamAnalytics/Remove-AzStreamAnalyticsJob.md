---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StreamAnalytics.dll-Help.xml
Module Name: Az.StreamAnalytics
ms.assetid: 2F3BDDFE-7585-4802-BFA5-D110F846A33E
online version: https://docs.microsoft.com/en-us/powershell/module/az.streamanalytics/remove-azstreamanalyticsjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/Remove-AzStreamAnalyticsJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/Remove-AzStreamAnalyticsJob.md
ms.openlocfilehash: 65d0e40fd522d223eed2d0462e5c66beb9e9709a
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100182932"
---
# <span data-ttu-id="7b43b-101">Remove-AzStreamAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="7b43b-101">Remove-AzStreamAnalyticsJob</span></span>

## <span data-ttu-id="7b43b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7b43b-102">SYNOPSIS</span></span>
<span data-ttu-id="7b43b-103">Stream Analytics 작업을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="7b43b-103">Removes a Stream Analytics job.</span></span>

## <span data-ttu-id="7b43b-104">구문</span><span class="sxs-lookup"><span data-stu-id="7b43b-104">SYNTAX</span></span>

```
Remove-AzStreamAnalyticsJob [-Name] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7b43b-105">설명</span><span class="sxs-lookup"><span data-stu-id="7b43b-105">DESCRIPTION</span></span>
<span data-ttu-id="7b43b-106">**Remove-AzStreamAnalyticsJob** cmdlet은 Azure에서 특정 Stream Analytics 작업을 비동기적으로 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="7b43b-106">The **Remove-AzStreamAnalyticsJob** cmdlet asynchronously deletes a specific Stream Analytics job in Azure.</span></span>

## <span data-ttu-id="7b43b-107">예제</span><span class="sxs-lookup"><span data-stu-id="7b43b-107">EXAMPLES</span></span>

### <span data-ttu-id="7b43b-108">예제 1: 작업 제거</span><span class="sxs-lookup"><span data-stu-id="7b43b-108">EXAMPLE 1: Remove a job</span></span>
```
PS C:\>Remove-AzStreamAnalyticsJob -ResourceGroupName "StreamAnalytics-Default-West-US" -Name "StreamingJob"
```

<span data-ttu-id="7b43b-109">이 명령은 StreamingJob 작업을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="7b43b-109">This command removes the job StreamingJob.</span></span>

## <span data-ttu-id="7b43b-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="7b43b-110">PARAMETERS</span></span>

### <span data-ttu-id="7b43b-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7b43b-111">-DefaultProfile</span></span>
<span data-ttu-id="7b43b-112">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="7b43b-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7b43b-113">-Name</span><span class="sxs-lookup"><span data-stu-id="7b43b-113">-Name</span></span>
<span data-ttu-id="7b43b-114">제거할 Azure Stream Analytics 작업의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="7b43b-114">Specifies the name of the Azure Stream Analytics job to remove.</span></span>

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

### <span data-ttu-id="7b43b-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7b43b-115">-ResourceGroupName</span></span>
<span data-ttu-id="7b43b-116">Azure Stream Analytics 작업이 속한 리소스 그룹의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="7b43b-116">Specifies the name of the resource group to which the Azure Stream Analytics job belongs.</span></span>

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

### <span data-ttu-id="7b43b-117">-Confirm</span><span class="sxs-lookup"><span data-stu-id="7b43b-117">-Confirm</span></span>
<span data-ttu-id="7b43b-118">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="7b43b-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7b43b-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7b43b-119">-WhatIf</span></span>
<span data-ttu-id="7b43b-120">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="7b43b-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7b43b-121">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="7b43b-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7b43b-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7b43b-122">CommonParameters</span></span>
<span data-ttu-id="7b43b-123">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="7b43b-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7b43b-124">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="7b43b-124">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7b43b-125">입력</span><span class="sxs-lookup"><span data-stu-id="7b43b-125">INPUTS</span></span>

### <span data-ttu-id="7b43b-126">System.String</span><span class="sxs-lookup"><span data-stu-id="7b43b-126">System.String</span></span>

## <span data-ttu-id="7b43b-127">출력</span><span class="sxs-lookup"><span data-stu-id="7b43b-127">OUTPUTS</span></span>

### <span data-ttu-id="7b43b-128">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="7b43b-128">System.Boolean</span></span>

## <span data-ttu-id="7b43b-129">참고 사항</span><span class="sxs-lookup"><span data-stu-id="7b43b-129">NOTES</span></span>

## <span data-ttu-id="7b43b-130">관련 링크</span><span class="sxs-lookup"><span data-stu-id="7b43b-130">RELATED LINKS</span></span>

[<span data-ttu-id="7b43b-131">Get-AzStreamAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="7b43b-131">Get-AzStreamAnalyticsJob</span></span>](./Get-AzStreamAnalyticsJob.md)

[<span data-ttu-id="7b43b-132">New-AzStreamAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="7b43b-132">New-AzStreamAnalyticsJob</span></span>](./New-AzStreamAnalyticsJob.md)

[<span data-ttu-id="7b43b-133">Start-AzStreamAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="7b43b-133">Start-AzStreamAnalyticsJob</span></span>](./Start-AzStreamAnalyticsJob.md)

[<span data-ttu-id="7b43b-134">Stop-AzStreamAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="7b43b-134">Stop-AzStreamAnalyticsJob</span></span>](./Stop-AzStreamAnalyticsJob.md)


