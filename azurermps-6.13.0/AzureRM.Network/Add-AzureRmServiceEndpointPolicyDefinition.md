---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/add-azurermserviceendpointpolicydefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Add-AzureRmServiceEndpointPolicyDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Add-AzureRmServiceEndpointPolicyDefinition.md
ms.openlocfilehash: ac58450295e0e2d988c12c308c0210b38ad71b4c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93703829"
---
# <span data-ttu-id="9e2c7-101">Add-AzureRmServiceEndpointPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="9e2c7-101">Add-AzureRmServiceEndpointPolicyDefinition</span></span>

## <span data-ttu-id="9e2c7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9e2c7-102">SYNOPSIS</span></span>
<span data-ttu-id="9e2c7-103">지정 된 정책에 서비스 끝점 정책 정의를 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="9e2c7-103">Adds a service endpoint policy definition to a specified policy.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9e2c7-104">구문과</span><span class="sxs-lookup"><span data-stu-id="9e2c7-104">SYNTAX</span></span>

```
Add-AzureRmServiceEndpointPolicyDefinition -Name <String> -ServiceEndpointPolicy <PSServiceEndpointPolicy>
 [-Description <String>] [-ServiceResource <System.Collections.Generic.List`1[System.String]>]
 [-Service <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9e2c7-105">설명은</span><span class="sxs-lookup"><span data-stu-id="9e2c7-105">DESCRIPTION</span></span>
<span data-ttu-id="9e2c7-106">**Add-AzureRmServiceEndpointPolicyDefinition** cmdlet은 서비스 끝점 정책 정의를 정책에 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="9e2c7-106">The **Add-AzureRmServiceEndpointPolicyDefinition** cmdlet add a service endpoint policy definition to the policy.</span></span>

## <span data-ttu-id="9e2c7-107">예제의</span><span class="sxs-lookup"><span data-stu-id="9e2c7-107">EXAMPLES</span></span>

### <span data-ttu-id="9e2c7-108">예제 1: 서비스 끝점 정책에서 서비스 끝점 정책 정의 업데이트</span><span class="sxs-lookup"><span data-stu-id="9e2c7-108">Example 1: Updates a service endpoint policy definition in a service endpoint policy</span></span>
```
$policydef= New-AzureRmServiceEndpointPolicyDefinition -Name "ServiceEndpointPolicyDefinition1" -ResourceGroupName "ResourceGroup01" -Service "Microsoft.Storage" -ServiceResources "subscriptions/sub1" -Description "New Definition"
```

<span data-ttu-id="9e2c7-109">이 명령은 이름 ServiceEndpointPolicyDefinition1, 서비스 Microsoft 저장소, 서비스 리소스 구독/e 3 및 설명 "새 정의"를 업데이트 하 여 ResourceGroup01 이라는 리소스 그룹에 속하고이를 $policydef 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="9e2c7-109">This command updated the service endpoint policy definition with name ServiceEndpointPolicyDefinition1,  service Microsoft.Storage, service resources subscriptions/sub1 and description "New Definition" that belongs to the resource group named ResourceGroup01 and stores it in the $policydef variable.</span></span>

## <span data-ttu-id="9e2c7-110">변수</span><span class="sxs-lookup"><span data-stu-id="9e2c7-110">PARAMETERS</span></span>

### <span data-ttu-id="9e2c7-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9e2c7-111">-DefaultProfile</span></span>
<span data-ttu-id="9e2c7-112">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="9e2c7-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9e2c7-113">-설명</span><span class="sxs-lookup"><span data-stu-id="9e2c7-113">-Description</span></span>
<span data-ttu-id="9e2c7-114">정의에 대 한 설명입니다.</span><span class="sxs-lookup"><span data-stu-id="9e2c7-114">The description of the definition</span></span>

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

### <span data-ttu-id="9e2c7-115">-이름</span><span class="sxs-lookup"><span data-stu-id="9e2c7-115">-Name</span></span>
<span data-ttu-id="9e2c7-116">서비스 끝점 정책 정의의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="9e2c7-116">The name of the service endpoint policy definition</span></span>

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

### <span data-ttu-id="9e2c7-117">-서비스</span><span class="sxs-lookup"><span data-stu-id="9e2c7-117">-Service</span></span>
<span data-ttu-id="9e2c7-118">서비스 이름</span><span class="sxs-lookup"><span data-stu-id="9e2c7-118">Name of the service</span></span>

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

### <span data-ttu-id="9e2c7-119">-ServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="9e2c7-119">-ServiceEndpointPolicy</span></span>
<span data-ttu-id="9e2c7-120">ServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="9e2c7-120">The ServiceEndpointPolicy</span></span>

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

### <span data-ttu-id="9e2c7-121">-ServiceResource</span><span class="sxs-lookup"><span data-stu-id="9e2c7-121">-ServiceResource</span></span>
<span data-ttu-id="9e2c7-122">서비스 리소스 목록</span><span class="sxs-lookup"><span data-stu-id="9e2c7-122">List of service resources</span></span>

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

### <span data-ttu-id="9e2c7-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9e2c7-123">CommonParameters</span></span>
<span data-ttu-id="9e2c7-124">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="9e2c7-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="9e2c7-125">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9e2c7-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9e2c7-126">입력</span><span class="sxs-lookup"><span data-stu-id="9e2c7-126">INPUTS</span></span>

### <span data-ttu-id="9e2c7-127">Microsoft. 네트워크. PSServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="9e2c7-127">Microsoft.Azure.Commands.Network.Models.PSServiceEndpointPolicy</span></span>


## <span data-ttu-id="9e2c7-128">출력</span><span class="sxs-lookup"><span data-stu-id="9e2c7-128">OUTPUTS</span></span>

### <span data-ttu-id="9e2c7-129">Microsoft. 네트워크. PSServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="9e2c7-129">Microsoft.Azure.Commands.Network.Models.PSServiceEndpointPolicy</span></span>


## <span data-ttu-id="9e2c7-130">상속자</span><span class="sxs-lookup"><span data-stu-id="9e2c7-130">NOTES</span></span>

## <span data-ttu-id="9e2c7-131">관련 링크</span><span class="sxs-lookup"><span data-stu-id="9e2c7-131">RELATED LINKS</span></span>
