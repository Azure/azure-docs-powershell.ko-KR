---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 3efb6270-f908-4734-bdb1-6c7e4e4eb382
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azexpressroutecrossconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRouteCrossConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRouteCrossConnection.md
ms.openlocfilehash: c15a8b57338a6c5e7c2f054e07a0d26d716627fc
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93700585"
---
# <span data-ttu-id="24a7a-101">Get-AzExpressRouteCrossConnection</span><span class="sxs-lookup"><span data-stu-id="24a7a-101">Get-AzExpressRouteCrossConnection</span></span>

## <span data-ttu-id="24a7a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="24a7a-102">SYNOPSIS</span></span>
<span data-ttu-id="24a7a-103">Azure에서 Azure Express 간 교차 연결을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="24a7a-103">Gets an Azure ExpressRoute cross connection from Azure.</span></span>

## <span data-ttu-id="24a7a-104">구문과</span><span class="sxs-lookup"><span data-stu-id="24a7a-104">SYNTAX</span></span>

```
Get-AzExpressRouteCrossConnection [-ResourceGroupName <String>] [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="24a7a-105">설명은</span><span class="sxs-lookup"><span data-stu-id="24a7a-105">DESCRIPTION</span></span>
<span data-ttu-id="24a7a-106">**AzExpressRouteCrossConnection** cmdlet은 구독에서 express 간 교차 연결 개체를 검색 하는 데 사용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="24a7a-106">The **Get-AzExpressRouteCrossConnection** cmdlet is used to retrieve an ExpressRoute cross connection object from your subscription.</span></span>
<span data-ttu-id="24a7a-107">AzureRmExpressRouteCrossConnection</span><span class="sxs-lookup"><span data-stu-id="24a7a-107">AzureRmExpressRouteCrossConnection</span></span>

## <span data-ttu-id="24a7a-108">예제의</span><span class="sxs-lookup"><span data-stu-id="24a7a-108">EXAMPLES</span></span>

### <span data-ttu-id="24a7a-109">예제 1: Express 경로 교차 연결 가져오기</span><span class="sxs-lookup"><span data-stu-id="24a7a-109">Example 1: Get the ExpressRoute cross connection</span></span>
```
Get-AzExpressRouteCrossConnection -Name $CrossConnectionName -ResourceGroupName $rg
```

### <span data-ttu-id="24a7a-110">예제 2: 필터를 사용 하 여 Express 경로 교차 연결 나열</span><span class="sxs-lookup"><span data-stu-id="24a7a-110">Example 2: List the ExpressRoute cross connections using a filter</span></span>
```
Get-AzExpressRouteCrossConnection -Name test*
```

<span data-ttu-id="24a7a-111">이 cmdlet은 "test"로 시작 하는 모든 Express 교차 연결을 나열 합니다.</span><span class="sxs-lookup"><span data-stu-id="24a7a-111">This cmdlet will list all ExpressRoute cross connections that begin with "test"</span></span>

## <span data-ttu-id="24a7a-112">변수</span><span class="sxs-lookup"><span data-stu-id="24a7a-112">PARAMETERS</span></span>

### <span data-ttu-id="24a7a-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="24a7a-113">-DefaultProfile</span></span>
<span data-ttu-id="24a7a-114">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="24a7a-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="24a7a-115">-이름</span><span class="sxs-lookup"><span data-stu-id="24a7a-115">-Name</span></span>
<span data-ttu-id="24a7a-116">Express 경로 교차 연결의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="24a7a-116">The name of the ExpressRoute cross connection.</span></span>

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

### <span data-ttu-id="24a7a-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="24a7a-117">-ResourceGroupName</span></span>
<span data-ttu-id="24a7a-118">Express 경로 간 연결을 포함 하는 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="24a7a-118">The name of the resource group that contains the ExpressRoute cross connection.</span></span>

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

### <span data-ttu-id="24a7a-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="24a7a-119">CommonParameters</span></span>
<span data-ttu-id="24a7a-120">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="24a7a-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="24a7a-121">자세한 내용은 [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="24a7a-121">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="24a7a-122">입력</span><span class="sxs-lookup"><span data-stu-id="24a7a-122">INPUTS</span></span>

### <span data-ttu-id="24a7a-123">않아야</span><span class="sxs-lookup"><span data-stu-id="24a7a-123">None</span></span>
<span data-ttu-id="24a7a-124">이 cmdlet은 입력을 허용 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="24a7a-124">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="24a7a-125">출력</span><span class="sxs-lookup"><span data-stu-id="24a7a-125">OUTPUTS</span></span>

### <span data-ttu-id="24a7a-126">PSExpressRouteCrossConnection에 대 한.</span><span class="sxs-lookup"><span data-stu-id="24a7a-126">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCrossConnection</span></span>

## <span data-ttu-id="24a7a-127">상속자</span><span class="sxs-lookup"><span data-stu-id="24a7a-127">NOTES</span></span>

## <span data-ttu-id="24a7a-128">관련 링크</span><span class="sxs-lookup"><span data-stu-id="24a7a-128">RELATED LINKS</span></span>

[<span data-ttu-id="24a7a-129">Set-AzExpressRouteCrossConnection</span><span class="sxs-lookup"><span data-stu-id="24a7a-129">Set-AzExpressRouteCrossConnection</span></span>](Set-AzExpressRouteCrossConnection.md)