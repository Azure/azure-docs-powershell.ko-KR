---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
ms.assetid: 5727E2CA-0A0B-4050-9F4A-7E06758D9B53
online version: https://docs.microsoft.com/en-us/powershell/module/az.cdn/remove-azcdncustomdomain
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Remove-AzCdnCustomDomain.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Remove-AzCdnCustomDomain.md
ms.openlocfilehash: 0645b3f5286526ba72db35fd8b9e048c895f4108
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98354633"
---
# <span data-ttu-id="4f567-101">Remove-AzCdnCustomDomain</span><span class="sxs-lookup"><span data-stu-id="4f567-101">Remove-AzCdnCustomDomain</span></span>

## <span data-ttu-id="4f567-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4f567-102">SYNOPSIS</span></span>
<span data-ttu-id="4f567-103">사용자 지정 도메인을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="4f567-103">Removes a custom domain.</span></span>

## <span data-ttu-id="4f567-104">구문</span><span class="sxs-lookup"><span data-stu-id="4f567-104">SYNTAX</span></span>

### <span data-ttu-id="4f567-105">ByFieldsParameterSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="4f567-105">ByFieldsParameterSet (Default)</span></span>
```
Remove-AzCdnCustomDomain -CustomDomainName <String> -EndpointName <String> -ProfileName <String>
 -ResourceGroupName <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="4f567-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="4f567-106">ByObjectParameterSet</span></span>
```
Remove-AzCdnCustomDomain -CdnCustomDomain <PSCustomDomain> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4f567-107">설명</span><span class="sxs-lookup"><span data-stu-id="4f567-107">DESCRIPTION</span></span>
<span data-ttu-id="4f567-108">**Remove-AzCdnCustomDomain** cmdlet은 Azure CDN(Content Delivery Network) 엔드포인트에서 사용자 지정 도메인을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="4f567-108">The **Remove-AzCdnCustomDomain** cmdlet removes the custom domain from an Azure Content Delivery Network (CDN) endpoint.</span></span>

## <span data-ttu-id="4f567-109">예제</span><span class="sxs-lookup"><span data-stu-id="4f567-109">EXAMPLES</span></span>

## <span data-ttu-id="4f567-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="4f567-110">PARAMETERS</span></span>

### <span data-ttu-id="4f567-111">-CdnCustomDomain</span><span class="sxs-lookup"><span data-stu-id="4f567-111">-CdnCustomDomain</span></span>
<span data-ttu-id="4f567-112">이 cmdlet이 제거하는 사용자 지정 도메인을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="4f567-112">Specifies the custom domain that this cmdlet removes.</span></span>

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

### <span data-ttu-id="4f567-113">-CustomDomainName</span><span class="sxs-lookup"><span data-stu-id="4f567-113">-CustomDomainName</span></span>
<span data-ttu-id="4f567-114">이 cmdlet에서 제거하는 사용자 지정 도메인의 리소스 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="4f567-114">Specifies the resource name of the custom domain that this cmdlet removes.</span></span>

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

### <span data-ttu-id="4f567-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4f567-115">-DefaultProfile</span></span>
<span data-ttu-id="4f567-116">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독</span><span class="sxs-lookup"><span data-stu-id="4f567-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="4f567-117">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="4f567-117">-EndpointName</span></span>
<span data-ttu-id="4f567-118">이 cmdlet이 사용자 지정 도메인을 제거하는 엔드포인트의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="4f567-118">Specifies the name of the endpoint from which this cmdlet removes a custom domain.</span></span>

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

### <span data-ttu-id="4f567-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="4f567-119">-PassThru</span></span>
<span data-ttu-id="4f567-120">작업하는 항목을 나타내는 개체를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="4f567-120">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="4f567-121">기본적으로 이 cmdlet은 출력을 생성하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="4f567-121">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="4f567-122">-ProfileName</span><span class="sxs-lookup"><span data-stu-id="4f567-122">-ProfileName</span></span>
<span data-ttu-id="4f567-123">이 cmdlet이 사용자 지정 도메인을 제거하는 프로필의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="4f567-123">Specifies the name of the profile from which this cmdlet removes a custom domain.</span></span>

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

### <span data-ttu-id="4f567-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4f567-124">-ResourceGroupName</span></span>
<span data-ttu-id="4f567-125">이 cmdlet이 사용자 지정 도메인을 제거하는 리소스 그룹의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="4f567-125">Specifies the name of the resource group from which this cmdlet removes a custom domain.</span></span>

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

### <span data-ttu-id="4f567-126">-Confirm</span><span class="sxs-lookup"><span data-stu-id="4f567-126">-Confirm</span></span>
<span data-ttu-id="4f567-127">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="4f567-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4f567-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4f567-128">-WhatIf</span></span>
<span data-ttu-id="4f567-129">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="4f567-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4f567-130">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="4f567-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4f567-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4f567-131">CommonParameters</span></span>
<span data-ttu-id="4f567-132">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="4f567-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4f567-133">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="4f567-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4f567-134">입력</span><span class="sxs-lookup"><span data-stu-id="4f567-134">INPUTS</span></span>

### <span data-ttu-id="4f567-135">Microsoft.Azure.Commands.Cdn.Models.CustomDomain.PSCustomDomain</span><span class="sxs-lookup"><span data-stu-id="4f567-135">Microsoft.Azure.Commands.Cdn.Models.CustomDomain.PSCustomDomain</span></span>

### <span data-ttu-id="4f567-136">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="4f567-136">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="4f567-137">출력</span><span class="sxs-lookup"><span data-stu-id="4f567-137">OUTPUTS</span></span>

### <span data-ttu-id="4f567-138">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="4f567-138">System.Boolean</span></span>

## <span data-ttu-id="4f567-139">참고 사항</span><span class="sxs-lookup"><span data-stu-id="4f567-139">NOTES</span></span>

## <span data-ttu-id="4f567-140">관련 링크</span><span class="sxs-lookup"><span data-stu-id="4f567-140">RELATED LINKS</span></span>

[<span data-ttu-id="4f567-141">Get-AzCdnCustomDomain</span><span class="sxs-lookup"><span data-stu-id="4f567-141">Get-AzCdnCustomDomain</span></span>](./Get-AzCdnCustomDomain.md)

[<span data-ttu-id="4f567-142">New-AzCdnCustomDomain</span><span class="sxs-lookup"><span data-stu-id="4f567-142">New-AzCdnCustomDomain</span></span>](./New-AzCdnCustomDomain.md)

[<span data-ttu-id="4f567-143">Test-AzCdnCustomDomain</span><span class="sxs-lookup"><span data-stu-id="4f567-143">Test-AzCdnCustomDomain</span></span>](./Test-AzCdnCustomDomain.md)


