---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
online version: https://docs.microsoft.com/en-us/powershell/module/az.cdn/remove-azcdnorigingroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Remove-AzCdnOriginGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Remove-AzCdnOriginGroup.md
ms.openlocfilehash: 081d5a73d6bd3cefff6f0c3bc57d3e0190f785a7
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98496152"
---
# <span data-ttu-id="4bc84-101">Remove-AzCdnOriginGroup</span><span class="sxs-lookup"><span data-stu-id="4bc84-101">Remove-AzCdnOriginGroup</span></span>

## <span data-ttu-id="4bc84-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4bc84-102">SYNOPSIS</span></span>
<span data-ttu-id="4bc84-103">CDN 원본 그룹을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="4bc84-103">Removes a CDN origin group</span></span>

## <span data-ttu-id="4bc84-104">구문</span><span class="sxs-lookup"><span data-stu-id="4bc84-104">SYNTAX</span></span>

### <span data-ttu-id="4bc84-105">ByFieldsParameterSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="4bc84-105">ByFieldsParameterSet (Default)</span></span>
```
Remove-AzCdnOriginGroup -OriginGroupName <String> -EndpointName <String> -ProfileName <String>
 -ResourceGroupName <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="4bc84-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="4bc84-106">ByResourceIdParameterSet</span></span>
```
Remove-AzCdnOriginGroup -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4bc84-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="4bc84-107">ByObjectParameterSet</span></span>
```
Remove-AzCdnOriginGroup [-PassThru] -CdnOriginGroup <PSOriginGroup> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4bc84-108">설명</span><span class="sxs-lookup"><span data-stu-id="4bc84-108">DESCRIPTION</span></span>
<span data-ttu-id="4bc84-109">Remove-AzCdnOriginGroup 엔드포인트에서 CDN 원본 그룹을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="4bc84-109">Remove-AzCdnOriginGroup will remove a CDN origin group from the specified endpoint.</span></span> 

## <span data-ttu-id="4bc84-110">예제</span><span class="sxs-lookup"><span data-stu-id="4bc84-110">EXAMPLES</span></span>

### <span data-ttu-id="4bc84-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="4bc84-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzCdnOriginGroup -ResourceGroupName $resourceGroupName -ProfileName $profileName -EndpointName $endpointName -OriginGroupName $originGroupName
```

<span data-ttu-id="4bc84-112">이 cmdlet은 지정된 엔드포인트에서 지정된 원본 그룹을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="4bc84-112">This cmdlet will remove the specified origin group from the given endpoint.</span></span> 

## <span data-ttu-id="4bc84-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="4bc84-113">PARAMETERS</span></span>

### <span data-ttu-id="4bc84-114">-CdnOriginGroup</span><span class="sxs-lookup"><span data-stu-id="4bc84-114">-CdnOriginGroup</span></span>
<span data-ttu-id="4bc84-115">CDN 원본 그룹 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="4bc84-115">The CDN origin group object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Cdn.Models.OriginGroup.PSOriginGroup
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="4bc84-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4bc84-116">-DefaultProfile</span></span>
<span data-ttu-id="4bc84-117">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="4bc84-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4bc84-118">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="4bc84-118">-EndpointName</span></span>
<span data-ttu-id="4bc84-119">Azure CDN 엔드포인트 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="4bc84-119">Azure CDN endpoint name.</span></span>

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

### <span data-ttu-id="4bc84-120">-OriginGroupName</span><span class="sxs-lookup"><span data-stu-id="4bc84-120">-OriginGroupName</span></span>
<span data-ttu-id="4bc84-121">Azure CDN 원본 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="4bc84-121">Azure CDN origin group name.</span></span>

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

### <span data-ttu-id="4bc84-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="4bc84-122">-PassThru</span></span>
<span data-ttu-id="4bc84-123">지정된 경우 개체를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="4bc84-123">Return object if specified.</span></span>

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

### <span data-ttu-id="4bc84-124">-ProfileName</span><span class="sxs-lookup"><span data-stu-id="4bc84-124">-ProfileName</span></span>
<span data-ttu-id="4bc84-125">Azure CDN 프로필 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="4bc84-125">Azure CDN profile name.</span></span>

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

### <span data-ttu-id="4bc84-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4bc84-126">-ResourceGroupName</span></span>
<span data-ttu-id="4bc84-127">Azure CDN 프로필의 리소스 그룹입니다.</span><span class="sxs-lookup"><span data-stu-id="4bc84-127">The resource group of the Azure CDN profile.</span></span>

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

### <span data-ttu-id="4bc84-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="4bc84-128">-ResourceId</span></span>
<span data-ttu-id="4bc84-129">Azure CDN 원본 그룹의 리소스 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="4bc84-129">The resource id of the Azure CDN origin group.</span></span>

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

### <span data-ttu-id="4bc84-130">-Confirm</span><span class="sxs-lookup"><span data-stu-id="4bc84-130">-Confirm</span></span>
<span data-ttu-id="4bc84-131">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="4bc84-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4bc84-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4bc84-132">-WhatIf</span></span>
<span data-ttu-id="4bc84-133">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="4bc84-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4bc84-134">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="4bc84-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4bc84-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4bc84-135">CommonParameters</span></span>
<span data-ttu-id="4bc84-136">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="4bc84-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4bc84-137">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="4bc84-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4bc84-138">입력</span><span class="sxs-lookup"><span data-stu-id="4bc84-138">INPUTS</span></span>

### <span data-ttu-id="4bc84-139">없음</span><span class="sxs-lookup"><span data-stu-id="4bc84-139">None</span></span>

## <span data-ttu-id="4bc84-140">출력</span><span class="sxs-lookup"><span data-stu-id="4bc84-140">OUTPUTS</span></span>

### <span data-ttu-id="4bc84-141">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="4bc84-141">System.Boolean</span></span>

## <span data-ttu-id="4bc84-142">참고 사항</span><span class="sxs-lookup"><span data-stu-id="4bc84-142">NOTES</span></span>

## <span data-ttu-id="4bc84-143">관련 링크</span><span class="sxs-lookup"><span data-stu-id="4bc84-143">RELATED LINKS</span></span>
