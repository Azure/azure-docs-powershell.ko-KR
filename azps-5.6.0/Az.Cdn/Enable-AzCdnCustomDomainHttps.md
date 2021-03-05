---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
online version: https://docs.microsoft.com/powershell/module/az.cdn/enable-azcdncustomdomainhttps
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Enable-AzCdnCustomDomainHttps.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Enable-AzCdnCustomDomainHttps.md
ms.openlocfilehash: 598dd0f386e82f7b195a57c72044756343ef9f56
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101972960"
---
# <span data-ttu-id="989f9-101">Enable-AzCdnCustomDomainHttps</span><span class="sxs-lookup"><span data-stu-id="989f9-101">Enable-AzCdnCustomDomainHttps</span></span>

## <span data-ttu-id="989f9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="989f9-102">SYNOPSIS</span></span>
<span data-ttu-id="989f9-103">사용자 지정 HTTPS를 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="989f9-103">Enables custom HTTPS.</span></span>

## <span data-ttu-id="989f9-104">구문</span><span class="sxs-lookup"><span data-stu-id="989f9-104">SYNTAX</span></span>

### <span data-ttu-id="989f9-105">ByFieldsParameterSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="989f9-105">ByFieldsParameterSet (Default)</span></span>
```
Enable-AzCdnCustomDomainHttps -ResourceGroupName <String> -ProfileName <String> -EndpointName <String>
 -CustomDomainName <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="989f9-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="989f9-106">ByObjectParameterSet</span></span>
```
Enable-AzCdnCustomDomainHttps -InputObject <PSCustomDomain> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="989f9-107">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="989f9-107">ByResourceIdParameterSet</span></span>
```
Enable-AzCdnCustomDomainHttps -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="989f9-108">설명</span><span class="sxs-lookup"><span data-stu-id="989f9-108">DESCRIPTION</span></span>
<span data-ttu-id="989f9-109">**Enable-AzCdnCustomDomainHttps** cmdlet을 사용하면 CDN 사용자 지정 도메인의 보안된 HTTPS 배달을 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="989f9-109">The **Enable-AzCdnCustomDomainHttps** cmdlet enables the secured HTTPS delivery of a CDN custom domain.</span></span>

## <span data-ttu-id="989f9-110">예제</span><span class="sxs-lookup"><span data-stu-id="989f9-110">EXAMPLES</span></span>

### <span data-ttu-id="989f9-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="989f9-111">Example 1</span></span>
```powershell
PS C:\> Enable-AzCdnCustomDomainHttps -ResourceGroupName $resourceGroupName -ProfileName $profileName -EndpointName $endpointName -CustomDomainName $customDomainName
```

<span data-ttu-id="989f9-112">사용자 지정 도메인의 안전한 배달을 사용하도록 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="989f9-112">Enable secure delivery of the custom domain.</span></span>

## <span data-ttu-id="989f9-113">매개 변수</span><span class="sxs-lookup"><span data-stu-id="989f9-113">PARAMETERS</span></span>

### <span data-ttu-id="989f9-114">-CustomDomainName</span><span class="sxs-lookup"><span data-stu-id="989f9-114">-CustomDomainName</span></span>
<span data-ttu-id="989f9-115">Azure CDN 사용자 지정 도메인 표시 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="989f9-115">Azure CDN custom domain display name.</span></span>

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

### <span data-ttu-id="989f9-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="989f9-116">-DefaultProfile</span></span>
<span data-ttu-id="989f9-117">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="989f9-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="989f9-118">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="989f9-118">-EndpointName</span></span>
<span data-ttu-id="989f9-119">Azure CDN 엔드포인트 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="989f9-119">Azure CDN endpoint name.</span></span>

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

### <span data-ttu-id="989f9-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="989f9-120">-InputObject</span></span>
<span data-ttu-id="989f9-121">사용자 지정 도메인 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="989f9-121">The custom domain object.</span></span>

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

### <span data-ttu-id="989f9-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="989f9-122">-PassThru</span></span>
<span data-ttu-id="989f9-123">지정된 경우 개체를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="989f9-123">Return object if specified.</span></span>

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

### <span data-ttu-id="989f9-124">-ProfileName</span><span class="sxs-lookup"><span data-stu-id="989f9-124">-ProfileName</span></span>
<span data-ttu-id="989f9-125">Azure CDN 프로필 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="989f9-125">Azure CDN profile name.</span></span>

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

### <span data-ttu-id="989f9-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="989f9-126">-ResourceGroupName</span></span>
<span data-ttu-id="989f9-127">Azure CDN 프로필의 리소스 그룹</span><span class="sxs-lookup"><span data-stu-id="989f9-127">The resource group of the Azure CDN profile</span></span>

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

### <span data-ttu-id="989f9-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="989f9-128">-ResourceId</span></span>
<span data-ttu-id="989f9-129">사용자 지정 도메인의 ResourceId</span><span class="sxs-lookup"><span data-stu-id="989f9-129">ResourceId of the Custom Domain</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="989f9-130">-확인</span><span class="sxs-lookup"><span data-stu-id="989f9-130">-Confirm</span></span>
<span data-ttu-id="989f9-131">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="989f9-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="989f9-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="989f9-132">-WhatIf</span></span>
<span data-ttu-id="989f9-133">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="989f9-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="989f9-134">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="989f9-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="989f9-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="989f9-135">CommonParameters</span></span>
<span data-ttu-id="989f9-136">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="989f9-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="989f9-137">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="989f9-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="989f9-138">입력</span><span class="sxs-lookup"><span data-stu-id="989f9-138">INPUTS</span></span>

### <span data-ttu-id="989f9-139">Microsoft.Azure.Commands.Cdn.Models.CustomDomain.PSCustomDomain</span><span class="sxs-lookup"><span data-stu-id="989f9-139">Microsoft.Azure.Commands.Cdn.Models.CustomDomain.PSCustomDomain</span></span>

### <span data-ttu-id="989f9-140">System.String</span><span class="sxs-lookup"><span data-stu-id="989f9-140">System.String</span></span>

## <span data-ttu-id="989f9-141">출력</span><span class="sxs-lookup"><span data-stu-id="989f9-141">OUTPUTS</span></span>

### <span data-ttu-id="989f9-142">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="989f9-142">System.Boolean</span></span>

## <span data-ttu-id="989f9-143">참고 사항</span><span class="sxs-lookup"><span data-stu-id="989f9-143">NOTES</span></span>

## <span data-ttu-id="989f9-144">관련 링크</span><span class="sxs-lookup"><span data-stu-id="989f9-144">RELATED LINKS</span></span>
