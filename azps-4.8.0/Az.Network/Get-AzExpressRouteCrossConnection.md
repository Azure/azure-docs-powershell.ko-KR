---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 3efb6270-f908-4734-bdb1-6c7e4e4eb382
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azexpressroutecrossconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRouteCrossConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRouteCrossConnection.md
ms.openlocfilehash: a6a3b973a893e3588b5df77700318a725bde11b9
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94204562"
---
# <span data-ttu-id="c8efc-101">Get-AzExpressRouteCrossConnection</span><span class="sxs-lookup"><span data-stu-id="c8efc-101">Get-AzExpressRouteCrossConnection</span></span>

## <span data-ttu-id="c8efc-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c8efc-102">SYNOPSIS</span></span>
<span data-ttu-id="c8efc-103">Azure에서 Azure Express 간 교차 연결을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="c8efc-103">Gets an Azure ExpressRoute cross connection from Azure.</span></span>

## <span data-ttu-id="c8efc-104">구문과</span><span class="sxs-lookup"><span data-stu-id="c8efc-104">SYNTAX</span></span>

```
Get-AzExpressRouteCrossConnection [-ResourceGroupName <String>] [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c8efc-105">설명은</span><span class="sxs-lookup"><span data-stu-id="c8efc-105">DESCRIPTION</span></span>
<span data-ttu-id="c8efc-106">**AzExpressRouteCrossConnection** cmdlet은 구독에서 express 간 교차 연결 개체를 검색 하는 데 사용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="c8efc-106">The **Get-AzExpressRouteCrossConnection** cmdlet is used to retrieve an ExpressRoute cross connection object from your subscription.</span></span>
<span data-ttu-id="c8efc-107">AzureRmExpressRouteCrossConnection</span><span class="sxs-lookup"><span data-stu-id="c8efc-107">AzureRmExpressRouteCrossConnection</span></span>

## <span data-ttu-id="c8efc-108">예제의</span><span class="sxs-lookup"><span data-stu-id="c8efc-108">EXAMPLES</span></span>

### <span data-ttu-id="c8efc-109">예제 1: Express 경로 교차 연결 가져오기</span><span class="sxs-lookup"><span data-stu-id="c8efc-109">Example 1: Get the ExpressRoute cross connection</span></span>
```
Get-AzExpressRouteCrossConnection -Name $CrossConnectionName -ResourceGroupName $rg
```

### <span data-ttu-id="c8efc-110">예제 2: 필터를 사용 하 여 Express 경로 교차 연결 나열</span><span class="sxs-lookup"><span data-stu-id="c8efc-110">Example 2: List the ExpressRoute cross connections using a filter</span></span>
```
Get-AzExpressRouteCrossConnection -Name test*
```

<span data-ttu-id="c8efc-111">이 cmdlet은 "test"로 시작 하는 모든 Express 교차 연결을 나열 합니다.</span><span class="sxs-lookup"><span data-stu-id="c8efc-111">This cmdlet will list all ExpressRoute cross connections that begin with "test"</span></span>

## <span data-ttu-id="c8efc-112">변수</span><span class="sxs-lookup"><span data-stu-id="c8efc-112">PARAMETERS</span></span>

### <span data-ttu-id="c8efc-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c8efc-113">-DefaultProfile</span></span>
<span data-ttu-id="c8efc-114">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="c8efc-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c8efc-115">-이름</span><span class="sxs-lookup"><span data-stu-id="c8efc-115">-Name</span></span>
<span data-ttu-id="c8efc-116">Express 경로 교차 연결의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="c8efc-116">The name of the ExpressRoute cross connection.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

### <span data-ttu-id="c8efc-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c8efc-117">-ResourceGroupName</span></span>
<span data-ttu-id="c8efc-118">Express 경로 간 연결을 포함 하는 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="c8efc-118">The name of the resource group that contains the ExpressRoute cross connection.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

### <span data-ttu-id="c8efc-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c8efc-119">CommonParameters</span></span>
<span data-ttu-id="c8efc-120">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="c8efc-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c8efc-121">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="c8efc-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c8efc-122">입력</span><span class="sxs-lookup"><span data-stu-id="c8efc-122">INPUTS</span></span>

### <span data-ttu-id="c8efc-123">않아야</span><span class="sxs-lookup"><span data-stu-id="c8efc-123">None</span></span>
<span data-ttu-id="c8efc-124">이 cmdlet은 입력을 허용 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="c8efc-124">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="c8efc-125">출력</span><span class="sxs-lookup"><span data-stu-id="c8efc-125">OUTPUTS</span></span>

### <span data-ttu-id="c8efc-126">PSExpressRouteCrossConnection에 대 한.</span><span class="sxs-lookup"><span data-stu-id="c8efc-126">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCrossConnection</span></span>

## <span data-ttu-id="c8efc-127">상속자</span><span class="sxs-lookup"><span data-stu-id="c8efc-127">NOTES</span></span>

## <span data-ttu-id="c8efc-128">관련 링크</span><span class="sxs-lookup"><span data-stu-id="c8efc-128">RELATED LINKS</span></span>

[<span data-ttu-id="c8efc-129">Set-AzExpressRouteCrossConnection</span><span class="sxs-lookup"><span data-stu-id="c8efc-129">Set-AzExpressRouteCrossConnection</span></span>](Set-AzExpressRouteCrossConnection.md)