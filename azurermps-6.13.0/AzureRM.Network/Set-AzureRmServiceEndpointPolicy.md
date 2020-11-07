---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/set-azurermserviceendpointpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmServiceEndpointPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmServiceEndpointPolicy.md
ms.openlocfilehash: ecd5a8eafc70a88b4ebda17a83f2b40139f5463f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93702915"
---
# <span data-ttu-id="19205-101">Set-AzureRmServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="19205-101">Set-AzureRmServiceEndpointPolicy</span></span>

## <span data-ttu-id="19205-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="19205-102">SYNOPSIS</span></span>
<span data-ttu-id="19205-103">{{Synopsis 채우기}}</span><span class="sxs-lookup"><span data-stu-id="19205-103">{{Fill in the Synopsis}}</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="19205-104">구문과</span><span class="sxs-lookup"><span data-stu-id="19205-104">SYNTAX</span></span>

```
Set-AzureRmServiceEndpointPolicy -ServiceEndpointPolicy <PSServiceEndpointPolicy>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="19205-105">설명은</span><span class="sxs-lookup"><span data-stu-id="19205-105">DESCRIPTION</span></span>
<span data-ttu-id="19205-106">**AzureRmServiceEndpointPolicy** cmdlet은 서비스 끝점 정책을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="19205-106">The **Set-AzureRmServiceEndpointPolicy** cmdlet create a service endpoint policy.</span></span>

## <span data-ttu-id="19205-107">예제의</span><span class="sxs-lookup"><span data-stu-id="19205-107">EXAMPLES</span></span>

### <span data-ttu-id="19205-108">예제 1: 서비스 끝점 정책 설정</span><span class="sxs-lookup"><span data-stu-id="19205-108">Example 1: Sets a service endpoint policy</span></span>
```
$serviceEndpointPolicy = Set-AzureRmServiceEndpointPolicy -Name "Policy1" -ServiceEndpointPolicy $serviceEndpointPolicy -ResourceGroup "resourcegroup1"
```

<span data-ttu-id="19205-109">이 명령은 Policy1 "resourcegroup1"에 속하는 개체 $serviceEndpointPolicy 정의 된 서비스 끝점 정책을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="19205-109">This command updates a service endpoint policy named Policy1 defined by the object $serviceEndpointPolicy belong to the resourcegroup "resourcegroup1".</span></span>

## <span data-ttu-id="19205-110">변수</span><span class="sxs-lookup"><span data-stu-id="19205-110">PARAMETERS</span></span>

### <span data-ttu-id="19205-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="19205-111">-DefaultProfile</span></span>
<span data-ttu-id="19205-112">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="19205-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="19205-113">-ServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="19205-113">-ServiceEndpointPolicy</span></span>
<span data-ttu-id="19205-114">ServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="19205-114">The ServiceEndpointPolicy</span></span>

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

### <span data-ttu-id="19205-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="19205-115">CommonParameters</span></span>
<span data-ttu-id="19205-116">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="19205-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="19205-117">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="19205-117">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="19205-118">입력</span><span class="sxs-lookup"><span data-stu-id="19205-118">INPUTS</span></span>

### <span data-ttu-id="19205-119">Microsoft. 네트워크. PSServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="19205-119">Microsoft.Azure.Commands.Network.Models.PSServiceEndpointPolicy</span></span>


## <span data-ttu-id="19205-120">출력</span><span class="sxs-lookup"><span data-stu-id="19205-120">OUTPUTS</span></span>

### <span data-ttu-id="19205-121">Microsoft. 네트워크. PSServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="19205-121">Microsoft.Azure.Commands.Network.Models.PSServiceEndpointPolicy</span></span>


## <span data-ttu-id="19205-122">상속자</span><span class="sxs-lookup"><span data-stu-id="19205-122">NOTES</span></span>

## <span data-ttu-id="19205-123">관련 링크</span><span class="sxs-lookup"><span data-stu-id="19205-123">RELATED LINKS</span></span>
