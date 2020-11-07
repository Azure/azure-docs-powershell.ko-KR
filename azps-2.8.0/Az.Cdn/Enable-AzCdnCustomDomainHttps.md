---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
online version: https://docs.microsoft.com/en-us/powershell/module/az.cdn/enable-azcdncustomdomainhttps
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Enable-AzCdnCustomDomainHttps.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Enable-AzCdnCustomDomainHttps.md
ms.openlocfilehash: eaabe7fd97f68bbf2e3bcc498fb8a12f606982e2
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93697615"
---
# <span data-ttu-id="e05d2-101">Enable-AzCdnCustomDomainHttps</span><span class="sxs-lookup"><span data-stu-id="e05d2-101">Enable-AzCdnCustomDomainHttps</span></span>

## <span data-ttu-id="e05d2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e05d2-102">SYNOPSIS</span></span>
<span data-ttu-id="e05d2-103">사용자 지정 HTTPS를 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="e05d2-103">Enables custom HTTPS.</span></span>

## <span data-ttu-id="e05d2-104">구문과</span><span class="sxs-lookup"><span data-stu-id="e05d2-104">SYNTAX</span></span>

### <span data-ttu-id="e05d2-105">ByFieldsParameterSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="e05d2-105">ByFieldsParameterSet (Default)</span></span>
```
Enable-AzCdnCustomDomainHttps -ResourceGroupName <String> -ProfileName <String> -EndpointName <String>
 -CustomDomainName <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="e05d2-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="e05d2-106">ByObjectParameterSet</span></span>
```
Enable-AzCdnCustomDomainHttps -InputObject <PSCustomDomain> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e05d2-107">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="e05d2-107">ByResourceIdParameterSet</span></span>
```
Enable-AzCdnCustomDomainHttps -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e05d2-108">설명은</span><span class="sxs-lookup"><span data-stu-id="e05d2-108">DESCRIPTION</span></span>
<span data-ttu-id="e05d2-109">AzCdnCustomDomainHttps cmdlet을 **사용** 하면 CDN 사용자 지정 도메인의 보안 HTTPS 배달을 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="e05d2-109">The **Enable-AzCdnCustomDomainHttps** cmdlet enables the secured HTTPS delivery of a CDN custom domain.</span></span>

## <span data-ttu-id="e05d2-110">예제의</span><span class="sxs-lookup"><span data-stu-id="e05d2-110">EXAMPLES</span></span>

### <span data-ttu-id="e05d2-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="e05d2-111">Example 1</span></span>
```powershell
PS C:\> Enable-AzCdnCustomDomainHttps -ResourceGroupName $resourceGroupName -ProfileName $profileName -EndpointName $endpointName -CustomDomainName $customDomainName
```

<span data-ttu-id="e05d2-112">사용자 지정 도메인의 보안 배달을 사용 하도록 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="e05d2-112">Enable secure delivery of the custom domain.</span></span>

## <span data-ttu-id="e05d2-113">변수</span><span class="sxs-lookup"><span data-stu-id="e05d2-113">PARAMETERS</span></span>

### <span data-ttu-id="e05d2-114">-CustomDomainName</span><span class="sxs-lookup"><span data-stu-id="e05d2-114">-CustomDomainName</span></span>
<span data-ttu-id="e05d2-115">Azure CDN 사용자 지정 도메인 표시 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="e05d2-115">Azure CDN custom domain display name.</span></span>

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

### <span data-ttu-id="e05d2-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e05d2-116">-DefaultProfile</span></span>
<span data-ttu-id="e05d2-117">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="e05d2-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e05d2-118">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="e05d2-118">-EndpointName</span></span>
<span data-ttu-id="e05d2-119">Azure CDN 끝점 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="e05d2-119">Azure CDN endpoint name.</span></span>

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

### <span data-ttu-id="e05d2-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e05d2-120">-InputObject</span></span>
<span data-ttu-id="e05d2-121">사용자 지정 도메인 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="e05d2-121">The custom domain object.</span></span>

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

### <span data-ttu-id="e05d2-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="e05d2-122">-PassThru</span></span>
<span data-ttu-id="e05d2-123">지정 된 경우 object 반환</span><span class="sxs-lookup"><span data-stu-id="e05d2-123">Return object if specified.</span></span>

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

### <span data-ttu-id="e05d2-124">-/Profile</span><span class="sxs-lookup"><span data-stu-id="e05d2-124">-ProfileName</span></span>
<span data-ttu-id="e05d2-125">Azure CDN 프로필 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="e05d2-125">Azure CDN profile name.</span></span>

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

### <span data-ttu-id="e05d2-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e05d2-126">-ResourceGroupName</span></span>
<span data-ttu-id="e05d2-127">Azure CDN 프로필의 리소스 그룹</span><span class="sxs-lookup"><span data-stu-id="e05d2-127">The resource group of the Azure CDN profile</span></span>

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

### <span data-ttu-id="e05d2-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="e05d2-128">-ResourceId</span></span>
<span data-ttu-id="e05d2-129">사용자 지정 도메인의 ResourceId</span><span class="sxs-lookup"><span data-stu-id="e05d2-129">ResourceId of the Custom Domain</span></span>

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

### <span data-ttu-id="e05d2-130">-확인</span><span class="sxs-lookup"><span data-stu-id="e05d2-130">-Confirm</span></span>
<span data-ttu-id="e05d2-131">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="e05d2-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e05d2-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e05d2-132">-WhatIf</span></span>
<span data-ttu-id="e05d2-133">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="e05d2-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e05d2-134">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="e05d2-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e05d2-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e05d2-135">CommonParameters</span></span>
<span data-ttu-id="e05d2-136">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="e05d2-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e05d2-137">자세한 내용은 [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="e05d2-137">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e05d2-138">입력</span><span class="sxs-lookup"><span data-stu-id="e05d2-138">INPUTS</span></span>

### <span data-ttu-id="e05d2-139">PSCustomDomain (.). c.</span><span class="sxs-lookup"><span data-stu-id="e05d2-139">Microsoft.Azure.Commands.Cdn.Models.CustomDomain.PSCustomDomain</span></span>

### <span data-ttu-id="e05d2-140">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="e05d2-140">System.String</span></span>

## <span data-ttu-id="e05d2-141">출력</span><span class="sxs-lookup"><span data-stu-id="e05d2-141">OUTPUTS</span></span>

### <span data-ttu-id="e05d2-142">시스템 부울</span><span class="sxs-lookup"><span data-stu-id="e05d2-142">System.Boolean</span></span>

## <span data-ttu-id="e05d2-143">상속자</span><span class="sxs-lookup"><span data-stu-id="e05d2-143">NOTES</span></span>

## <span data-ttu-id="e05d2-144">관련 링크</span><span class="sxs-lookup"><span data-stu-id="e05d2-144">RELATED LINKS</span></span>
