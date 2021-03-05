---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
online version: https://docs.microsoft.com/powershell/module/az.cdn/set-azcdnorigingroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Set-AzCdnOriginGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Set-AzCdnOriginGroup.md
ms.openlocfilehash: c70c08ad88491d7624b078babb5e62437c22e116
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101985329"
---
# <span data-ttu-id="a0bff-101">Set-AzCdnOriginGroup</span><span class="sxs-lookup"><span data-stu-id="a0bff-101">Set-AzCdnOriginGroup</span></span>

## <span data-ttu-id="a0bff-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a0bff-102">SYNOPSIS</span></span>
<span data-ttu-id="a0bff-103">CDN 원본 그룹 업데이트</span><span class="sxs-lookup"><span data-stu-id="a0bff-103">Updates the CDN origin group</span></span>

## <span data-ttu-id="a0bff-104">구문</span><span class="sxs-lookup"><span data-stu-id="a0bff-104">SYNTAX</span></span>

### <span data-ttu-id="a0bff-105">ByFieldsParameterSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="a0bff-105">ByFieldsParameterSet (Default)</span></span>
```
Set-AzCdnOriginGroup -EndpointName <String> -OriginGroupName <String>
 -OriginId <System.Collections.Generic.List`1[System.String]> [-ProbeIntervalInSeconds <Int32>]
 [-ProbePath <String>] [-ProbeProtocol <String>] [-ProbeRequestType <String>] -ProfileName <String>
 -ResourceGroupName <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="a0bff-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="a0bff-106">ByObjectParameterSet</span></span>
