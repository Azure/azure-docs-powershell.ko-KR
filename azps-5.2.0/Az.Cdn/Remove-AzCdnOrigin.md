---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
online version: https://docs.microsoft.com/en-us/powershell/module/az.cdn/remove-azcdnorigin
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Remove-AzCdnOrigin.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Remove-AzCdnOrigin.md
ms.openlocfilehash: 8198d189d9619528bdc7fb80d30285ce9126dfed
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98336782"
---
# <span data-ttu-id="786a8-101">Remove-AzCdnOrigin</span><span class="sxs-lookup"><span data-stu-id="786a8-101">Remove-AzCdnOrigin</span></span>

## <span data-ttu-id="786a8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="786a8-102">SYNOPSIS</span></span>
<span data-ttu-id="786a8-103">CDN 원본을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="786a8-103">Removes a CDN origin</span></span>

## <span data-ttu-id="786a8-104">구문</span><span class="sxs-lookup"><span data-stu-id="786a8-104">SYNTAX</span></span>

### <span data-ttu-id="786a8-105">ByFieldsParameterSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="786a8-105">ByFieldsParameterSet (Default)</span></span>
```
Remove-AzCdnOrigin -OriginName <String> -EndpointName <String> -ProfileName <String>
 -ResourceGroupName <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="786a8-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="786a8-106">ByResourceIdParameterSet</span></span>
```
Remove-AzCdnOrigin -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="786a8-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="786a8-107">ByObjectParameterSet</span></span>
```
Remove-AzCdnOrigin [-PassThru] -CdnOrigin <PSOrigin> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="786a8-108">설명</span><span class="sxs-lookup"><span data-stu-id="786a8-108">DESCRIPTION</span></span>
<span data-ttu-id="786a8-109">Remove-AzCdnOrigin 엔드포인트에서 CDN 원본을 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="786a8-109">Remove-AzCdnOrigin will delete a CDN origin from the given endpoint.</span></span> <span data-ttu-id="786a8-110">원본이 지정된 엔드포인트 내의 유일한 원본인 경우 1개 이상의 원본이 필요하기 때문에 해당 원본이 실패합니다.</span><span class="sxs-lookup"><span data-stu-id="786a8-110">If the origin is the only origin within the specified endpoint, then the deletion will fail since at least 1 origin is needed.</span></span> 

## <span data-ttu-id="786a8-111">예제</span><span class="sxs-lookup"><span data-stu-id="786a8-111">EXAMPLES</span></span>

### <span data-ttu-id="786a8-112">예제 1</span><span class="sxs-lookup"><span data-stu-id="786a8-112">Example 1</span></span>
```powershell
PS C:\> Remove-AzCdnOrigin -ResourceGroupName $resourceGroupName -ProfileName $profileName -EndpointName $endpointName -OriginName $originName 
```
<span data-ttu-id="786a8-113">이 cmdlet은 지정된 엔드포인트에서 지정된 원본을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="786a8-113">This cmdlet will remove the specified origin from the given endpoint.</span></span> 

## <span data-ttu-id="786a8-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="786a8-114">PARAMETERS</span></span>

### <span data-ttu-id="786a8-115">-CdnOrigin</span><span class="sxs-lookup"><span data-stu-id="786a8-115">-CdnOrigin</span></span>
<span data-ttu-id="786a8-116">CDN 원본 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="786a8-116">The CDN origin object.</span></span>

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

### <span data-ttu-id="786a8-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="786a8-117">-DefaultProfile</span></span>
<span data-ttu-id="786a8-118">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="786a8-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="786a8-119">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="786a8-119">-EndpointName</span></span>
<span data-ttu-id="786a8-120">Azure CDN 엔드포인트 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="786a8-120">Azure CDN endpoint name.</span></span>

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

### <span data-ttu-id="786a8-121">-OriginName</span><span class="sxs-lookup"><span data-stu-id="786a8-121">-OriginName</span></span>
<span data-ttu-id="786a8-122">Azure CDN 원본 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="786a8-122">Azure CDN origin name.</span></span>

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

### <span data-ttu-id="786a8-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="786a8-123">-PassThru</span></span>
<span data-ttu-id="786a8-124">지정된 경우 개체를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="786a8-124">Return object if specified.</span></span>

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

### <span data-ttu-id="786a8-125">-ProfileName</span><span class="sxs-lookup"><span data-stu-id="786a8-125">-ProfileName</span></span>
<span data-ttu-id="786a8-126">Azure CDN 프로필 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="786a8-126">Azure CDN profile name.</span></span>

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

### <span data-ttu-id="786a8-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="786a8-127">-ResourceGroupName</span></span>
<span data-ttu-id="786a8-128">Azure CDN 프로필의 리소스 그룹입니다.</span><span class="sxs-lookup"><span data-stu-id="786a8-128">The resource group of the Azure CDN profile.</span></span>

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

### <span data-ttu-id="786a8-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="786a8-129">-ResourceId</span></span>
<span data-ttu-id="786a8-130">Azure CDN 원본의 리소스 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="786a8-130">The resource id of the Azure CDN origin.</span></span>

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

### <span data-ttu-id="786a8-131">-Confirm</span><span class="sxs-lookup"><span data-stu-id="786a8-131">-Confirm</span></span>
<span data-ttu-id="786a8-132">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="786a8-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="786a8-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="786a8-133">-WhatIf</span></span>
<span data-ttu-id="786a8-134">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="786a8-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="786a8-135">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="786a8-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="786a8-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="786a8-136">CommonParameters</span></span>
<span data-ttu-id="786a8-137">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="786a8-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="786a8-138">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="786a8-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="786a8-139">입력</span><span class="sxs-lookup"><span data-stu-id="786a8-139">INPUTS</span></span>

### <span data-ttu-id="786a8-140">없음</span><span class="sxs-lookup"><span data-stu-id="786a8-140">None</span></span>

## <span data-ttu-id="786a8-141">출력</span><span class="sxs-lookup"><span data-stu-id="786a8-141">OUTPUTS</span></span>

### <span data-ttu-id="786a8-142">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="786a8-142">System.Boolean</span></span>

## <span data-ttu-id="786a8-143">참고 사항</span><span class="sxs-lookup"><span data-stu-id="786a8-143">NOTES</span></span>

## <span data-ttu-id="786a8-144">관련 링크</span><span class="sxs-lookup"><span data-stu-id="786a8-144">RELATED LINKS</span></span>
