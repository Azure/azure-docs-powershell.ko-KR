---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 3efb6270-f908-4734-bdb1-6c7e4e4eb382
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azexpressroutecrossconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRouteCrossConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRouteCrossConnection.md
ms.openlocfilehash: a6a3b973a893e3588b5df77700318a725bde11b9
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100187209"
---
# <span data-ttu-id="9d059-101">Get-AzExpressRouteCrossConnection</span><span class="sxs-lookup"><span data-stu-id="9d059-101">Get-AzExpressRouteCrossConnection</span></span>

## <span data-ttu-id="9d059-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9d059-102">SYNOPSIS</span></span>
<span data-ttu-id="9d059-103">Azure에서 Azure ExpressRoute 교차 연결을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="9d059-103">Gets an Azure ExpressRoute cross connection from Azure.</span></span>

## <span data-ttu-id="9d059-104">구문</span><span class="sxs-lookup"><span data-stu-id="9d059-104">SYNTAX</span></span>

```
Get-AzExpressRouteCrossConnection [-ResourceGroupName <String>] [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9d059-105">설명</span><span class="sxs-lookup"><span data-stu-id="9d059-105">DESCRIPTION</span></span>
<span data-ttu-id="9d059-106">**Get-AzExpressRouteCrossConnection** cmdlet은 구독에서 ExpressRoute 교차 연결 개체를 검색하는 데 사용됩니다.</span><span class="sxs-lookup"><span data-stu-id="9d059-106">The **Get-AzExpressRouteCrossConnection** cmdlet is used to retrieve an ExpressRoute cross connection object from your subscription.</span></span>
<span data-ttu-id="9d059-107">AzureRmExpressRouteCrossConnection</span><span class="sxs-lookup"><span data-stu-id="9d059-107">AzureRmExpressRouteCrossConnection</span></span>

## <span data-ttu-id="9d059-108">예제</span><span class="sxs-lookup"><span data-stu-id="9d059-108">EXAMPLES</span></span>

### <span data-ttu-id="9d059-109">예제 1: ExpressRoute 교차 연결 얻기</span><span class="sxs-lookup"><span data-stu-id="9d059-109">Example 1: Get the ExpressRoute cross connection</span></span>
```
Get-AzExpressRouteCrossConnection -Name $CrossConnectionName -ResourceGroupName $rg
```

### <span data-ttu-id="9d059-110">예제 2: 필터를 사용하여 ExpressRoute 교차 연결 나열</span><span class="sxs-lookup"><span data-stu-id="9d059-110">Example 2: List the ExpressRoute cross connections using a filter</span></span>
```
Get-AzExpressRouteCrossConnection -Name test*
```

<span data-ttu-id="9d059-111">이 cmdlet은 "test"로 시작하는 모든 ExpressRoute 교차 연결을 나열합니다.</span><span class="sxs-lookup"><span data-stu-id="9d059-111">This cmdlet will list all ExpressRoute cross connections that begin with "test"</span></span>

## <span data-ttu-id="9d059-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="9d059-112">PARAMETERS</span></span>

### <span data-ttu-id="9d059-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9d059-113">-DefaultProfile</span></span>
<span data-ttu-id="9d059-114">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="9d059-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9d059-115">-Name</span><span class="sxs-lookup"><span data-stu-id="9d059-115">-Name</span></span>
<span data-ttu-id="9d059-116">ExpressRoute 교차 연결의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="9d059-116">The name of the ExpressRoute cross connection.</span></span>

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

### <span data-ttu-id="9d059-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9d059-117">-ResourceGroupName</span></span>
<span data-ttu-id="9d059-118">ExpressRoute 교차 연결을 포함하는 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="9d059-118">The name of the resource group that contains the ExpressRoute cross connection.</span></span>

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

### <span data-ttu-id="9d059-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9d059-119">CommonParameters</span></span>
<span data-ttu-id="9d059-120">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="9d059-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9d059-121">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="9d059-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9d059-122">입력</span><span class="sxs-lookup"><span data-stu-id="9d059-122">INPUTS</span></span>

### <span data-ttu-id="9d059-123">없음</span><span class="sxs-lookup"><span data-stu-id="9d059-123">None</span></span>
<span data-ttu-id="9d059-124">이 cmdlet은 입력을 허용하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="9d059-124">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="9d059-125">출력</span><span class="sxs-lookup"><span data-stu-id="9d059-125">OUTPUTS</span></span>

### <span data-ttu-id="9d059-126">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCrossConnection</span><span class="sxs-lookup"><span data-stu-id="9d059-126">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCrossConnection</span></span>

## <span data-ttu-id="9d059-127">참고 사항</span><span class="sxs-lookup"><span data-stu-id="9d059-127">NOTES</span></span>

## <span data-ttu-id="9d059-128">관련 링크</span><span class="sxs-lookup"><span data-stu-id="9d059-128">RELATED LINKS</span></span>

[<span data-ttu-id="9d059-129">Set-AzExpressRouteCrossConnection</span><span class="sxs-lookup"><span data-stu-id="9d059-129">Set-AzExpressRouteCrossConnection</span></span>](Set-AzExpressRouteCrossConnection.md)