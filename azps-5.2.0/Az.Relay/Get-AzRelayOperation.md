---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Relay.dll-Help.xml
Module Name: Az.Relay
online version: https://docs.microsoft.com/en-us/powershell/module/az.relay/get-azrelayoperation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Relay/Relay/help/Get-AzRelayOperation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Relay/Relay/help/Get-AzRelayOperation.md
ms.openlocfilehash: 21bf1e235d9e6b2f6bb4d2017b69f607e559e46b
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98335865"
---
# <span data-ttu-id="c01eb-101">Get-AzRelayOperation</span><span class="sxs-lookup"><span data-stu-id="c01eb-101">Get-AzRelayOperation</span></span>

## <span data-ttu-id="c01eb-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c01eb-102">SYNOPSIS</span></span>
<span data-ttu-id="c01eb-103">지원되는 릴레이 작업 나열</span><span class="sxs-lookup"><span data-stu-id="c01eb-103">List supported Relay Operations</span></span>

## <span data-ttu-id="c01eb-104">구문</span><span class="sxs-lookup"><span data-stu-id="c01eb-104">SYNTAX</span></span>

```
Get-AzRelayOperation [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c01eb-105">설명</span><span class="sxs-lookup"><span data-stu-id="c01eb-105">DESCRIPTION</span></span>
<span data-ttu-id="c01eb-106">**Get-AzRelayOperation** cmdlet은 릴레이 지원 작업을 나열합니다.</span><span class="sxs-lookup"><span data-stu-id="c01eb-106">The **Get-AzRelayOperation** cmdlet Lists the Relay supported Operations.</span></span>

## <span data-ttu-id="c01eb-107">예제</span><span class="sxs-lookup"><span data-stu-id="c01eb-107">EXAMPLES</span></span>

### <span data-ttu-id="c01eb-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="c01eb-108">Example 1</span></span>
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

<span data-ttu-id="c01eb-109">릴레이 지원 작업 나열</span><span class="sxs-lookup"><span data-stu-id="c01eb-109">Lists Relay supported operations</span></span>

## <span data-ttu-id="c01eb-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c01eb-110">PARAMETERS</span></span>

### <span data-ttu-id="c01eb-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c01eb-111">-DefaultProfile</span></span>
<span data-ttu-id="c01eb-112">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="c01eb-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c01eb-113">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c01eb-113">CommonParameters</span></span>
<span data-ttu-id="c01eb-114">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="c01eb-114">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c01eb-115">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="c01eb-115">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c01eb-116">입력</span><span class="sxs-lookup"><span data-stu-id="c01eb-116">INPUTS</span></span>

### <span data-ttu-id="c01eb-117">없음</span><span class="sxs-lookup"><span data-stu-id="c01eb-117">None</span></span>

## <span data-ttu-id="c01eb-118">출력</span><span class="sxs-lookup"><span data-stu-id="c01eb-118">OUTPUTS</span></span>

### <span data-ttu-id="c01eb-119">Microsoft.Azure.Commands.Relay.Models.PSOperationAttributes</span><span class="sxs-lookup"><span data-stu-id="c01eb-119">Microsoft.Azure.Commands.Relay.Models.PSOperationAttributes</span></span>

## <span data-ttu-id="c01eb-120">참고 사항</span><span class="sxs-lookup"><span data-stu-id="c01eb-120">NOTES</span></span>

## <span data-ttu-id="c01eb-121">관련 링크</span><span class="sxs-lookup"><span data-stu-id="c01eb-121">RELATED LINKS</span></span>
