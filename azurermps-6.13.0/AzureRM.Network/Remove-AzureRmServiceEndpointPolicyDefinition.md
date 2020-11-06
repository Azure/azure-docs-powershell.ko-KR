---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/remove-azurermserviceendpointpolicydefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmServiceEndpointPolicyDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmServiceEndpointPolicyDefinition.md
ms.openlocfilehash: 3d406bf0dffb0ee250e1494fc05727d0a4c983ab
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93535739"
---
# <span data-ttu-id="b22a9-101">Remove-AzureRmServiceEndpointPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="b22a9-101">Remove-AzureRmServiceEndpointPolicyDefinition</span></span>

## <span data-ttu-id="b22a9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b22a9-102">SYNOPSIS</span></span>
<span data-ttu-id="b22a9-103">{{Synopsis 채우기}}</span><span class="sxs-lookup"><span data-stu-id="b22a9-103">{{Fill in the Synopsis}}</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b22a9-104">구문과</span><span class="sxs-lookup"><span data-stu-id="b22a9-104">SYNTAX</span></span>

```
Remove-AzureRmServiceEndpointPolicyDefinition [-Name <String>] -ServiceEndpointPolicy <PSServiceEndpointPolicy>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b22a9-105">설명은</span><span class="sxs-lookup"><span data-stu-id="b22a9-105">DESCRIPTION</span></span>
<span data-ttu-id="b22a9-106">**AzureRmServiceEndpointPolicy** cmdlet은 서비스 끝점 정책을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="b22a9-106">The **Remove-AzureRmServiceEndpointPolicy** cmdlet removes a service endpoint policy.</span></span>

## <span data-ttu-id="b22a9-107">예제의</span><span class="sxs-lookup"><span data-stu-id="b22a9-107">EXAMPLES</span></span>

### <span data-ttu-id="b22a9-108">예제 1: 이름을 사용 하 여 서비스 끝점 정책 제거</span><span class="sxs-lookup"><span data-stu-id="b22a9-108">Example 1: Removes a service endpoint policy using name</span></span>
```
Remove-AzureRmServiceEndpointPolicyDefinition -Name "PolicyDef1"
```

<span data-ttu-id="b22a9-109">이 명령은 이름이 PolicyDef1 인 서비스 끝점 정책을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="b22a9-109">This command removes a service endpoint policy with name PolicyDef1</span></span>

## <span data-ttu-id="b22a9-110">변수</span><span class="sxs-lookup"><span data-stu-id="b22a9-110">PARAMETERS</span></span>

### <span data-ttu-id="b22a9-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b22a9-111">-DefaultProfile</span></span>
<span data-ttu-id="b22a9-112">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="b22a9-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b22a9-113">-이름</span><span class="sxs-lookup"><span data-stu-id="b22a9-113">-Name</span></span>
<span data-ttu-id="b22a9-114">서비스 끝점 정의의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="b22a9-114">The name of the service endpoint definition</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b22a9-115">-ServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="b22a9-115">-ServiceEndpointPolicy</span></span>
<span data-ttu-id="b22a9-116">ServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="b22a9-116">The ServiceEndpointPolicy</span></span>

```yaml
Type: PSServiceEndpointPolicy
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b22a9-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b22a9-117">CommonParameters</span></span>
<span data-ttu-id="b22a9-118">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="b22a9-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="b22a9-119">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b22a9-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b22a9-120">입력</span><span class="sxs-lookup"><span data-stu-id="b22a9-120">INPUTS</span></span>

### <span data-ttu-id="b22a9-121">Microsoft. 네트워크. PSServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="b22a9-121">Microsoft.Azure.Commands.Network.Models.PSServiceEndpointPolicy</span></span>


## <span data-ttu-id="b22a9-122">출력</span><span class="sxs-lookup"><span data-stu-id="b22a9-122">OUTPUTS</span></span>

### <span data-ttu-id="b22a9-123">Microsoft. 네트워크. PSServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="b22a9-123">Microsoft.Azure.Commands.Network.Models.PSServiceEndpointPolicy</span></span>


## <span data-ttu-id="b22a9-124">상속자</span><span class="sxs-lookup"><span data-stu-id="b22a9-124">NOTES</span></span>

## <span data-ttu-id="b22a9-125">관련 링크</span><span class="sxs-lookup"><span data-stu-id="b22a9-125">RELATED LINKS</span></span>
