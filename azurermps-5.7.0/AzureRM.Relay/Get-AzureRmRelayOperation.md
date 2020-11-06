---
external help file: Microsoft.Azure.Commands.Relay.dll-Help.xml
Module Name: AzureRM
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.relay/get-azurermrelayoperation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Relay/Commands.Relay/help/Get-AzureRmRelayOperation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Relay/Commands.Relay/help/Get-AzureRmRelayOperation.md
ms.openlocfilehash: 2ec1fc27912fce9c218793d711a989d1dac285df
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93534735"
---
# <span data-ttu-id="b78d3-101">Get-AzureRmRelayOperation</span><span class="sxs-lookup"><span data-stu-id="b78d3-101">Get-AzureRmRelayOperation</span></span>

## <span data-ttu-id="b78d3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b78d3-102">SYNOPSIS</span></span>
<span data-ttu-id="b78d3-103">지원 되는 릴레이 작업 나열</span><span class="sxs-lookup"><span data-stu-id="b78d3-103">List supported Relay Operations</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b78d3-104">구문과</span><span class="sxs-lookup"><span data-stu-id="b78d3-104">SYNTAX</span></span>

```
Get-AzureRmRelayOperation [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b78d3-105">설명은</span><span class="sxs-lookup"><span data-stu-id="b78d3-105">DESCRIPTION</span></span>
<span data-ttu-id="b78d3-106">**AzureRmRelayOperation** Cmdlet은 릴레이 지원 작업을 나열 합니다.</span><span class="sxs-lookup"><span data-stu-id="b78d3-106">The **Get-AzureRmRelayOperation** cmdlet Lists the Relay supported Operations.</span></span>

## <span data-ttu-id="b78d3-107">예제의</span><span class="sxs-lookup"><span data-stu-id="b78d3-107">EXAMPLES</span></span>

### <span data-ttu-id="b78d3-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="b78d3-108">Example 1</span></span>
```
PS C:\> Get-AzureRmRelayOperation
```

<span data-ttu-id="b78d3-109">릴레이가 지원 되는 작업 나열</span><span class="sxs-lookup"><span data-stu-id="b78d3-109">Lists Relay supported operations</span></span>

## <span data-ttu-id="b78d3-110">변수</span><span class="sxs-lookup"><span data-stu-id="b78d3-110">PARAMETERS</span></span>

### <span data-ttu-id="b78d3-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b78d3-111">-DefaultProfile</span></span>
<span data-ttu-id="b78d3-112">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="b78d3-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b78d3-113">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b78d3-113">CommonParameters</span></span>
<span data-ttu-id="b78d3-114">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="b78d3-114">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b78d3-115">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b78d3-115">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b78d3-116">입력</span><span class="sxs-lookup"><span data-stu-id="b78d3-116">INPUTS</span></span>

### <span data-ttu-id="b78d3-117">않아야</span><span class="sxs-lookup"><span data-stu-id="b78d3-117">None</span></span>

## <span data-ttu-id="b78d3-118">출력</span><span class="sxs-lookup"><span data-stu-id="b78d3-118">OUTPUTS</span></span>

### <span data-ttu-id="b78d3-119">System.webserver. List ' 1 [[Microsoft Azure. e. 모델]. 0.1.0.0, Version =, Culture = 중립, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="b78d3-119">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.Relay.Models.OperationAttributes, Microsoft.Azure.Commands.Relay, Version=0.1.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>
<span data-ttu-id="b78d3-120">이름 표시</span><span class="sxs-lookup"><span data-stu-id="b78d3-120">Name                                                                            Display</span></span>
----                                                                            -------
<span data-ttu-id="b78d3-121">Microsoft.Relay/checkNamespaceAvailability/action Microsoft.Azure.Commands.Relay.Models.OperationDisplayAttributes Microsoft.Relay/register/action Microsoft.Azure.Commands.Relay.Models.OperationDisplayAttributes Microsoft.Relay/namespaces/write Microsoft.Azure.Commands.Relay.Models.OperationDisplayAttributes Microsoft.Relay/namespaces/read Microsoft.Azure.Commands.Relay.Models.OperationDisplayAttributes Microsoft.Relay/namespaces/Delete Microsoft.Azure.Commands.Relay.Models.OperationDisplayAttributes Microsoft.Relay/namespaces/authorizationRules/write Microsoft.Azure.Commands.Relay.Models.OperationDisplayAttributes Microsoft.Relay/namespaces/authorizationRules/delete Microsoft.Azure.Commands.Relay.Models.OperationDisplayAttributes Microsoft.Relay/namespaces/authorizationRules/listkeys/action Microsoft.Azure.Commands.Relay.Models.OperationDisplayAttributes Microsoft.Relay/namespaces/HybridConnections/write Microsoft.Azure.Commands.Relay.Models.OperationDisplayAttributes Microsoft.Relay/namespaces/HybridConnections/read Microsoft.Azure.Commands.Relay.Models.OperationDisplayAttributes Microsoft.Relay/namespaces/HybridConnections/Delete Microsoft.Azure.Commands.Relay.Models.OperationDisplayAttributes Microsoft.Relay/namespaces/HybridConnections/authorizationRules/write Microsoft.Azure.Commands.Relay.Models.OperationDisplayAttributes Microsoft.Relay/namespaces/HybridConnections/authorizationRules/delete Microsoft.Azure.Commands.Relay.Models.OperationDisplayAttributes Microsoft.Relay/namespaces/HybridConnections/authorizationRules/listkeys/action Microsoft.Azure.Commands.Relay.Models.OperationDisplayAttributes Microsoft.Relay/namespaces/WcfRelays/write Microsoft.Azure.Commands.Relay.Models.OperationDisplayAttributes Microsoft.Relay/namespaces/WcfRelays/read Microsoft.Azure.Commands.Relay.Models.OperationDisplayAttributes Microsoft.Relay/namespaces/WcfRelays/Delete Microsoft.Azure.Commands.Relay.Models.OperationDisplayAttributes Microsoft.Relay/namespaces/WcfRelays/authorizationRules/write Microsoft.Azure.Commands.Relay.Models.OperationDisplayAttributes Microsoft.Relay/namespaces/WcfRelays/authorizationRules/delete Microsoft.Azure.Commands.Relay.Models.OperationDisplayAttributes Microsoft.Relay/namespaces/WcfRelays/authorizationRules/listkeys/action Microsoft.Azure.Commands.Relay.Models.OperationDisplayAttributes</span><span class="sxs-lookup"><span data-stu-id="b78d3-121">Microsoft.Relay/checkNamespaceAvailability/action                               Microsoft.Azure.Commands.Relay.Models.OperationDisplayAttributes Microsoft.Relay/register/action                                                 Microsoft.Azure.Commands.Relay.Models.OperationDisplayAttributes Microsoft.Relay/namespaces/write                                                Microsoft.Azure.Commands.Relay.Models.OperationDisplayAttributes Microsoft.Relay/namespaces/read                                                 Microsoft.Azure.Commands.Relay.Models.OperationDisplayAttributes Microsoft.Relay/namespaces/Delete                                               Microsoft.Azure.Commands.Relay.Models.OperationDisplayAttributes Microsoft.Relay/namespaces/authorizationRules/write                             Microsoft.Azure.Commands.Relay.Models.OperationDisplayAttributes Microsoft.Relay/namespaces/authorizationRules/delete                            Microsoft.Azure.Commands.Relay.Models.OperationDisplayAttributes Microsoft.Relay/namespaces/authorizationRules/listkeys/action                   Microsoft.Azure.Commands.Relay.Models.OperationDisplayAttributes Microsoft.Relay/namespaces/HybridConnections/write                              Microsoft.Azure.Commands.Relay.Models.OperationDisplayAttributes Microsoft.Relay/namespaces/HybridConnections/read                               Microsoft.Azure.Commands.Relay.Models.OperationDisplayAttributes Microsoft.Relay/namespaces/HybridConnections/Delete                             Microsoft.Azure.Commands.Relay.Models.OperationDisplayAttributes Microsoft.Relay/namespaces/HybridConnections/authorizationRules/write           Microsoft.Azure.Commands.Relay.Models.OperationDisplayAttributes Microsoft.Relay/namespaces/HybridConnections/authorizationRules/delete          Microsoft.Azure.Commands.Relay.Models.OperationDisplayAttributes Microsoft.Relay/namespaces/HybridConnections/authorizationRules/listkeys/action Microsoft.Azure.Commands.Relay.Models.OperationDisplayAttributes Microsoft.Relay/namespaces/WcfRelays/write                                      Microsoft.Azure.Commands.Relay.Models.OperationDisplayAttributes Microsoft.Relay/namespaces/WcfRelays/read                                       Microsoft.Azure.Commands.Relay.Models.OperationDisplayAttributes Microsoft.Relay/namespaces/WcfRelays/Delete                                     Microsoft.Azure.Commands.Relay.Models.OperationDisplayAttributes Microsoft.Relay/namespaces/WcfRelays/authorizationRules/write                   Microsoft.Azure.Commands.Relay.Models.OperationDisplayAttributes Microsoft.Relay/namespaces/WcfRelays/authorizationRules/delete                  Microsoft.Azure.Commands.Relay.Models.OperationDisplayAttributes Microsoft.Relay/namespaces/WcfRelays/authorizationRules/listkeys/action         Microsoft.Azure.Commands.Relay.Models.OperationDisplayAttributes</span></span>

## <span data-ttu-id="b78d3-122">상속자</span><span class="sxs-lookup"><span data-stu-id="b78d3-122">NOTES</span></span>

## <span data-ttu-id="b78d3-123">관련 링크</span><span class="sxs-lookup"><span data-stu-id="b78d3-123">RELATED LINKS</span></span>

