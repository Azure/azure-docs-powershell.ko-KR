---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
online version: https://docs.microsoft.com/en-us/powershell/module/az.cdn/new-azcdnorigingroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/New-AzCdnOriginGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/New-AzCdnOriginGroup.md
ms.openlocfilehash: 9c499fe716df97edc4644729dc996bd4f9bae992
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94216263"
---
# <span data-ttu-id="a7c77-101">New-AzCdnOriginGroup</span><span class="sxs-lookup"><span data-stu-id="a7c77-101">New-AzCdnOriginGroup</span></span>

## <span data-ttu-id="a7c77-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a7c77-102">SYNOPSIS</span></span>
<span data-ttu-id="a7c77-103">새 CDN 원본 그룹을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="a7c77-103">Creates a new CDN origin group</span></span>

## <span data-ttu-id="a7c77-104">구문과</span><span class="sxs-lookup"><span data-stu-id="a7c77-104">SYNTAX</span></span>

### <span data-ttu-id="a7c77-105">ByFieldsParameterSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="a7c77-105">ByFieldsParameterSet (Default)</span></span>
```
New-AzCdnOriginGroup -EndpointName <String> -OriginGroupName <String>
 -OriginId <System.Collections.Generic.List`1[System.String]> [-ProbeIntervalInSeconds <Int32>]
 [-ProbePath <String>] [-ProbeProtocol <String>] [-ProbeRequestType <String>] -ProfileName <String>
 -ResourceGroupName <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="a7c77-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="a7c77-106">ByObjectParameterSet</span></span>
