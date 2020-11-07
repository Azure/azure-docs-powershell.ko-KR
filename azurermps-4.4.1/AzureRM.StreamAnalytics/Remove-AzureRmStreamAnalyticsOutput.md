---
external help file: Microsoft.Azure.Commands.StreamAnalytics.dll-Help.xml
Module Name: AzureRM.StreamAnalytics
ms.assetid: EE41BE86-37D4-4A2B-9007-D019CD62BA9D
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/StreamAnalytics/Commands.StreamAnalytics/help/Remove-AzureRmStreamAnalyticsOutput.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/StreamAnalytics/Commands.StreamAnalytics/help/Remove-AzureRmStreamAnalyticsOutput.md
ms.openlocfilehash: 9904699d95429e029f330e5c3ca3e5957eb4c35e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93702183"
---
# <span data-ttu-id="80794-101">Remove-AzureRmStreamAnalyticsOutput</span><span class="sxs-lookup"><span data-stu-id="80794-101">Remove-AzureRmStreamAnalyticsOutput</span></span>

## <span data-ttu-id="80794-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="80794-102">SYNOPSIS</span></span>
<span data-ttu-id="80794-103">Stream Analytics 작업에서 출력을 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="80794-103">Deletes an output from a Stream Analytics job.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="80794-104">구문과</span><span class="sxs-lookup"><span data-stu-id="80794-104">SYNTAX</span></span>

```
Remove-AzureRmStreamAnalyticsOutput [-JobName] <String> [-Name] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="80794-105">설명은</span><span class="sxs-lookup"><span data-stu-id="80794-105">DESCRIPTION</span></span>
<span data-ttu-id="80794-106">**AzureRmStreamAnalyticsOutput** Cmdlet은 Azure에서 Stream Analytics 작업의 출력을 비동기적으로 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="80794-106">The **Remove-AzureRmStreamAnalyticsOutput** cmdlet asynchronously deletes an output from a Stream Analytics job in Azure.</span></span>

## <span data-ttu-id="80794-107">예제의</span><span class="sxs-lookup"><span data-stu-id="80794-107">EXAMPLES</span></span>

### <span data-ttu-id="80794-108">예제 1: 작업에서 출력 제거</span><span class="sxs-lookup"><span data-stu-id="80794-108">EXAMPLE 1: Remove an output from a job</span></span>
```
PS C:\>Remove-AzureRmStreamAnalyticsOutput -ResourceGroupName "StreamAnalytics-Default-West-US" -JobName "StreamingJob" -Name "Output"
```

<span data-ttu-id="80794-109">이 명령은 작업 StreamingJob에서 출력 출력을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="80794-109">This command removes the output Output in the job StreamingJob.</span></span>

## <span data-ttu-id="80794-110">변수</span><span class="sxs-lookup"><span data-stu-id="80794-110">PARAMETERS</span></span>

### <span data-ttu-id="80794-111">-JobName</span><span class="sxs-lookup"><span data-stu-id="80794-111">-JobName</span></span>
<span data-ttu-id="80794-112">Azure Stream Analytics 출력이 속한 Azure Stream Analytics 작업의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="80794-112">Specifies the name of the Azure Stream Analytics job to which the Azure Stream Analytics output belongs.</span></span>

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

### <span data-ttu-id="80794-113">-이름</span><span class="sxs-lookup"><span data-stu-id="80794-113">-Name</span></span>
<span data-ttu-id="80794-114">제거할 Azure Stream Analytics 출력의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="80794-114">Specifies the name of the Azure Stream Analytics output to remove.</span></span>

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

### <span data-ttu-id="80794-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="80794-115">-ResourceGroupName</span></span>
<span data-ttu-id="80794-116">Azure Stream Analytics 출력이 속한 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="80794-116">Specifies the name of the resource group to which the Azure Stream Analytics output belongs.</span></span>

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

### <span data-ttu-id="80794-117">-확인</span><span class="sxs-lookup"><span data-stu-id="80794-117">-Confirm</span></span>
<span data-ttu-id="80794-118">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="80794-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="80794-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="80794-119">-WhatIf</span></span>
<span data-ttu-id="80794-120">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="80794-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="80794-121">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="80794-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="80794-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="80794-122">-DefaultProfile</span></span>
<span data-ttu-id="80794-123">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="80794-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="80794-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="80794-124">CommonParameters</span></span>
<span data-ttu-id="80794-125">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="80794-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="80794-126">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="80794-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="80794-127">입력</span><span class="sxs-lookup"><span data-stu-id="80794-127">INPUTS</span></span>

## <span data-ttu-id="80794-128">출력</span><span class="sxs-lookup"><span data-stu-id="80794-128">OUTPUTS</span></span>

### <span data-ttu-id="80794-129">System. 개체</span><span class="sxs-lookup"><span data-stu-id="80794-129">System.Object</span></span>

## <span data-ttu-id="80794-130">상속자</span><span class="sxs-lookup"><span data-stu-id="80794-130">NOTES</span></span>

## <span data-ttu-id="80794-131">관련 링크</span><span class="sxs-lookup"><span data-stu-id="80794-131">RELATED LINKS</span></span>

[<span data-ttu-id="80794-132">Get-AzureRmStreamAnalyticsOutput</span><span class="sxs-lookup"><span data-stu-id="80794-132">Get-AzureRmStreamAnalyticsOutput</span></span>](./Get-AzureRmStreamAnalyticsOutput.md)

[<span data-ttu-id="80794-133">새로운 AzureRmStreamAnalyticsOutput</span><span class="sxs-lookup"><span data-stu-id="80794-133">New-AzureRmStreamAnalyticsOutput</span></span>](./New-AzureRmStreamAnalyticsOutput.md)

[<span data-ttu-id="80794-134">테스트-AzureRmStreamAnalyticsOutput</span><span class="sxs-lookup"><span data-stu-id="80794-134">Test-AzureRmStreamAnalyticsOutput</span></span>](./Test-AzureRmStreamAnalyticsOutput.md)


