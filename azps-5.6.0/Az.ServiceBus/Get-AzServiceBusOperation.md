---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/powershell/module/az.servicebus/get-azservicebusoperation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Get-AzServiceBusOperation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Get-AzServiceBusOperation.md
ms.openlocfilehash: 85dd98ac4eeb262564dcca58ec57f1f5df80842a
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101993398"
---
# <span data-ttu-id="2bc81-101">Get-AzServiceBusOperation</span><span class="sxs-lookup"><span data-stu-id="2bc81-101">Get-AzServiceBusOperation</span></span>

## <span data-ttu-id="2bc81-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2bc81-102">SYNOPSIS</span></span>
<span data-ttu-id="2bc81-103">지원되는 ServiceBus 작업 나열</span><span class="sxs-lookup"><span data-stu-id="2bc81-103">List supported ServiceBus Operations</span></span>

## <span data-ttu-id="2bc81-104">구문</span><span class="sxs-lookup"><span data-stu-id="2bc81-104">SYNTAX</span></span>

```
Get-AzServiceBusOperation [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2bc81-105">설명</span><span class="sxs-lookup"><span data-stu-id="2bc81-105">DESCRIPTION</span></span>
<span data-ttu-id="2bc81-106">**Get-AzServiceBusOperation** cmdlet에는 ServiceBus 지원되는 작업이 나열됩니다.</span><span class="sxs-lookup"><span data-stu-id="2bc81-106">The **Get-AzServiceBusOperation** cmdlet Lists the ServiceBus supported Operations.</span></span>

## <span data-ttu-id="2bc81-107">예제</span><span class="sxs-lookup"><span data-stu-id="2bc81-107">EXAMPLES</span></span>

### <span data-ttu-id="2bc81-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="2bc81-108">Example 1</span></span>
```
PS C:\> Get-AzServiceBusOperation
```

<span data-ttu-id="2bc81-109">ServiceBus 지원되는 작업을 나열합니다.</span><span class="sxs-lookup"><span data-stu-id="2bc81-109">Lists ServiceBus supported operations</span></span>

## <span data-ttu-id="2bc81-110">매개 변수</span><span class="sxs-lookup"><span data-stu-id="2bc81-110">PARAMETERS</span></span>

### <span data-ttu-id="2bc81-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2bc81-111">-DefaultProfile</span></span>
<span data-ttu-id="2bc81-112">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="2bc81-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2bc81-113">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2bc81-113">CommonParameters</span></span>
<span data-ttu-id="2bc81-114">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="2bc81-114">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2bc81-115">자세한 내용은 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="2bc81-115">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2bc81-116">입력</span><span class="sxs-lookup"><span data-stu-id="2bc81-116">INPUTS</span></span>

### <span data-ttu-id="2bc81-117">없음</span><span class="sxs-lookup"><span data-stu-id="2bc81-117">None</span></span>

## <span data-ttu-id="2bc81-118">출력</span><span class="sxs-lookup"><span data-stu-id="2bc81-118">OUTPUTS</span></span>

### <span data-ttu-id="2bc81-119">Microsoft.Azure.Commands.ServiceBus.Models.PSOperationAttributes</span><span class="sxs-lookup"><span data-stu-id="2bc81-119">Microsoft.Azure.Commands.ServiceBus.Models.PSOperationAttributes</span></span>

## <span data-ttu-id="2bc81-120">참고 사항</span><span class="sxs-lookup"><span data-stu-id="2bc81-120">NOTES</span></span>

## <span data-ttu-id="2bc81-121">관련 링크</span><span class="sxs-lookup"><span data-stu-id="2bc81-121">RELATED LINKS</span></span>
