---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/Get-AzSecurityLocation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzSecurityLocation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzSecurityLocation.md
ms.openlocfilehash: 2de4a80f2770624bb520aa4236a5d92bea97fdf0
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93699244"
---
# <span data-ttu-id="bed48-101">Get-AzSecurityLocation</span><span class="sxs-lookup"><span data-stu-id="bed48-101">Get-AzSecurityLocation</span></span>

## <span data-ttu-id="bed48-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="bed48-102">SYNOPSIS</span></span>
<span data-ttu-id="bed48-103">Azure 보안 센터에서 특정 구독에 대 한 데이터를 자동으로 저장 하는 위치를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="bed48-103">Gets the location where Azure Security Center will automatically save data for the specific subscription</span></span>

## <span data-ttu-id="bed48-104">구문과</span><span class="sxs-lookup"><span data-stu-id="bed48-104">SYNTAX</span></span>

### <span data-ttu-id="bed48-105">구독 범위 (기본값)</span><span class="sxs-lookup"><span data-stu-id="bed48-105">SubscriptionScope (Default)</span></span>
```
Get-AzSecurityLocation [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="bed48-106">구독 Levelresource</span><span class="sxs-lookup"><span data-stu-id="bed48-106">SubscriptionLevelResource</span></span>
```
Get-AzSecurityLocation -Name <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="bed48-107">리소스</span><span class="sxs-lookup"><span data-stu-id="bed48-107">ResourceId</span></span>
```
Get-AzSecurityLocation -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="bed48-108">설명은</span><span class="sxs-lookup"><span data-stu-id="bed48-108">DESCRIPTION</span></span>
<span data-ttu-id="bed48-109">Azure 보안 센터에서 자동으로 위치를 결정 하 여 일부 데이터를 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="bed48-109">Azure Security Center will automatically decide on a location to save some of your data.</span></span>
<span data-ttu-id="bed48-110">이 cmdlet을 사용 하 여 해당 위치를 검색 합니다.</span><span class="sxs-lookup"><span data-stu-id="bed48-110">Use this cmdlet to discover that location.</span></span>

## <span data-ttu-id="bed48-111">예제의</span><span class="sxs-lookup"><span data-stu-id="bed48-111">EXAMPLES</span></span>

### <span data-ttu-id="bed48-112">예제 1</span><span class="sxs-lookup"><span data-stu-id="bed48-112">Example 1</span></span>
```powershell
PS C:\> Get-AzSecurityLocation
Id                                                                                                   Name
--                                                                                                   ----
/subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/providers/Microsoft.Security/locations/centralus centralus
```

<span data-ttu-id="bed48-113">Azure 보안 센터에서 계산 된 보안 데이터를 저장 하는 위치를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="bed48-113">Gets the location where Azure Security Center saves the calculated security data.</span></span>

## <span data-ttu-id="bed48-114">변수</span><span class="sxs-lookup"><span data-stu-id="bed48-114">PARAMETERS</span></span>

### <span data-ttu-id="bed48-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bed48-115">-DefaultProfile</span></span>
<span data-ttu-id="bed48-116">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="bed48-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="bed48-117">-이름</span><span class="sxs-lookup"><span data-stu-id="bed48-117">-Name</span></span>
<span data-ttu-id="bed48-118">리소스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="bed48-118">Resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: SubscriptionLevelResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bed48-119">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="bed48-119">-ResourceId</span></span>
<span data-ttu-id="bed48-120">리소스 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="bed48-120">Resource ID.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bed48-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bed48-121">CommonParameters</span></span>
<span data-ttu-id="bed48-122">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="bed48-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bed48-123">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bed48-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bed48-124">입력</span><span class="sxs-lookup"><span data-stu-id="bed48-124">INPUTS</span></span>

### <span data-ttu-id="bed48-125">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="bed48-125">System.String</span></span>

## <span data-ttu-id="bed48-126">출력</span><span class="sxs-lookup"><span data-stu-id="bed48-126">OUTPUTS</span></span>

### <span data-ttu-id="bed48-127">Microsoft. Azure. 위치. PSSecurityLocation</span><span class="sxs-lookup"><span data-stu-id="bed48-127">Microsoft.Azure.Commands.Security.Models.Locations.PSSecurityLocation</span></span>

## <span data-ttu-id="bed48-128">상속자</span><span class="sxs-lookup"><span data-stu-id="bed48-128">NOTES</span></span>

## <span data-ttu-id="bed48-129">관련 링크</span><span class="sxs-lookup"><span data-stu-id="bed48-129">RELATED LINKS</span></span>
