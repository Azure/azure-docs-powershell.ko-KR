---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
online version: https://docs.microsoft.com/powershell/module/az.cdn/new-azcdnorigingroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/New-AzCdnOriginGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/New-AzCdnOriginGroup.md
ms.openlocfilehash: 34d5b4dccb43f604625652f1c39b2250926058d8
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101998937"
---
# <span data-ttu-id="648fb-101">New-AzCdnOriginGroup</span><span class="sxs-lookup"><span data-stu-id="648fb-101">New-AzCdnOriginGroup</span></span>

## <span data-ttu-id="648fb-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="648fb-102">SYNOPSIS</span></span>
<span data-ttu-id="648fb-103">새 CDN 원본 그룹 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="648fb-103">Creates a new CDN origin group</span></span>

## <span data-ttu-id="648fb-104">구문</span><span class="sxs-lookup"><span data-stu-id="648fb-104">SYNTAX</span></span>

### <span data-ttu-id="648fb-105">ByFieldsParameterSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="648fb-105">ByFieldsParameterSet (Default)</span></span>
```
New-AzCdnOriginGroup -EndpointName <String> -OriginGroupName <String>
 -OriginId <System.Collections.Generic.List`1[System.String]> [-ProbeIntervalInSeconds <Int32>]
 [-ProbePath <String>] [-ProbeProtocol <String>] [-ProbeRequestType <String>] -ProfileName <String>
 -ResourceGroupName <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="648fb-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="648fb-106">ByObjectParameterSet</span></span>
