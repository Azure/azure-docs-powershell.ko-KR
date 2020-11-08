---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
online version: https://docs.microsoft.com/en-us/powershell/module/az.cdn/enable-azcdncustomdomain
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Enable-AzCdnCustomDomain.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Enable-AzCdnCustomDomain.md
ms.openlocfilehash: eebc75ba8f8f1a55fb4c1db2e7929ce233d93a23
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94219211"
---
# <span data-ttu-id="f2f1f-101">Enable-AzCdnCustomDomain</span><span class="sxs-lookup"><span data-stu-id="f2f1f-101">Enable-AzCdnCustomDomain</span></span>

## <span data-ttu-id="f2f1f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f2f1f-102">SYNOPSIS</span></span>
<span data-ttu-id="f2f1f-103">사용자 지정 도메인 HTTPS (사용 되지 않음)를 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="f2f1f-103">Enables Custom Domain HTTPS (Deprecated).</span></span>

## <span data-ttu-id="f2f1f-104">구문과</span><span class="sxs-lookup"><span data-stu-id="f2f1f-104">SYNTAX</span></span>

### <span data-ttu-id="f2f1f-105">ByFieldsParameterSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="f2f1f-105">ByFieldsParameterSet (Default)</span></span>
```
Enable-AzCdnCustomDomain -CustomDomainName <String> -EndpointName <String> -ProfileName <String>
 -ResourceGroupName <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="f2f1f-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="f2f1f-106">ByObjectParameterSet</span></span>
```
Enable-AzCdnCustomDomain -InputObject <PSCustomDomain> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f2f1f-107">설명은</span><span class="sxs-lookup"><span data-stu-id="f2f1f-107">DESCRIPTION</span></span>
<span data-ttu-id="f2f1f-108">AzCdnCustomDomain cmdlet을 **사용** 하면 CDN 사용자 지정 도메인의 보안 HTTPS 배달을 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="f2f1f-108">The **Enable-AzCdnCustomDomain** cmdlet enables the secured HTTPS delivery of a CDN custom domain.</span></span>

## <span data-ttu-id="f2f1f-109">예제의</span><span class="sxs-lookup"><span data-stu-id="f2f1f-109">EXAMPLES</span></span>

### <span data-ttu-id="f2f1f-110">예제 1</span><span class="sxs-lookup"><span data-stu-id="f2f1f-110">Example 1</span></span>
```powershell
Enable-AzCdnCustomDomain -CustomDomainName $customDomainName -EndpointName $endpointName -ProfileName $profileName -ResourceGroupName $resourceGroupName
true
```

<span data-ttu-id="f2f1f-111">사용자 지정 도메인의 https 배달을 사용 하도록 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="f2f1f-111">Enable https delivery of the custom domain.</span></span>

## <span data-ttu-id="f2f1f-112">변수</span><span class="sxs-lookup"><span data-stu-id="f2f1f-112">PARAMETERS</span></span>

### <span data-ttu-id="f2f1f-113">-CustomDomainName</span><span class="sxs-lookup"><span data-stu-id="f2f1f-113">-CustomDomainName</span></span>
<span data-ttu-id="f2f1f-114">Azure CDN 사용자 지정 도메인 표시 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="f2f1f-114">Azure CDN custom domain display name.</span></span>

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

### <span data-ttu-id="f2f1f-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f2f1f-115">-DefaultProfile</span></span>
<span data-ttu-id="f2f1f-116">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="f2f1f-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f2f1f-117">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="f2f1f-117">-EndpointName</span></span>
<span data-ttu-id="f2f1f-118">Azure CDN 끝점 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="f2f1f-118">Azure CDN endpoint name.</span></span>

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

### <span data-ttu-id="f2f1f-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="f2f1f-119">-InputObject</span></span>
<span data-ttu-id="f2f1f-120">사용자 지정 도메인 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="f2f1f-120">The custom domain object.</span></span>

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

### <span data-ttu-id="f2f1f-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="f2f1f-121">-PassThru</span></span>
<span data-ttu-id="f2f1f-122">Object (지정 된 경우)를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="f2f1f-122">Return object (if specified).</span></span>

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

### <span data-ttu-id="f2f1f-123">-/Profile</span><span class="sxs-lookup"><span data-stu-id="f2f1f-123">-ProfileName</span></span>
<span data-ttu-id="f2f1f-124">Azure CDN 프로필 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="f2f1f-124">Azure CDN profile name.</span></span>

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

### <span data-ttu-id="f2f1f-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f2f1f-125">-ResourceGroupName</span></span>
<span data-ttu-id="f2f1f-126">Azure CDN 프로필의 리소스 그룹입니다.</span><span class="sxs-lookup"><span data-stu-id="f2f1f-126">The resource group of the Azure CDN profile.</span></span>

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

### <span data-ttu-id="f2f1f-127">-확인</span><span class="sxs-lookup"><span data-stu-id="f2f1f-127">-Confirm</span></span>
<span data-ttu-id="f2f1f-128">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="f2f1f-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f2f1f-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f2f1f-129">-WhatIf</span></span>
<span data-ttu-id="f2f1f-130">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="f2f1f-130">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="f2f1f-131">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="f2f1f-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f2f1f-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f2f1f-132">CommonParameters</span></span>
<span data-ttu-id="f2f1f-133">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="f2f1f-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f2f1f-134">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="f2f1f-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f2f1f-135">입력</span><span class="sxs-lookup"><span data-stu-id="f2f1f-135">INPUTS</span></span>

### <span data-ttu-id="f2f1f-136">PSCustomDomain (.). c.</span><span class="sxs-lookup"><span data-stu-id="f2f1f-136">Microsoft.Azure.Commands.Cdn.Models.CustomDomain.PSCustomDomain</span></span>

## <span data-ttu-id="f2f1f-137">출력</span><span class="sxs-lookup"><span data-stu-id="f2f1f-137">OUTPUTS</span></span>

### <span data-ttu-id="f2f1f-138">시스템 부울</span><span class="sxs-lookup"><span data-stu-id="f2f1f-138">System.Boolean</span></span>

## <span data-ttu-id="f2f1f-139">상속자</span><span class="sxs-lookup"><span data-stu-id="f2f1f-139">NOTES</span></span>

## <span data-ttu-id="f2f1f-140">관련 링크</span><span class="sxs-lookup"><span data-stu-id="f2f1f-140">RELATED LINKS</span></span>
