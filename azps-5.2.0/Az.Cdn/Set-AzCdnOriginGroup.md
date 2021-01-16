---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
online version: https://docs.microsoft.com/en-us/powershell/module/az.cdn/set-azcdnorigingroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Set-AzCdnOriginGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Set-AzCdnOriginGroup.md
ms.openlocfilehash: 58a9d45c29a9a11b31bff510e6b4e1c63844dd5d
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98349034"
---
# <span data-ttu-id="7e622-101">Set-AzCdnOriginGroup</span><span class="sxs-lookup"><span data-stu-id="7e622-101">Set-AzCdnOriginGroup</span></span>

## <span data-ttu-id="7e622-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7e622-102">SYNOPSIS</span></span>
<span data-ttu-id="7e622-103">CDN 원본 그룹을 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="7e622-103">Updates the CDN origin group</span></span>

## <span data-ttu-id="7e622-104">구문</span><span class="sxs-lookup"><span data-stu-id="7e622-104">SYNTAX</span></span>

### <span data-ttu-id="7e622-105">ByFieldsParameterSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="7e622-105">ByFieldsParameterSet (Default)</span></span>
```
Set-AzCdnOriginGroup -EndpointName <String> -OriginGroupName <String>
 -OriginId <System.Collections.Generic.List`1[System.String]> [-ProbeIntervalInSeconds <Int32>]
 [-ProbePath <String>] [-ProbeProtocol <String>] [-ProbeRequestType <String>] -ProfileName <String>
 -ResourceGroupName <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="7e622-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="7e622-106">ByObjectParameterSet</span></span>
