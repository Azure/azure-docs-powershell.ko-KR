---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/approve-azprivateendpointconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Approve-AzPrivateEndpointConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Approve-AzPrivateEndpointConnection.md
ms.openlocfilehash: 8fe3058b122c88448403293ad4f109aa5d62b23f
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98359591"
---
# <span data-ttu-id="d170a-101">Approve-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="d170a-101">Approve-AzPrivateEndpointConnection</span></span>

## <span data-ttu-id="d170a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d170a-102">SYNOPSIS</span></span>
<span data-ttu-id="d170a-103">개인 엔드포인트 연결을 승인합니다.</span><span class="sxs-lookup"><span data-stu-id="d170a-103">Approves a private endpoint connection.</span></span>

## <span data-ttu-id="d170a-104">구문</span><span class="sxs-lookup"><span data-stu-id="d170a-104">SYNTAX</span></span>

### <span data-ttu-id="d170a-105">ByResourceId(기본값)</span><span class="sxs-lookup"><span data-stu-id="d170a-105">ByResourceId (Default)</span></span>
```
Approve-AzPrivateEndpointConnection -ResourceId <String> [-Description <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d170a-106">ByResource</span><span class="sxs-lookup"><span data-stu-id="d170a-106">ByResource</span></span>
```
Approve-AzPrivateEndpointConnection -Name <String> -ServiceName <String> -ResourceGroupName <String>
 [-PrivateLinkResourceType <string>][-Description <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d170a-107">설명</span><span class="sxs-lookup"><span data-stu-id="d170a-107">DESCRIPTION</span></span>
<span data-ttu-id="d170a-108">**승인-AzPrivateEndpointConnection** cmdlet은 개인 엔드포인트 연결을 승인합니다.</span><span class="sxs-lookup"><span data-stu-id="d170a-108">The **Approve-AzPrivateEndpointConnection** cmdlet approves a private endpoint connection.</span></span>

## <span data-ttu-id="d170a-109">예제</span><span class="sxs-lookup"><span data-stu-id="d170a-109">EXAMPLES</span></span>

### <span data-ttu-id="d170a-110">예제 1</span><span class="sxs-lookup"><span data-stu-id="d170a-110">Example 1</span></span>
```
Approve-AzPrivateEndpointConnection -Name TestPrivateEndpointConnection -ResourceGroupName TestResourceGroup -ServiceName TestPrivateLinkService
```

<span data-ttu-id="d170a-111">이 예제에서는 개인 엔드포인트 연결을 승인합니다.</span><span class="sxs-lookup"><span data-stu-id="d170a-111">This example approves a private endpoint connection.</span></span>

## <span data-ttu-id="d170a-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d170a-112">PARAMETERS</span></span>

### <span data-ttu-id="d170a-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d170a-113">-DefaultProfile</span></span>
<span data-ttu-id="d170a-114">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="d170a-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d170a-115">-Description</span><span class="sxs-lookup"><span data-stu-id="d170a-115">-Description</span></span>
<span data-ttu-id="d170a-116">작업 이유입니다.</span><span class="sxs-lookup"><span data-stu-id="d170a-116">The reason of action.</span></span>

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

### <span data-ttu-id="d170a-117">-Name</span><span class="sxs-lookup"><span data-stu-id="d170a-117">-Name</span></span>
<span data-ttu-id="d170a-118">리소스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="d170a-118">The resource name.</span></span>

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

### <span data-ttu-id="d170a-119">-PrivateLinkResourceType</span><span class="sxs-lookup"><span data-stu-id="d170a-119">-PrivateLinkResourceType</span></span>
<span data-ttu-id="d170a-120">개인 링크 리소스 유형입니다.</span><span class="sxs-lookup"><span data-stu-id="d170a-120">The private link resource type.</span></span>

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

### <span data-ttu-id="d170a-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d170a-121">-ResourceGroupName</span></span>
<span data-ttu-id="d170a-122">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="d170a-122">The resource group name.</span></span>

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

### <span data-ttu-id="d170a-123">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="d170a-123">-ResourceId</span></span>
<span data-ttu-id="d170a-124">개인 엔드포인트 연결의 Azure Resource Manager ID입니다.</span><span class="sxs-lookup"><span data-stu-id="d170a-124">The Azure resource manager id of the private endpoint connection.</span></span>

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

### <span data-ttu-id="d170a-125">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="d170a-125">-ServiceName</span></span>
<span data-ttu-id="d170a-126">개인 링크 서비스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="d170a-126">The private link service name.</span></span>

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


### <span data-ttu-id="d170a-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d170a-127">CommonParameters</span></span>
<span data-ttu-id="d170a-128">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="d170a-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d170a-129">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="d170a-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d170a-130">입력</span><span class="sxs-lookup"><span data-stu-id="d170a-130">INPUTS</span></span>

### <span data-ttu-id="d170a-131">System.String</span><span class="sxs-lookup"><span data-stu-id="d170a-131">System.String</span></span>

## <span data-ttu-id="d170a-132">출력</span><span class="sxs-lookup"><span data-stu-id="d170a-132">OUTPUTS</span></span>

### <span data-ttu-id="d170a-133">Microsoft.Azure.Commands.Network.Models.PSPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="d170a-133">Microsoft.Azure.Commands.Network.Models.PSPrivateLinkService</span></span>

## <span data-ttu-id="d170a-134">참고 사항</span><span class="sxs-lookup"><span data-stu-id="d170a-134">NOTES</span></span>

## <span data-ttu-id="d170a-135">관련 링크</span><span class="sxs-lookup"><span data-stu-id="d170a-135">RELATED LINKS</span></span>

[<span data-ttu-id="d170a-136">Deny-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="d170a-136">Deny-AzPrivateEndpointConnection</span></span>](./Deny-AzPrivateEndpointConnection.md)

[<span data-ttu-id="d170a-137">Get-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="d170a-137">Get-AzPrivateEndpointConnection</span></span>](./Get-AzPrivateEndpointConnection.md)

[<span data-ttu-id="d170a-138">Remove-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="d170a-138">Remove-AzPrivateEndpointConnection</span></span>](./Remove-AzPrivateEndpointConnection.md)

[<span data-ttu-id="d170a-139">Set-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="d170a-139">Set-AzPrivateEndpointConnection</span></span>](./Set-AzPrivateEndpointConnection.md)