```
Set-AzCdnOriginGroup -CdnOriginGroup <PSOriginGroup> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a0bff-107">설명</span><span class="sxs-lookup"><span data-stu-id="a0bff-107">DESCRIPTION</span></span>
<span data-ttu-id="a0bff-108">Set-AzCdnOriginGroup 엔드포인트 내에서 지정된 원본 그룹을 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="a0bff-108">Set-AzCdnOriginGroup will update the specified origin group within the given endpoint.</span></span> 

## <span data-ttu-id="a0bff-109">예제</span><span class="sxs-lookup"><span data-stu-id="a0bff-109">EXAMPLES</span></span>

### <span data-ttu-id="a0bff-110">예제 1</span><span class="sxs-lookup"><span data-stu-id="a0bff-110">Example 1</span></span>
```powershell
PS C:\> Set-AzCdnOriginGroup -ResourceGroupName $resourceGroupName -ProfileName $profileName -EndpointName $endpointName -OriginGroupName $originGroupName -OriginId $originIds -ProbeIntervalInSeconds $probeInterval 
```
<span data-ttu-id="a0bff-111">이 cmdlet은 원본 그룹의 ProbeIntervalInSeconds 속성을 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="a0bff-111">This cmdlet will update the ProbeIntervalInSeconds property in the origin group.</span></span> 

## <span data-ttu-id="a0bff-112">매개 변수</span><span class="sxs-lookup"><span data-stu-id="a0bff-112">PARAMETERS</span></span>

### <span data-ttu-id="a0bff-113">-CdnOriginGroup</span><span class="sxs-lookup"><span data-stu-id="a0bff-113">-CdnOriginGroup</span></span>
<span data-ttu-id="a0bff-114">CDN 원본 그룹 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="a0bff-114">The CDN origin group object.</span></span>

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

### <span data-ttu-id="a0bff-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a0bff-115">-DefaultProfile</span></span>
<span data-ttu-id="a0bff-116">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="a0bff-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a0bff-117">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="a0bff-117">-EndpointName</span></span>
<span data-ttu-id="a0bff-118">Azure CDN 엔드포인트 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="a0bff-118">Azure CDN endpoint name.</span></span>

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

### <span data-ttu-id="a0bff-119">-OriginGroupName</span><span class="sxs-lookup"><span data-stu-id="a0bff-119">-OriginGroupName</span></span>
<span data-ttu-id="a0bff-120">Azure CDN 원본 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="a0bff-120">Azure CDN origin group name.</span></span>

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

### <span data-ttu-id="a0bff-121">-OriginId</span><span class="sxs-lookup"><span data-stu-id="a0bff-121">-OriginId</span></span>
<span data-ttu-id="a0bff-122">Azure CDN 원본 그룹 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="a0bff-122">Azure CDN origin group ids.</span></span>

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

### <span data-ttu-id="a0bff-123">-ProbeIntervalInSeconds</span><span class="sxs-lookup"><span data-stu-id="a0bff-123">-ProbeIntervalInSeconds</span></span>
<span data-ttu-id="a0bff-124">상태 프로브 사이의 초 수입니다.</span><span class="sxs-lookup"><span data-stu-id="a0bff-124">The number of seconds between health probes.</span></span>

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

### <span data-ttu-id="a0bff-125">-ProbePath</span><span class="sxs-lookup"><span data-stu-id="a0bff-125">-ProbePath</span></span>
<span data-ttu-id="a0bff-126">원본의 상태 확인에 사용되는 원본을 상대로 하는 경로입니다.</span><span class="sxs-lookup"><span data-stu-id="a0bff-126">The path relative to the origin that is used to determine the health of the origin.</span></span>

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

### <span data-ttu-id="a0bff-127">-ProbeProtocol</span><span class="sxs-lookup"><span data-stu-id="a0bff-127">-ProbeProtocol</span></span>
<span data-ttu-id="a0bff-128">상태 프로브에 사용할 프로토콜입니다.</span><span class="sxs-lookup"><span data-stu-id="a0bff-128">Protocol to use for health probe.</span></span>

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

### <span data-ttu-id="a0bff-129">-ProbeRequestType</span><span class="sxs-lookup"><span data-stu-id="a0bff-129">-ProbeRequestType</span></span>
<span data-ttu-id="a0bff-130">만든 상태 프로브 요청의 형식입니다.</span><span class="sxs-lookup"><span data-stu-id="a0bff-130">The type of health probe request that is made.</span></span>

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

### <span data-ttu-id="a0bff-131">-ProfileName</span><span class="sxs-lookup"><span data-stu-id="a0bff-131">-ProfileName</span></span>
<span data-ttu-id="a0bff-132">Azure CDN 프로필 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="a0bff-132">Azure CDN profile name.</span></span>

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

### <span data-ttu-id="a0bff-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a0bff-133">-ResourceGroupName</span></span>
<span data-ttu-id="a0bff-134">Azure CDN 프로필의 리소스 그룹입니다.</span><span class="sxs-lookup"><span data-stu-id="a0bff-134">The resource group of the Azure CDN profile.</span></span>

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

### <span data-ttu-id="a0bff-135">-확인</span><span class="sxs-lookup"><span data-stu-id="a0bff-135">-Confirm</span></span>
<span data-ttu-id="a0bff-136">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="a0bff-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a0bff-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a0bff-137">-WhatIf</span></span>
<span data-ttu-id="a0bff-138">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="a0bff-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a0bff-139">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="a0bff-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a0bff-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a0bff-140">CommonParameters</span></span>
<span data-ttu-id="a0bff-141">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="a0bff-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a0bff-142">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="a0bff-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a0bff-143">입력</span><span class="sxs-lookup"><span data-stu-id="a0bff-143">INPUTS</span></span>

### <span data-ttu-id="a0bff-144">System.Object</span><span class="sxs-lookup"><span data-stu-id="a0bff-144">System.Object</span></span>

## <span data-ttu-id="a0bff-145">출력</span><span class="sxs-lookup"><span data-stu-id="a0bff-145">OUTPUTS</span></span>

### <span data-ttu-id="a0bff-146">System.Object</span><span class="sxs-lookup"><span data-stu-id="a0bff-146">System.Object</span></span>

## <span data-ttu-id="a0bff-147">참고 사항</span><span class="sxs-lookup"><span data-stu-id="a0bff-147">NOTES</span></span>

## <span data-ttu-id="a0bff-148">관련 링크</span><span class="sxs-lookup"><span data-stu-id="a0bff-148">RELATED LINKS</span></span>
