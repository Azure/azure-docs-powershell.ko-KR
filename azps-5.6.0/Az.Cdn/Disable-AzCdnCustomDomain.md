---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
online version: https://docs.microsoft.com/powershell/module/az.cdn/disable-azcdncustomdomain
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Disable-AzCdnCustomDomain.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Disable-AzCdnCustomDomain.md
ms.openlocfilehash: 21914b5420d25a42b7670756fe34f18c17db9023
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "102007248"
---
# <span data-ttu-id="d4fdc-101">Disable-AzCdnCustomDomain</span><span class="sxs-lookup"><span data-stu-id="d4fdc-101">Disable-AzCdnCustomDomain</span></span>

## <span data-ttu-id="d4fdc-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d4fdc-102">SYNOPSIS</span></span>
<span data-ttu-id="d4fdc-103">사용자 지정 도메인 HTTPS를 사용하지 않도록 설정(사용되지 않습니다).</span><span class="sxs-lookup"><span data-stu-id="d4fdc-103">Disables Custom Domain HTTPS (Deprecated).</span></span>

## <span data-ttu-id="d4fdc-104">구문</span><span class="sxs-lookup"><span data-stu-id="d4fdc-104">SYNTAX</span></span>

### <span data-ttu-id="d4fdc-105">ByFieldsParameterSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="d4fdc-105">ByFieldsParameterSet (Default)</span></span>
```
Disable-AzCdnCustomDomain -CustomDomainName <String> -EndpointName <String> -ProfileName <String>
 -ResourceGroupName <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="d4fdc-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="d4fdc-106">ByObjectParameterSet</span></span>
```
Disable-AzCdnCustomDomain -InputObject <PSCustomDomain> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d4fdc-107">설명</span><span class="sxs-lookup"><span data-stu-id="d4fdc-107">DESCRIPTION</span></span>
<span data-ttu-id="d4fdc-108">**Disable-AzCdnCustomDomain** cmdlet은 CDN 사용자 지정 도메인의 보안 HTTPS 배달을 사용하지 않도록 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="d4fdc-108">The **Disable-AzCdnCustomDomain** cmdlet disables the secured HTTPS delivery of a CDN custom domain.</span></span>

## <span data-ttu-id="d4fdc-109">예제</span><span class="sxs-lookup"><span data-stu-id="d4fdc-109">EXAMPLES</span></span>

### <span data-ttu-id="d4fdc-110">예제 1</span><span class="sxs-lookup"><span data-stu-id="d4fdc-110">Example 1</span></span>
```powershell
Disable-AzCdnCustomDomain -CustomDomainName $customDomainName -EndpointName $endpointName -ProfileName $profileName -ResourceGroupName $resourceGroupName
true
```

<span data-ttu-id="d4fdc-111">사용자 지정 도메인의 https 배달을 사용하지 않도록 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="d4fdc-111">Disable https delivery of the custom domain.</span></span>

## <span data-ttu-id="d4fdc-112">매개 변수</span><span class="sxs-lookup"><span data-stu-id="d4fdc-112">PARAMETERS</span></span>

### <span data-ttu-id="d4fdc-113">-CustomDomainName</span><span class="sxs-lookup"><span data-stu-id="d4fdc-113">-CustomDomainName</span></span>
<span data-ttu-id="d4fdc-114">Azure CDN 사용자 지정 도메인 표시 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="d4fdc-114">Azure CDN custom domain display name.</span></span>

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

### <span data-ttu-id="d4fdc-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d4fdc-115">-DefaultProfile</span></span>
<span data-ttu-id="d4fdc-116">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="d4fdc-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d4fdc-117">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="d4fdc-117">-EndpointName</span></span>
<span data-ttu-id="d4fdc-118">Azure CDN 엔드포인트 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="d4fdc-118">Azure CDN endpoint name.</span></span>

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

### <span data-ttu-id="d4fdc-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d4fdc-119">-InputObject</span></span>
<span data-ttu-id="d4fdc-120">사용자 지정 도메인 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="d4fdc-120">The custom domain object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Cdn.Models.CustomDomain.PSCustomDomain
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d4fdc-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="d4fdc-121">-PassThru</span></span>
<span data-ttu-id="d4fdc-122">개체를 반환합니다(지정된 경우).</span><span class="sxs-lookup"><span data-stu-id="d4fdc-122">Return object (if specified).</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d4fdc-123">-ProfileName</span><span class="sxs-lookup"><span data-stu-id="d4fdc-123">-ProfileName</span></span>
<span data-ttu-id="d4fdc-124">Azure CDN 프로필 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="d4fdc-124">Azure CDN profile name.</span></span>

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

### <span data-ttu-id="d4fdc-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d4fdc-125">-ResourceGroupName</span></span>
<span data-ttu-id="d4fdc-126">Azure CDN 프로필의 리소스 그룹입니다.</span><span class="sxs-lookup"><span data-stu-id="d4fdc-126">The resource group of the Azure CDN profile.</span></span>

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

### <span data-ttu-id="d4fdc-127">-확인</span><span class="sxs-lookup"><span data-stu-id="d4fdc-127">-Confirm</span></span>
<span data-ttu-id="d4fdc-128">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="d4fdc-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d4fdc-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d4fdc-129">-WhatIf</span></span>
<span data-ttu-id="d4fdc-130">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="d4fdc-130">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="d4fdc-131">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="d4fdc-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d4fdc-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d4fdc-132">CommonParameters</span></span>
<span data-ttu-id="d4fdc-133">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="d4fdc-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d4fdc-134">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="d4fdc-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d4fdc-135">입력</span><span class="sxs-lookup"><span data-stu-id="d4fdc-135">INPUTS</span></span>

### <span data-ttu-id="d4fdc-136">Microsoft.Azure.Commands.Cdn.Models.CustomDomain.PSCustomDomain</span><span class="sxs-lookup"><span data-stu-id="d4fdc-136">Microsoft.Azure.Commands.Cdn.Models.CustomDomain.PSCustomDomain</span></span>

## <span data-ttu-id="d4fdc-137">출력</span><span class="sxs-lookup"><span data-stu-id="d4fdc-137">OUTPUTS</span></span>

### <span data-ttu-id="d4fdc-138">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="d4fdc-138">System.Boolean</span></span>

## <span data-ttu-id="d4fdc-139">참고 사항</span><span class="sxs-lookup"><span data-stu-id="d4fdc-139">NOTES</span></span>

## <span data-ttu-id="d4fdc-140">관련 링크</span><span class="sxs-lookup"><span data-stu-id="d4fdc-140">RELATED LINKS</span></span>
