---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/set-azurermserviceendpointpolicydefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmServiceEndpointPolicyDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmServiceEndpointPolicyDefinition.md
ms.openlocfilehash: 1348eff2e4a2ac755ac0f425ddb29816438199b7
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93702914"
---
# <span data-ttu-id="089d3-101">Set-AzureRmServiceEndpointPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="089d3-101">Set-AzureRmServiceEndpointPolicyDefinition</span></span>

## <span data-ttu-id="089d3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="089d3-102">SYNOPSIS</span></span>
<span data-ttu-id="089d3-103">{{Synopsis 채우기}}</span><span class="sxs-lookup"><span data-stu-id="089d3-103">{{Fill in the Synopsis}}</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="089d3-104">구문과</span><span class="sxs-lookup"><span data-stu-id="089d3-104">SYNTAX</span></span>

```
Set-AzureRmServiceEndpointPolicyDefinition -Name <String> -ServiceEndpointPolicy <PSServiceEndpointPolicy>
 [-Description <String>] [-ServiceResource <System.Collections.Generic.List`1[System.String]>]
 [-Service <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="089d3-105">설명은</span><span class="sxs-lookup"><span data-stu-id="089d3-105">DESCRIPTION</span></span>
<span data-ttu-id="089d3-106">**AzureRmServiceEndpointPolicyDefinition** cmdlet은 서비스 끝점 정책 정의를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="089d3-106">The **Set-AzureRmServiceEndpointPolicyDefinition** cmdlet create a service endpoint policy definition.</span></span>

## <span data-ttu-id="089d3-107">예제의</span><span class="sxs-lookup"><span data-stu-id="089d3-107">EXAMPLES</span></span>

### <span data-ttu-id="089d3-108">예제 1: 서비스 끝점 정책에서 서비스 끝점 정책 정의 업데이트</span><span class="sxs-lookup"><span data-stu-id="089d3-108">Example 1: Updates a service endpoint policy definition in a service endpoint policy</span></span>
```
$serviceEndpointPolicy = Set-AzureRmServiceEndpointPolicyDefinition -Name "Policydef1" -ServiceEndpointPolicy $serviceEndpointPolicy
```

<span data-ttu-id="089d3-109">이 명령은 $ServiceEndpointPolicy 개체에 정의 된 서비스 끝점 정책의 Policydef1 이라는 서비스 끝점 정책 정의를 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="089d3-109">This command updates a service endpoint policy definition named Policydef1 in the service endpoint policy defined by the object $ServiceEndpointPolicy.</span></span>

## <span data-ttu-id="089d3-110">변수</span><span class="sxs-lookup"><span data-stu-id="089d3-110">PARAMETERS</span></span>

### <span data-ttu-id="089d3-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="089d3-111">-DefaultProfile</span></span>
<span data-ttu-id="089d3-112">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="089d3-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="089d3-113">-설명</span><span class="sxs-lookup"><span data-stu-id="089d3-113">-Description</span></span>
<span data-ttu-id="089d3-114">정의에 대 한 설명입니다.</span><span class="sxs-lookup"><span data-stu-id="089d3-114">The description of the definition</span></span>

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

### <span data-ttu-id="089d3-115">-이름</span><span class="sxs-lookup"><span data-stu-id="089d3-115">-Name</span></span>
<span data-ttu-id="089d3-116">규칙의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="089d3-116">The name of the rule</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="089d3-117">-서비스</span><span class="sxs-lookup"><span data-stu-id="089d3-117">-Service</span></span>
<span data-ttu-id="089d3-118">서비스 이름</span><span class="sxs-lookup"><span data-stu-id="089d3-118">Name of the service</span></span>

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

### <span data-ttu-id="089d3-119">-ServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="089d3-119">-ServiceEndpointPolicy</span></span>
<span data-ttu-id="089d3-120">NetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="089d3-120">The NetworkSecurityGroup</span></span>

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

### <span data-ttu-id="089d3-121">-ServiceResource</span><span class="sxs-lookup"><span data-stu-id="089d3-121">-ServiceResource</span></span>
<span data-ttu-id="089d3-122">서비스 리소스 목록</span><span class="sxs-lookup"><span data-stu-id="089d3-122">List of service resources</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="089d3-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="089d3-123">CommonParameters</span></span>
<span data-ttu-id="089d3-124">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="089d3-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="089d3-125">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="089d3-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="089d3-126">입력</span><span class="sxs-lookup"><span data-stu-id="089d3-126">INPUTS</span></span>

### <span data-ttu-id="089d3-127">Microsoft. 네트워크. PSServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="089d3-127">Microsoft.Azure.Commands.Network.Models.PSServiceEndpointPolicy</span></span>


## <span data-ttu-id="089d3-128">출력</span><span class="sxs-lookup"><span data-stu-id="089d3-128">OUTPUTS</span></span>

### <span data-ttu-id="089d3-129">Microsoft. 네트워크. PSServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="089d3-129">Microsoft.Azure.Commands.Network.Models.PSServiceEndpointPolicy</span></span>


## <span data-ttu-id="089d3-130">상속자</span><span class="sxs-lookup"><span data-stu-id="089d3-130">NOTES</span></span>

## <span data-ttu-id="089d3-131">관련 링크</span><span class="sxs-lookup"><span data-stu-id="089d3-131">RELATED LINKS</span></span>
