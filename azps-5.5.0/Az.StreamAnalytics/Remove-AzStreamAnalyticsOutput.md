---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StreamAnalytics.dll-Help.xml
Module Name: Az.StreamAnalytics
ms.assetid: EE41BE86-37D4-4A2B-9007-D019CD62BA9D
online version: https://docs.microsoft.com/en-us/powershell/module/az.streamanalytics/remove-azstreamanalyticsoutput
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/Remove-AzStreamAnalyticsOutput.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/Remove-AzStreamAnalyticsOutput.md
ms.openlocfilehash: 23f7c8270f3d5c0073be9705e43086aae3a3e903
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100182924"
---
# <span data-ttu-id="b1a3f-101">Remove-AzStreamAnalyticsOutput</span><span class="sxs-lookup"><span data-stu-id="b1a3f-101">Remove-AzStreamAnalyticsOutput</span></span>

## <span data-ttu-id="b1a3f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b1a3f-102">SYNOPSIS</span></span>
<span data-ttu-id="b1a3f-103">Stream Analytics 작업에서 출력을 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="b1a3f-103">Deletes an output from a Stream Analytics job.</span></span>

## <span data-ttu-id="b1a3f-104">구문</span><span class="sxs-lookup"><span data-stu-id="b1a3f-104">SYNTAX</span></span>

```
Remove-AzStreamAnalyticsOutput [-JobName] <String> [-Name] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b1a3f-105">설명</span><span class="sxs-lookup"><span data-stu-id="b1a3f-105">DESCRIPTION</span></span>
<span data-ttu-id="b1a3f-106">**Remove-AzStreamAnalyticsOutput** cmdlet은 Azure의 Stream Analytics 작업에서 출력을 비동기적으로 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="b1a3f-106">The **Remove-AzStreamAnalyticsOutput** cmdlet asynchronously deletes an output from a Stream Analytics job in Azure.</span></span>

## <span data-ttu-id="b1a3f-107">예제</span><span class="sxs-lookup"><span data-stu-id="b1a3f-107">EXAMPLES</span></span>

### <span data-ttu-id="b1a3f-108">예제 1: 작업에서 출력 제거</span><span class="sxs-lookup"><span data-stu-id="b1a3f-108">EXAMPLE 1: Remove an output from a job</span></span>
```
PS C:\>Remove-AzStreamAnalyticsOutput -ResourceGroupName "StreamAnalytics-Default-West-US" -JobName "StreamingJob" -Name "Output"
```

<span data-ttu-id="b1a3f-109">이 명령은 StreamingJob 작업의 출력 출력을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="b1a3f-109">This command removes the output Output in the job StreamingJob.</span></span>

## <span data-ttu-id="b1a3f-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b1a3f-110">PARAMETERS</span></span>

### <span data-ttu-id="b1a3f-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b1a3f-111">-DefaultProfile</span></span>
<span data-ttu-id="b1a3f-112">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="b1a3f-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b1a3f-113">-JobName</span><span class="sxs-lookup"><span data-stu-id="b1a3f-113">-JobName</span></span>
<span data-ttu-id="b1a3f-114">Azure Stream Analytics 출력이 속한 Azure Stream Analytics 작업의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="b1a3f-114">Specifies the name of the Azure Stream Analytics job to which the Azure Stream Analytics output belongs.</span></span>

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

### <span data-ttu-id="b1a3f-115">-Name</span><span class="sxs-lookup"><span data-stu-id="b1a3f-115">-Name</span></span>
<span data-ttu-id="b1a3f-116">제거할 Azure Stream Analytics 출력의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="b1a3f-116">Specifies the name of the Azure Stream Analytics output to remove.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b1a3f-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b1a3f-117">-ResourceGroupName</span></span>
<span data-ttu-id="b1a3f-118">Azure Stream Analytics 출력이 속한 리소스 그룹의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="b1a3f-118">Specifies the name of the resource group to which the Azure Stream Analytics output belongs.</span></span>

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

### <span data-ttu-id="b1a3f-119">-Confirm</span><span class="sxs-lookup"><span data-stu-id="b1a3f-119">-Confirm</span></span>
<span data-ttu-id="b1a3f-120">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="b1a3f-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b1a3f-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b1a3f-121">-WhatIf</span></span>
<span data-ttu-id="b1a3f-122">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="b1a3f-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b1a3f-123">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="b1a3f-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b1a3f-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b1a3f-124">CommonParameters</span></span>
<span data-ttu-id="b1a3f-125">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="b1a3f-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b1a3f-126">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="b1a3f-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b1a3f-127">입력</span><span class="sxs-lookup"><span data-stu-id="b1a3f-127">INPUTS</span></span>

### <span data-ttu-id="b1a3f-128">System.String</span><span class="sxs-lookup"><span data-stu-id="b1a3f-128">System.String</span></span>

## <span data-ttu-id="b1a3f-129">출력</span><span class="sxs-lookup"><span data-stu-id="b1a3f-129">OUTPUTS</span></span>

### <span data-ttu-id="b1a3f-130">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="b1a3f-130">System.Boolean</span></span>

## <span data-ttu-id="b1a3f-131">참고 사항</span><span class="sxs-lookup"><span data-stu-id="b1a3f-131">NOTES</span></span>

## <span data-ttu-id="b1a3f-132">관련 링크</span><span class="sxs-lookup"><span data-stu-id="b1a3f-132">RELATED LINKS</span></span>

[<span data-ttu-id="b1a3f-133">Get-AzStreamAnalyticsOutput</span><span class="sxs-lookup"><span data-stu-id="b1a3f-133">Get-AzStreamAnalyticsOutput</span></span>](./Get-AzStreamAnalyticsOutput.md)

[<span data-ttu-id="b1a3f-134">New-AzStreamAnalyticsOutput</span><span class="sxs-lookup"><span data-stu-id="b1a3f-134">New-AzStreamAnalyticsOutput</span></span>](./New-AzStreamAnalyticsOutput.md)

[<span data-ttu-id="b1a3f-135">Test-AzStreamAnalyticsOutput</span><span class="sxs-lookup"><span data-stu-id="b1a3f-135">Test-AzStreamAnalyticsOutput</span></span>](./Test-AzStreamAnalyticsOutput.md)


