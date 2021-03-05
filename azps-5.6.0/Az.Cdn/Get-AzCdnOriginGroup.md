---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
online version: https://docs.microsoft.com/powershell/module/az.cdn/get-azcdnorigingroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Get-AzCdnOriginGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Get-AzCdnOriginGroup.md
ms.openlocfilehash: f79b3b4e8347c485230141416461c1f320d3d7b4
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101996912"
---
# <span data-ttu-id="2f0a9-101">Get-AzCdnOriginGroup</span><span class="sxs-lookup"><span data-stu-id="2f0a9-101">Get-AzCdnOriginGroup</span></span>

## <span data-ttu-id="2f0a9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2f0a9-102">SYNOPSIS</span></span>
<span data-ttu-id="2f0a9-103">CDN 원본 그룹을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="2f0a9-103">Gets a CDN origin group</span></span>

## <span data-ttu-id="2f0a9-104">구문</span><span class="sxs-lookup"><span data-stu-id="2f0a9-104">SYNTAX</span></span>

### <span data-ttu-id="2f0a9-105">ByFieldsParameterSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="2f0a9-105">ByFieldsParameterSet (Default)</span></span>
```
Get-AzCdnOriginGroup -EndpointName <String> -OriginGroupName <String> -ProfileName <String>
 -ResourceGroupName <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2f0a9-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="2f0a9-106">ByResourceIdParameterSet</span></span>
```
Get-AzCdnOriginGroup -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2f0a9-107">설명</span><span class="sxs-lookup"><span data-stu-id="2f0a9-107">DESCRIPTION</span></span>
<span data-ttu-id="2f0a9-108">Get-AzCdnOriginGroup cmdlet은 CDN 원본 그룹을 검색합니다.</span><span class="sxs-lookup"><span data-stu-id="2f0a9-108">The Get-AzCdnOriginGroup cmdlet retrieves a CDN origin group.</span></span>

## <span data-ttu-id="2f0a9-109">예제</span><span class="sxs-lookup"><span data-stu-id="2f0a9-109">EXAMPLES</span></span>

### <span data-ttu-id="2f0a9-110">예제 1</span><span class="sxs-lookup"><span data-stu-id="2f0a9-110">Example 1</span></span>
```powershell
PS C:\> Get-AzCdnOriginGroup -ResourceGroupName $resourceGroupName -ProfileName $profileName -EndpointName $endpointName -OriginGroupName $originGroupName
```

<span data-ttu-id="2f0a9-111">이 명령은 지정된 엔드포인트 내에서 원본 그룹을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="2f0a9-111">This command will get the origin group within the specified endpoint.</span></span>

## <span data-ttu-id="2f0a9-112">매개 변수</span><span class="sxs-lookup"><span data-stu-id="2f0a9-112">PARAMETERS</span></span>

### <span data-ttu-id="2f0a9-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2f0a9-113">-DefaultProfile</span></span>
<span data-ttu-id="2f0a9-114">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="2f0a9-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2f0a9-115">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="2f0a9-115">-EndpointName</span></span>
<span data-ttu-id="2f0a9-116">Azure CDN 엔드포인트 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="2f0a9-116">Azure CDN endpoint name.</span></span>

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

### <span data-ttu-id="2f0a9-117">-OriginGroupName</span><span class="sxs-lookup"><span data-stu-id="2f0a9-117">-OriginGroupName</span></span>
<span data-ttu-id="2f0a9-118">Azure CDN 원본 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="2f0a9-118">Azure CDN origin group name.</span></span>

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

### <span data-ttu-id="2f0a9-119">-ProfileName</span><span class="sxs-lookup"><span data-stu-id="2f0a9-119">-ProfileName</span></span>
<span data-ttu-id="2f0a9-120">Azure CDN 프로필 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="2f0a9-120">Azure CDN profile name.</span></span>

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

### <span data-ttu-id="2f0a9-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2f0a9-121">-ResourceGroupName</span></span>
<span data-ttu-id="2f0a9-122">Azure CDN 프로필의 리소스 그룹입니다.</span><span class="sxs-lookup"><span data-stu-id="2f0a9-122">The resource group of the Azure CDN profile.</span></span>

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

### <span data-ttu-id="2f0a9-123">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="2f0a9-123">-ResourceId</span></span>
<span data-ttu-id="2f0a9-124">원본 그룹에 대한 리소스 ID</span><span class="sxs-lookup"><span data-stu-id="2f0a9-124">Resource Id for the the origin group</span></span>

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

### <span data-ttu-id="2f0a9-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2f0a9-125">CommonParameters</span></span>
<span data-ttu-id="2f0a9-126">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="2f0a9-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2f0a9-127">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="2f0a9-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2f0a9-128">입력</span><span class="sxs-lookup"><span data-stu-id="2f0a9-128">INPUTS</span></span>

### <span data-ttu-id="2f0a9-129">없음</span><span class="sxs-lookup"><span data-stu-id="2f0a9-129">None</span></span>

## <span data-ttu-id="2f0a9-130">출력</span><span class="sxs-lookup"><span data-stu-id="2f0a9-130">OUTPUTS</span></span>

### <span data-ttu-id="2f0a9-131">System.Object</span><span class="sxs-lookup"><span data-stu-id="2f0a9-131">System.Object</span></span>

## <span data-ttu-id="2f0a9-132">참고 사항</span><span class="sxs-lookup"><span data-stu-id="2f0a9-132">NOTES</span></span>

## <span data-ttu-id="2f0a9-133">관련 링크</span><span class="sxs-lookup"><span data-stu-id="2f0a9-133">RELATED LINKS</span></span>
