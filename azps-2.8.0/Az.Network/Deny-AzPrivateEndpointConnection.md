---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/deny-azprivateendpointconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Deny-AzPrivateEndpointConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Deny-AzPrivateEndpointConnection.md
ms.openlocfilehash: 4a67914fd3709ef972adac8eba6b1b2fa211fbf6
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93870305"
---
# <span data-ttu-id="a12af-101">Deny-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="a12af-101">Deny-AzPrivateEndpointConnection</span></span>

## <span data-ttu-id="a12af-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a12af-102">SYNOPSIS</span></span>
<span data-ttu-id="a12af-103">개인 끝점 연결을 거부 합니다.</span><span class="sxs-lookup"><span data-stu-id="a12af-103">denies a private endpoint connection.</span></span>

## <span data-ttu-id="a12af-104">구문과</span><span class="sxs-lookup"><span data-stu-id="a12af-104">SYNTAX</span></span>

### <span data-ttu-id="a12af-105">ByResourceId (기본값)</span><span class="sxs-lookup"><span data-stu-id="a12af-105">ByResourceId (Default)</span></span>
```
Deny-AzPrivateEndpointConnection -ResourceId <String> [-Description <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a12af-106">ByResource</span><span class="sxs-lookup"><span data-stu-id="a12af-106">ByResource</span></span>
```
Deny-AzPrivateEndpointConnection -Name <String> -ServiceName <String> -ResourceGroupName <String>
 [-Description <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a12af-107">설명은</span><span class="sxs-lookup"><span data-stu-id="a12af-107">DESCRIPTION</span></span>
<span data-ttu-id="a12af-108">**Deny-AzPrivateEndpointConnection** cmdlet은 개인 끝점 연결을 거부 합니다.</span><span class="sxs-lookup"><span data-stu-id="a12af-108">The **Deny-AzPrivateEndpointConnection** cmdlet denies a private endpoint connection.</span></span>

## <span data-ttu-id="a12af-109">예제의</span><span class="sxs-lookup"><span data-stu-id="a12af-109">EXAMPLES</span></span>

### <span data-ttu-id="a12af-110">예제 1</span><span class="sxs-lookup"><span data-stu-id="a12af-110">Example 1</span></span>
```
Deny-AzPrivateEndpointConnection -Name TestPrivateEndpointConnection -ResourceGroupName TestResourceGroup -ServiceName TestPrivateLinkService
```

<span data-ttu-id="a12af-111">이 예제에서는 개인 끝점 연결을 거부 합니다.</span><span class="sxs-lookup"><span data-stu-id="a12af-111">This example denies a private endpoint connection.</span></span>

## <span data-ttu-id="a12af-112">변수</span><span class="sxs-lookup"><span data-stu-id="a12af-112">PARAMETERS</span></span>

### <span data-ttu-id="a12af-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a12af-113">-DefaultProfile</span></span>
<span data-ttu-id="a12af-114">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="a12af-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a12af-115">-설명</span><span class="sxs-lookup"><span data-stu-id="a12af-115">-Description</span></span>
<span data-ttu-id="a12af-116">작업의 이유입니다.</span><span class="sxs-lookup"><span data-stu-id="a12af-116">The reason of action.</span></span>

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

### <span data-ttu-id="a12af-117">-이름</span><span class="sxs-lookup"><span data-stu-id="a12af-117">-Name</span></span>
<span data-ttu-id="a12af-118">자원 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="a12af-118">The resource name.</span></span>

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

### <span data-ttu-id="a12af-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a12af-119">-ResourceGroupName</span></span>
<span data-ttu-id="a12af-120">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="a12af-120">The resource group name.</span></span>

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

### <span data-ttu-id="a12af-121">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="a12af-121">-ResourceId</span></span>
<span data-ttu-id="a12af-122">개인 끝점 연결의 Azure resource manager id입니다.</span><span class="sxs-lookup"><span data-stu-id="a12af-122">The Azure resource manager id of the private endpoint connection.</span></span>

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

### <span data-ttu-id="a12af-123">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="a12af-123">-ServiceName</span></span>
<span data-ttu-id="a12af-124">개인 링크 서비스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="a12af-124">The private link service name.</span></span>

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

### <span data-ttu-id="a12af-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a12af-125">CommonParameters</span></span>
<span data-ttu-id="a12af-126">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="a12af-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a12af-127">자세한 내용은 [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="a12af-127">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a12af-128">입력</span><span class="sxs-lookup"><span data-stu-id="a12af-128">INPUTS</span></span>

### <span data-ttu-id="a12af-129">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="a12af-129">System.String</span></span>

## <span data-ttu-id="a12af-130">출력</span><span class="sxs-lookup"><span data-stu-id="a12af-130">OUTPUTS</span></span>

### <span data-ttu-id="a12af-131">PSPrivateLinkService에 대 한.</span><span class="sxs-lookup"><span data-stu-id="a12af-131">Microsoft.Azure.Commands.Network.Models.PSPrivateLinkService</span></span>

## <span data-ttu-id="a12af-132">상속자</span><span class="sxs-lookup"><span data-stu-id="a12af-132">NOTES</span></span>

## <span data-ttu-id="a12af-133">관련 링크</span><span class="sxs-lookup"><span data-stu-id="a12af-133">RELATED LINKS</span></span>

[<span data-ttu-id="a12af-134">Get-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="a12af-134">Get-AzPrivateEndpointConnection</span></span>](./Get-AzPrivateEndpointConnection.md)

[<span data-ttu-id="a12af-135">Deny-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="a12af-135">Deny-AzPrivateEndpointConnection</span></span>](./Deny-AzPrivateEndpointConnection.md)

[<span data-ttu-id="a12af-136">제거-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="a12af-136">Remove-AzPrivateEndpointConnection</span></span>](./Remove-AzPrivateEndpointConnection.md)