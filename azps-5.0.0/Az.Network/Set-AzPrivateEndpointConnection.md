---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azprivateendpointconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzPrivateEndpointConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzPrivateEndpointConnection.md
ms.openlocfilehash: b8625e5909ca1928b2e0e828b7ecb83f93252b27
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94311342"
---
# <span data-ttu-id="dc436-101">Set-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="dc436-101">Set-AzPrivateEndpointConnection</span></span>

## <span data-ttu-id="dc436-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="dc436-102">SYNOPSIS</span></span>
<span data-ttu-id="dc436-103">개인 링크 서비스에서 개인 끝점 연결 상태를 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="dc436-103">Updates a private endpoint connection state on private link service.</span></span>

## <span data-ttu-id="dc436-104">구문과</span><span class="sxs-lookup"><span data-stu-id="dc436-104">SYNTAX</span></span>

### <span data-ttu-id="dc436-105">ByResourceId (기본값)</span><span class="sxs-lookup"><span data-stu-id="dc436-105">ByResourceId (Default)</span></span>
```
Set-AzPrivateEndpointConnection -ResourceId <String>
 -PrivateLinkServiceConnectionState <String> [-Description <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="dc436-106">ByResource</span><span class="sxs-lookup"><span data-stu-id="dc436-106">ByResource</span></span>
```
Set-AzPrivateEndpointConnection -Name <String> -ServiceName <String> -ResourceGroupName <String> [-PrivateLinkResourceType <String>]
 -PrivateLinkServiceConnectionState <String> [-Description <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="dc436-107">설명은</span><span class="sxs-lookup"><span data-stu-id="dc436-107">DESCRIPTION</span></span>
<span data-ttu-id="dc436-108">**AzPrivateEndpointConnection** cmdlet은 개인 링크 서비스에서 개인 끝점 연결 상태를 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="dc436-108">The **Set-AzPrivateEndpointConnection** cmdlet updates a private endpoint connection state on a private link service</span></span>

## <span data-ttu-id="dc436-109">예제의</span><span class="sxs-lookup"><span data-stu-id="dc436-109">EXAMPLES</span></span>

### <span data-ttu-id="dc436-110">예제 1</span><span class="sxs-lookup"><span data-stu-id="dc436-110">Example 1</span></span>
```
Set-AzPrivateEndpointConnection -Name TestPrivateEndpointConnection -ResourceGroupName TestResourceGroup -ServiceName TestPrivateLinkService -PrivateLinkServiceConnectionState "Approved"
```

<span data-ttu-id="dc436-111">이 예제에서는 개인 끝점 연결 상태를 승인 됨으로 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="dc436-111">This example updates a private endpoint connection state to Approved.</span></span>

## <span data-ttu-id="dc436-112">변수</span><span class="sxs-lookup"><span data-stu-id="dc436-112">PARAMETERS</span></span>

### <span data-ttu-id="dc436-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dc436-113">-DefaultProfile</span></span>
<span data-ttu-id="dc436-114">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="dc436-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="dc436-115">-설명</span><span class="sxs-lookup"><span data-stu-id="dc436-115">-Description</span></span>
<span data-ttu-id="dc436-116">작업의 이유입니다.</span><span class="sxs-lookup"><span data-stu-id="dc436-116">The reason of action.</span></span>

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

### <span data-ttu-id="dc436-117">-이름</span><span class="sxs-lookup"><span data-stu-id="dc436-117">-Name</span></span>
<span data-ttu-id="dc436-118">자원 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="dc436-118">The resource name.</span></span>

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

### <span data-ttu-id="dc436-119">-PrivateLinkResourceType</span><span class="sxs-lookup"><span data-stu-id="dc436-119">-PrivateLinkResourceType</span></span>
<span data-ttu-id="dc436-120">개인 링크 리소스 종류입니다.</span><span class="sxs-lookup"><span data-stu-id="dc436-120">The private link resource type.</span></span>

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

### <span data-ttu-id="dc436-121">-PrivateLinkServiceConnectionState</span><span class="sxs-lookup"><span data-stu-id="dc436-121">-PrivateLinkServiceConnectionState</span></span>
<span data-ttu-id="dc436-122">리소스를 승인 또는 거부 했습니다.</span><span class="sxs-lookup"><span data-stu-id="dc436-122">Approved or rejected the resource.</span></span>

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

### <span data-ttu-id="dc436-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dc436-123">-ResourceGroupName</span></span>
<span data-ttu-id="dc436-124">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="dc436-124">The resource group name.</span></span>

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

### <span data-ttu-id="dc436-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="dc436-125">-ResourceId</span></span>
<span data-ttu-id="dc436-126">개인 끝점 연결의 Azure resource manager id입니다.</span><span class="sxs-lookup"><span data-stu-id="dc436-126">The Azure resource manager id of the private endpoint connection.</span></span>

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

### <span data-ttu-id="dc436-127">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="dc436-127">-ServiceName</span></span>
<span data-ttu-id="dc436-128">개인 링크 서비스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="dc436-128">The private link service name.</span></span>

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

### <span data-ttu-id="dc436-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dc436-129">CommonParameters</span></span>
<span data-ttu-id="dc436-130">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="dc436-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dc436-131">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="dc436-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dc436-132">입력</span><span class="sxs-lookup"><span data-stu-id="dc436-132">INPUTS</span></span>

### <span data-ttu-id="dc436-133">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="dc436-133">System.String</span></span>

## <span data-ttu-id="dc436-134">출력</span><span class="sxs-lookup"><span data-stu-id="dc436-134">OUTPUTS</span></span>

### <span data-ttu-id="dc436-135">PSPrivateLinkService에 대 한.</span><span class="sxs-lookup"><span data-stu-id="dc436-135">Microsoft.Azure.Commands.Network.Models.PSPrivateLinkService</span></span>

## <span data-ttu-id="dc436-136">상속자</span><span class="sxs-lookup"><span data-stu-id="dc436-136">NOTES</span></span>

## <span data-ttu-id="dc436-137">관련 링크</span><span class="sxs-lookup"><span data-stu-id="dc436-137">RELATED LINKS</span></span>

[<span data-ttu-id="dc436-138">승인-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="dc436-138">Approve-AzPrivateEndpointConnection</span></span>](./Approve-AzPrivateEndpointConnection.md)

[<span data-ttu-id="dc436-139">Deny-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="dc436-139">Deny-AzPrivateEndpointConnection</span></span>](./Deny-AzPrivateEndpointConnection.md)

[<span data-ttu-id="dc436-140">Get-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="dc436-140">Get-AzPrivateEndpointConnection</span></span>](./Get-AzPrivateEndpointConnection.md)

[<span data-ttu-id="dc436-141">제거-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="dc436-141">Remove-AzPrivateEndpointConnection</span></span>](./Remove-AzPrivateEndpointConnection.md)