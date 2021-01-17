---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StreamAnalytics.dll-Help.xml
Module Name: Az.StreamAnalytics
ms.assetid: 1449F64F-A8F9-4E8E-B62B-17DEF3A0FB30
online version: https://docs.microsoft.com/en-us/powershell/module/az.streamanalytics/remove-azstreamanalyticsinput
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/Remove-AzStreamAnalyticsInput.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/Remove-AzStreamAnalyticsInput.md
ms.openlocfilehash: d3c5e578e6921297d7d5edc467e10b9a2b4e9e53
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98384280"
---
# <span data-ttu-id="828b7-101">Remove-AzStreamAnalyticsInput</span><span class="sxs-lookup"><span data-stu-id="828b7-101">Remove-AzStreamAnalyticsInput</span></span>

## <span data-ttu-id="828b7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="828b7-102">SYNOPSIS</span></span>
<span data-ttu-id="828b7-103">Stream Analytics 작업에서 입력을 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="828b7-103">Deletes an input from a Stream Analytics job.</span></span>

## <span data-ttu-id="828b7-104">구문</span><span class="sxs-lookup"><span data-stu-id="828b7-104">SYNTAX</span></span>

```
Remove-AzStreamAnalyticsInput [-JobName] <String> [-Name] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="828b7-105">설명</span><span class="sxs-lookup"><span data-stu-id="828b7-105">DESCRIPTION</span></span>
<span data-ttu-id="828b7-106">**Remove-AzStreamAnalyticsInput** cmdlet은 Azure의 Stream Analytics 작업에서 입력을 비동기적으로 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="828b7-106">The **Remove-AzStreamAnalyticsInput** cmdlet asynchronously deletes an input from a Stream Analytics job in Azure.</span></span>

## <span data-ttu-id="828b7-107">예제</span><span class="sxs-lookup"><span data-stu-id="828b7-107">EXAMPLES</span></span>

### <span data-ttu-id="828b7-108">예제 1: 작업에서 입력 스트림 제거</span><span class="sxs-lookup"><span data-stu-id="828b7-108">EXAMPLE 1: Remove an input stream from a job</span></span>
```
PS C:\>Remove-AzStreamAnalyticsInput -ResourceGroupName "StreamAnalytics-Default-West-US" -JobName "StreamingJob" -Name "EventStream"
```

<span data-ttu-id="828b7-109">이 명령은 StreamingJob에서 입력 EventStream을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="828b7-109">This command removes the input EventStream from StreamingJob.</span></span>

## <span data-ttu-id="828b7-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="828b7-110">PARAMETERS</span></span>

### <span data-ttu-id="828b7-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="828b7-111">-DefaultProfile</span></span>
<span data-ttu-id="828b7-112">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="828b7-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="828b7-113">-JobName</span><span class="sxs-lookup"><span data-stu-id="828b7-113">-JobName</span></span>
<span data-ttu-id="828b7-114">Azure Stream Analytics 입력이 속한 Azure Stream Analytics 작업의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="828b7-114">Specifies the name of the Azure Stream Analytics job to which the Azure Stream Analytics input belongs.</span></span>

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

### <span data-ttu-id="828b7-115">-Name</span><span class="sxs-lookup"><span data-stu-id="828b7-115">-Name</span></span>
<span data-ttu-id="828b7-116">제거할 Azure Stream Analytics 입력의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="828b7-116">Specifies the name of the Azure Stream Analytics input to remove.</span></span>

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

### <span data-ttu-id="828b7-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="828b7-117">-ResourceGroupName</span></span>
<span data-ttu-id="828b7-118">Azure Stream Analytics 입력이 속한 리소스 그룹의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="828b7-118">Specifies the name of the resource group to which the Azure Stream Analytics input belongs.</span></span>

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

### <span data-ttu-id="828b7-119">-Confirm</span><span class="sxs-lookup"><span data-stu-id="828b7-119">-Confirm</span></span>
<span data-ttu-id="828b7-120">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="828b7-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="828b7-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="828b7-121">-WhatIf</span></span>
<span data-ttu-id="828b7-122">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="828b7-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="828b7-123">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="828b7-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="828b7-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="828b7-124">CommonParameters</span></span>
<span data-ttu-id="828b7-125">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="828b7-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="828b7-126">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="828b7-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="828b7-127">입력</span><span class="sxs-lookup"><span data-stu-id="828b7-127">INPUTS</span></span>

### <span data-ttu-id="828b7-128">System.String</span><span class="sxs-lookup"><span data-stu-id="828b7-128">System.String</span></span>

## <span data-ttu-id="828b7-129">출력</span><span class="sxs-lookup"><span data-stu-id="828b7-129">OUTPUTS</span></span>

### <span data-ttu-id="828b7-130">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="828b7-130">System.Boolean</span></span>

## <span data-ttu-id="828b7-131">참고 사항</span><span class="sxs-lookup"><span data-stu-id="828b7-131">NOTES</span></span>

## <span data-ttu-id="828b7-132">관련 링크</span><span class="sxs-lookup"><span data-stu-id="828b7-132">RELATED LINKS</span></span>

[<span data-ttu-id="828b7-133">New-AzStreamAnalyticsInput</span><span class="sxs-lookup"><span data-stu-id="828b7-133">New-AzStreamAnalyticsInput</span></span>](./New-AzStreamAnalyticsInput.md)

[<span data-ttu-id="828b7-134">Get-AzStreamAnalyticsInput</span><span class="sxs-lookup"><span data-stu-id="828b7-134">Get-AzStreamAnalyticsInput</span></span>](./Get-AzStreamAnalyticsInput.md)

[<span data-ttu-id="828b7-135">Test-AzStreamAnalyticsInput</span><span class="sxs-lookup"><span data-stu-id="828b7-135">Test-AzStreamAnalyticsInput</span></span>](./Test-AzStreamAnalyticsInput.md)


