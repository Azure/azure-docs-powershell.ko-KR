---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/approve-azprivateendpointconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Approve-AzPrivateEndpointConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Approve-AzPrivateEndpointConnection.md
ms.openlocfilehash: 8fe3058b122c88448403293ad4f109aa5d62b23f
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94042519"
---
# <span data-ttu-id="b04a2-101">Approve-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="b04a2-101">Approve-AzPrivateEndpointConnection</span></span>

## <span data-ttu-id="b04a2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b04a2-102">SYNOPSIS</span></span>
<span data-ttu-id="b04a2-103">개인 끝점 연결을 승인 합니다.</span><span class="sxs-lookup"><span data-stu-id="b04a2-103">Approves a private endpoint connection.</span></span>

## <span data-ttu-id="b04a2-104">구문과</span><span class="sxs-lookup"><span data-stu-id="b04a2-104">SYNTAX</span></span>

### <span data-ttu-id="b04a2-105">ByResourceId (기본값)</span><span class="sxs-lookup"><span data-stu-id="b04a2-105">ByResourceId (Default)</span></span>
```
Approve-AzPrivateEndpointConnection -ResourceId <String> [-Description <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b04a2-106">ByResource</span><span class="sxs-lookup"><span data-stu-id="b04a2-106">ByResource</span></span>
```
Approve-AzPrivateEndpointConnection -Name <String> -ServiceName <String> -ResourceGroupName <String>
 [-PrivateLinkResourceType <string>][-Description <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b04a2-107">설명은</span><span class="sxs-lookup"><span data-stu-id="b04a2-107">DESCRIPTION</span></span>
<span data-ttu-id="b04a2-108">**승인-AzPrivateEndpointConnection** cmdlet은 개인 끝점 연결을 승인 합니다.</span><span class="sxs-lookup"><span data-stu-id="b04a2-108">The **Approve-AzPrivateEndpointConnection** cmdlet approves a private endpoint connection.</span></span>

## <span data-ttu-id="b04a2-109">예제의</span><span class="sxs-lookup"><span data-stu-id="b04a2-109">EXAMPLES</span></span>

### <span data-ttu-id="b04a2-110">예제 1</span><span class="sxs-lookup"><span data-stu-id="b04a2-110">Example 1</span></span>
```
Approve-AzPrivateEndpointConnection -Name TestPrivateEndpointConnection -ResourceGroupName TestResourceGroup -ServiceName TestPrivateLinkService
```

<span data-ttu-id="b04a2-111">이 예제에서는 개인 끝점 연결을 승인 합니다.</span><span class="sxs-lookup"><span data-stu-id="b04a2-111">This example approves a private endpoint connection.</span></span>

## <span data-ttu-id="b04a2-112">변수</span><span class="sxs-lookup"><span data-stu-id="b04a2-112">PARAMETERS</span></span>

### <span data-ttu-id="b04a2-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b04a2-113">-DefaultProfile</span></span>
<span data-ttu-id="b04a2-114">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="b04a2-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b04a2-115">-설명</span><span class="sxs-lookup"><span data-stu-id="b04a2-115">-Description</span></span>
<span data-ttu-id="b04a2-116">작업의 이유입니다.</span><span class="sxs-lookup"><span data-stu-id="b04a2-116">The reason of action.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b04a2-117">-이름</span><span class="sxs-lookup"><span data-stu-id="b04a2-117">-Name</span></span>
<span data-ttu-id="b04a2-118">자원 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="b04a2-118">The resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResource
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b04a2-119">-PrivateLinkResourceType</span><span class="sxs-lookup"><span data-stu-id="b04a2-119">-PrivateLinkResourceType</span></span>
<span data-ttu-id="b04a2-120">개인 링크 리소스 종류입니다.</span><span class="sxs-lookup"><span data-stu-id="b04a2-120">The private link resource type.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResource
Aliases:

Required: False
Position: Named
Default value: 'Microsoft.Network/privateLinkServices'
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b04a2-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b04a2-121">-ResourceGroupName</span></span>
<span data-ttu-id="b04a2-122">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="b04a2-122">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b04a2-123">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="b04a2-123">-ResourceId</span></span>
<span data-ttu-id="b04a2-124">개인 끝점 연결의 Azure resource manager id입니다.</span><span class="sxs-lookup"><span data-stu-id="b04a2-124">The Azure resource manager id of the private endpoint connection.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b04a2-125">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="b04a2-125">-ServiceName</span></span>
<span data-ttu-id="b04a2-126">개인 링크 서비스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="b04a2-126">The private link service name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```


### <span data-ttu-id="b04a2-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b04a2-127">CommonParameters</span></span>
<span data-ttu-id="b04a2-128">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="b04a2-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b04a2-129">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="b04a2-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b04a2-130">입력</span><span class="sxs-lookup"><span data-stu-id="b04a2-130">INPUTS</span></span>

### <span data-ttu-id="b04a2-131">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="b04a2-131">System.String</span></span>

## <span data-ttu-id="b04a2-132">출력</span><span class="sxs-lookup"><span data-stu-id="b04a2-132">OUTPUTS</span></span>

### <span data-ttu-id="b04a2-133">PSPrivateLinkService에 대 한.</span><span class="sxs-lookup"><span data-stu-id="b04a2-133">Microsoft.Azure.Commands.Network.Models.PSPrivateLinkService</span></span>

## <span data-ttu-id="b04a2-134">상속자</span><span class="sxs-lookup"><span data-stu-id="b04a2-134">NOTES</span></span>

## <span data-ttu-id="b04a2-135">관련 링크</span><span class="sxs-lookup"><span data-stu-id="b04a2-135">RELATED LINKS</span></span>

[<span data-ttu-id="b04a2-136">Deny-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="b04a2-136">Deny-AzPrivateEndpointConnection</span></span>](./Deny-AzPrivateEndpointConnection.md)

[<span data-ttu-id="b04a2-137">Get-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="b04a2-137">Get-AzPrivateEndpointConnection</span></span>](./Get-AzPrivateEndpointConnection.md)

[<span data-ttu-id="b04a2-138">제거-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="b04a2-138">Remove-AzPrivateEndpointConnection</span></span>](./Remove-AzPrivateEndpointConnection.md)

[<span data-ttu-id="b04a2-139">Set-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="b04a2-139">Set-AzPrivateEndpointConnection</span></span>](./Set-AzPrivateEndpointConnection.md)