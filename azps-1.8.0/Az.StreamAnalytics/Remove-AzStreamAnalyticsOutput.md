---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StreamAnalytics.dll-Help.xml
Module Name: Az.StreamAnalytics
ms.assetid: EE41BE86-37D4-4A2B-9007-D019CD62BA9D
online version: https://docs.microsoft.com/en-us/powershell/module/az.streamanalytics/remove-azstreamanalyticsoutput
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/Remove-AzStreamAnalyticsOutput.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/Remove-AzStreamAnalyticsOutput.md
ms.openlocfilehash: 53bd361d67829fdf30741540f1435032067508e7
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93698441"
---
# <span data-ttu-id="8ddd3-101">Remove-AzStreamAnalyticsOutput</span><span class="sxs-lookup"><span data-stu-id="8ddd3-101">Remove-AzStreamAnalyticsOutput</span></span>

## <span data-ttu-id="8ddd3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8ddd3-102">SYNOPSIS</span></span>
<span data-ttu-id="8ddd3-103">Stream Analytics 작업에서 출력을 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="8ddd3-103">Deletes an output from a Stream Analytics job.</span></span>

## <span data-ttu-id="8ddd3-104">구문과</span><span class="sxs-lookup"><span data-stu-id="8ddd3-104">SYNTAX</span></span>

```
Remove-AzStreamAnalyticsOutput [-JobName] <String> [-Name] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8ddd3-105">설명은</span><span class="sxs-lookup"><span data-stu-id="8ddd3-105">DESCRIPTION</span></span>
<span data-ttu-id="8ddd3-106">**AzStreamAnalyticsOutput** Cmdlet은 Azure에서 Stream Analytics 작업의 출력을 비동기적으로 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="8ddd3-106">The **Remove-AzStreamAnalyticsOutput** cmdlet asynchronously deletes an output from a Stream Analytics job in Azure.</span></span>

## <span data-ttu-id="8ddd3-107">예제의</span><span class="sxs-lookup"><span data-stu-id="8ddd3-107">EXAMPLES</span></span>

### <span data-ttu-id="8ddd3-108">예제 1: 작업에서 출력 제거</span><span class="sxs-lookup"><span data-stu-id="8ddd3-108">EXAMPLE 1: Remove an output from a job</span></span>
```
PS C:\>Remove-AzStreamAnalyticsOutput -ResourceGroupName "StreamAnalytics-Default-West-US" -JobName "StreamingJob" -Name "Output"
```

<span data-ttu-id="8ddd3-109">이 명령은 작업 StreamingJob에서 출력 출력을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="8ddd3-109">This command removes the output Output in the job StreamingJob.</span></span>

## <span data-ttu-id="8ddd3-110">변수</span><span class="sxs-lookup"><span data-stu-id="8ddd3-110">PARAMETERS</span></span>

### <span data-ttu-id="8ddd3-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8ddd3-111">-DefaultProfile</span></span>
<span data-ttu-id="8ddd3-112">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="8ddd3-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8ddd3-113">-JobName</span><span class="sxs-lookup"><span data-stu-id="8ddd3-113">-JobName</span></span>
<span data-ttu-id="8ddd3-114">Azure Stream Analytics 출력이 속한 Azure Stream Analytics 작업의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="8ddd3-114">Specifies the name of the Azure Stream Analytics job to which the Azure Stream Analytics output belongs.</span></span>

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

### <span data-ttu-id="8ddd3-115">-이름</span><span class="sxs-lookup"><span data-stu-id="8ddd3-115">-Name</span></span>
<span data-ttu-id="8ddd3-116">제거할 Azure Stream Analytics 출력의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="8ddd3-116">Specifies the name of the Azure Stream Analytics output to remove.</span></span>

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

### <span data-ttu-id="8ddd3-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8ddd3-117">-ResourceGroupName</span></span>
<span data-ttu-id="8ddd3-118">Azure Stream Analytics 출력이 속한 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="8ddd3-118">Specifies the name of the resource group to which the Azure Stream Analytics output belongs.</span></span>

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

### <span data-ttu-id="8ddd3-119">-확인</span><span class="sxs-lookup"><span data-stu-id="8ddd3-119">-Confirm</span></span>
<span data-ttu-id="8ddd3-120">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="8ddd3-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8ddd3-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8ddd3-121">-WhatIf</span></span>
<span data-ttu-id="8ddd3-122">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="8ddd3-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8ddd3-123">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="8ddd3-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8ddd3-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8ddd3-124">CommonParameters</span></span>
<span data-ttu-id="8ddd3-125">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="8ddd3-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8ddd3-126">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8ddd3-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8ddd3-127">입력</span><span class="sxs-lookup"><span data-stu-id="8ddd3-127">INPUTS</span></span>

### <span data-ttu-id="8ddd3-128">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="8ddd3-128">System.String</span></span>

## <span data-ttu-id="8ddd3-129">출력</span><span class="sxs-lookup"><span data-stu-id="8ddd3-129">OUTPUTS</span></span>

### <span data-ttu-id="8ddd3-130">시스템 부울</span><span class="sxs-lookup"><span data-stu-id="8ddd3-130">System.Boolean</span></span>

## <span data-ttu-id="8ddd3-131">상속자</span><span class="sxs-lookup"><span data-stu-id="8ddd3-131">NOTES</span></span>

## <span data-ttu-id="8ddd3-132">관련 링크</span><span class="sxs-lookup"><span data-stu-id="8ddd3-132">RELATED LINKS</span></span>

[<span data-ttu-id="8ddd3-133">Get-AzStreamAnalyticsOutput</span><span class="sxs-lookup"><span data-stu-id="8ddd3-133">Get-AzStreamAnalyticsOutput</span></span>](./Get-AzStreamAnalyticsOutput.md)

[<span data-ttu-id="8ddd3-134">새로운 AzStreamAnalyticsOutput</span><span class="sxs-lookup"><span data-stu-id="8ddd3-134">New-AzStreamAnalyticsOutput</span></span>](./New-AzStreamAnalyticsOutput.md)

[<span data-ttu-id="8ddd3-135">테스트-AzStreamAnalyticsOutput</span><span class="sxs-lookup"><span data-stu-id="8ddd3-135">Test-AzStreamAnalyticsOutput</span></span>](./Test-AzStreamAnalyticsOutput.md)


