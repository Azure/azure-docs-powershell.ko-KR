---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
online version: https://docs.microsoft.com/en-us/powershell/module/az.cdn/remove-azcdnorigingroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Remove-AzCdnOriginGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Remove-AzCdnOriginGroup.md
ms.openlocfilehash: 081d5a73d6bd3cefff6f0c3bc57d3e0190f785a7
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94219095"
---
# <span data-ttu-id="101fe-101">Remove-AzCdnOriginGroup</span><span class="sxs-lookup"><span data-stu-id="101fe-101">Remove-AzCdnOriginGroup</span></span>

## <span data-ttu-id="101fe-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="101fe-102">SYNOPSIS</span></span>
<span data-ttu-id="101fe-103">CDN 원본 그룹을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="101fe-103">Removes a CDN origin group</span></span>

## <span data-ttu-id="101fe-104">구문과</span><span class="sxs-lookup"><span data-stu-id="101fe-104">SYNTAX</span></span>

### <span data-ttu-id="101fe-105">ByFieldsParameterSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="101fe-105">ByFieldsParameterSet (Default)</span></span>
```
Remove-AzCdnOriginGroup -OriginGroupName <String> -EndpointName <String> -ProfileName <String>
 -ResourceGroupName <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="101fe-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="101fe-106">ByResourceIdParameterSet</span></span>
```
Remove-AzCdnOriginGroup -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="101fe-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="101fe-107">ByObjectParameterSet</span></span>
```
Remove-AzCdnOriginGroup [-PassThru] -CdnOriginGroup <PSOriginGroup> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="101fe-108">설명은</span><span class="sxs-lookup"><span data-stu-id="101fe-108">DESCRIPTION</span></span>
<span data-ttu-id="101fe-109">Remove-AzCdnOriginGroup는 지정 된 끝점에서 CDN 원본 그룹을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="101fe-109">Remove-AzCdnOriginGroup will remove a CDN origin group from the specified endpoint.</span></span> 

## <span data-ttu-id="101fe-110">예제의</span><span class="sxs-lookup"><span data-stu-id="101fe-110">EXAMPLES</span></span>

### <span data-ttu-id="101fe-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="101fe-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzCdnOriginGroup -ResourceGroupName $resourceGroupName -ProfileName $profileName -EndpointName $endpointName -OriginGroupName $originGroupName
```

<span data-ttu-id="101fe-112">이 cmdlet은 지정 된 끝점에서 지정한 원본 그룹을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="101fe-112">This cmdlet will remove the specified origin group from the given endpoint.</span></span> 

## <span data-ttu-id="101fe-113">변수</span><span class="sxs-lookup"><span data-stu-id="101fe-113">PARAMETERS</span></span>

### <span data-ttu-id="101fe-114">-CdnOriginGroup</span><span class="sxs-lookup"><span data-stu-id="101fe-114">-CdnOriginGroup</span></span>
<span data-ttu-id="101fe-115">CDN 원본 그룹 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="101fe-115">The CDN origin group object.</span></span>

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

### <span data-ttu-id="101fe-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="101fe-116">-DefaultProfile</span></span>
<span data-ttu-id="101fe-117">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="101fe-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="101fe-118">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="101fe-118">-EndpointName</span></span>
<span data-ttu-id="101fe-119">Azure CDN 끝점 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="101fe-119">Azure CDN endpoint name.</span></span>

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

### <span data-ttu-id="101fe-120">-OriginGroupName</span><span class="sxs-lookup"><span data-stu-id="101fe-120">-OriginGroupName</span></span>
<span data-ttu-id="101fe-121">Azure CDN 원본 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="101fe-121">Azure CDN origin group name.</span></span>

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

### <span data-ttu-id="101fe-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="101fe-122">-PassThru</span></span>
<span data-ttu-id="101fe-123">지정 된 경우 object 반환</span><span class="sxs-lookup"><span data-stu-id="101fe-123">Return object if specified.</span></span>

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

### <span data-ttu-id="101fe-124">-/Profile</span><span class="sxs-lookup"><span data-stu-id="101fe-124">-ProfileName</span></span>
<span data-ttu-id="101fe-125">Azure CDN 프로필 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="101fe-125">Azure CDN profile name.</span></span>

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

### <span data-ttu-id="101fe-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="101fe-126">-ResourceGroupName</span></span>
<span data-ttu-id="101fe-127">Azure CDN 프로필의 리소스 그룹입니다.</span><span class="sxs-lookup"><span data-stu-id="101fe-127">The resource group of the Azure CDN profile.</span></span>

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

### <span data-ttu-id="101fe-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="101fe-128">-ResourceId</span></span>
<span data-ttu-id="101fe-129">Azure CDN 원본 그룹의 리소스 id입니다.</span><span class="sxs-lookup"><span data-stu-id="101fe-129">The resource id of the Azure CDN origin group.</span></span>

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

### <span data-ttu-id="101fe-130">-확인</span><span class="sxs-lookup"><span data-stu-id="101fe-130">-Confirm</span></span>
<span data-ttu-id="101fe-131">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="101fe-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="101fe-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="101fe-132">-WhatIf</span></span>
<span data-ttu-id="101fe-133">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="101fe-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="101fe-134">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="101fe-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="101fe-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="101fe-135">CommonParameters</span></span>
<span data-ttu-id="101fe-136">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="101fe-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="101fe-137">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="101fe-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="101fe-138">입력</span><span class="sxs-lookup"><span data-stu-id="101fe-138">INPUTS</span></span>

### <span data-ttu-id="101fe-139">않아야</span><span class="sxs-lookup"><span data-stu-id="101fe-139">None</span></span>

## <span data-ttu-id="101fe-140">출력</span><span class="sxs-lookup"><span data-stu-id="101fe-140">OUTPUTS</span></span>

### <span data-ttu-id="101fe-141">시스템 부울</span><span class="sxs-lookup"><span data-stu-id="101fe-141">System.Boolean</span></span>

## <span data-ttu-id="101fe-142">상속자</span><span class="sxs-lookup"><span data-stu-id="101fe-142">NOTES</span></span>

## <span data-ttu-id="101fe-143">관련 링크</span><span class="sxs-lookup"><span data-stu-id="101fe-143">RELATED LINKS</span></span>
