---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Peering.dll-Help.xml
Module Name: Az.Peering
online version: https://docs.microsoft.com/en-us/powershell/module/az.peering/get-azpeeringservicelocation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Get-AzPeeringServiceLocation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Get-AzPeeringServiceLocation.md
ms.openlocfilehash: 6f869cee7258c38e941ca8fbb7c8ac31b47171af
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94204939"
---
# <span data-ttu-id="e1f7a-101">Get-AzPeeringServiceLocation</span><span class="sxs-lookup"><span data-stu-id="e1f7a-101">Get-AzPeeringServiceLocation</span></span>

## <span data-ttu-id="e1f7a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e1f7a-102">SYNOPSIS</span></span>
<span data-ttu-id="e1f7a-103">Microsoft에서 제공 하는 피어 링 서비스 위치의 목록을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="e1f7a-103">Gets a list of peering service locations offered by Microsoft.</span></span>

## <span data-ttu-id="e1f7a-104">구문과</span><span class="sxs-lookup"><span data-stu-id="e1f7a-104">SYNTAX</span></span>

```
Get-AzPeeringServiceLocation [-Country <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="e1f7a-105">설명은</span><span class="sxs-lookup"><span data-stu-id="e1f7a-105">DESCRIPTION</span></span>
<span data-ttu-id="e1f7a-106">피어 링 위치를 나열 합니다.</span><span class="sxs-lookup"><span data-stu-id="e1f7a-106">List peering locations.</span></span>

## <span data-ttu-id="e1f7a-107">예제의</span><span class="sxs-lookup"><span data-stu-id="e1f7a-107">EXAMPLES</span></span>

### <span data-ttu-id="e1f7a-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="e1f7a-108">Example 1</span></span>
```powershell
PS C:\>Get-AzPeeringServiceLocation -Country "United States" | Where-Object { $_.State -match "Washington"}

Country     : United States
State       : Washington
AzureRegion : West US
Name        : Washington
Id          :
Type        : Microsoft.Peering/peeringServiceLocations
```

<span data-ttu-id="e1f7a-109">인천에 대 한 피어 링 위치를 검색 합니다.</span><span class="sxs-lookup"><span data-stu-id="e1f7a-109">Retrieves the peering locations for washington.</span></span>

### <span data-ttu-id="e1f7a-110">예제 2</span><span class="sxs-lookup"><span data-stu-id="e1f7a-110">Example 2</span></span>
```powershell
PS C:\>Get-AzPeeringServiceLocation -Country "United States"

Country     : United States
State       : Alabama
AzureRegion : East US
Name        : Alabama
Id          :
Type        : Microsoft.Peering/peeringServiceLocations

Country     : United States
State       : Arizona
AzureRegion : West US
Name        : Arizona
Id          :
Type        : Microsoft.Peering/peeringServiceLocations

...
```

<span data-ttu-id="e1f7a-111">인천에 대 한 피어 링 위치를 검색 합니다.</span><span class="sxs-lookup"><span data-stu-id="e1f7a-111">Retrieves the peering locations for washington.</span></span>

## <span data-ttu-id="e1f7a-112">변수</span><span class="sxs-lookup"><span data-stu-id="e1f7a-112">PARAMETERS</span></span>

### <span data-ttu-id="e1f7a-113">-국가</span><span class="sxs-lookup"><span data-stu-id="e1f7a-113">-Country</span></span>
<span data-ttu-id="e1f7a-114">국가 필터</span><span class="sxs-lookup"><span data-stu-id="e1f7a-114">The country filter</span></span>

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

### <span data-ttu-id="e1f7a-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e1f7a-115">-DefaultProfile</span></span>
<span data-ttu-id="e1f7a-116">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="e1f7a-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e1f7a-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e1f7a-117">CommonParameters</span></span>
<span data-ttu-id="e1f7a-118">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="e1f7a-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e1f7a-119">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="e1f7a-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e1f7a-120">입력</span><span class="sxs-lookup"><span data-stu-id="e1f7a-120">INPUTS</span></span>

### <span data-ttu-id="e1f7a-121">않아야</span><span class="sxs-lookup"><span data-stu-id="e1f7a-121">None</span></span>

## <span data-ttu-id="e1f7a-122">출력</span><span class="sxs-lookup"><span data-stu-id="e1f7a-122">OUTPUTS</span></span>

### <span data-ttu-id="e1f7a-123">PSPeeringServiceLocation (Microsoft. PowerShell.</span><span class="sxs-lookup"><span data-stu-id="e1f7a-123">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeeringServiceLocation</span></span>

## <span data-ttu-id="e1f7a-124">상속자</span><span class="sxs-lookup"><span data-stu-id="e1f7a-124">NOTES</span></span>

## <span data-ttu-id="e1f7a-125">관련 링크</span><span class="sxs-lookup"><span data-stu-id="e1f7a-125">RELATED LINKS</span></span>
