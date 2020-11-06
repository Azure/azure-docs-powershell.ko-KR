---
external help file: Microsoft.Azure.Commands.ServiceBus.dll-Help.xml
Module Name: AzureRM.ServiceBus
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Get-AzureRmServiceBusOperation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Get-AzureRmServiceBusOperation.md
ms.openlocfilehash: fbbac617687712208730393b978a3df5b404aeb5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93530669"
---
# <span data-ttu-id="272fd-101">Get-AzureRmServiceBusOperation</span><span class="sxs-lookup"><span data-stu-id="272fd-101">Get-AzureRmServiceBusOperation</span></span>

## <span data-ttu-id="272fd-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="272fd-102">SYNOPSIS</span></span>
<span data-ttu-id="272fd-103">지원 되는 ServiceBus 작업 나열</span><span class="sxs-lookup"><span data-stu-id="272fd-103">List supported ServiceBus Operations</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="272fd-104">구문과</span><span class="sxs-lookup"><span data-stu-id="272fd-104">SYNTAX</span></span>

```
Get-AzureRmServiceBusOperation [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="272fd-105">설명은</span><span class="sxs-lookup"><span data-stu-id="272fd-105">DESCRIPTION</span></span>
<span data-ttu-id="272fd-106">**AzureRmServiceBusOperation** cmdlet에는 ServiceBus 지원 되는 작업이 나열 됩니다.</span><span class="sxs-lookup"><span data-stu-id="272fd-106">The **Get-AzureRmServiceBusOperation** cmdlet Lists the ServiceBus supported Operations.</span></span>

## <span data-ttu-id="272fd-107">예제의</span><span class="sxs-lookup"><span data-stu-id="272fd-107">EXAMPLES</span></span>

### <span data-ttu-id="272fd-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="272fd-108">Example 1</span></span>
```
PS C:\> Get-AzureRmServiceBusOperation
```

<span data-ttu-id="272fd-109">ServiceBus 지원 되는 작업 나열</span><span class="sxs-lookup"><span data-stu-id="272fd-109">Lists ServiceBus supported operations</span></span>

## <span data-ttu-id="272fd-110">변수</span><span class="sxs-lookup"><span data-stu-id="272fd-110">PARAMETERS</span></span>

### <span data-ttu-id="272fd-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="272fd-111">-DefaultProfile</span></span>
<span data-ttu-id="272fd-112">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="272fd-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="272fd-113">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="272fd-113">CommonParameters</span></span>
<span data-ttu-id="272fd-114">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="272fd-114">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="272fd-115">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="272fd-115">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="272fd-116">입력</span><span class="sxs-lookup"><span data-stu-id="272fd-116">INPUTS</span></span>

### <span data-ttu-id="272fd-117">않아야</span><span class="sxs-lookup"><span data-stu-id="272fd-117">None</span></span>

### <span data-ttu-id="272fd-118">System.webserver. List ' 1 [[ServiceBus]. ServiceBus, Version = 0.4.2.0, Culture = 중립, PublicKeyToken = null]]을 목록으로 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="272fd-118">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.ServiceBus.Models.OperationAttributes, Microsoft.Azure.Commands.ServiceBus, Version=0.4.2.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="272fd-119">출력</span><span class="sxs-lookup"><span data-stu-id="272fd-119">OUTPUTS</span></span>

### <span data-ttu-id="272fd-120">System.webserver. List ' 1 [ServiceBus. e n t].</span><span class="sxs-lookup"><span data-stu-id="272fd-120">System.Collections.Generic.List\`1[Microsoft.Azure.Commands.ServiceBus.Models.OperationAttributes]</span></span>

## <span data-ttu-id="272fd-121">상속자</span><span class="sxs-lookup"><span data-stu-id="272fd-121">NOTES</span></span>

## <span data-ttu-id="272fd-122">관련 링크</span><span class="sxs-lookup"><span data-stu-id="272fd-122">RELATED LINKS</span></span>

