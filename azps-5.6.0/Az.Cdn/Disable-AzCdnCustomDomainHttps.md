---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
online version: https://docs.microsoft.com/powershell/module/az.cdn/disable-azcdncustomdomainhttps
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Disable-AzCdnCustomDomainHttps.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Disable-AzCdnCustomDomainHttps.md
ms.openlocfilehash: 837def99279905e3c647ecd8805ed0284840f5a4
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101978832"
---
# <span data-ttu-id="0145f-101">Disable-AzCdnCustomDomainHttps</span><span class="sxs-lookup"><span data-stu-id="0145f-101">Disable-AzCdnCustomDomainHttps</span></span>

## <span data-ttu-id="0145f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0145f-102">SYNOPSIS</span></span>
<span data-ttu-id="0145f-103">사용자 지정 도메인 HTTPS를 사용하지 않도록 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="0145f-103">Disables Custom Domain HTTPS.</span></span>

## <span data-ttu-id="0145f-104">구문</span><span class="sxs-lookup"><span data-stu-id="0145f-104">SYNTAX</span></span>

### <span data-ttu-id="0145f-105">ByFieldsParameterSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="0145f-105">ByFieldsParameterSet (Default)</span></span>
```
Disable-AzCdnCustomDomainHttps -ResourceGroupName <String> -ProfileName <String> -EndpointName <String>
 -CustomDomainName <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="0145f-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="0145f-106">ByObjectParameterSet</span></span>
```
Disable-AzCdnCustomDomainHttps -InputObject <PSCustomDomain> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0145f-107">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="0145f-107">ByResourceIdParameterSet</span></span>
```
Disable-AzCdnCustomDomainHttps -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0145f-108">설명</span><span class="sxs-lookup"><span data-stu-id="0145f-108">DESCRIPTION</span></span>
<span data-ttu-id="0145f-109">**Disable-AzCdnCustomDomainHttps** cmdlet은 CDN 사용자 지정 도메인의 보안 HTTPS 배달을 사용하지 않도록 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="0145f-109">The **Disable-AzCdnCustomDomainHttps** cmdlet disables the secured HTTPS delivery of a CDN custom domain.</span></span>

## <span data-ttu-id="0145f-110">예제</span><span class="sxs-lookup"><span data-stu-id="0145f-110">EXAMPLES</span></span>

### <span data-ttu-id="0145f-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="0145f-111">Example 1</span></span>
```powershell
PS C:\> Disable-AzCdnCustomDomainHttps -ResourceGroupName $resourceGroupName -ProfileName $profileName -EndpointName $endpointName -CustomDomainName $customDomainName
```

<span data-ttu-id="0145f-112">사용자 지정 도메인의 보안 배달을 사용하지 않도록 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="0145f-112">Disable secure delivery of the custom domain.</span></span>

## <span data-ttu-id="0145f-113">매개 변수</span><span class="sxs-lookup"><span data-stu-id="0145f-113">PARAMETERS</span></span>

### <span data-ttu-id="0145f-114">-CustomDomainName</span><span class="sxs-lookup"><span data-stu-id="0145f-114">-CustomDomainName</span></span>
<span data-ttu-id="0145f-115">Azure CDN 사용자 지정 도메인 표시 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="0145f-115">Azure CDN custom domain display name.</span></span>

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

### <span data-ttu-id="0145f-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0145f-116">-DefaultProfile</span></span>
<span data-ttu-id="0145f-117">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="0145f-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0145f-118">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="0145f-118">-EndpointName</span></span>
<span data-ttu-id="0145f-119">Azure CDN 엔드포인트 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="0145f-119">Azure CDN endpoint name.</span></span>

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

### <span data-ttu-id="0145f-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="0145f-120">-InputObject</span></span>
<span data-ttu-id="0145f-121">사용자 지정 도메인 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="0145f-121">The custom domain object.</span></span>

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

### <span data-ttu-id="0145f-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="0145f-122">-PassThru</span></span>
<span data-ttu-id="0145f-123">지정된 경우 개체를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="0145f-123">Return object if specified.</span></span>

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

### <span data-ttu-id="0145f-124">-ProfileName</span><span class="sxs-lookup"><span data-stu-id="0145f-124">-ProfileName</span></span>
<span data-ttu-id="0145f-125">Azure CDN 프로필 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="0145f-125">Azure CDN profile name.</span></span>

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

### <span data-ttu-id="0145f-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0145f-126">-ResourceGroupName</span></span>
<span data-ttu-id="0145f-127">Azure CDN 프로필의 리소스 그룹</span><span class="sxs-lookup"><span data-stu-id="0145f-127">The resource group of the Azure CDN profile</span></span>

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

### <span data-ttu-id="0145f-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="0145f-128">-ResourceId</span></span>
<span data-ttu-id="0145f-129">사용자 지정 도메인의 ResourceId</span><span class="sxs-lookup"><span data-stu-id="0145f-129">ResourceId of the Custom Domain</span></span>

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

### <span data-ttu-id="0145f-130">-확인</span><span class="sxs-lookup"><span data-stu-id="0145f-130">-Confirm</span></span>
<span data-ttu-id="0145f-131">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="0145f-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0145f-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0145f-132">-WhatIf</span></span>
<span data-ttu-id="0145f-133">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="0145f-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0145f-134">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="0145f-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0145f-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0145f-135">CommonParameters</span></span>
<span data-ttu-id="0145f-136">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="0145f-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0145f-137">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="0145f-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0145f-138">입력</span><span class="sxs-lookup"><span data-stu-id="0145f-138">INPUTS</span></span>

### <span data-ttu-id="0145f-139">Microsoft.Azure.Commands.Cdn.Models.CustomDomain.PSCustomDomain</span><span class="sxs-lookup"><span data-stu-id="0145f-139">Microsoft.Azure.Commands.Cdn.Models.CustomDomain.PSCustomDomain</span></span>

### <span data-ttu-id="0145f-140">System.String</span><span class="sxs-lookup"><span data-stu-id="0145f-140">System.String</span></span>

## <span data-ttu-id="0145f-141">출력</span><span class="sxs-lookup"><span data-stu-id="0145f-141">OUTPUTS</span></span>

### <span data-ttu-id="0145f-142">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="0145f-142">System.Boolean</span></span>

## <span data-ttu-id="0145f-143">참고 사항</span><span class="sxs-lookup"><span data-stu-id="0145f-143">NOTES</span></span>

## <span data-ttu-id="0145f-144">관련 링크</span><span class="sxs-lookup"><span data-stu-id="0145f-144">RELATED LINKS</span></span>
