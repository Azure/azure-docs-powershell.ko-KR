---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azavailableprivateendpointtype
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzAvailablePrivateEndpointType.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzAvailablePrivateEndpointType.md
ms.openlocfilehash: 1ca9e604a1371d83fdedd2986534fa8926b6286b
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94226682"
---
# <span data-ttu-id="a3f75-101">Get-AzAvailablePrivateEndpointType</span><span class="sxs-lookup"><span data-stu-id="a3f75-101">Get-AzAvailablePrivateEndpointType</span></span>

## <span data-ttu-id="a3f75-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a3f75-102">SYNOPSIS</span></span>
<span data-ttu-id="a3f75-103">위치에서 사용 가능한 개인 끝점 형식을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="a3f75-103">Return available private end point types in the location.</span></span>

## <span data-ttu-id="a3f75-104">구문과</span><span class="sxs-lookup"><span data-stu-id="a3f75-104">SYNTAX</span></span>

```
Get-AzAvailablePrivateEndpointType -Location <String> [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a3f75-105">설명은</span><span class="sxs-lookup"><span data-stu-id="a3f75-105">DESCRIPTION</span></span>
<span data-ttu-id="a3f75-106">**AzAvailablePrivateEndpointType** cmdlet은 위치에서 사용할 수 있는 모든 비공개 끝점 형식을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="a3f75-106">The **Get-AzAvailablePrivateEndpointType** cmdlet returns all available private end point types in the location.</span></span>

## <span data-ttu-id="a3f75-107">예제의</span><span class="sxs-lookup"><span data-stu-id="a3f75-107">EXAMPLES</span></span>

### <span data-ttu-id="a3f75-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="a3f75-108">Example 1</span></span>
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

<span data-ttu-id="a3f75-109">이 예제는 위치에서 사용 가능한 모든 비공개 끝점 형식을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="a3f75-109">This example returns all available private end point types in the location.</span></span>

## <span data-ttu-id="a3f75-110">변수</span><span class="sxs-lookup"><span data-stu-id="a3f75-110">PARAMETERS</span></span>

### <span data-ttu-id="a3f75-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a3f75-111">-DefaultProfile</span></span>
<span data-ttu-id="a3f75-112">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="a3f75-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a3f75-113">-위치</span><span class="sxs-lookup"><span data-stu-id="a3f75-113">-Location</span></span>
<span data-ttu-id="a3f75-114">위치입니다.</span><span class="sxs-lookup"><span data-stu-id="a3f75-114">The location.</span></span>

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

### <span data-ttu-id="a3f75-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a3f75-115">-ResourceGroupName</span></span>
<span data-ttu-id="a3f75-116">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="a3f75-116">The resource group name.</span></span>

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

### <span data-ttu-id="a3f75-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a3f75-117">CommonParameters</span></span>
<span data-ttu-id="a3f75-118">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="a3f75-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a3f75-119">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="a3f75-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a3f75-120">입력</span><span class="sxs-lookup"><span data-stu-id="a3f75-120">INPUTS</span></span>

### <span data-ttu-id="a3f75-121">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="a3f75-121">System.String</span></span>

## <span data-ttu-id="a3f75-122">출력</span><span class="sxs-lookup"><span data-stu-id="a3f75-122">OUTPUTS</span></span>

### <span data-ttu-id="a3f75-123">PSAvailablePrivateEndpointType에 대 한.</span><span class="sxs-lookup"><span data-stu-id="a3f75-123">Microsoft.Azure.Commands.Network.Models.PSAvailablePrivateEndpointType</span></span>

## <span data-ttu-id="a3f75-124">상속자</span><span class="sxs-lookup"><span data-stu-id="a3f75-124">NOTES</span></span>

## <span data-ttu-id="a3f75-125">관련 링크</span><span class="sxs-lookup"><span data-stu-id="a3f75-125">RELATED LINKS</span></span>
