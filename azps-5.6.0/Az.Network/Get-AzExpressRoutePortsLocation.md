---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/get-azexpressrouteportslocation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRoutePortsLocation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRoutePortsLocation.md
ms.openlocfilehash: d16b5d916f3a807de818c58de94f7f0841e04d17
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101956976"
---
# <span data-ttu-id="ec2b0-101">Get-AzExpressRoutePortsLocation</span><span class="sxs-lookup"><span data-stu-id="ec2b0-101">Get-AzExpressRoutePortsLocation</span></span>

## <span data-ttu-id="ec2b0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ec2b0-102">SYNOPSIS</span></span>
<span data-ttu-id="ec2b0-103">ExpressRoutePort 리소스를 사용할 수 있는 위치를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="ec2b0-103">Gets the locations at which ExpressRoutePort resources are available.</span></span>

## <span data-ttu-id="ec2b0-104">구문</span><span class="sxs-lookup"><span data-stu-id="ec2b0-104">SYNTAX</span></span>

```
Get-AzExpressRoutePortsLocation [-LocationName <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="ec2b0-105">설명</span><span class="sxs-lookup"><span data-stu-id="ec2b0-105">DESCRIPTION</span></span>
<span data-ttu-id="ec2b0-106">**Get-AzExpressRoutePortsLocation** cmdlet은 ExpressRoutePort 리소스를 사용할 수 있는 위치를 검색하는 데 사용됩니다.</span><span class="sxs-lookup"><span data-stu-id="ec2b0-106">The **Get-AzExpressRoutePortsLocation** cmdlet is used to retrieve the locations at which ExpressRoutePort resources are available.</span></span> <span data-ttu-id="ec2b0-107">특정 위치를 입력으로 지정하면 cmdlet에 해당 위치의 세부 정보(예: 해당 위치에서 사용 가능한 대역폭 목록)가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="ec2b0-107">Given a specific location as input, the cmdlet displays the details of that location i.e., list of available bandwidths at that location.</span></span>

## <span data-ttu-id="ec2b0-108">예제</span><span class="sxs-lookup"><span data-stu-id="ec2b0-108">EXAMPLES</span></span>

### <span data-ttu-id="ec2b0-109">예제 1</span><span class="sxs-lookup"><span data-stu-id="ec2b0-109">Example 1</span></span>
```powershell
PS C:\> Get-AzExpressRoutePortsLocation
```

<span data-ttu-id="ec2b0-110">ExpressRoutePort 리소스를 사용할 수 있는 위치를 나열합니다.</span><span class="sxs-lookup"><span data-stu-id="ec2b0-110">Lists the locations at which ExpressRoutePort resources are available.</span></span>

### <span data-ttu-id="ec2b0-111">예제 2</span><span class="sxs-lookup"><span data-stu-id="ec2b0-111">Example 2</span></span>
```powershell
PS C:\> Get-AzExpressRoutePortsLocation -LocationName $loc
```

<span data-ttu-id="ec2b0-112">위치에서 사용할 수 있는 ExpressRoutePort 대역폭을 $loc.</span><span class="sxs-lookup"><span data-stu-id="ec2b0-112">Lists the ExpressRoutePort bandwidths available at location $loc.</span></span>

## <span data-ttu-id="ec2b0-113">매개 변수</span><span class="sxs-lookup"><span data-stu-id="ec2b0-113">PARAMETERS</span></span>

### <span data-ttu-id="ec2b0-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ec2b0-114">-DefaultProfile</span></span>
<span data-ttu-id="ec2b0-115">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="ec2b0-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ec2b0-116">-LocationName</span><span class="sxs-lookup"><span data-stu-id="ec2b0-116">-LocationName</span></span>
<span data-ttu-id="ec2b0-117">위치의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="ec2b0-117">The name of the location.</span></span>

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

### <span data-ttu-id="ec2b0-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ec2b0-118">CommonParameters</span></span>
<span data-ttu-id="ec2b0-119">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="ec2b0-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ec2b0-120">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="ec2b0-120">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ec2b0-121">입력</span><span class="sxs-lookup"><span data-stu-id="ec2b0-121">INPUTS</span></span>

### <span data-ttu-id="ec2b0-122">System.String</span><span class="sxs-lookup"><span data-stu-id="ec2b0-122">System.String</span></span>

## <span data-ttu-id="ec2b0-123">출력</span><span class="sxs-lookup"><span data-stu-id="ec2b0-123">OUTPUTS</span></span>

### <span data-ttu-id="ec2b0-124">Microsoft.Azure.Commands.Network.Models.PSExpressRoutePortsLocation</span><span class="sxs-lookup"><span data-stu-id="ec2b0-124">Microsoft.Azure.Commands.Network.Models.PSExpressRoutePortsLocation</span></span>

## <span data-ttu-id="ec2b0-125">참고 사항</span><span class="sxs-lookup"><span data-stu-id="ec2b0-125">NOTES</span></span>

## <span data-ttu-id="ec2b0-126">관련 링크</span><span class="sxs-lookup"><span data-stu-id="ec2b0-126">RELATED LINKS</span></span>
