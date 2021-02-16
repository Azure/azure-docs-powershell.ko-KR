---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
online version: https://docs.microsoft.com/en-us/powershell/module/az.cdn/disable-azcdncustomdomain
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Disable-AzCdnCustomDomain.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Disable-AzCdnCustomDomain.md
ms.openlocfilehash: 3352991d73bcef2e4f5b6475c9c71d5f48eaa526
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100200833"
---
# <span data-ttu-id="f3c67-101">Disable-AzCdnCustomDomain</span><span class="sxs-lookup"><span data-stu-id="f3c67-101">Disable-AzCdnCustomDomain</span></span>

## <span data-ttu-id="f3c67-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f3c67-102">SYNOPSIS</span></span>
<span data-ttu-id="f3c67-103">사용자 지정 도메인 HTTPS를 사용하지 않도록 설정(사용되지 않습니다.)</span><span class="sxs-lookup"><span data-stu-id="f3c67-103">Disables Custom Domain HTTPS (Deprecated).</span></span>

## <span data-ttu-id="f3c67-104">구문</span><span class="sxs-lookup"><span data-stu-id="f3c67-104">SYNTAX</span></span>

### <span data-ttu-id="f3c67-105">ByFieldsParameterSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="f3c67-105">ByFieldsParameterSet (Default)</span></span>
```
Disable-AzCdnCustomDomain -CustomDomainName <String> -EndpointName <String> -ProfileName <String>
 -ResourceGroupName <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="f3c67-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="f3c67-106">ByObjectParameterSet</span></span>
```
Disable-AzCdnCustomDomain -InputObject <PSCustomDomain> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f3c67-107">설명</span><span class="sxs-lookup"><span data-stu-id="f3c67-107">DESCRIPTION</span></span>
<span data-ttu-id="f3c67-108">**Disable-AzCdnCustomDomain** cmdlet은 CDN 사용자 지정 도메인의 보안 HTTPS 배달을 비활성화합니다.</span><span class="sxs-lookup"><span data-stu-id="f3c67-108">The **Disable-AzCdnCustomDomain** cmdlet disables the secured HTTPS delivery of a CDN custom domain.</span></span>

## <span data-ttu-id="f3c67-109">예제</span><span class="sxs-lookup"><span data-stu-id="f3c67-109">EXAMPLES</span></span>

### <span data-ttu-id="f3c67-110">예제 1</span><span class="sxs-lookup"><span data-stu-id="f3c67-110">Example 1</span></span>
```powershell
Disable-AzCdnCustomDomain -CustomDomainName $customDomainName -EndpointName $endpointName -ProfileName $profileName -ResourceGroupName $resourceGroupName
true
```

<span data-ttu-id="f3c67-111">사용자 지정 도메인의 https 배달을 사용하지 않도록 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="f3c67-111">Disable https delivery of the custom domain.</span></span>

## <span data-ttu-id="f3c67-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f3c67-112">PARAMETERS</span></span>

### <span data-ttu-id="f3c67-113">-CustomDomainName</span><span class="sxs-lookup"><span data-stu-id="f3c67-113">-CustomDomainName</span></span>
<span data-ttu-id="f3c67-114">Azure CDN 사용자 지정 도메인 표시 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="f3c67-114">Azure CDN custom domain display name.</span></span>

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

### <span data-ttu-id="f3c67-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f3c67-115">-DefaultProfile</span></span>
<span data-ttu-id="f3c67-116">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="f3c67-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f3c67-117">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="f3c67-117">-EndpointName</span></span>
<span data-ttu-id="f3c67-118">Azure CDN 엔드포인트 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="f3c67-118">Azure CDN endpoint name.</span></span>

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

### <span data-ttu-id="f3c67-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="f3c67-119">-InputObject</span></span>
<span data-ttu-id="f3c67-120">사용자 지정 도메인 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="f3c67-120">The custom domain object.</span></span>

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

### <span data-ttu-id="f3c67-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="f3c67-121">-PassThru</span></span>
<span data-ttu-id="f3c67-122">개체를 반환합니다(지정된 경우).</span><span class="sxs-lookup"><span data-stu-id="f3c67-122">Return object (if specified).</span></span>

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

### <span data-ttu-id="f3c67-123">-ProfileName</span><span class="sxs-lookup"><span data-stu-id="f3c67-123">-ProfileName</span></span>
<span data-ttu-id="f3c67-124">Azure CDN 프로필 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="f3c67-124">Azure CDN profile name.</span></span>

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

### <span data-ttu-id="f3c67-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f3c67-125">-ResourceGroupName</span></span>
<span data-ttu-id="f3c67-126">Azure CDN 프로필의 리소스 그룹입니다.</span><span class="sxs-lookup"><span data-stu-id="f3c67-126">The resource group of the Azure CDN profile.</span></span>

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

### <span data-ttu-id="f3c67-127">-Confirm</span><span class="sxs-lookup"><span data-stu-id="f3c67-127">-Confirm</span></span>
<span data-ttu-id="f3c67-128">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="f3c67-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f3c67-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f3c67-129">-WhatIf</span></span>
<span data-ttu-id="f3c67-130">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="f3c67-130">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="f3c67-131">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="f3c67-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f3c67-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f3c67-132">CommonParameters</span></span>
<span data-ttu-id="f3c67-133">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="f3c67-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f3c67-134">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="f3c67-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f3c67-135">입력</span><span class="sxs-lookup"><span data-stu-id="f3c67-135">INPUTS</span></span>

### <span data-ttu-id="f3c67-136">Microsoft.Azure.Commands.Cdn.Models.CustomDomain.PSCustomDomain</span><span class="sxs-lookup"><span data-stu-id="f3c67-136">Microsoft.Azure.Commands.Cdn.Models.CustomDomain.PSCustomDomain</span></span>

## <span data-ttu-id="f3c67-137">출력</span><span class="sxs-lookup"><span data-stu-id="f3c67-137">OUTPUTS</span></span>

### <span data-ttu-id="f3c67-138">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="f3c67-138">System.Boolean</span></span>

## <span data-ttu-id="f3c67-139">참고 사항</span><span class="sxs-lookup"><span data-stu-id="f3c67-139">NOTES</span></span>

## <span data-ttu-id="f3c67-140">관련 링크</span><span class="sxs-lookup"><span data-stu-id="f3c67-140">RELATED LINKS</span></span>