```
New-AzCdnOriginGroup -CdnOriginGroup <PSOriginGroup> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="648fb-107">설명</span><span class="sxs-lookup"><span data-stu-id="648fb-107">DESCRIPTION</span></span>
<span data-ttu-id="648fb-108">New-AzCdnOriginGroup 엔드포인트 내에서 새 원본 그룹을 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="648fb-108">The New-AzCdnOriginGroup will create a new origin group within the specified endpoint.</span></span> <span data-ttu-id="648fb-109">엔드포인트의 첫 번째 원본 그룹인 경우 DefaultOriginGroup 속성도 설정해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="648fb-109">If this is the first origin group for endpoint, then the DefaultOriginGroup property must also be set.</span></span>

## <span data-ttu-id="648fb-110">예제</span><span class="sxs-lookup"><span data-stu-id="648fb-110">EXAMPLES</span></span>

### <span data-ttu-id="648fb-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="648fb-111">Example 1</span></span>
```powershell
PS C:\> New-AzCdnOriginGroup -ResourceGroupName $resourceGroupName -ProfileName $profileName -EndpointName $endpointName -OriginGroupName $originGroupName -OriginId $originId
```
<span data-ttu-id="648fb-112">이 cmdlet은 지정된 엔드포인트 내에서 새 원본 그룹을 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="648fb-112">This cmdlet will create a new origin group within the specified endpoint.</span></span> <span data-ttu-id="648fb-113">원본 집합으로 주어진 원본 ID를 활용합니다.</span><span class="sxs-lookup"><span data-stu-id="648fb-113">It will utilize the given origin ids as the set of origins.</span></span>

## <span data-ttu-id="648fb-114">매개 변수</span><span class="sxs-lookup"><span data-stu-id="648fb-114">PARAMETERS</span></span>

### <span data-ttu-id="648fb-115">-CdnOriginGroup</span><span class="sxs-lookup"><span data-stu-id="648fb-115">-CdnOriginGroup</span></span>
<span data-ttu-id="648fb-116">CDN 원본 그룹 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="648fb-116">The CDN origin group object.</span></span>

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

### <span data-ttu-id="648fb-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="648fb-117">-DefaultProfile</span></span>
<span data-ttu-id="648fb-118">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="648fb-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="648fb-119">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="648fb-119">-EndpointName</span></span>
<span data-ttu-id="648fb-120">Azure CDN 엔드포인트 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="648fb-120">Azure CDN endpoint name.</span></span>

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

### <span data-ttu-id="648fb-121">-OriginGroupName</span><span class="sxs-lookup"><span data-stu-id="648fb-121">-OriginGroupName</span></span>
<span data-ttu-id="648fb-122">Azure CDN 원본 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="648fb-122">Azure CDN origin group name.</span></span>

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

### <span data-ttu-id="648fb-123">-OriginId</span><span class="sxs-lookup"><span data-stu-id="648fb-123">-OriginId</span></span>
<span data-ttu-id="648fb-124">Azure CDN 원본 그룹 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="648fb-124">Azure CDN origin group ids.</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="648fb-125">-ProbeIntervalInSeconds</span><span class="sxs-lookup"><span data-stu-id="648fb-125">-ProbeIntervalInSeconds</span></span>
<span data-ttu-id="648fb-126">상태 프로브 사이의 초 수입니다.</span><span class="sxs-lookup"><span data-stu-id="648fb-126">The number of seconds between health probes.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="648fb-127">-ProbePath</span><span class="sxs-lookup"><span data-stu-id="648fb-127">-ProbePath</span></span>
<span data-ttu-id="648fb-128">원본의 상태 확인에 사용되는 원본을 상대로 하는 경로입니다.</span><span class="sxs-lookup"><span data-stu-id="648fb-128">The path relative to the origin that is used to determine the health of the origin.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="648fb-129">-ProbeProtocol</span><span class="sxs-lookup"><span data-stu-id="648fb-129">-ProbeProtocol</span></span>
<span data-ttu-id="648fb-130">상태 프로브에 사용할 프로토콜입니다.</span><span class="sxs-lookup"><span data-stu-id="648fb-130">Protocol to use for health probe.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="648fb-131">-ProbeRequestType</span><span class="sxs-lookup"><span data-stu-id="648fb-131">-ProbeRequestType</span></span>
<span data-ttu-id="648fb-132">만든 상태 프로브 요청의 형식입니다.</span><span class="sxs-lookup"><span data-stu-id="648fb-132">The type of health probe request that is made.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="648fb-133">-ProfileName</span><span class="sxs-lookup"><span data-stu-id="648fb-133">-ProfileName</span></span>
<span data-ttu-id="648fb-134">Azure CDN 프로필 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="648fb-134">Azure CDN profile name.</span></span>

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

### <span data-ttu-id="648fb-135">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="648fb-135">-ResourceGroupName</span></span>
<span data-ttu-id="648fb-136">Azure CDN 프로필의 리소스 그룹입니다.</span><span class="sxs-lookup"><span data-stu-id="648fb-136">The resource group of the Azure CDN profile.</span></span>

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

### <span data-ttu-id="648fb-137">-확인</span><span class="sxs-lookup"><span data-stu-id="648fb-137">-Confirm</span></span>
<span data-ttu-id="648fb-138">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="648fb-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="648fb-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="648fb-139">-WhatIf</span></span>
<span data-ttu-id="648fb-140">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="648fb-140">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="648fb-141">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="648fb-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="648fb-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="648fb-142">CommonParameters</span></span>
<span data-ttu-id="648fb-143">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="648fb-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="648fb-144">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="648fb-144">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="648fb-145">입력</span><span class="sxs-lookup"><span data-stu-id="648fb-145">INPUTS</span></span>

### <span data-ttu-id="648fb-146">System.Object</span><span class="sxs-lookup"><span data-stu-id="648fb-146">System.Object</span></span>

## <span data-ttu-id="648fb-147">출력</span><span class="sxs-lookup"><span data-stu-id="648fb-147">OUTPUTS</span></span>

### <span data-ttu-id="648fb-148">System.Object</span><span class="sxs-lookup"><span data-stu-id="648fb-148">System.Object</span></span>

## <span data-ttu-id="648fb-149">참고 사항</span><span class="sxs-lookup"><span data-stu-id="648fb-149">NOTES</span></span>

## <span data-ttu-id="648fb-150">관련 링크</span><span class="sxs-lookup"><span data-stu-id="648fb-150">RELATED LINKS</span></span>
