---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StreamAnalytics.dll-Help.xml
Module Name: Az.StreamAnalytics
ms.assetid: 2F3BDDFE-7585-4802-BFA5-D110F846A33E
online version: https://docs.microsoft.com/en-us/powershell/module/az.streamanalytics/remove-azstreamanalyticsjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/Remove-AzStreamAnalyticsJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/Remove-AzStreamAnalyticsJob.md
ms.openlocfilehash: 2b15c1a3b4b69b1a1db3eb25dd953cf62644c8a0
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93873544"
---
# <span data-ttu-id="475fd-101">Remove-AzStreamAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="475fd-101">Remove-AzStreamAnalyticsJob</span></span>

## <span data-ttu-id="475fd-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="475fd-102">SYNOPSIS</span></span>
<span data-ttu-id="475fd-103">Stream Analytics 작업을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="475fd-103">Removes a Stream Analytics job.</span></span>

## <span data-ttu-id="475fd-104">구문과</span><span class="sxs-lookup"><span data-stu-id="475fd-104">SYNTAX</span></span>

```
Remove-AzStreamAnalyticsJob [-Name] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="475fd-105">설명은</span><span class="sxs-lookup"><span data-stu-id="475fd-105">DESCRIPTION</span></span>
<span data-ttu-id="475fd-106">**AzStreamAnalyticsJob** Cmdlet은 Azure에서 특정 Stream Analytics 작업을 비동기적으로 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="475fd-106">The **Remove-AzStreamAnalyticsJob** cmdlet asynchronously deletes a specific Stream Analytics job in Azure.</span></span>

## <span data-ttu-id="475fd-107">예제의</span><span class="sxs-lookup"><span data-stu-id="475fd-107">EXAMPLES</span></span>

### <span data-ttu-id="475fd-108">예제 1: 작업 제거</span><span class="sxs-lookup"><span data-stu-id="475fd-108">EXAMPLE 1: Remove a job</span></span>
```
PS C:\>Remove-AzStreamAnalyticsJob -ResourceGroupName "StreamAnalytics-Default-West-US" -Name "StreamingJob"
```

<span data-ttu-id="475fd-109">이 명령은 작업 StreamingJob을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="475fd-109">This command removes the job StreamingJob.</span></span>

## <span data-ttu-id="475fd-110">변수</span><span class="sxs-lookup"><span data-stu-id="475fd-110">PARAMETERS</span></span>

### <span data-ttu-id="475fd-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="475fd-111">-DefaultProfile</span></span>
<span data-ttu-id="475fd-112">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="475fd-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="475fd-113">-이름</span><span class="sxs-lookup"><span data-stu-id="475fd-113">-Name</span></span>
<span data-ttu-id="475fd-114">제거할 Azure Stream Analytics 작업의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="475fd-114">Specifies the name of the Azure Stream Analytics job to remove.</span></span>

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

### <span data-ttu-id="475fd-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="475fd-115">-ResourceGroupName</span></span>
<span data-ttu-id="475fd-116">Azure Stream Analytics 작업이 속한 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="475fd-116">Specifies the name of the resource group to which the Azure Stream Analytics job belongs.</span></span>

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

### <span data-ttu-id="475fd-117">-확인</span><span class="sxs-lookup"><span data-stu-id="475fd-117">-Confirm</span></span>
<span data-ttu-id="475fd-118">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="475fd-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="475fd-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="475fd-119">-WhatIf</span></span>
<span data-ttu-id="475fd-120">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="475fd-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="475fd-121">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="475fd-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="475fd-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="475fd-122">CommonParameters</span></span>
<span data-ttu-id="475fd-123">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="475fd-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="475fd-124">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="475fd-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="475fd-125">입력</span><span class="sxs-lookup"><span data-stu-id="475fd-125">INPUTS</span></span>

### <span data-ttu-id="475fd-126">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="475fd-126">System.String</span></span>

## <span data-ttu-id="475fd-127">출력</span><span class="sxs-lookup"><span data-stu-id="475fd-127">OUTPUTS</span></span>

### <span data-ttu-id="475fd-128">시스템 부울</span><span class="sxs-lookup"><span data-stu-id="475fd-128">System.Boolean</span></span>

## <span data-ttu-id="475fd-129">상속자</span><span class="sxs-lookup"><span data-stu-id="475fd-129">NOTES</span></span>

## <span data-ttu-id="475fd-130">관련 링크</span><span class="sxs-lookup"><span data-stu-id="475fd-130">RELATED LINKS</span></span>

[<span data-ttu-id="475fd-131">Get-AzStreamAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="475fd-131">Get-AzStreamAnalyticsJob</span></span>](./Get-AzStreamAnalyticsJob.md)

[<span data-ttu-id="475fd-132">새로운 AzStreamAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="475fd-132">New-AzStreamAnalyticsJob</span></span>](./New-AzStreamAnalyticsJob.md)

[<span data-ttu-id="475fd-133">시작-AzStreamAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="475fd-133">Start-AzStreamAnalyticsJob</span></span>](./Start-AzStreamAnalyticsJob.md)

[<span data-ttu-id="475fd-134">중지-AzStreamAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="475fd-134">Stop-AzStreamAnalyticsJob</span></span>](./Stop-AzStreamAnalyticsJob.md)


