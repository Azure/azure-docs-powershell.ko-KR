---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Peering.dll-Help.xml
Module Name: Az.Peering
online version: https://docs.microsoft.com/en-us/powershell/module/az.peering/get-azpeeringservicelocation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Get-AzPeeringServiceLocation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Get-AzPeeringServiceLocation.md
ms.openlocfilehash: 6f869cee7258c38e941ca8fbb7c8ac31b47171af
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100179177"
---
# <span data-ttu-id="84dbb-101">Get-AzPeeringServiceLocation</span><span class="sxs-lookup"><span data-stu-id="84dbb-101">Get-AzPeeringServiceLocation</span></span>

## <span data-ttu-id="84dbb-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="84dbb-102">SYNOPSIS</span></span>
<span data-ttu-id="84dbb-103">Microsoft에서 제공하는 피어링 서비스 위치 목록을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="84dbb-103">Gets a list of peering service locations offered by Microsoft.</span></span>

## <span data-ttu-id="84dbb-104">구문</span><span class="sxs-lookup"><span data-stu-id="84dbb-104">SYNTAX</span></span>

```
Get-AzPeeringServiceLocation [-Country <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="84dbb-105">설명</span><span class="sxs-lookup"><span data-stu-id="84dbb-105">DESCRIPTION</span></span>
<span data-ttu-id="84dbb-106">피어링 위치를 나열합니다.</span><span class="sxs-lookup"><span data-stu-id="84dbb-106">List peering locations.</span></span>

## <span data-ttu-id="84dbb-107">예제</span><span class="sxs-lookup"><span data-stu-id="84dbb-107">EXAMPLES</span></span>

### <span data-ttu-id="84dbb-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="84dbb-108">Example 1</span></span>
```powershell
PS C:\>Get-AzPeeringServiceLocation -Country "United States" | Where-Object { $_.State -match "Washington"}

Country     : United States
State       : Washington
AzureRegion : West US
Name        : Washington
Id          :
Type        : Microsoft.Peering/peeringServiceLocations
```

<span data-ttu-id="84dbb-109">워싱턴에 대한 피어링 위치를 검색합니다.</span><span class="sxs-lookup"><span data-stu-id="84dbb-109">Retrieves the peering locations for washington.</span></span>

### <span data-ttu-id="84dbb-110">예제 2</span><span class="sxs-lookup"><span data-stu-id="84dbb-110">Example 2</span></span>
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

<span data-ttu-id="84dbb-111">워싱턴에 대한 피어링 위치를 검색합니다.</span><span class="sxs-lookup"><span data-stu-id="84dbb-111">Retrieves the peering locations for washington.</span></span>

## <span data-ttu-id="84dbb-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="84dbb-112">PARAMETERS</span></span>

### <span data-ttu-id="84dbb-113">-Country</span><span class="sxs-lookup"><span data-stu-id="84dbb-113">-Country</span></span>
<span data-ttu-id="84dbb-114">국가 필터</span><span class="sxs-lookup"><span data-stu-id="84dbb-114">The country filter</span></span>

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

### <span data-ttu-id="84dbb-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="84dbb-115">-DefaultProfile</span></span>
<span data-ttu-id="84dbb-116">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="84dbb-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="84dbb-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="84dbb-117">CommonParameters</span></span>
<span data-ttu-id="84dbb-118">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="84dbb-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="84dbb-119">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="84dbb-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="84dbb-120">입력</span><span class="sxs-lookup"><span data-stu-id="84dbb-120">INPUTS</span></span>

### <span data-ttu-id="84dbb-121">없음</span><span class="sxs-lookup"><span data-stu-id="84dbb-121">None</span></span>

## <span data-ttu-id="84dbb-122">출력</span><span class="sxs-lookup"><span data-stu-id="84dbb-122">OUTPUTS</span></span>

### <span data-ttu-id="84dbb-123">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeeringServiceLocation</span><span class="sxs-lookup"><span data-stu-id="84dbb-123">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeeringServiceLocation</span></span>

## <span data-ttu-id="84dbb-124">참고 사항</span><span class="sxs-lookup"><span data-stu-id="84dbb-124">NOTES</span></span>

## <span data-ttu-id="84dbb-125">관련 링크</span><span class="sxs-lookup"><span data-stu-id="84dbb-125">RELATED LINKS</span></span>
