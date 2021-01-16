---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azprivateendpointconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzPrivateEndpointConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzPrivateEndpointConnection.md
ms.openlocfilehash: b8625e5909ca1928b2e0e828b7ecb83f93252b27
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98344174"
---
# <span data-ttu-id="c1063-101">Set-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="c1063-101">Set-AzPrivateEndpointConnection</span></span>

## <span data-ttu-id="c1063-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c1063-102">SYNOPSIS</span></span>
<span data-ttu-id="c1063-103">개인 링크 서비스에서 개인 엔드포인트 연결 상태를 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="c1063-103">Updates a private endpoint connection state on private link service.</span></span>

## <span data-ttu-id="c1063-104">구문</span><span class="sxs-lookup"><span data-stu-id="c1063-104">SYNTAX</span></span>

### <span data-ttu-id="c1063-105">ByResourceId(기본값)</span><span class="sxs-lookup"><span data-stu-id="c1063-105">ByResourceId (Default)</span></span>
```
Set-AzPrivateEndpointConnection -ResourceId <String>
 -PrivateLinkServiceConnectionState <String> [-Description <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c1063-106">ByResource</span><span class="sxs-lookup"><span data-stu-id="c1063-106">ByResource</span></span>
```
Set-AzPrivateEndpointConnection -Name <String> -ServiceName <String> -ResourceGroupName <String> [-PrivateLinkResourceType <String>]
 -PrivateLinkServiceConnectionState <String> [-Description <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c1063-107">설명</span><span class="sxs-lookup"><span data-stu-id="c1063-107">DESCRIPTION</span></span>
<span data-ttu-id="c1063-108">**Set-AzPrivateEndpointConnection** cmdlet은 개인 링크 서비스에서 개인 엔드포인트 연결 상태를 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="c1063-108">The **Set-AzPrivateEndpointConnection** cmdlet updates a private endpoint connection state on a private link service</span></span>

## <span data-ttu-id="c1063-109">예제</span><span class="sxs-lookup"><span data-stu-id="c1063-109">EXAMPLES</span></span>

### <span data-ttu-id="c1063-110">예제 1</span><span class="sxs-lookup"><span data-stu-id="c1063-110">Example 1</span></span>
```
Set-AzPrivateEndpointConnection -Name TestPrivateEndpointConnection -ResourceGroupName TestResourceGroup -ServiceName TestPrivateLinkService -PrivateLinkServiceConnectionState "Approved"
```

<span data-ttu-id="c1063-111">이 예제에서는 개인 엔드포인트 연결 상태를 Approved로 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="c1063-111">This example updates a private endpoint connection state to Approved.</span></span>

## <span data-ttu-id="c1063-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c1063-112">PARAMETERS</span></span>

### <span data-ttu-id="c1063-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c1063-113">-DefaultProfile</span></span>
<span data-ttu-id="c1063-114">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="c1063-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c1063-115">-Description</span><span class="sxs-lookup"><span data-stu-id="c1063-115">-Description</span></span>
<span data-ttu-id="c1063-116">작업 이유입니다.</span><span class="sxs-lookup"><span data-stu-id="c1063-116">The reason of action.</span></span>

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

### <span data-ttu-id="c1063-117">-Name</span><span class="sxs-lookup"><span data-stu-id="c1063-117">-Name</span></span>
<span data-ttu-id="c1063-118">리소스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="c1063-118">The resource name.</span></span>

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

### <span data-ttu-id="c1063-119">-PrivateLinkResourceType</span><span class="sxs-lookup"><span data-stu-id="c1063-119">-PrivateLinkResourceType</span></span>
<span data-ttu-id="c1063-120">개인 링크 리소스 유형입니다.</span><span class="sxs-lookup"><span data-stu-id="c1063-120">The private link resource type.</span></span>

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

### <span data-ttu-id="c1063-121">-PrivateLinkServiceConnectionState</span><span class="sxs-lookup"><span data-stu-id="c1063-121">-PrivateLinkServiceConnectionState</span></span>
<span data-ttu-id="c1063-122">리소스를 승인하거나 거부합니다.</span><span class="sxs-lookup"><span data-stu-id="c1063-122">Approved or rejected the resource.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c1063-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c1063-123">-ResourceGroupName</span></span>
<span data-ttu-id="c1063-124">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="c1063-124">The resource group name.</span></span>

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

### <span data-ttu-id="c1063-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="c1063-125">-ResourceId</span></span>
<span data-ttu-id="c1063-126">개인 엔드포인트 연결의 Azure Resource Manager ID입니다.</span><span class="sxs-lookup"><span data-stu-id="c1063-126">The Azure resource manager id of the private endpoint connection.</span></span>

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

### <span data-ttu-id="c1063-127">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="c1063-127">-ServiceName</span></span>
<span data-ttu-id="c1063-128">개인 링크 서비스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="c1063-128">The private link service name.</span></span>

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

### <span data-ttu-id="c1063-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c1063-129">CommonParameters</span></span>
<span data-ttu-id="c1063-130">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="c1063-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c1063-131">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="c1063-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c1063-132">입력</span><span class="sxs-lookup"><span data-stu-id="c1063-132">INPUTS</span></span>

### <span data-ttu-id="c1063-133">System.String</span><span class="sxs-lookup"><span data-stu-id="c1063-133">System.String</span></span>

## <span data-ttu-id="c1063-134">출력</span><span class="sxs-lookup"><span data-stu-id="c1063-134">OUTPUTS</span></span>

### <span data-ttu-id="c1063-135">Microsoft.Azure.Commands.Network.Models.PSPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="c1063-135">Microsoft.Azure.Commands.Network.Models.PSPrivateLinkService</span></span>

## <span data-ttu-id="c1063-136">참고 사항</span><span class="sxs-lookup"><span data-stu-id="c1063-136">NOTES</span></span>

## <span data-ttu-id="c1063-137">관련 링크</span><span class="sxs-lookup"><span data-stu-id="c1063-137">RELATED LINKS</span></span>

[<span data-ttu-id="c1063-138">Approve-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="c1063-138">Approve-AzPrivateEndpointConnection</span></span>](./Approve-AzPrivateEndpointConnection.md)

[<span data-ttu-id="c1063-139">Deny-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="c1063-139">Deny-AzPrivateEndpointConnection</span></span>](./Deny-AzPrivateEndpointConnection.md)

[<span data-ttu-id="c1063-140">Get-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="c1063-140">Get-AzPrivateEndpointConnection</span></span>](./Get-AzPrivateEndpointConnection.md)

[<span data-ttu-id="c1063-141">Remove-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="c1063-141">Remove-AzPrivateEndpointConnection</span></span>](./Remove-AzPrivateEndpointConnection.md)