```
Set-AzCdnOriginGroup -CdnOriginGroup <PSOriginGroup> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7e622-107">설명</span><span class="sxs-lookup"><span data-stu-id="7e622-107">DESCRIPTION</span></span>
<span data-ttu-id="7e622-108">Set-AzCdnOriginGroup 엔드포인트 내에서 지정된 원본 그룹을 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="7e622-108">Set-AzCdnOriginGroup will update the specified origin group within the given endpoint.</span></span> 

## <span data-ttu-id="7e622-109">예제</span><span class="sxs-lookup"><span data-stu-id="7e622-109">EXAMPLES</span></span>

### <span data-ttu-id="7e622-110">예제 1</span><span class="sxs-lookup"><span data-stu-id="7e622-110">Example 1</span></span>
```powershell
PS C:\> Set-AzCdnOriginGroup -ResourceGroupName $resourceGroupName -ProfileName $profileName -EndpointName $endpointName -OriginGroupName $originGroupName -OriginId $originIds -ProbeIntervalInSeconds $probeInterval 
```
<span data-ttu-id="7e622-111">이 cmdlet은 원본 그룹의 ProbeIntervalInSeconds 속성을 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="7e622-111">This cmdlet will update the ProbeIntervalInSeconds property in the origin group.</span></span> 

## <span data-ttu-id="7e622-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="7e622-112">PARAMETERS</span></span>

### <span data-ttu-id="7e622-113">-CdnOriginGroup</span><span class="sxs-lookup"><span data-stu-id="7e622-113">-CdnOriginGroup</span></span>
<span data-ttu-id="7e622-114">CDN 원본 그룹 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="7e622-114">The CDN origin group object.</span></span>

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

### <span data-ttu-id="7e622-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7e622-115">-DefaultProfile</span></span>
<span data-ttu-id="7e622-116">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="7e622-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7e622-117">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="7e622-117">-EndpointName</span></span>
<span data-ttu-id="7e622-118">Azure CDN 엔드포인트 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="7e622-118">Azure CDN endpoint name.</span></span>

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

### <span data-ttu-id="7e622-119">-OriginGroupName</span><span class="sxs-lookup"><span data-stu-id="7e622-119">-OriginGroupName</span></span>
<span data-ttu-id="7e622-120">Azure CDN 원본 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="7e622-120">Azure CDN origin group name.</span></span>

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

### <span data-ttu-id="7e622-121">-OriginId</span><span class="sxs-lookup"><span data-stu-id="7e622-121">-OriginId</span></span>
<span data-ttu-id="7e622-122">Azure CDN 원본 그룹 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="7e622-122">Azure CDN origin group ids.</span></span>

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

### <span data-ttu-id="7e622-123">-ProbeIntervalInSeconds</span><span class="sxs-lookup"><span data-stu-id="7e622-123">-ProbeIntervalInSeconds</span></span>
<span data-ttu-id="7e622-124">상태 프로브 사이의 시간(초)입니다.</span><span class="sxs-lookup"><span data-stu-id="7e622-124">The number of seconds between health probes.</span></span>

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

### <span data-ttu-id="7e622-125">-ProbePath</span><span class="sxs-lookup"><span data-stu-id="7e622-125">-ProbePath</span></span>
<span data-ttu-id="7e622-126">원본의 상태 확인에 사용되는 원본에 대한 상대 경로입니다.</span><span class="sxs-lookup"><span data-stu-id="7e622-126">The path relative to the origin that is used to determine the health of the origin.</span></span>

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

### <span data-ttu-id="7e622-127">-ProbeProtocol</span><span class="sxs-lookup"><span data-stu-id="7e622-127">-ProbeProtocol</span></span>
<span data-ttu-id="7e622-128">상태 프로브에 사용할 프로토콜입니다.</span><span class="sxs-lookup"><span data-stu-id="7e622-128">Protocol to use for health probe.</span></span>

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

### <span data-ttu-id="7e622-129">-ProbeRequestType</span><span class="sxs-lookup"><span data-stu-id="7e622-129">-ProbeRequestType</span></span>
<span data-ttu-id="7e622-130">만들어진 상태 프로브 요청의 유형입니다.</span><span class="sxs-lookup"><span data-stu-id="7e622-130">The type of health probe request that is made.</span></span>

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

### <span data-ttu-id="7e622-131">-ProfileName</span><span class="sxs-lookup"><span data-stu-id="7e622-131">-ProfileName</span></span>
<span data-ttu-id="7e622-132">Azure CDN 프로필 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="7e622-132">Azure CDN profile name.</span></span>

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

### <span data-ttu-id="7e622-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7e622-133">-ResourceGroupName</span></span>
<span data-ttu-id="7e622-134">Azure CDN 프로필의 리소스 그룹입니다.</span><span class="sxs-lookup"><span data-stu-id="7e622-134">The resource group of the Azure CDN profile.</span></span>

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

### <span data-ttu-id="7e622-135">-Confirm</span><span class="sxs-lookup"><span data-stu-id="7e622-135">-Confirm</span></span>
<span data-ttu-id="7e622-136">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="7e622-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7e622-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7e622-137">-WhatIf</span></span>
<span data-ttu-id="7e622-138">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="7e622-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7e622-139">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="7e622-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7e622-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7e622-140">CommonParameters</span></span>
<span data-ttu-id="7e622-141">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="7e622-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7e622-142">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="7e622-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7e622-143">입력</span><span class="sxs-lookup"><span data-stu-id="7e622-143">INPUTS</span></span>

### <span data-ttu-id="7e622-144">System.Object</span><span class="sxs-lookup"><span data-stu-id="7e622-144">System.Object</span></span>

## <span data-ttu-id="7e622-145">출력</span><span class="sxs-lookup"><span data-stu-id="7e622-145">OUTPUTS</span></span>

### <span data-ttu-id="7e622-146">System.Object</span><span class="sxs-lookup"><span data-stu-id="7e622-146">System.Object</span></span>

## <span data-ttu-id="7e622-147">참고 사항</span><span class="sxs-lookup"><span data-stu-id="7e622-147">NOTES</span></span>

## <span data-ttu-id="7e622-148">관련 링크</span><span class="sxs-lookup"><span data-stu-id="7e622-148">RELATED LINKS</span></span>
