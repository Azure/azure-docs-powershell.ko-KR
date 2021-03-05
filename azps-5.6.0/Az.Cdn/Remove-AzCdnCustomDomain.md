---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
ms.assetid: 5727E2CA-0A0B-4050-9F4A-7E06758D9B53
online version: https://docs.microsoft.com/powershell/module/az.cdn/remove-azcdncustomdomain
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Remove-AzCdnCustomDomain.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Remove-AzCdnCustomDomain.md
ms.openlocfilehash: c76e8d9da78fed592f506ba9aca39b68d4d119c6
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101975563"
---
# <span data-ttu-id="bd39c-101">Remove-AzCdnCustomDomain</span><span class="sxs-lookup"><span data-stu-id="bd39c-101">Remove-AzCdnCustomDomain</span></span>

## <span data-ttu-id="bd39c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="bd39c-102">SYNOPSIS</span></span>
<span data-ttu-id="bd39c-103">사용자 지정 도메인을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="bd39c-103">Removes a custom domain.</span></span>

## <span data-ttu-id="bd39c-104">구문</span><span class="sxs-lookup"><span data-stu-id="bd39c-104">SYNTAX</span></span>

### <span data-ttu-id="bd39c-105">ByFieldsParameterSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="bd39c-105">ByFieldsParameterSet (Default)</span></span>
```
Remove-AzCdnCustomDomain -CustomDomainName <String> -EndpointName <String> -ProfileName <String>
 -ResourceGroupName <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="bd39c-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="bd39c-106">ByObjectParameterSet</span></span>
```
Remove-AzCdnCustomDomain -CdnCustomDomain <PSCustomDomain> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="bd39c-107">설명</span><span class="sxs-lookup"><span data-stu-id="bd39c-107">DESCRIPTION</span></span>
<span data-ttu-id="bd39c-108">**Remove-AzCdnCustomDomain** cmdlet은 AZURE CDN(콘텐츠 배달 네트워크) 엔드포인트에서 사용자 지정 도메인을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="bd39c-108">The **Remove-AzCdnCustomDomain** cmdlet removes the custom domain from an Azure Content Delivery Network (CDN) endpoint.</span></span>

## <span data-ttu-id="bd39c-109">예제</span><span class="sxs-lookup"><span data-stu-id="bd39c-109">EXAMPLES</span></span>

## <span data-ttu-id="bd39c-110">매개 변수</span><span class="sxs-lookup"><span data-stu-id="bd39c-110">PARAMETERS</span></span>

### <span data-ttu-id="bd39c-111">-CdnCustomDomain</span><span class="sxs-lookup"><span data-stu-id="bd39c-111">-CdnCustomDomain</span></span>
<span data-ttu-id="bd39c-112">이 cmdlet이 제거한 사용자 지정 도메인을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="bd39c-112">Specifies the custom domain that this cmdlet removes.</span></span>

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

### <span data-ttu-id="bd39c-113">-CustomDomainName</span><span class="sxs-lookup"><span data-stu-id="bd39c-113">-CustomDomainName</span></span>
<span data-ttu-id="bd39c-114">이 cmdlet이 제거한 사용자 지정 도메인의 리소스 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="bd39c-114">Specifies the resource name of the custom domain that this cmdlet removes.</span></span>

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

### <span data-ttu-id="bd39c-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bd39c-115">-DefaultProfile</span></span>
<span data-ttu-id="bd39c-116">azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독</span><span class="sxs-lookup"><span data-stu-id="bd39c-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="bd39c-117">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="bd39c-117">-EndpointName</span></span>
<span data-ttu-id="bd39c-118">이 cmdlet에서 사용자 지정 도메인을 제거하는 엔드포인트의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="bd39c-118">Specifies the name of the endpoint from which this cmdlet removes a custom domain.</span></span>

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

### <span data-ttu-id="bd39c-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="bd39c-119">-PassThru</span></span>
<span data-ttu-id="bd39c-120">작업하는 항목을 나타내는 개체를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="bd39c-120">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="bd39c-121">기본적으로 이 cmdlet은 출력을 생성하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="bd39c-121">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="bd39c-122">-ProfileName</span><span class="sxs-lookup"><span data-stu-id="bd39c-122">-ProfileName</span></span>
<span data-ttu-id="bd39c-123">이 cmdlet에서 사용자 지정 도메인을 제거하는 프로필 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="bd39c-123">Specifies the name of the profile from which this cmdlet removes a custom domain.</span></span>

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

### <span data-ttu-id="bd39c-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bd39c-124">-ResourceGroupName</span></span>
<span data-ttu-id="bd39c-125">이 cmdlet에서 사용자 지정 도메인을 제거하는 리소스 그룹의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="bd39c-125">Specifies the name of the resource group from which this cmdlet removes a custom domain.</span></span>

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

### <span data-ttu-id="bd39c-126">-확인</span><span class="sxs-lookup"><span data-stu-id="bd39c-126">-Confirm</span></span>
<span data-ttu-id="bd39c-127">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="bd39c-127">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bd39c-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bd39c-128">-WhatIf</span></span>
<span data-ttu-id="bd39c-129">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="bd39c-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bd39c-130">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="bd39c-130">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bd39c-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bd39c-131">CommonParameters</span></span>
<span data-ttu-id="bd39c-132">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="bd39c-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bd39c-133">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="bd39c-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bd39c-134">입력</span><span class="sxs-lookup"><span data-stu-id="bd39c-134">INPUTS</span></span>

### <span data-ttu-id="bd39c-135">Microsoft.Azure.Commands.Cdn.Models.CustomDomain.PSCustomDomain</span><span class="sxs-lookup"><span data-stu-id="bd39c-135">Microsoft.Azure.Commands.Cdn.Models.CustomDomain.PSCustomDomain</span></span>

### <span data-ttu-id="bd39c-136">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="bd39c-136">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="bd39c-137">출력</span><span class="sxs-lookup"><span data-stu-id="bd39c-137">OUTPUTS</span></span>

### <span data-ttu-id="bd39c-138">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="bd39c-138">System.Boolean</span></span>

## <span data-ttu-id="bd39c-139">참고 사항</span><span class="sxs-lookup"><span data-stu-id="bd39c-139">NOTES</span></span>

## <span data-ttu-id="bd39c-140">관련 링크</span><span class="sxs-lookup"><span data-stu-id="bd39c-140">RELATED LINKS</span></span>

[<span data-ttu-id="bd39c-141">Get-AzCdnCustomDomain</span><span class="sxs-lookup"><span data-stu-id="bd39c-141">Get-AzCdnCustomDomain</span></span>](./Get-AzCdnCustomDomain.md)

[<span data-ttu-id="bd39c-142">New-AzCdnCustomDomain</span><span class="sxs-lookup"><span data-stu-id="bd39c-142">New-AzCdnCustomDomain</span></span>](./New-AzCdnCustomDomain.md)

[<span data-ttu-id="bd39c-143">Test-AzCdnCustomDomain</span><span class="sxs-lookup"><span data-stu-id="bd39c-143">Test-AzCdnCustomDomain</span></span>](./Test-AzCdnCustomDomain.md)


