---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azprivatelinkserviceconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzPrivateLinkServiceConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzPrivateLinkServiceConnection.md
ms.openlocfilehash: 8669eed6e34b2f03d4da8f1f6490a95e4762241d
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93871370"
---
# <span data-ttu-id="00942-101">New-AzPrivateLinkServiceConnection</span><span class="sxs-lookup"><span data-stu-id="00942-101">New-AzPrivateLinkServiceConnection</span></span>

## <span data-ttu-id="00942-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="00942-102">SYNOPSIS</span></span>
<span data-ttu-id="00942-103">개인 링크 서비스 연결 구성을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="00942-103">Creates a private link service connection configuration.</span></span>

## <span data-ttu-id="00942-104">구문과</span><span class="sxs-lookup"><span data-stu-id="00942-104">SYNTAX</span></span>

### <span data-ttu-id="00942-105">SetByResource (기본값)</span><span class="sxs-lookup"><span data-stu-id="00942-105">SetByResource (Default)</span></span>
```
New-AzPrivateLinkServiceConnection -Name <String> -PrivateLinkService <PSPrivateLinkService>
 [-GroupId <String[]>] [-RequestMessage <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="00942-106">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="00942-106">SetByResourceId</span></span>
```
New-AzPrivateLinkServiceConnection -Name <String> -PrivateLinkServiceId <String> [-GroupId <String[]>]
 [-RequestMessage <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="00942-107">설명은</span><span class="sxs-lookup"><span data-stu-id="00942-107">DESCRIPTION</span></span>
<span data-ttu-id="00942-108">**새 AzPrivateLinkServiceConnection Cmdlet은** 개인 링크 서비스 연결 구성을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="00942-108">**The New-AzPrivateLinkServiceConnection** cmdlet creates a private link service connection configuration.</span></span>

## <span data-ttu-id="00942-109">예제의</span><span class="sxs-lookup"><span data-stu-id="00942-109">EXAMPLES</span></span>

### <span data-ttu-id="00942-110">예제 1</span><span class="sxs-lookup"><span data-stu-id="00942-110">Example 1</span></span>
```
New-AzPrivateLinkServiceConnection -Name MyPLSConnection -PrivateLinkServiceId "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/TestResourceGroup/providers/Microsoft.Network/privateLinkServices/privateLinkService" -RequestMessage "Please Approve my request"
```

<span data-ttu-id="00942-111">이 예제에서는 전용 끝점을 만들 때 사용 하는 전용 링크 서비스 연결 개체를 메모리에 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="00942-111">This example create a private link service connection object in memory for using in creating private endpoint.</span></span>

## <span data-ttu-id="00942-112">변수</span><span class="sxs-lookup"><span data-stu-id="00942-112">PARAMETERS</span></span>

### <span data-ttu-id="00942-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="00942-113">-DefaultProfile</span></span>
<span data-ttu-id="00942-114">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="00942-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="00942-115">-GroupId</span><span class="sxs-lookup"><span data-stu-id="00942-115">-GroupId</span></span>
<span data-ttu-id="00942-116">그룹 id의 목록입니다.</span><span class="sxs-lookup"><span data-stu-id="00942-116">The list of group id.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="00942-117">-이름</span><span class="sxs-lookup"><span data-stu-id="00942-117">-Name</span></span>
<span data-ttu-id="00942-118">개인 링크 서비스의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="00942-118">The name of private link service.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="00942-119">-PrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="00942-119">-PrivateLinkService</span></span>
<span data-ttu-id="00942-120">개인 링크 서비스.</span><span class="sxs-lookup"><span data-stu-id="00942-120">The private link service.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSPrivateLinkService
Parameter Sets: SetByResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="00942-121">-PrivateLinkServiceId</span><span class="sxs-lookup"><span data-stu-id="00942-121">-PrivateLinkServiceId</span></span>
<span data-ttu-id="00942-122">개인 링크 서비스의 id입니다.</span><span class="sxs-lookup"><span data-stu-id="00942-122">The id of private link service.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="00942-123">-전송한</span><span class="sxs-lookup"><span data-stu-id="00942-123">-RequestMessage</span></span>
<span data-ttu-id="00942-124">요청 메시지입니다.</span><span class="sxs-lookup"><span data-stu-id="00942-124">The request message.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="00942-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="00942-125">CommonParameters</span></span>
<span data-ttu-id="00942-126">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="00942-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="00942-127">자세한 내용은 [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="00942-127">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="00942-128">입력</span><span class="sxs-lookup"><span data-stu-id="00942-128">INPUTS</span></span>

### <span data-ttu-id="00942-129">않아야</span><span class="sxs-lookup"><span data-stu-id="00942-129">None</span></span>

## <span data-ttu-id="00942-130">출력</span><span class="sxs-lookup"><span data-stu-id="00942-130">OUTPUTS</span></span>

### <span data-ttu-id="00942-131">PSPrivateLinkServiceConnection에 대 한.</span><span class="sxs-lookup"><span data-stu-id="00942-131">Microsoft.Azure.Commands.Network.Models.PSPrivateLinkServiceConnection</span></span>

## <span data-ttu-id="00942-132">상속자</span><span class="sxs-lookup"><span data-stu-id="00942-132">NOTES</span></span>

## <span data-ttu-id="00942-133">관련 링크</span><span class="sxs-lookup"><span data-stu-id="00942-133">RELATED LINKS</span></span>

[<span data-ttu-id="00942-134">새로운 AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="00942-134">New-AzPrivateEndpoint</span></span>](./New-AzPrivateEndpoint.md)