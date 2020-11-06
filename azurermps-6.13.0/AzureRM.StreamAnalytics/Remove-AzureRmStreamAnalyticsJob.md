---
external help file: Microsoft.Azure.Commands.StreamAnalytics.dll-Help.xml
Module Name: AzureRM.StreamAnalytics
ms.assetid: 2F3BDDFE-7585-4802-BFA5-D110F846A33E
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.streamanalytics/remove-azurermstreamanalyticsjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/StreamAnalytics/Commands.StreamAnalytics/help/Remove-AzureRmStreamAnalyticsJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/StreamAnalytics/Commands.StreamAnalytics/help/Remove-AzureRmStreamAnalyticsJob.md
ms.openlocfilehash: b6c703b1c3373e4e0f1347d9bb2a9819ac1e5de6
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93530842"
---
# <span data-ttu-id="53aba-101">Remove-AzureRmStreamAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="53aba-101">Remove-AzureRmStreamAnalyticsJob</span></span>

## <span data-ttu-id="53aba-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="53aba-102">SYNOPSIS</span></span>
<span data-ttu-id="53aba-103">Stream Analytics 작업을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="53aba-103">Removes a Stream Analytics job.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="53aba-104">구문과</span><span class="sxs-lookup"><span data-stu-id="53aba-104">SYNTAX</span></span>

```
Remove-AzureRmStreamAnalyticsJob [-Name] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="53aba-105">설명은</span><span class="sxs-lookup"><span data-stu-id="53aba-105">DESCRIPTION</span></span>
<span data-ttu-id="53aba-106">**AzureRmStreamAnalyticsJob** Cmdlet은 Azure에서 특정 Stream Analytics 작업을 비동기적으로 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="53aba-106">The **Remove-AzureRmStreamAnalyticsJob** cmdlet asynchronously deletes a specific Stream Analytics job in Azure.</span></span>

## <span data-ttu-id="53aba-107">예제의</span><span class="sxs-lookup"><span data-stu-id="53aba-107">EXAMPLES</span></span>

### <span data-ttu-id="53aba-108">예제 1: 작업 제거</span><span class="sxs-lookup"><span data-stu-id="53aba-108">EXAMPLE 1: Remove a job</span></span>
```
PS C:\>Remove-AzureRmStreamAnalyticsJob -ResourceGroupName "StreamAnalytics-Default-West-US" -Name "StreamingJob"
```

<span data-ttu-id="53aba-109">이 명령은 작업 StreamingJob을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="53aba-109">This command removes the job StreamingJob.</span></span>

## <span data-ttu-id="53aba-110">변수</span><span class="sxs-lookup"><span data-stu-id="53aba-110">PARAMETERS</span></span>

### <span data-ttu-id="53aba-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="53aba-111">-DefaultProfile</span></span>
<span data-ttu-id="53aba-112">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="53aba-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="53aba-113">-이름</span><span class="sxs-lookup"><span data-stu-id="53aba-113">-Name</span></span>
<span data-ttu-id="53aba-114">제거할 Azure Stream Analytics 작업의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="53aba-114">Specifies the name of the Azure Stream Analytics job to remove.</span></span>

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

### <span data-ttu-id="53aba-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="53aba-115">-ResourceGroupName</span></span>
<span data-ttu-id="53aba-116">Azure Stream Analytics 작업이 속한 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="53aba-116">Specifies the name of the resource group to which the Azure Stream Analytics job belongs.</span></span>

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

### <span data-ttu-id="53aba-117">-확인</span><span class="sxs-lookup"><span data-stu-id="53aba-117">-Confirm</span></span>
<span data-ttu-id="53aba-118">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="53aba-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="53aba-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="53aba-119">-WhatIf</span></span>
<span data-ttu-id="53aba-120">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="53aba-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="53aba-121">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="53aba-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="53aba-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="53aba-122">CommonParameters</span></span>
<span data-ttu-id="53aba-123">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="53aba-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="53aba-124">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="53aba-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="53aba-125">입력</span><span class="sxs-lookup"><span data-stu-id="53aba-125">INPUTS</span></span>

### <span data-ttu-id="53aba-126">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="53aba-126">System.String</span></span>

## <span data-ttu-id="53aba-127">출력</span><span class="sxs-lookup"><span data-stu-id="53aba-127">OUTPUTS</span></span>

### <span data-ttu-id="53aba-128">시스템 부울</span><span class="sxs-lookup"><span data-stu-id="53aba-128">System.Boolean</span></span>

## <span data-ttu-id="53aba-129">상속자</span><span class="sxs-lookup"><span data-stu-id="53aba-129">NOTES</span></span>

## <span data-ttu-id="53aba-130">관련 링크</span><span class="sxs-lookup"><span data-stu-id="53aba-130">RELATED LINKS</span></span>

[<span data-ttu-id="53aba-131">Get-AzureRmStreamAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="53aba-131">Get-AzureRmStreamAnalyticsJob</span></span>](./Get-AzureRmStreamAnalyticsJob.md)

[<span data-ttu-id="53aba-132">새로운 AzureRmStreamAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="53aba-132">New-AzureRmStreamAnalyticsJob</span></span>](./New-AzureRmStreamAnalyticsJob.md)

[<span data-ttu-id="53aba-133">시작-AzureRmStreamAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="53aba-133">Start-AzureRmStreamAnalyticsJob</span></span>](./Start-AzureRmStreamAnalyticsJob.md)

[<span data-ttu-id="53aba-134">중지-AzureRmStreamAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="53aba-134">Stop-AzureRmStreamAnalyticsJob</span></span>](./Stop-AzureRmStreamAnalyticsJob.md)


