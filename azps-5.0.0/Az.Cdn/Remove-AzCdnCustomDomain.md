---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
ms.assetid: 5727E2CA-0A0B-4050-9F4A-7E06758D9B53
online version: https://docs.microsoft.com/en-us/powershell/module/az.cdn/remove-azcdncustomdomain
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Remove-AzCdnCustomDomain.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Remove-AzCdnCustomDomain.md
ms.openlocfilehash: 0645b3f5286526ba72db35fd8b9e048c895f4108
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94216254"
---
# <span data-ttu-id="e76dc-101">Remove-AzCdnCustomDomain</span><span class="sxs-lookup"><span data-stu-id="e76dc-101">Remove-AzCdnCustomDomain</span></span>

## <span data-ttu-id="e76dc-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e76dc-102">SYNOPSIS</span></span>
<span data-ttu-id="e76dc-103">사용자 지정 도메인을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="e76dc-103">Removes a custom domain.</span></span>

## <span data-ttu-id="e76dc-104">구문과</span><span class="sxs-lookup"><span data-stu-id="e76dc-104">SYNTAX</span></span>

### <span data-ttu-id="e76dc-105">ByFieldsParameterSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="e76dc-105">ByFieldsParameterSet (Default)</span></span>
```
Remove-AzCdnCustomDomain -CustomDomainName <String> -EndpointName <String> -ProfileName <String>
 -ResourceGroupName <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="e76dc-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="e76dc-106">ByObjectParameterSet</span></span>
```
Remove-AzCdnCustomDomain -CdnCustomDomain <PSCustomDomain> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e76dc-107">설명은</span><span class="sxs-lookup"><span data-stu-id="e76dc-107">DESCRIPTION</span></span>
<span data-ttu-id="e76dc-108">**AzCdnCustomDomain** CMDLET은 CDN (Azure Content Delivery Network) 끝점에서 사용자 지정 도메인을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="e76dc-108">The **Remove-AzCdnCustomDomain** cmdlet removes the custom domain from an Azure Content Delivery Network (CDN) endpoint.</span></span>

## <span data-ttu-id="e76dc-109">예제의</span><span class="sxs-lookup"><span data-stu-id="e76dc-109">EXAMPLES</span></span>

## <span data-ttu-id="e76dc-110">변수</span><span class="sxs-lookup"><span data-stu-id="e76dc-110">PARAMETERS</span></span>

### <span data-ttu-id="e76dc-111">-CdnCustomDomain</span><span class="sxs-lookup"><span data-stu-id="e76dc-111">-CdnCustomDomain</span></span>
<span data-ttu-id="e76dc-112">이 cmdlet이 제거 하는 사용자 지정 도메인을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="e76dc-112">Specifies the custom domain that this cmdlet removes.</span></span>

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

### <span data-ttu-id="e76dc-113">-CustomDomainName</span><span class="sxs-lookup"><span data-stu-id="e76dc-113">-CustomDomainName</span></span>
<span data-ttu-id="e76dc-114">이 cmdlet이 제거 하는 사용자 지정 도메인의 리소스 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="e76dc-114">Specifies the resource name of the custom domain that this cmdlet removes.</span></span>

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

### <span data-ttu-id="e76dc-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e76dc-115">-DefaultProfile</span></span>
<span data-ttu-id="e76dc-116">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="e76dc-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="e76dc-117">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="e76dc-117">-EndpointName</span></span>
<span data-ttu-id="e76dc-118">이 cmdlet이 사용자 지정 도메인을 제거 하는 끝점의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="e76dc-118">Specifies the name of the endpoint from which this cmdlet removes a custom domain.</span></span>

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

### <span data-ttu-id="e76dc-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="e76dc-119">-PassThru</span></span>
<span data-ttu-id="e76dc-120">작업 중인 항목을 나타내는 개체를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="e76dc-120">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="e76dc-121">기본적으로이 cmdlet은 출력을 생성 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="e76dc-121">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="e76dc-122">-/Profile</span><span class="sxs-lookup"><span data-stu-id="e76dc-122">-ProfileName</span></span>
<span data-ttu-id="e76dc-123">이 cmdlet에서 사용자 지정 도메인을 제거 하는 프로필의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="e76dc-123">Specifies the name of the profile from which this cmdlet removes a custom domain.</span></span>

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

### <span data-ttu-id="e76dc-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e76dc-124">-ResourceGroupName</span></span>
<span data-ttu-id="e76dc-125">이 cmdlet이 사용자 지정 도메인을 제거 하는 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="e76dc-125">Specifies the name of the resource group from which this cmdlet removes a custom domain.</span></span>

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

### <span data-ttu-id="e76dc-126">-확인</span><span class="sxs-lookup"><span data-stu-id="e76dc-126">-Confirm</span></span>
<span data-ttu-id="e76dc-127">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="e76dc-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e76dc-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e76dc-128">-WhatIf</span></span>
<span data-ttu-id="e76dc-129">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="e76dc-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e76dc-130">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="e76dc-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e76dc-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e76dc-131">CommonParameters</span></span>
<span data-ttu-id="e76dc-132">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="e76dc-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e76dc-133">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="e76dc-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e76dc-134">입력</span><span class="sxs-lookup"><span data-stu-id="e76dc-134">INPUTS</span></span>

### <span data-ttu-id="e76dc-135">PSCustomDomain (.). c.</span><span class="sxs-lookup"><span data-stu-id="e76dc-135">Microsoft.Azure.Commands.Cdn.Models.CustomDomain.PSCustomDomain</span></span>

### <span data-ttu-id="e76dc-136">System.webserver 매개 변수</span><span class="sxs-lookup"><span data-stu-id="e76dc-136">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="e76dc-137">출력</span><span class="sxs-lookup"><span data-stu-id="e76dc-137">OUTPUTS</span></span>

### <span data-ttu-id="e76dc-138">시스템 부울</span><span class="sxs-lookup"><span data-stu-id="e76dc-138">System.Boolean</span></span>

## <span data-ttu-id="e76dc-139">상속자</span><span class="sxs-lookup"><span data-stu-id="e76dc-139">NOTES</span></span>

## <span data-ttu-id="e76dc-140">관련 링크</span><span class="sxs-lookup"><span data-stu-id="e76dc-140">RELATED LINKS</span></span>

[<span data-ttu-id="e76dc-141">Get-AzCdnCustomDomain</span><span class="sxs-lookup"><span data-stu-id="e76dc-141">Get-AzCdnCustomDomain</span></span>](./Get-AzCdnCustomDomain.md)

[<span data-ttu-id="e76dc-142">새로운 AzCdnCustomDomain</span><span class="sxs-lookup"><span data-stu-id="e76dc-142">New-AzCdnCustomDomain</span></span>](./New-AzCdnCustomDomain.md)

[<span data-ttu-id="e76dc-143">테스트-AzCdnCustomDomain</span><span class="sxs-lookup"><span data-stu-id="e76dc-143">Test-AzCdnCustomDomain</span></span>](./Test-AzCdnCustomDomain.md)


