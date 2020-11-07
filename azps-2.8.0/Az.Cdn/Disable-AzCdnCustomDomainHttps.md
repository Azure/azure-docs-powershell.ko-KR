---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
online version: https://docs.microsoft.com/en-us/powershell/module/az.cdn/disable-azcdncustomdomainhttps
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Disable-AzCdnCustomDomainHttps.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Disable-AzCdnCustomDomainHttps.md
ms.openlocfilehash: c3b2cadcdcc57ffc2cba8281af804e0c98c800bd
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93697618"
---
# <span data-ttu-id="0bd85-101">Disable-AzCdnCustomDomainHttps</span><span class="sxs-lookup"><span data-stu-id="0bd85-101">Disable-AzCdnCustomDomainHttps</span></span>

## <span data-ttu-id="0bd85-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0bd85-102">SYNOPSIS</span></span>
<span data-ttu-id="0bd85-103">사용자 지정 도메인 HTTPS를 사용 하지 않도록 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="0bd85-103">Disables Custom Domain HTTPS.</span></span>

## <span data-ttu-id="0bd85-104">구문과</span><span class="sxs-lookup"><span data-stu-id="0bd85-104">SYNTAX</span></span>

### <span data-ttu-id="0bd85-105">ByFieldsParameterSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="0bd85-105">ByFieldsParameterSet (Default)</span></span>
```
Disable-AzCdnCustomDomainHttps -ResourceGroupName <String> -ProfileName <String> -EndpointName <String>
 -CustomDomainName <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="0bd85-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="0bd85-106">ByObjectParameterSet</span></span>
```
Disable-AzCdnCustomDomainHttps -InputObject <PSCustomDomain> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0bd85-107">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="0bd85-107">ByResourceIdParameterSet</span></span>
```
Disable-AzCdnCustomDomainHttps -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0bd85-108">설명은</span><span class="sxs-lookup"><span data-stu-id="0bd85-108">DESCRIPTION</span></span>
<span data-ttu-id="0bd85-109">AzCdnCustomDomainHttps cmdlet을 **사용** 하면 CDN 사용자 지정 도메인의 보안 HTTPS 배달을 사용할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="0bd85-109">The **Disable-AzCdnCustomDomainHttps** cmdlet disables the secured HTTPS delivery of a CDN custom domain.</span></span>

## <span data-ttu-id="0bd85-110">예제의</span><span class="sxs-lookup"><span data-stu-id="0bd85-110">EXAMPLES</span></span>

### <span data-ttu-id="0bd85-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="0bd85-111">Example 1</span></span>
```powershell
PS C:\> Disable-AzCdnCustomDomainHttps -ResourceGroupName $resourceGroupName -ProfileName $profileName -EndpointName $endpointName -CustomDomainName $customDomainName
```

<span data-ttu-id="0bd85-112">사용자 지정 도메인의 보안 배달을 사용 하지 않도록 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="0bd85-112">Disable secure delivery of the custom domain.</span></span>

## <span data-ttu-id="0bd85-113">변수</span><span class="sxs-lookup"><span data-stu-id="0bd85-113">PARAMETERS</span></span>

### <span data-ttu-id="0bd85-114">-CustomDomainName</span><span class="sxs-lookup"><span data-stu-id="0bd85-114">-CustomDomainName</span></span>
<span data-ttu-id="0bd85-115">Azure CDN 사용자 지정 도메인 표시 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="0bd85-115">Azure CDN custom domain display name.</span></span>

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

### <span data-ttu-id="0bd85-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0bd85-116">-DefaultProfile</span></span>
<span data-ttu-id="0bd85-117">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="0bd85-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0bd85-118">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="0bd85-118">-EndpointName</span></span>
<span data-ttu-id="0bd85-119">Azure CDN 끝점 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="0bd85-119">Azure CDN endpoint name.</span></span>

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

### <span data-ttu-id="0bd85-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="0bd85-120">-InputObject</span></span>
<span data-ttu-id="0bd85-121">사용자 지정 도메인 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="0bd85-121">The custom domain object.</span></span>

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

### <span data-ttu-id="0bd85-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="0bd85-122">-PassThru</span></span>
<span data-ttu-id="0bd85-123">지정 된 경우 object 반환</span><span class="sxs-lookup"><span data-stu-id="0bd85-123">Return object if specified.</span></span>

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

### <span data-ttu-id="0bd85-124">-/Profile</span><span class="sxs-lookup"><span data-stu-id="0bd85-124">-ProfileName</span></span>
<span data-ttu-id="0bd85-125">Azure CDN 프로필 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="0bd85-125">Azure CDN profile name.</span></span>

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

### <span data-ttu-id="0bd85-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0bd85-126">-ResourceGroupName</span></span>
<span data-ttu-id="0bd85-127">Azure CDN 프로필의 리소스 그룹</span><span class="sxs-lookup"><span data-stu-id="0bd85-127">The resource group of the Azure CDN profile</span></span>

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

### <span data-ttu-id="0bd85-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="0bd85-128">-ResourceId</span></span>
<span data-ttu-id="0bd85-129">사용자 지정 도메인의 ResourceId</span><span class="sxs-lookup"><span data-stu-id="0bd85-129">ResourceId of the Custom Domain</span></span>

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

### <span data-ttu-id="0bd85-130">-확인</span><span class="sxs-lookup"><span data-stu-id="0bd85-130">-Confirm</span></span>
<span data-ttu-id="0bd85-131">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="0bd85-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0bd85-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0bd85-132">-WhatIf</span></span>
<span data-ttu-id="0bd85-133">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="0bd85-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0bd85-134">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="0bd85-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0bd85-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0bd85-135">CommonParameters</span></span>
<span data-ttu-id="0bd85-136">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="0bd85-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0bd85-137">자세한 내용은 [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="0bd85-137">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0bd85-138">입력</span><span class="sxs-lookup"><span data-stu-id="0bd85-138">INPUTS</span></span>

### <span data-ttu-id="0bd85-139">PSCustomDomain (.). c.</span><span class="sxs-lookup"><span data-stu-id="0bd85-139">Microsoft.Azure.Commands.Cdn.Models.CustomDomain.PSCustomDomain</span></span>

### <span data-ttu-id="0bd85-140">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="0bd85-140">System.String</span></span>

## <span data-ttu-id="0bd85-141">출력</span><span class="sxs-lookup"><span data-stu-id="0bd85-141">OUTPUTS</span></span>

### <span data-ttu-id="0bd85-142">시스템 부울</span><span class="sxs-lookup"><span data-stu-id="0bd85-142">System.Boolean</span></span>

## <span data-ttu-id="0bd85-143">상속자</span><span class="sxs-lookup"><span data-stu-id="0bd85-143">NOTES</span></span>

## <span data-ttu-id="0bd85-144">관련 링크</span><span class="sxs-lookup"><span data-stu-id="0bd85-144">RELATED LINKS</span></span>
