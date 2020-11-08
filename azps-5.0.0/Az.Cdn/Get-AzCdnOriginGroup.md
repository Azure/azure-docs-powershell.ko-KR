---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
online version: https://docs.microsoft.com/en-us/powershell/module/az.cdn/get-azcdnorigingroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Get-AzCdnOriginGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Get-AzCdnOriginGroup.md
ms.openlocfilehash: 98c41f8e9e1592cf0405f42701fc19f3badd9553
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94226252"
---
# <span data-ttu-id="3aeae-101">Get-AzCdnOriginGroup</span><span class="sxs-lookup"><span data-stu-id="3aeae-101">Get-AzCdnOriginGroup</span></span>

## <span data-ttu-id="3aeae-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3aeae-102">SYNOPSIS</span></span>
<span data-ttu-id="3aeae-103">CDN 원본 그룹을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="3aeae-103">Gets a CDN origin group</span></span>

## <span data-ttu-id="3aeae-104">구문과</span><span class="sxs-lookup"><span data-stu-id="3aeae-104">SYNTAX</span></span>

### <span data-ttu-id="3aeae-105">ByFieldsParameterSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="3aeae-105">ByFieldsParameterSet (Default)</span></span>
```
Get-AzCdnOriginGroup -EndpointName <String> -OriginGroupName <String> -ProfileName <String>
 -ResourceGroupName <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3aeae-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="3aeae-106">ByResourceIdParameterSet</span></span>
```
Get-AzCdnOriginGroup -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3aeae-107">설명은</span><span class="sxs-lookup"><span data-stu-id="3aeae-107">DESCRIPTION</span></span>
<span data-ttu-id="3aeae-108">Get-AzCdnOriginGroup cmdlet은 CDN 원본 그룹을 검색 합니다.</span><span class="sxs-lookup"><span data-stu-id="3aeae-108">The Get-AzCdnOriginGroup cmdlet retrieves a CDN origin group.</span></span>

## <span data-ttu-id="3aeae-109">예제의</span><span class="sxs-lookup"><span data-stu-id="3aeae-109">EXAMPLES</span></span>

### <span data-ttu-id="3aeae-110">예제 1</span><span class="sxs-lookup"><span data-stu-id="3aeae-110">Example 1</span></span>
```powershell
PS C:\> Get-AzCdnOriginGroup -ResourceGroupName $resourceGroupName -ProfileName $profileName -EndpointName $endpointName -OriginGroupName $originGroupName
```

<span data-ttu-id="3aeae-111">이 명령은 지정 된 끝점 내의 원본 그룹을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="3aeae-111">This command will get the origin group within the specified endpoint.</span></span>

## <span data-ttu-id="3aeae-112">변수</span><span class="sxs-lookup"><span data-stu-id="3aeae-112">PARAMETERS</span></span>

### <span data-ttu-id="3aeae-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3aeae-113">-DefaultProfile</span></span>
<span data-ttu-id="3aeae-114">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="3aeae-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3aeae-115">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="3aeae-115">-EndpointName</span></span>
<span data-ttu-id="3aeae-116">Azure CDN 끝점 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="3aeae-116">Azure CDN endpoint name.</span></span>

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

### <span data-ttu-id="3aeae-117">-OriginGroupName</span><span class="sxs-lookup"><span data-stu-id="3aeae-117">-OriginGroupName</span></span>
<span data-ttu-id="3aeae-118">Azure CDN 원본 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="3aeae-118">Azure CDN origin group name.</span></span>

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

### <span data-ttu-id="3aeae-119">-/Profile</span><span class="sxs-lookup"><span data-stu-id="3aeae-119">-ProfileName</span></span>
<span data-ttu-id="3aeae-120">Azure CDN 프로필 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="3aeae-120">Azure CDN profile name.</span></span>

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

### <span data-ttu-id="3aeae-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3aeae-121">-ResourceGroupName</span></span>
<span data-ttu-id="3aeae-122">Azure CDN 프로필의 리소스 그룹입니다.</span><span class="sxs-lookup"><span data-stu-id="3aeae-122">The resource group of the Azure CDN profile.</span></span>

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

### <span data-ttu-id="3aeae-123">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="3aeae-123">-ResourceId</span></span>
<span data-ttu-id="3aeae-124">원본 그룹의 리소스 Id</span><span class="sxs-lookup"><span data-stu-id="3aeae-124">Resource Id for the the origin group</span></span>

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

### <span data-ttu-id="3aeae-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3aeae-125">CommonParameters</span></span>
<span data-ttu-id="3aeae-126">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="3aeae-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3aeae-127">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="3aeae-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3aeae-128">입력</span><span class="sxs-lookup"><span data-stu-id="3aeae-128">INPUTS</span></span>

### <span data-ttu-id="3aeae-129">않아야</span><span class="sxs-lookup"><span data-stu-id="3aeae-129">None</span></span>

## <span data-ttu-id="3aeae-130">출력</span><span class="sxs-lookup"><span data-stu-id="3aeae-130">OUTPUTS</span></span>

### <span data-ttu-id="3aeae-131">System. 개체</span><span class="sxs-lookup"><span data-stu-id="3aeae-131">System.Object</span></span>

## <span data-ttu-id="3aeae-132">상속자</span><span class="sxs-lookup"><span data-stu-id="3aeae-132">NOTES</span></span>

## <span data-ttu-id="3aeae-133">관련 링크</span><span class="sxs-lookup"><span data-stu-id="3aeae-133">RELATED LINKS</span></span>
