---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
online version: https://docs.microsoft.com/en-us/powershell/module/az.cdn/set-azcdnorigingroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Set-AzCdnOriginGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Set-AzCdnOriginGroup.md
ms.openlocfilehash: 58a9d45c29a9a11b31bff510e6b4e1c63844dd5d
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94217639"
---
# <span data-ttu-id="26625-101">Set-AzCdnOriginGroup</span><span class="sxs-lookup"><span data-stu-id="26625-101">Set-AzCdnOriginGroup</span></span>

## <span data-ttu-id="26625-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="26625-102">SYNOPSIS</span></span>
<span data-ttu-id="26625-103">CDN 원본 그룹을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="26625-103">Updates the CDN origin group</span></span>

## <span data-ttu-id="26625-104">구문과</span><span class="sxs-lookup"><span data-stu-id="26625-104">SYNTAX</span></span>

### <span data-ttu-id="26625-105">ByFieldsParameterSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="26625-105">ByFieldsParameterSet (Default)</span></span>
```
Set-AzCdnOriginGroup -EndpointName <String> -OriginGroupName <String>
 -OriginId <System.Collections.Generic.List`1[System.String]> [-ProbeIntervalInSeconds <Int32>]
 [-ProbePath <String>] [-ProbeProtocol <String>] [-ProbeRequestType <String>] -ProfileName <String>
 -ResourceGroupName <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="26625-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="26625-106">ByObjectParameterSet</span></span>
```
Set-AzCdnOriginGroup -CdnOriginGroup <PSOriginGroup> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="26625-107">설명은</span><span class="sxs-lookup"><span data-stu-id="26625-107">DESCRIPTION</span></span>
<span data-ttu-id="26625-108">Set-AzCdnOriginGroup은 지정 된 끝점 내에서 지정 된 원본 그룹을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="26625-108">Set-AzCdnOriginGroup will update the specified origin group within the given endpoint.</span></span> 

## <span data-ttu-id="26625-109">예제의</span><span class="sxs-lookup"><span data-stu-id="26625-109">EXAMPLES</span></span>

### <span data-ttu-id="26625-110">예제 1</span><span class="sxs-lookup"><span data-stu-id="26625-110">Example 1</span></span>
```powershell
PS C:\> Set-AzCdnOriginGroup -ResourceGroupName $resourceGroupName -ProfileName $profileName -EndpointName $endpointName -OriginGroupName $originGroupName -OriginId $originIds -ProbeIntervalInSeconds $probeInterval 
```
<span data-ttu-id="26625-111">이 cmdlet은 원본 그룹의 ProbeIntervalInSeconds 속성을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="26625-111">This cmdlet will update the ProbeIntervalInSeconds property in the origin group.</span></span> 

## <span data-ttu-id="26625-112">변수</span><span class="sxs-lookup"><span data-stu-id="26625-112">PARAMETERS</span></span>

### <span data-ttu-id="26625-113">-CdnOriginGroup</span><span class="sxs-lookup"><span data-stu-id="26625-113">-CdnOriginGroup</span></span>
<span data-ttu-id="26625-114">CDN 원본 그룹 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="26625-114">The CDN origin group object.</span></span>

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

### <span data-ttu-id="26625-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="26625-115">-DefaultProfile</span></span>
<span data-ttu-id="26625-116">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="26625-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="26625-117">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="26625-117">-EndpointName</span></span>
<span data-ttu-id="26625-118">Azure CDN 끝점 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="26625-118">Azure CDN endpoint name.</span></span>

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

### <span data-ttu-id="26625-119">-OriginGroupName</span><span class="sxs-lookup"><span data-stu-id="26625-119">-OriginGroupName</span></span>
<span data-ttu-id="26625-120">Azure CDN 원본 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="26625-120">Azure CDN origin group name.</span></span>

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

### <span data-ttu-id="26625-121">-OriginId</span><span class="sxs-lookup"><span data-stu-id="26625-121">-OriginId</span></span>
<span data-ttu-id="26625-122">Azure CDN 원본 그룹 id입니다.</span><span class="sxs-lookup"><span data-stu-id="26625-122">Azure CDN origin group ids.</span></span>

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

### <span data-ttu-id="26625-123">-ProbeIntervalInSeconds</span><span class="sxs-lookup"><span data-stu-id="26625-123">-ProbeIntervalInSeconds</span></span>
<span data-ttu-id="26625-124">상태 프로브 사이의 초 수입니다.</span><span class="sxs-lookup"><span data-stu-id="26625-124">The number of seconds between health probes.</span></span>

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

### <span data-ttu-id="26625-125">-ProbePath</span><span class="sxs-lookup"><span data-stu-id="26625-125">-ProbePath</span></span>
<span data-ttu-id="26625-126">원점의 상태를 확인 하는 데 사용 되는 원점을 기준으로 하는 경로입니다.</span><span class="sxs-lookup"><span data-stu-id="26625-126">The path relative to the origin that is used to determine the health of the origin.</span></span>

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

### <span data-ttu-id="26625-127">-ProbeProtocol</span><span class="sxs-lookup"><span data-stu-id="26625-127">-ProbeProtocol</span></span>
<span data-ttu-id="26625-128">상태 프로브에 사용 하는 프로토콜입니다.</span><span class="sxs-lookup"><span data-stu-id="26625-128">Protocol to use for health probe.</span></span>

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

### <span data-ttu-id="26625-129">-ProbeRequestType</span><span class="sxs-lookup"><span data-stu-id="26625-129">-ProbeRequestType</span></span>
<span data-ttu-id="26625-130">적용 되는 상태 프로브 요청의 유형입니다.</span><span class="sxs-lookup"><span data-stu-id="26625-130">The type of health probe request that is made.</span></span>

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

### <span data-ttu-id="26625-131">-/Profile</span><span class="sxs-lookup"><span data-stu-id="26625-131">-ProfileName</span></span>
<span data-ttu-id="26625-132">Azure CDN 프로필 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="26625-132">Azure CDN profile name.</span></span>

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

### <span data-ttu-id="26625-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="26625-133">-ResourceGroupName</span></span>
<span data-ttu-id="26625-134">Azure CDN 프로필의 리소스 그룹입니다.</span><span class="sxs-lookup"><span data-stu-id="26625-134">The resource group of the Azure CDN profile.</span></span>

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

### <span data-ttu-id="26625-135">-확인</span><span class="sxs-lookup"><span data-stu-id="26625-135">-Confirm</span></span>
<span data-ttu-id="26625-136">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="26625-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="26625-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="26625-137">-WhatIf</span></span>
<span data-ttu-id="26625-138">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="26625-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="26625-139">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="26625-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="26625-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="26625-140">CommonParameters</span></span>
<span data-ttu-id="26625-141">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="26625-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="26625-142">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="26625-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="26625-143">입력</span><span class="sxs-lookup"><span data-stu-id="26625-143">INPUTS</span></span>

### <span data-ttu-id="26625-144">System. 개체</span><span class="sxs-lookup"><span data-stu-id="26625-144">System.Object</span></span>

## <span data-ttu-id="26625-145">출력</span><span class="sxs-lookup"><span data-stu-id="26625-145">OUTPUTS</span></span>

### <span data-ttu-id="26625-146">System. 개체</span><span class="sxs-lookup"><span data-stu-id="26625-146">System.Object</span></span>

## <span data-ttu-id="26625-147">상속자</span><span class="sxs-lookup"><span data-stu-id="26625-147">NOTES</span></span>

## <span data-ttu-id="26625-148">관련 링크</span><span class="sxs-lookup"><span data-stu-id="26625-148">RELATED LINKS</span></span>