```
New-AzCdnOriginGroup -CdnOriginGroup <PSOriginGroup> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a7c77-107">설명은</span><span class="sxs-lookup"><span data-stu-id="a7c77-107">DESCRIPTION</span></span>
<span data-ttu-id="a7c77-108">New-AzCdnOriginGroup에서는 지정 된 끝점 내에 새 원본 그룹을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="a7c77-108">The New-AzCdnOriginGroup will create a new origin group within the specified endpoint.</span></span> <span data-ttu-id="a7c77-109">끝점의 첫 번째 원본 그룹인 경우 DefaultOriginGroup 속성도 설정 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="a7c77-109">If this is the first origin group for endpoint, then the DefaultOriginGroup property must also be set.</span></span>

## <span data-ttu-id="a7c77-110">예제의</span><span class="sxs-lookup"><span data-stu-id="a7c77-110">EXAMPLES</span></span>

### <span data-ttu-id="a7c77-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="a7c77-111">Example 1</span></span>
```powershell
PS C:\> New-AzCdnOriginGroup -ResourceGroupName $resourceGroupName -ProfileName $profileName -EndpointName $endpointName -OriginGroupName $originGroupName -OriginId $originId
```
<span data-ttu-id="a7c77-112">이 cmdlet은 지정 된 끝점 내에 새 근원 그룹을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="a7c77-112">This cmdlet will create a new origin group within the specified endpoint.</span></span> <span data-ttu-id="a7c77-113">지정 된 출처 id를 원본 집합으로 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="a7c77-113">It will utilize the given origin ids as the set of origins.</span></span>

## <span data-ttu-id="a7c77-114">변수</span><span class="sxs-lookup"><span data-stu-id="a7c77-114">PARAMETERS</span></span>

### <span data-ttu-id="a7c77-115">-CdnOriginGroup</span><span class="sxs-lookup"><span data-stu-id="a7c77-115">-CdnOriginGroup</span></span>
<span data-ttu-id="a7c77-116">CDN 원본 그룹 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="a7c77-116">The CDN origin group object.</span></span>

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

### <span data-ttu-id="a7c77-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a7c77-117">-DefaultProfile</span></span>
<span data-ttu-id="a7c77-118">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="a7c77-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a7c77-119">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="a7c77-119">-EndpointName</span></span>
<span data-ttu-id="a7c77-120">Azure CDN 끝점 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="a7c77-120">Azure CDN endpoint name.</span></span>

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

### <span data-ttu-id="a7c77-121">-OriginGroupName</span><span class="sxs-lookup"><span data-stu-id="a7c77-121">-OriginGroupName</span></span>
<span data-ttu-id="a7c77-122">Azure CDN 원본 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="a7c77-122">Azure CDN origin group name.</span></span>

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

### <span data-ttu-id="a7c77-123">-OriginId</span><span class="sxs-lookup"><span data-stu-id="a7c77-123">-OriginId</span></span>
<span data-ttu-id="a7c77-124">Azure CDN 원본 그룹 id입니다.</span><span class="sxs-lookup"><span data-stu-id="a7c77-124">Azure CDN origin group ids.</span></span>

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

### <span data-ttu-id="a7c77-125">-ProbeIntervalInSeconds</span><span class="sxs-lookup"><span data-stu-id="a7c77-125">-ProbeIntervalInSeconds</span></span>
<span data-ttu-id="a7c77-126">상태 프로브 사이의 초 수입니다.</span><span class="sxs-lookup"><span data-stu-id="a7c77-126">The number of seconds between health probes.</span></span>

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

### <span data-ttu-id="a7c77-127">-ProbePath</span><span class="sxs-lookup"><span data-stu-id="a7c77-127">-ProbePath</span></span>
<span data-ttu-id="a7c77-128">원점의 상태를 확인 하는 데 사용 되는 원점을 기준으로 하는 경로입니다.</span><span class="sxs-lookup"><span data-stu-id="a7c77-128">The path relative to the origin that is used to determine the health of the origin.</span></span>

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

### <span data-ttu-id="a7c77-129">-ProbeProtocol</span><span class="sxs-lookup"><span data-stu-id="a7c77-129">-ProbeProtocol</span></span>
<span data-ttu-id="a7c77-130">상태 프로브에 사용 하는 프로토콜입니다.</span><span class="sxs-lookup"><span data-stu-id="a7c77-130">Protocol to use for health probe.</span></span>

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

### <span data-ttu-id="a7c77-131">-ProbeRequestType</span><span class="sxs-lookup"><span data-stu-id="a7c77-131">-ProbeRequestType</span></span>
<span data-ttu-id="a7c77-132">적용 되는 상태 프로브 요청의 유형입니다.</span><span class="sxs-lookup"><span data-stu-id="a7c77-132">The type of health probe request that is made.</span></span>

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

### <span data-ttu-id="a7c77-133">-/Profile</span><span class="sxs-lookup"><span data-stu-id="a7c77-133">-ProfileName</span></span>
<span data-ttu-id="a7c77-134">Azure CDN 프로필 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="a7c77-134">Azure CDN profile name.</span></span>

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

### <span data-ttu-id="a7c77-135">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a7c77-135">-ResourceGroupName</span></span>
<span data-ttu-id="a7c77-136">Azure CDN 프로필의 리소스 그룹입니다.</span><span class="sxs-lookup"><span data-stu-id="a7c77-136">The resource group of the Azure CDN profile.</span></span>

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

### <span data-ttu-id="a7c77-137">-확인</span><span class="sxs-lookup"><span data-stu-id="a7c77-137">-Confirm</span></span>
<span data-ttu-id="a7c77-138">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="a7c77-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a7c77-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a7c77-139">-WhatIf</span></span>
<span data-ttu-id="a7c77-140">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="a7c77-140">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="a7c77-141">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="a7c77-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a7c77-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a7c77-142">CommonParameters</span></span>
<span data-ttu-id="a7c77-143">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="a7c77-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a7c77-144">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="a7c77-144">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a7c77-145">입력</span><span class="sxs-lookup"><span data-stu-id="a7c77-145">INPUTS</span></span>

### <span data-ttu-id="a7c77-146">System. 개체</span><span class="sxs-lookup"><span data-stu-id="a7c77-146">System.Object</span></span>

## <span data-ttu-id="a7c77-147">출력</span><span class="sxs-lookup"><span data-stu-id="a7c77-147">OUTPUTS</span></span>

### <span data-ttu-id="a7c77-148">System. 개체</span><span class="sxs-lookup"><span data-stu-id="a7c77-148">System.Object</span></span>

## <span data-ttu-id="a7c77-149">상속자</span><span class="sxs-lookup"><span data-stu-id="a7c77-149">NOTES</span></span>

## <span data-ttu-id="a7c77-150">관련 링크</span><span class="sxs-lookup"><span data-stu-id="a7c77-150">RELATED LINKS</span></span>
