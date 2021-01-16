---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
online version: https://docs.microsoft.com/en-us/powershell/module/az.cdn/get-azcdnorigingroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Get-AzCdnOriginGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Get-AzCdnOriginGroup.md
ms.openlocfilehash: 98c41f8e9e1592cf0405f42701fc19f3badd9553
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98364575"
---
# <span data-ttu-id="b1aa8-101">Get-AzCdnOriginGroup</span><span class="sxs-lookup"><span data-stu-id="b1aa8-101">Get-AzCdnOriginGroup</span></span>

## <span data-ttu-id="b1aa8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b1aa8-102">SYNOPSIS</span></span>
<span data-ttu-id="b1aa8-103">CDN 원본 그룹을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="b1aa8-103">Gets a CDN origin group</span></span>

## <span data-ttu-id="b1aa8-104">구문</span><span class="sxs-lookup"><span data-stu-id="b1aa8-104">SYNTAX</span></span>

### <span data-ttu-id="b1aa8-105">ByFieldsParameterSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="b1aa8-105">ByFieldsParameterSet (Default)</span></span>
```
Get-AzCdnOriginGroup -EndpointName <String> -OriginGroupName <String> -ProfileName <String>
 -ResourceGroupName <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b1aa8-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="b1aa8-106">ByResourceIdParameterSet</span></span>
```
Get-AzCdnOriginGroup -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b1aa8-107">설명</span><span class="sxs-lookup"><span data-stu-id="b1aa8-107">DESCRIPTION</span></span>
<span data-ttu-id="b1aa8-108">Get-AzCdnOriginGroup cmdlet은 CDN 원본 그룹을 검색합니다.</span><span class="sxs-lookup"><span data-stu-id="b1aa8-108">The Get-AzCdnOriginGroup cmdlet retrieves a CDN origin group.</span></span>

## <span data-ttu-id="b1aa8-109">예제</span><span class="sxs-lookup"><span data-stu-id="b1aa8-109">EXAMPLES</span></span>

### <span data-ttu-id="b1aa8-110">예제 1</span><span class="sxs-lookup"><span data-stu-id="b1aa8-110">Example 1</span></span>
```powershell
PS C:\> Get-AzCdnOriginGroup -ResourceGroupName $resourceGroupName -ProfileName $profileName -EndpointName $endpointName -OriginGroupName $originGroupName
```

<span data-ttu-id="b1aa8-111">이 명령은 지정된 엔드포인트 내에서 원본 그룹을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="b1aa8-111">This command will get the origin group within the specified endpoint.</span></span>

## <span data-ttu-id="b1aa8-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b1aa8-112">PARAMETERS</span></span>

### <span data-ttu-id="b1aa8-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b1aa8-113">-DefaultProfile</span></span>
<span data-ttu-id="b1aa8-114">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="b1aa8-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b1aa8-115">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="b1aa8-115">-EndpointName</span></span>
<span data-ttu-id="b1aa8-116">Azure CDN 엔드포인트 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="b1aa8-116">Azure CDN endpoint name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b1aa8-117">-OriginGroupName</span><span class="sxs-lookup"><span data-stu-id="b1aa8-117">-OriginGroupName</span></span>
<span data-ttu-id="b1aa8-118">Azure CDN 원본 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="b1aa8-118">Azure CDN origin group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b1aa8-119">-ProfileName</span><span class="sxs-lookup"><span data-stu-id="b1aa8-119">-ProfileName</span></span>
<span data-ttu-id="b1aa8-120">Azure CDN 프로필 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="b1aa8-120">Azure CDN profile name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b1aa8-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b1aa8-121">-ResourceGroupName</span></span>
<span data-ttu-id="b1aa8-122">Azure CDN 프로필의 리소스 그룹입니다.</span><span class="sxs-lookup"><span data-stu-id="b1aa8-122">The resource group of the Azure CDN profile.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b1aa8-123">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="b1aa8-123">-ResourceId</span></span>
<span data-ttu-id="b1aa8-124">원본 그룹에 대한 리소스 ID</span><span class="sxs-lookup"><span data-stu-id="b1aa8-124">Resource Id for the the origin group</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b1aa8-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b1aa8-125">CommonParameters</span></span>
<span data-ttu-id="b1aa8-126">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="b1aa8-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b1aa8-127">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="b1aa8-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b1aa8-128">입력</span><span class="sxs-lookup"><span data-stu-id="b1aa8-128">INPUTS</span></span>

### <span data-ttu-id="b1aa8-129">없음</span><span class="sxs-lookup"><span data-stu-id="b1aa8-129">None</span></span>

## <span data-ttu-id="b1aa8-130">출력</span><span class="sxs-lookup"><span data-stu-id="b1aa8-130">OUTPUTS</span></span>

### <span data-ttu-id="b1aa8-131">System.Object</span><span class="sxs-lookup"><span data-stu-id="b1aa8-131">System.Object</span></span>

## <span data-ttu-id="b1aa8-132">참고 사항</span><span class="sxs-lookup"><span data-stu-id="b1aa8-132">NOTES</span></span>

## <span data-ttu-id="b1aa8-133">관련 링크</span><span class="sxs-lookup"><span data-stu-id="b1aa8-133">RELATED LINKS</span></span>
