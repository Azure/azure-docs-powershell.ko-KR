---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
online version: https://docs.microsoft.com/en-us/powershell/module/az.cdn/remove-azcdnorigin
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Remove-AzCdnOrigin.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Remove-AzCdnOrigin.md
ms.openlocfilehash: 8198d189d9619528bdc7fb80d30285ce9126dfed
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100200756"
---
# <span data-ttu-id="68c9b-101">Remove-AzCdnOrigin</span><span class="sxs-lookup"><span data-stu-id="68c9b-101">Remove-AzCdnOrigin</span></span>

## <span data-ttu-id="68c9b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="68c9b-102">SYNOPSIS</span></span>
<span data-ttu-id="68c9b-103">CDN 원본을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="68c9b-103">Removes a CDN origin</span></span>

## <span data-ttu-id="68c9b-104">구문</span><span class="sxs-lookup"><span data-stu-id="68c9b-104">SYNTAX</span></span>

### <span data-ttu-id="68c9b-105">ByFieldsParameterSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="68c9b-105">ByFieldsParameterSet (Default)</span></span>
```
Remove-AzCdnOrigin -OriginName <String> -EndpointName <String> -ProfileName <String>
 -ResourceGroupName <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="68c9b-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="68c9b-106">ByResourceIdParameterSet</span></span>
```
Remove-AzCdnOrigin -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="68c9b-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="68c9b-107">ByObjectParameterSet</span></span>
```
Remove-AzCdnOrigin [-PassThru] -CdnOrigin <PSOrigin> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="68c9b-108">설명</span><span class="sxs-lookup"><span data-stu-id="68c9b-108">DESCRIPTION</span></span>
<span data-ttu-id="68c9b-109">Remove-AzCdnOrigin 엔드포인트에서 CDN 원본을 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="68c9b-109">Remove-AzCdnOrigin will delete a CDN origin from the given endpoint.</span></span> <span data-ttu-id="68c9b-110">원본이 지정된 엔드포인트 내의 유일한 원본인 경우 1개 이상의 원본이 필요하기 때문에 해당 원본이 실패합니다.</span><span class="sxs-lookup"><span data-stu-id="68c9b-110">If the origin is the only origin within the specified endpoint, then the deletion will fail since at least 1 origin is needed.</span></span> 

## <span data-ttu-id="68c9b-111">예제</span><span class="sxs-lookup"><span data-stu-id="68c9b-111">EXAMPLES</span></span>

### <span data-ttu-id="68c9b-112">예제 1</span><span class="sxs-lookup"><span data-stu-id="68c9b-112">Example 1</span></span>
```powershell
PS C:\> Remove-AzCdnOrigin -ResourceGroupName $resourceGroupName -ProfileName $profileName -EndpointName $endpointName -OriginName $originName 
```
<span data-ttu-id="68c9b-113">이 cmdlet은 지정된 엔드포인트에서 지정된 원본을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="68c9b-113">This cmdlet will remove the specified origin from the given endpoint.</span></span> 

## <span data-ttu-id="68c9b-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="68c9b-114">PARAMETERS</span></span>

### <span data-ttu-id="68c9b-115">-CdnOrigin</span><span class="sxs-lookup"><span data-stu-id="68c9b-115">-CdnOrigin</span></span>
<span data-ttu-id="68c9b-116">CDN 원본 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="68c9b-116">The CDN origin object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Cdn.Models.Origin.PSOrigin
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="68c9b-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="68c9b-117">-DefaultProfile</span></span>
<span data-ttu-id="68c9b-118">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="68c9b-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="68c9b-119">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="68c9b-119">-EndpointName</span></span>
<span data-ttu-id="68c9b-120">Azure CDN 엔드포인트 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="68c9b-120">Azure CDN endpoint name.</span></span>

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

### <span data-ttu-id="68c9b-121">-OriginName</span><span class="sxs-lookup"><span data-stu-id="68c9b-121">-OriginName</span></span>
<span data-ttu-id="68c9b-122">Azure CDN 원본 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="68c9b-122">Azure CDN origin name.</span></span>

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

### <span data-ttu-id="68c9b-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="68c9b-123">-PassThru</span></span>
<span data-ttu-id="68c9b-124">지정된 경우 개체를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="68c9b-124">Return object if specified.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="68c9b-125">-ProfileName</span><span class="sxs-lookup"><span data-stu-id="68c9b-125">-ProfileName</span></span>
<span data-ttu-id="68c9b-126">Azure CDN 프로필 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="68c9b-126">Azure CDN profile name.</span></span>

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

### <span data-ttu-id="68c9b-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="68c9b-127">-ResourceGroupName</span></span>
<span data-ttu-id="68c9b-128">Azure CDN 프로필의 리소스 그룹입니다.</span><span class="sxs-lookup"><span data-stu-id="68c9b-128">The resource group of the Azure CDN profile.</span></span>

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

### <span data-ttu-id="68c9b-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="68c9b-129">-ResourceId</span></span>
<span data-ttu-id="68c9b-130">Azure CDN 원본의 리소스 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="68c9b-130">The resource id of the Azure CDN origin.</span></span>

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

### <span data-ttu-id="68c9b-131">-Confirm</span><span class="sxs-lookup"><span data-stu-id="68c9b-131">-Confirm</span></span>
<span data-ttu-id="68c9b-132">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="68c9b-132">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="68c9b-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="68c9b-133">-WhatIf</span></span>
<span data-ttu-id="68c9b-134">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="68c9b-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="68c9b-135">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="68c9b-135">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="68c9b-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="68c9b-136">CommonParameters</span></span>
<span data-ttu-id="68c9b-137">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="68c9b-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="68c9b-138">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="68c9b-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="68c9b-139">입력</span><span class="sxs-lookup"><span data-stu-id="68c9b-139">INPUTS</span></span>

### <span data-ttu-id="68c9b-140">없음</span><span class="sxs-lookup"><span data-stu-id="68c9b-140">None</span></span>

## <span data-ttu-id="68c9b-141">출력</span><span class="sxs-lookup"><span data-stu-id="68c9b-141">OUTPUTS</span></span>

### <span data-ttu-id="68c9b-142">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="68c9b-142">System.Boolean</span></span>

## <span data-ttu-id="68c9b-143">참고 사항</span><span class="sxs-lookup"><span data-stu-id="68c9b-143">NOTES</span></span>

## <span data-ttu-id="68c9b-144">관련 링크</span><span class="sxs-lookup"><span data-stu-id="68c9b-144">RELATED LINKS</span></span>
