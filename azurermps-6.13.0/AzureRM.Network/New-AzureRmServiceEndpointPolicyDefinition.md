---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermserviceendpointpolicydefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmServiceEndpointPolicyDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmServiceEndpointPolicyDefinition.md
ms.openlocfilehash: 12d809ad4c1df021891ab5acf384415d64aa08a3
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93534231"
---
# <span data-ttu-id="c9115-101">New-AzureRmServiceEndpointPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="c9115-101">New-AzureRmServiceEndpointPolicyDefinition</span></span>

## <span data-ttu-id="c9115-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c9115-102">SYNOPSIS</span></span>
<span data-ttu-id="c9115-103">{{Synopsis 채우기}}</span><span class="sxs-lookup"><span data-stu-id="c9115-103">{{Fill in the Synopsis}}</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c9115-104">구문과</span><span class="sxs-lookup"><span data-stu-id="c9115-104">SYNTAX</span></span>

```
New-AzureRmServiceEndpointPolicyDefinition -Name <String> [-Description <String>]
 [-ServiceResource <System.Collections.Generic.List`1[System.String]>] [-Service <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c9115-105">설명은</span><span class="sxs-lookup"><span data-stu-id="c9115-105">DESCRIPTION</span></span>
<span data-ttu-id="c9115-106">**새 AzureRmServiceEndpointPolicyDefinition** cmdlet은 서비스 끝점 정책 정의를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="c9115-106">The **New-AzureRmServiceEndpointPolicyDefinition** cmdlet create a service endpoint policy definition.</span></span>

## <span data-ttu-id="c9115-107">예제의</span><span class="sxs-lookup"><span data-stu-id="c9115-107">EXAMPLES</span></span>

### <span data-ttu-id="c9115-108">예제 1: 서비스 끝점 정책 만들기</span><span class="sxs-lookup"><span data-stu-id="c9115-108">Example 1: Creates a service endpoint policy</span></span>
```
$policydef= New-AzureRmServiceEndpointPolicyDefinition -Name "ServiceEndpointPolicyDefinition1" -ResourceGroupName "ResourceGroup01" -Service "Microsoft.Storage" -ServiceResources "subscriptions/sub1" -Description "New Definition"
```

<span data-ttu-id="c9115-109">이 명령은 name ServiceEndpointPolicyDefinition1, 서비스 리소스 구독/e 5 및 설명 "새 정의"가 ResourceGroup01 이라는 리소스 그룹에 속하고이를 $policydef 변수에 저장 하는 서비스 끝점 정책 정의를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="c9115-109">This command creates the service endpoint policy definition with name ServiceEndpointPolicyDefinition1,  service Microsoft.Storage, service resources subscriptions/sub1 and description "New Definition" that belongs to the resource group named ResourceGroup01 and stores it in the $policydef variable.</span></span>

## <span data-ttu-id="c9115-110">변수</span><span class="sxs-lookup"><span data-stu-id="c9115-110">PARAMETERS</span></span>

### <span data-ttu-id="c9115-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c9115-111">-DefaultProfile</span></span>
<span data-ttu-id="c9115-112">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="c9115-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c9115-113">-설명</span><span class="sxs-lookup"><span data-stu-id="c9115-113">-Description</span></span>
<span data-ttu-id="c9115-114">정의에 대 한 설명입니다.</span><span class="sxs-lookup"><span data-stu-id="c9115-114">The description of the definition</span></span>

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

### <span data-ttu-id="c9115-115">-이름</span><span class="sxs-lookup"><span data-stu-id="c9115-115">-Name</span></span>
<span data-ttu-id="c9115-116">서비스 끝점 정책의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="c9115-116">The name of the service endpoint policy</span></span>

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

### <span data-ttu-id="c9115-117">-서비스</span><span class="sxs-lookup"><span data-stu-id="c9115-117">-Service</span></span>
<span data-ttu-id="c9115-118">서비스 이름</span><span class="sxs-lookup"><span data-stu-id="c9115-118">Name of the service</span></span>

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

### <span data-ttu-id="c9115-119">-ServiceResource</span><span class="sxs-lookup"><span data-stu-id="c9115-119">-ServiceResource</span></span>
<span data-ttu-id="c9115-120">서비스 리소스 목록</span><span class="sxs-lookup"><span data-stu-id="c9115-120">List of service resources</span></span>

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

### <span data-ttu-id="c9115-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c9115-121">CommonParameters</span></span>
<span data-ttu-id="c9115-122">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="c9115-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="c9115-123">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c9115-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c9115-124">입력</span><span class="sxs-lookup"><span data-stu-id="c9115-124">INPUTS</span></span>

### <span data-ttu-id="c9115-125">않아야</span><span class="sxs-lookup"><span data-stu-id="c9115-125">None</span></span>


## <span data-ttu-id="c9115-126">출력</span><span class="sxs-lookup"><span data-stu-id="c9115-126">OUTPUTS</span></span>

### <span data-ttu-id="c9115-127">Microsoft. m a w. PSServiceEndpointPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="c9115-127">Microsoft.Azure.Commands.Network.Models.PSServiceEndpointPolicyDefinition</span></span>


## <span data-ttu-id="c9115-128">상속자</span><span class="sxs-lookup"><span data-stu-id="c9115-128">NOTES</span></span>

## <span data-ttu-id="c9115-129">관련 링크</span><span class="sxs-lookup"><span data-stu-id="c9115-129">RELATED LINKS</span></span>
