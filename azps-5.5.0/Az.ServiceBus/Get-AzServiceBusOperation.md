---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicebus/get-azservicebusoperation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Get-AzServiceBusOperation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Get-AzServiceBusOperation.md
ms.openlocfilehash: d1ae8cf3d0fd05acf4fa4897d362bd2cde70b346
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100208173"
---
# <span data-ttu-id="47bb0-101">Get-AzServiceBusOperation</span><span class="sxs-lookup"><span data-stu-id="47bb0-101">Get-AzServiceBusOperation</span></span>

## <span data-ttu-id="47bb0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="47bb0-102">SYNOPSIS</span></span>
<span data-ttu-id="47bb0-103">지원되는 ServiceBus 작업 나열</span><span class="sxs-lookup"><span data-stu-id="47bb0-103">List supported ServiceBus Operations</span></span>

## <span data-ttu-id="47bb0-104">구문</span><span class="sxs-lookup"><span data-stu-id="47bb0-104">SYNTAX</span></span>

```
Get-AzServiceBusOperation [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="47bb0-105">설명</span><span class="sxs-lookup"><span data-stu-id="47bb0-105">DESCRIPTION</span></span>
<span data-ttu-id="47bb0-106">**Get-AzServiceBusOperation** cmdlet은 ServiceBus 지원 작업을 나열합니다.</span><span class="sxs-lookup"><span data-stu-id="47bb0-106">The **Get-AzServiceBusOperation** cmdlet Lists the ServiceBus supported Operations.</span></span>

## <span data-ttu-id="47bb0-107">예제</span><span class="sxs-lookup"><span data-stu-id="47bb0-107">EXAMPLES</span></span>

### <span data-ttu-id="47bb0-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="47bb0-108">Example 1</span></span>
```
PS C:\> Get-AzServiceBusOperation
```

<span data-ttu-id="47bb0-109">ServiceBus 지원 작업을 나열합니다.</span><span class="sxs-lookup"><span data-stu-id="47bb0-109">Lists ServiceBus supported operations</span></span>

## <span data-ttu-id="47bb0-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="47bb0-110">PARAMETERS</span></span>

### <span data-ttu-id="47bb0-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="47bb0-111">-DefaultProfile</span></span>
<span data-ttu-id="47bb0-112">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="47bb0-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="47bb0-113">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="47bb0-113">CommonParameters</span></span>
<span data-ttu-id="47bb0-114">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="47bb0-114">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="47bb0-115">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="47bb0-115">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="47bb0-116">입력</span><span class="sxs-lookup"><span data-stu-id="47bb0-116">INPUTS</span></span>

### <span data-ttu-id="47bb0-117">없음</span><span class="sxs-lookup"><span data-stu-id="47bb0-117">None</span></span>

## <span data-ttu-id="47bb0-118">출력</span><span class="sxs-lookup"><span data-stu-id="47bb0-118">OUTPUTS</span></span>

### <span data-ttu-id="47bb0-119">Microsoft.Azure.Commands.ServiceBus.Models.PSOperationAttributes</span><span class="sxs-lookup"><span data-stu-id="47bb0-119">Microsoft.Azure.Commands.ServiceBus.Models.PSOperationAttributes</span></span>

## <span data-ttu-id="47bb0-120">참고 사항</span><span class="sxs-lookup"><span data-stu-id="47bb0-120">NOTES</span></span>

## <span data-ttu-id="47bb0-121">관련 링크</span><span class="sxs-lookup"><span data-stu-id="47bb0-121">RELATED LINKS</span></span>
