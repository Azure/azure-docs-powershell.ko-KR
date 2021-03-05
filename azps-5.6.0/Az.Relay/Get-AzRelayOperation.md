---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Relay.dll-Help.xml
Module Name: Az.Relay
online version: https://docs.microsoft.com/powershell/module/az.relay/get-azrelayoperation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Relay/Relay/help/Get-AzRelayOperation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Relay/Relay/help/Get-AzRelayOperation.md
ms.openlocfilehash: 72f9e3290af5aad665213c1ffdebf5f3b2edcf92
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "102000603"
---
# <span data-ttu-id="95e15-101">Get-AzRelayOperation</span><span class="sxs-lookup"><span data-stu-id="95e15-101">Get-AzRelayOperation</span></span>

## <span data-ttu-id="95e15-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="95e15-102">SYNOPSIS</span></span>
<span data-ttu-id="95e15-103">지원되는 릴레이 작업 나열</span><span class="sxs-lookup"><span data-stu-id="95e15-103">List supported Relay Operations</span></span>

## <span data-ttu-id="95e15-104">구문</span><span class="sxs-lookup"><span data-stu-id="95e15-104">SYNTAX</span></span>

```
Get-AzRelayOperation [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="95e15-105">설명</span><span class="sxs-lookup"><span data-stu-id="95e15-105">DESCRIPTION</span></span>
<span data-ttu-id="95e15-106">**Get-AzRelayOperation** cmdlet에는 지원되는 릴레이 작업이 나열됩니다.</span><span class="sxs-lookup"><span data-stu-id="95e15-106">The **Get-AzRelayOperation** cmdlet Lists the Relay supported Operations.</span></span>

## <span data-ttu-id="95e15-107">예제</span><span class="sxs-lookup"><span data-stu-id="95e15-107">EXAMPLES</span></span>

### <span data-ttu-id="95e15-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="95e15-108">Example 1</span></span>
```
PS C:\> Get-AzRelayOperation

Name                                                                            Display
----                                                                            -------
Microsoft.Relay/checkNamespaceAvailability/action                               Microsoft.Azure.Commands.Relay.Models.OperationDisplayAttributes
Microsoft.Relay/register/action                                                 Microsoft.Azure.Commands.Relay.Models.OperationDisplayAttributes
Microsoft.Relay/namespaces/write                                                Microsoft.Azure.Commands.Relay.Models.OperationDisplayAttributes
Microsoft.Relay/namespaces/read                                                 Microsoft.Azure.Commands.Relay.Models.OperationDisplayAttributes
Microsoft.Relay/namespaces/Delete                                               Microsoft.Azure.Commands.Relay.Models.OperationDisplayAttributes
Microsoft.Relay/namespaces/authorizationRules/write                             Microsoft.Azure.Commands.Relay.Models.OperationDisplayAttributes
Microsoft.Relay/namespaces/authorizationRules/delete                            Microsoft.Azure.Commands.Relay.Models.OperationDisplayAttributes
Microsoft.Relay/namespaces/authorizationRules/listkeys/action                   Microsoft.Azure.Commands.Relay.Models.OperationDisplayAttributes
Microsoft.Relay/namespaces/HybridConnections/write                              Microsoft.Azure.Commands.Relay.Models.OperationDisplayAttributes
Microsoft.Relay/namespaces/HybridConnections/read                               Microsoft.Azure.Commands.Relay.Models.OperationDisplayAttributes
Microsoft.Relay/namespaces/HybridConnections/Delete                             Microsoft.Azure.Commands.Relay.Models.OperationDisplayAttributes
Microsoft.Relay/namespaces/HybridConnections/authorizationRules/write           Microsoft.Azure.Commands.Relay.Models.OperationDisplayAttributes
Microsoft.Relay/namespaces/HybridConnections/authorizationRules/delete          Microsoft.Azure.Commands.Relay.Models.OperationDisplayAttributes
Microsoft.Relay/namespaces/HybridConnections/authorizationRules/listkeys/action Microsoft.Azure.Commands.Relay.Models.OperationDisplayAttributes
Microsoft.Relay/namespaces/WcfRelays/write                                      Microsoft.Azure.Commands.Relay.Models.OperationDisplayAttributes
Microsoft.Relay/namespaces/WcfRelays/read                                       Microsoft.Azure.Commands.Relay.Models.OperationDisplayAttributes
Microsoft.Relay/namespaces/WcfRelays/Delete                                     Microsoft.Azure.Commands.Relay.Models.OperationDisplayAttributes
Microsoft.Relay/namespaces/WcfRelays/authorizationRules/write                   Microsoft.Azure.Commands.Relay.Models.OperationDisplayAttributes
Microsoft.Relay/namespaces/WcfRelays/authorizationRules/delete                  Microsoft.Azure.Commands.Relay.Models.OperationDisplayAttributes
Microsoft.Relay/namespaces/WcfRelays/authorizationRules/listkeys/action         Microsoft.Azure.Commands.Relay.Models.OperationDisplayAttributes
```

<span data-ttu-id="95e15-109">지원되는 릴레이 작업 나열</span><span class="sxs-lookup"><span data-stu-id="95e15-109">Lists Relay supported operations</span></span>

## <span data-ttu-id="95e15-110">매개 변수</span><span class="sxs-lookup"><span data-stu-id="95e15-110">PARAMETERS</span></span>

### <span data-ttu-id="95e15-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="95e15-111">-DefaultProfile</span></span>
<span data-ttu-id="95e15-112">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="95e15-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="95e15-113">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="95e15-113">CommonParameters</span></span>
<span data-ttu-id="95e15-114">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="95e15-114">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="95e15-115">자세한 내용은 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="95e15-115">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="95e15-116">입력</span><span class="sxs-lookup"><span data-stu-id="95e15-116">INPUTS</span></span>

### <span data-ttu-id="95e15-117">없음</span><span class="sxs-lookup"><span data-stu-id="95e15-117">None</span></span>

## <span data-ttu-id="95e15-118">출력</span><span class="sxs-lookup"><span data-stu-id="95e15-118">OUTPUTS</span></span>

### <span data-ttu-id="95e15-119">Microsoft.Azure.Commands.Relay.Models.PSOperationAttributes</span><span class="sxs-lookup"><span data-stu-id="95e15-119">Microsoft.Azure.Commands.Relay.Models.PSOperationAttributes</span></span>

## <span data-ttu-id="95e15-120">참고 사항</span><span class="sxs-lookup"><span data-stu-id="95e15-120">NOTES</span></span>

## <span data-ttu-id="95e15-121">관련 링크</span><span class="sxs-lookup"><span data-stu-id="95e15-121">RELATED LINKS</span></span>
