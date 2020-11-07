---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azprivateendpointconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzPrivateEndpointConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzPrivateEndpointConnection.md
ms.openlocfilehash: 588402480cbd626a747208705ec59fd10c572075
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93872185"
---
# <span data-ttu-id="4b43b-101">Set-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="4b43b-101">Set-AzPrivateEndpointConnection</span></span>

## <span data-ttu-id="4b43b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4b43b-102">SYNOPSIS</span></span>
<span data-ttu-id="4b43b-103">개인 링크 서비스에서 개인 끝점 연결 상태를 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="4b43b-103">Updates a private endpoint connection state on private link service.</span></span>

## <span data-ttu-id="4b43b-104">구문과</span><span class="sxs-lookup"><span data-stu-id="4b43b-104">SYNTAX</span></span>

```
Set-AzPrivateEndpointConnection -Name <String> -ServiceName <String> -ResourceGroupName <String>
 -PrivateLinkServiceConnectionState <String> [-Description <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="4b43b-105">설명은</span><span class="sxs-lookup"><span data-stu-id="4b43b-105">DESCRIPTION</span></span>
<span data-ttu-id="4b43b-106">**AzPrivateEndpointConnection** cmdlet은 개인 링크 서비스에서 개인 끝점 연결 상태를 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="4b43b-106">The **Set-AzPrivateEndpointConnection** cmdlet updates a private endpoint connection state on a private link service</span></span>

## <span data-ttu-id="4b43b-107">예제의</span><span class="sxs-lookup"><span data-stu-id="4b43b-107">EXAMPLES</span></span>

### <span data-ttu-id="4b43b-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="4b43b-108">Example 1</span></span>
```
Set-AzPrivateEndpointConnection -Name TestPrivateEndpointConnection -ResourceGroupName TestResourceGroup -ServiceName TestPrivateLinkService -PrivateLinkServiceConnectionState "Approved"
```

<span data-ttu-id="4b43b-109">이 예제에서는 개인 끝점 연결 상태를 승인 됨으로 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="4b43b-109">This example updates a private endpoint connection state to Approved.</span></span>

## <span data-ttu-id="4b43b-110">변수</span><span class="sxs-lookup"><span data-stu-id="4b43b-110">PARAMETERS</span></span>

### <span data-ttu-id="4b43b-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4b43b-111">-DefaultProfile</span></span>
<span data-ttu-id="4b43b-112">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="4b43b-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4b43b-113">-설명</span><span class="sxs-lookup"><span data-stu-id="4b43b-113">-Description</span></span>
<span data-ttu-id="4b43b-114">작업의 이유입니다.</span><span class="sxs-lookup"><span data-stu-id="4b43b-114">The reason of action.</span></span>

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

### <span data-ttu-id="4b43b-115">-이름</span><span class="sxs-lookup"><span data-stu-id="4b43b-115">-Name</span></span>
<span data-ttu-id="4b43b-116">자원 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="4b43b-116">The resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4b43b-117">-PrivateLinkServiceConnectionState</span><span class="sxs-lookup"><span data-stu-id="4b43b-117">-PrivateLinkServiceConnectionState</span></span>
<span data-ttu-id="4b43b-118">리소스를 승인 또는 거부 했습니다.</span><span class="sxs-lookup"><span data-stu-id="4b43b-118">Approved or rejected the resource.</span></span>

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

### <span data-ttu-id="4b43b-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4b43b-119">-ResourceGroupName</span></span>
<span data-ttu-id="4b43b-120">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="4b43b-120">The resource group name.</span></span>

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

### <span data-ttu-id="4b43b-121">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="4b43b-121">-ServiceName</span></span>
<span data-ttu-id="4b43b-122">개인 링크 서비스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="4b43b-122">The private link service name.</span></span>

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

### <span data-ttu-id="4b43b-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4b43b-123">CommonParameters</span></span>
<span data-ttu-id="4b43b-124">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="4b43b-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4b43b-125">자세한 내용은 [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="4b43b-125">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4b43b-126">입력</span><span class="sxs-lookup"><span data-stu-id="4b43b-126">INPUTS</span></span>

### <span data-ttu-id="4b43b-127">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="4b43b-127">System.String</span></span>

## <span data-ttu-id="4b43b-128">출력</span><span class="sxs-lookup"><span data-stu-id="4b43b-128">OUTPUTS</span></span>

### <span data-ttu-id="4b43b-129">PSPrivateLinkService에 대 한.</span><span class="sxs-lookup"><span data-stu-id="4b43b-129">Microsoft.Azure.Commands.Network.Models.PSPrivateLinkService</span></span>

## <span data-ttu-id="4b43b-130">상속자</span><span class="sxs-lookup"><span data-stu-id="4b43b-130">NOTES</span></span>

## <span data-ttu-id="4b43b-131">관련 링크</span><span class="sxs-lookup"><span data-stu-id="4b43b-131">RELATED LINKS</span></span>
