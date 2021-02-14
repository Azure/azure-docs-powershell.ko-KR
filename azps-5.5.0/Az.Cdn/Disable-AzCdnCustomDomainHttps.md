---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
online version: https://docs.microsoft.com/en-us/powershell/module/az.cdn/disable-azcdncustomdomainhttps
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Disable-AzCdnCustomDomainHttps.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Disable-AzCdnCustomDomainHttps.md
ms.openlocfilehash: be3e4d0437e24a282c1933cf82e1818dd9f88221
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100181881"
---
# <span data-ttu-id="d649c-101">Disable-AzCdnCustomDomainHttps</span><span class="sxs-lookup"><span data-stu-id="d649c-101">Disable-AzCdnCustomDomainHttps</span></span>

## <span data-ttu-id="d649c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d649c-102">SYNOPSIS</span></span>
<span data-ttu-id="d649c-103">사용자 지정 도메인 HTTPS를 사용하지 않도록 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="d649c-103">Disables Custom Domain HTTPS.</span></span>

## <span data-ttu-id="d649c-104">구문</span><span class="sxs-lookup"><span data-stu-id="d649c-104">SYNTAX</span></span>

### <span data-ttu-id="d649c-105">ByFieldsParameterSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="d649c-105">ByFieldsParameterSet (Default)</span></span>
```
Disable-AzCdnCustomDomainHttps -ResourceGroupName <String> -ProfileName <String> -EndpointName <String>
 -CustomDomainName <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="d649c-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="d649c-106">ByObjectParameterSet</span></span>
```
Disable-AzCdnCustomDomainHttps -InputObject <PSCustomDomain> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d649c-107">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="d649c-107">ByResourceIdParameterSet</span></span>
```
Disable-AzCdnCustomDomainHttps -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d649c-108">설명</span><span class="sxs-lookup"><span data-stu-id="d649c-108">DESCRIPTION</span></span>
<span data-ttu-id="d649c-109">**Disable-AzCdnCustomDomainHttps** cmdlet은 CDN 사용자 지정 도메인의 보안 HTTPS 배달을 비활성화합니다.</span><span class="sxs-lookup"><span data-stu-id="d649c-109">The **Disable-AzCdnCustomDomainHttps** cmdlet disables the secured HTTPS delivery of a CDN custom domain.</span></span>

## <span data-ttu-id="d649c-110">예제</span><span class="sxs-lookup"><span data-stu-id="d649c-110">EXAMPLES</span></span>

### <span data-ttu-id="d649c-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="d649c-111">Example 1</span></span>
```powershell
PS C:\> Disable-AzCdnCustomDomainHttps -ResourceGroupName $resourceGroupName -ProfileName $profileName -EndpointName $endpointName -CustomDomainName $customDomainName
```

<span data-ttu-id="d649c-112">사용자 지정 도메인의 보안 배달을 사용하지 않도록 설정</span><span class="sxs-lookup"><span data-stu-id="d649c-112">Disable secure delivery of the custom domain.</span></span>

## <span data-ttu-id="d649c-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d649c-113">PARAMETERS</span></span>

### <span data-ttu-id="d649c-114">-CustomDomainName</span><span class="sxs-lookup"><span data-stu-id="d649c-114">-CustomDomainName</span></span>
<span data-ttu-id="d649c-115">Azure CDN 사용자 지정 도메인 표시 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="d649c-115">Azure CDN custom domain display name.</span></span>

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

### <span data-ttu-id="d649c-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d649c-116">-DefaultProfile</span></span>
<span data-ttu-id="d649c-117">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="d649c-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d649c-118">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="d649c-118">-EndpointName</span></span>
<span data-ttu-id="d649c-119">Azure CDN 엔드포인트 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="d649c-119">Azure CDN endpoint name.</span></span>

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

### <span data-ttu-id="d649c-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d649c-120">-InputObject</span></span>
<span data-ttu-id="d649c-121">사용자 지정 도메인 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="d649c-121">The custom domain object.</span></span>

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

### <span data-ttu-id="d649c-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="d649c-122">-PassThru</span></span>
<span data-ttu-id="d649c-123">지정된 경우 개체를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="d649c-123">Return object if specified.</span></span>

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

### <span data-ttu-id="d649c-124">-ProfileName</span><span class="sxs-lookup"><span data-stu-id="d649c-124">-ProfileName</span></span>
<span data-ttu-id="d649c-125">Azure CDN 프로필 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="d649c-125">Azure CDN profile name.</span></span>

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

### <span data-ttu-id="d649c-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d649c-126">-ResourceGroupName</span></span>
<span data-ttu-id="d649c-127">Azure CDN 프로필의 리소스 그룹</span><span class="sxs-lookup"><span data-stu-id="d649c-127">The resource group of the Azure CDN profile</span></span>

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

### <span data-ttu-id="d649c-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="d649c-128">-ResourceId</span></span>
<span data-ttu-id="d649c-129">사용자 지정 도메인의 ResourceId</span><span class="sxs-lookup"><span data-stu-id="d649c-129">ResourceId of the Custom Domain</span></span>

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

### <span data-ttu-id="d649c-130">-Confirm</span><span class="sxs-lookup"><span data-stu-id="d649c-130">-Confirm</span></span>
<span data-ttu-id="d649c-131">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="d649c-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d649c-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d649c-132">-WhatIf</span></span>
<span data-ttu-id="d649c-133">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="d649c-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d649c-134">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="d649c-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d649c-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d649c-135">CommonParameters</span></span>
<span data-ttu-id="d649c-136">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="d649c-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d649c-137">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="d649c-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d649c-138">입력</span><span class="sxs-lookup"><span data-stu-id="d649c-138">INPUTS</span></span>

### <span data-ttu-id="d649c-139">Microsoft.Azure.Commands.Cdn.Models.CustomDomain.PSCustomDomain</span><span class="sxs-lookup"><span data-stu-id="d649c-139">Microsoft.Azure.Commands.Cdn.Models.CustomDomain.PSCustomDomain</span></span>

### <span data-ttu-id="d649c-140">System.String</span><span class="sxs-lookup"><span data-stu-id="d649c-140">System.String</span></span>

## <span data-ttu-id="d649c-141">출력</span><span class="sxs-lookup"><span data-stu-id="d649c-141">OUTPUTS</span></span>

### <span data-ttu-id="d649c-142">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="d649c-142">System.Boolean</span></span>

## <span data-ttu-id="d649c-143">참고 사항</span><span class="sxs-lookup"><span data-stu-id="d649c-143">NOTES</span></span>

## <span data-ttu-id="d649c-144">관련 링크</span><span class="sxs-lookup"><span data-stu-id="d649c-144">RELATED LINKS</span></span>
