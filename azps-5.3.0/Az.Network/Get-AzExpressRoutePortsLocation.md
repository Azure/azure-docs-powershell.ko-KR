---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azexpressrouteportslocation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRoutePortsLocation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRoutePortsLocation.md
ms.openlocfilehash: 918ef18717cb09bad28ee10b91f635181dd5b3cb
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98380129"
---
# <span data-ttu-id="1f5f8-101">Get-AzExpressRoutePortsLocation</span><span class="sxs-lookup"><span data-stu-id="1f5f8-101">Get-AzExpressRoutePortsLocation</span></span>

## <span data-ttu-id="1f5f8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1f5f8-102">SYNOPSIS</span></span>
<span data-ttu-id="1f5f8-103">ExpressRoutePort 리소스를 사용할 수 있는 위치를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="1f5f8-103">Gets the locations at which ExpressRoutePort resources are available.</span></span>

## <span data-ttu-id="1f5f8-104">구문</span><span class="sxs-lookup"><span data-stu-id="1f5f8-104">SYNTAX</span></span>

```
Get-AzExpressRoutePortsLocation [-LocationName <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="1f5f8-105">설명</span><span class="sxs-lookup"><span data-stu-id="1f5f8-105">DESCRIPTION</span></span>
<span data-ttu-id="1f5f8-106">**Get-AzExpressRoutePortsLocation** cmdlet은 ExpressRoutePort 리소스를 사용할 수 있는 위치를 검색하는 데 사용됩니다.</span><span class="sxs-lookup"><span data-stu-id="1f5f8-106">The **Get-AzExpressRoutePortsLocation** cmdlet is used to retrieve the locations at which ExpressRoutePort resources are available.</span></span> <span data-ttu-id="1f5f8-107">특정 위치를 입력으로 지정하면 cmdlet에 해당 위치의 세부 정보(예: 해당 위치의 사용 가능한 대역폭 목록)가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="1f5f8-107">Given a specific location as input, the cmdlet displays the details of that location i.e., list of available bandwidths at that location.</span></span>

## <span data-ttu-id="1f5f8-108">예제</span><span class="sxs-lookup"><span data-stu-id="1f5f8-108">EXAMPLES</span></span>

### <span data-ttu-id="1f5f8-109">예제 1</span><span class="sxs-lookup"><span data-stu-id="1f5f8-109">Example 1</span></span>
```powershell
PS C:\> Get-AzExpressRoutePortsLocation
```

<span data-ttu-id="1f5f8-110">ExpressRoutePort 리소스를 사용할 수 있는 위치를 나열합니다.</span><span class="sxs-lookup"><span data-stu-id="1f5f8-110">Lists the locations at which ExpressRoutePort resources are available.</span></span>

### <span data-ttu-id="1f5f8-111">예제 2</span><span class="sxs-lookup"><span data-stu-id="1f5f8-111">Example 2</span></span>
```powershell
PS C:\> Get-AzExpressRoutePortsLocation -LocationName $loc
```

<span data-ttu-id="1f5f8-112">위치 및 위치에서 사용할 수 있는 ExpressRoutePort 대역폭을 $loc.</span><span class="sxs-lookup"><span data-stu-id="1f5f8-112">Lists the ExpressRoutePort bandwidths available at location $loc.</span></span>

## <span data-ttu-id="1f5f8-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="1f5f8-113">PARAMETERS</span></span>

### <span data-ttu-id="1f5f8-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1f5f8-114">-DefaultProfile</span></span>
<span data-ttu-id="1f5f8-115">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="1f5f8-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1f5f8-116">-LocationName</span><span class="sxs-lookup"><span data-stu-id="1f5f8-116">-LocationName</span></span>
<span data-ttu-id="1f5f8-117">위치의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="1f5f8-117">The name of the location.</span></span>

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

### <span data-ttu-id="1f5f8-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1f5f8-118">CommonParameters</span></span>
<span data-ttu-id="1f5f8-119">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="1f5f8-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1f5f8-120">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="1f5f8-120">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1f5f8-121">입력</span><span class="sxs-lookup"><span data-stu-id="1f5f8-121">INPUTS</span></span>

### <span data-ttu-id="1f5f8-122">System.String</span><span class="sxs-lookup"><span data-stu-id="1f5f8-122">System.String</span></span>

## <span data-ttu-id="1f5f8-123">출력</span><span class="sxs-lookup"><span data-stu-id="1f5f8-123">OUTPUTS</span></span>

### <span data-ttu-id="1f5f8-124">Microsoft.Azure.Commands.Network.Models.PSExpressRoutePortsLocation</span><span class="sxs-lookup"><span data-stu-id="1f5f8-124">Microsoft.Azure.Commands.Network.Models.PSExpressRoutePortsLocation</span></span>

## <span data-ttu-id="1f5f8-125">참고 사항</span><span class="sxs-lookup"><span data-stu-id="1f5f8-125">NOTES</span></span>

## <span data-ttu-id="1f5f8-126">관련 링크</span><span class="sxs-lookup"><span data-stu-id="1f5f8-126">RELATED LINKS</span></span>
