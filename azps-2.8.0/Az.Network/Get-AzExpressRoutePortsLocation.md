---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azexpressrouteportslocation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRoutePortsLocation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRoutePortsLocation.md
ms.openlocfilehash: 196cc354ddac7f317400b7baa665b8975dcc9df9
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93870186"
---
# <span data-ttu-id="e83b8-101">Get-AzExpressRoutePortsLocation</span><span class="sxs-lookup"><span data-stu-id="e83b8-101">Get-AzExpressRoutePortsLocation</span></span>

## <span data-ttu-id="e83b8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e83b8-102">SYNOPSIS</span></span>
<span data-ttu-id="e83b8-103">ExpressRoutePort 리소스를 사용할 수 있는 위치를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="e83b8-103">Gets the locations at which ExpressRoutePort resources are available.</span></span>

## <span data-ttu-id="e83b8-104">구문과</span><span class="sxs-lookup"><span data-stu-id="e83b8-104">SYNTAX</span></span>

```
Get-AzExpressRoutePortsLocation [-LocationName <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="e83b8-105">설명은</span><span class="sxs-lookup"><span data-stu-id="e83b8-105">DESCRIPTION</span></span>
<span data-ttu-id="e83b8-106">**AzExpressRoutePortsLocation** Cmdlet은 ExpressRoutePort 리소스를 사용할 수 있는 위치를 검색 하는 데 사용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="e83b8-106">The **Get-AzExpressRoutePortsLocation** cmdlet is used to retrieve the locations at which ExpressRoutePort resources are available.</span></span> <span data-ttu-id="e83b8-107">특정 위치를 입력으로 제공 하면 cmdlet은 해당 위치의 세부 정보, 즉 해당 위치의 사용 가능한 대역폭 목록 등을 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="e83b8-107">Given a specific location as input, the cmdlet displays the details of that location i.e., list of available bandwidths at that location.</span></span>

## <span data-ttu-id="e83b8-108">예제의</span><span class="sxs-lookup"><span data-stu-id="e83b8-108">EXAMPLES</span></span>

### <span data-ttu-id="e83b8-109">예제 1</span><span class="sxs-lookup"><span data-stu-id="e83b8-109">Example 1</span></span>
```powershell
PS C:\> Get-AzExpressRoutePortsLocation
```

<span data-ttu-id="e83b8-110">ExpressRoutePort 리소스를 사용할 수 있는 위치를 나열 합니다.</span><span class="sxs-lookup"><span data-stu-id="e83b8-110">Lists the locations at which ExpressRoutePort resources are available.</span></span>

### <span data-ttu-id="e83b8-111">예제 2</span><span class="sxs-lookup"><span data-stu-id="e83b8-111">Example 2</span></span>
```powershell
PS C:\> Get-AzExpressRoutePortsLocation -LocationName $loc
```

<span data-ttu-id="e83b8-112">$Loc 위치에서 사용할 수 있는 ExpressRoutePort 대역폭을 나열 합니다.</span><span class="sxs-lookup"><span data-stu-id="e83b8-112">Lists the ExpressRoutePort bandwidths available at location $loc.</span></span>

## <span data-ttu-id="e83b8-113">변수</span><span class="sxs-lookup"><span data-stu-id="e83b8-113">PARAMETERS</span></span>

### <span data-ttu-id="e83b8-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e83b8-114">-DefaultProfile</span></span>
<span data-ttu-id="e83b8-115">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="e83b8-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e83b8-116">-LocationName</span><span class="sxs-lookup"><span data-stu-id="e83b8-116">-LocationName</span></span>
<span data-ttu-id="e83b8-117">위치의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="e83b8-117">The name of the location.</span></span>

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

### <span data-ttu-id="e83b8-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e83b8-118">CommonParameters</span></span>
<span data-ttu-id="e83b8-119">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="e83b8-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e83b8-120">자세한 내용은 [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="e83b8-120">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e83b8-121">입력</span><span class="sxs-lookup"><span data-stu-id="e83b8-121">INPUTS</span></span>

### <span data-ttu-id="e83b8-122">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="e83b8-122">System.String</span></span>

## <span data-ttu-id="e83b8-123">출력</span><span class="sxs-lookup"><span data-stu-id="e83b8-123">OUTPUTS</span></span>

### <span data-ttu-id="e83b8-124">PSExpressRoutePortsLocation에 대 한.</span><span class="sxs-lookup"><span data-stu-id="e83b8-124">Microsoft.Azure.Commands.Network.Models.PSExpressRoutePortsLocation</span></span>

## <span data-ttu-id="e83b8-125">상속자</span><span class="sxs-lookup"><span data-stu-id="e83b8-125">NOTES</span></span>

## <span data-ttu-id="e83b8-126">관련 링크</span><span class="sxs-lookup"><span data-stu-id="e83b8-126">RELATED LINKS</span></span>
