---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azavailableprivateendpointtype
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzAvailablePrivateEndpointType.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzAvailablePrivateEndpointType.md
ms.openlocfilehash: 1ca9e604a1371d83fdedd2986534fa8926b6286b
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98338078"
---
# <span data-ttu-id="ba1f4-101">Get-AzAvailablePrivateEndpointType</span><span class="sxs-lookup"><span data-stu-id="ba1f4-101">Get-AzAvailablePrivateEndpointType</span></span>

## <span data-ttu-id="ba1f4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ba1f4-102">SYNOPSIS</span></span>
<span data-ttu-id="ba1f4-103">위치에서 사용 가능한 개인 끝점 유형을 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="ba1f4-103">Return available private end point types in the location.</span></span>

## <span data-ttu-id="ba1f4-104">구문</span><span class="sxs-lookup"><span data-stu-id="ba1f4-104">SYNTAX</span></span>

```
Get-AzAvailablePrivateEndpointType -Location <String> [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ba1f4-105">설명</span><span class="sxs-lookup"><span data-stu-id="ba1f4-105">DESCRIPTION</span></span>
<span data-ttu-id="ba1f4-106">**Get-AzAvailablePrivateEndpointType** cmdlet은 해당 위치에서 사용 가능한 모든 개인 끝점 유형을 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="ba1f4-106">The **Get-AzAvailablePrivateEndpointType** cmdlet returns all available private end point types in the location.</span></span>

## <span data-ttu-id="ba1f4-107">예제</span><span class="sxs-lookup"><span data-stu-id="ba1f4-107">EXAMPLES</span></span>

### <span data-ttu-id="ba1f4-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="ba1f4-108">Example 1</span></span>
```powershell
Get-AzAvailablePrivateEndpointType -Location eastus

[
  {
    "id": "subscriptions/00000000-0000-0000-0000-000000000000/providers/Microsoft.Network/locations/availablePrivateEndpointTypes/typename1",
    "type": "Microsoft.Network/availablePrivateEndpointType",
    "resourceName": "Microsoft.Sql/servers"
  },
  {
    "id": "subscriptions/00000000-0000-0000-0000-000000000000/providers/Microsoft.Network/locations/availablePrivateEndpointTypes/typename2",
    "type": "Microsoft.Network/availablePrivateEndpointType",
    "resourceName": "Microsoft.Storage/accounts"
  },
  {
    "id": "subscriptions/00000000-0000-0000-0000-000000000000/providers/Microsoft.Network/locations/availablePrivateEndpointTypes/typename3",
    "type": "Microsoft.Network/availablePrivateEndpointType",
    "resourceName": "Microsoft.Cosmos/cosmosDbAccounts"
  }
]
```

<span data-ttu-id="ba1f4-109">이 예제에서는 해당 위치에서 사용 가능한 모든 개인 끝점 유형을 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="ba1f4-109">This example returns all available private end point types in the location.</span></span>

## <span data-ttu-id="ba1f4-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ba1f4-110">PARAMETERS</span></span>

### <span data-ttu-id="ba1f4-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ba1f4-111">-DefaultProfile</span></span>
<span data-ttu-id="ba1f4-112">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="ba1f4-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ba1f4-113">-Location</span><span class="sxs-lookup"><span data-stu-id="ba1f4-113">-Location</span></span>
<span data-ttu-id="ba1f4-114">위치입니다.</span><span class="sxs-lookup"><span data-stu-id="ba1f4-114">The location.</span></span>

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

### <span data-ttu-id="ba1f4-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ba1f4-115">-ResourceGroupName</span></span>
<span data-ttu-id="ba1f4-116">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="ba1f4-116">The resource group name.</span></span>

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

### <span data-ttu-id="ba1f4-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ba1f4-117">CommonParameters</span></span>
<span data-ttu-id="ba1f4-118">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="ba1f4-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ba1f4-119">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="ba1f4-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ba1f4-120">입력</span><span class="sxs-lookup"><span data-stu-id="ba1f4-120">INPUTS</span></span>

### <span data-ttu-id="ba1f4-121">System.String</span><span class="sxs-lookup"><span data-stu-id="ba1f4-121">System.String</span></span>

## <span data-ttu-id="ba1f4-122">출력</span><span class="sxs-lookup"><span data-stu-id="ba1f4-122">OUTPUTS</span></span>

### <span data-ttu-id="ba1f4-123">Microsoft.Azure.Commands.Network.Models.PSAvailablePrivateEndpointType</span><span class="sxs-lookup"><span data-stu-id="ba1f4-123">Microsoft.Azure.Commands.Network.Models.PSAvailablePrivateEndpointType</span></span>

## <span data-ttu-id="ba1f4-124">참고 사항</span><span class="sxs-lookup"><span data-stu-id="ba1f4-124">NOTES</span></span>

## <span data-ttu-id="ba1f4-125">관련 링크</span><span class="sxs-lookup"><span data-stu-id="ba1f4-125">RELATED LINKS</span></span>