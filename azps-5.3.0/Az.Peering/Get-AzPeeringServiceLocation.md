---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Peering.dll-Help.xml
Module Name: Az.Peering
online version: https://docs.microsoft.com/en-us/powershell/module/az.peering/get-azpeeringservicelocation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Get-AzPeeringServiceLocation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Get-AzPeeringServiceLocation.md
ms.openlocfilehash: 6f869cee7258c38e941ca8fbb7c8ac31b47171af
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98384875"
---
# <span data-ttu-id="213f4-101">Get-AzPeeringServiceLocation</span><span class="sxs-lookup"><span data-stu-id="213f4-101">Get-AzPeeringServiceLocation</span></span>

## <span data-ttu-id="213f4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="213f4-102">SYNOPSIS</span></span>
<span data-ttu-id="213f4-103">Microsoft에서 제공하는 피어링 서비스 위치 목록을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="213f4-103">Gets a list of peering service locations offered by Microsoft.</span></span>

## <span data-ttu-id="213f4-104">구문</span><span class="sxs-lookup"><span data-stu-id="213f4-104">SYNTAX</span></span>

```
Get-AzPeeringServiceLocation [-Country <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="213f4-105">설명</span><span class="sxs-lookup"><span data-stu-id="213f4-105">DESCRIPTION</span></span>
<span data-ttu-id="213f4-106">피어링 위치를 나열합니다.</span><span class="sxs-lookup"><span data-stu-id="213f4-106">List peering locations.</span></span>

## <span data-ttu-id="213f4-107">예제</span><span class="sxs-lookup"><span data-stu-id="213f4-107">EXAMPLES</span></span>

### <span data-ttu-id="213f4-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="213f4-108">Example 1</span></span>
```powershell
PS C:\>Get-AzPeeringServiceLocation -Country "United States" | Where-Object { $_.State -match "Washington"}

Country     : United States
State       : Washington
AzureRegion : West US
Name        : Washington
Id          :
Type        : Microsoft.Peering/peeringServiceLocations
```

<span data-ttu-id="213f4-109">워싱턴에 대한 피어링 위치를 검색합니다.</span><span class="sxs-lookup"><span data-stu-id="213f4-109">Retrieves the peering locations for washington.</span></span>

### <span data-ttu-id="213f4-110">예제 2</span><span class="sxs-lookup"><span data-stu-id="213f4-110">Example 2</span></span>
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

<span data-ttu-id="213f4-111">워싱턴에 대한 피어링 위치를 검색합니다.</span><span class="sxs-lookup"><span data-stu-id="213f4-111">Retrieves the peering locations for washington.</span></span>

## <span data-ttu-id="213f4-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="213f4-112">PARAMETERS</span></span>

### <span data-ttu-id="213f4-113">-Country</span><span class="sxs-lookup"><span data-stu-id="213f4-113">-Country</span></span>
<span data-ttu-id="213f4-114">국가 필터</span><span class="sxs-lookup"><span data-stu-id="213f4-114">The country filter</span></span>

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

### <span data-ttu-id="213f4-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="213f4-115">-DefaultProfile</span></span>
<span data-ttu-id="213f4-116">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="213f4-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="213f4-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="213f4-117">CommonParameters</span></span>
<span data-ttu-id="213f4-118">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="213f4-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="213f4-119">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="213f4-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="213f4-120">입력</span><span class="sxs-lookup"><span data-stu-id="213f4-120">INPUTS</span></span>

### <span data-ttu-id="213f4-121">없음</span><span class="sxs-lookup"><span data-stu-id="213f4-121">None</span></span>

## <span data-ttu-id="213f4-122">출력</span><span class="sxs-lookup"><span data-stu-id="213f4-122">OUTPUTS</span></span>

### <span data-ttu-id="213f4-123">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeeringServiceLocation</span><span class="sxs-lookup"><span data-stu-id="213f4-123">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeeringServiceLocation</span></span>

## <span data-ttu-id="213f4-124">참고 사항</span><span class="sxs-lookup"><span data-stu-id="213f4-124">NOTES</span></span>

## <span data-ttu-id="213f4-125">관련 링크</span><span class="sxs-lookup"><span data-stu-id="213f4-125">RELATED LINKS</span></span>
