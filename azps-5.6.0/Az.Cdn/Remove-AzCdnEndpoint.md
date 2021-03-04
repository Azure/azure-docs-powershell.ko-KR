---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
ms.assetid: 7ADF4CDE-638B-4E00-88B1-688702B084A5
online version: https://docs.microsoft.com/powershell/module/az.cdn/remove-azcdnendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Remove-AzCdnEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Remove-AzCdnEndpoint.md
ms.openlocfilehash: e6c45f74f149cb2c087419a10f3e31cdfeb26610
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101959003"
---
# <span data-ttu-id="2c19b-101">Remove-AzCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="2c19b-101">Remove-AzCdnEndpoint</span></span>

## <span data-ttu-id="2c19b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2c19b-102">SYNOPSIS</span></span>
<span data-ttu-id="2c19b-103">CDN 엔드포인트를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="2c19b-103">Removes a CDN endpoint.</span></span>

## <span data-ttu-id="2c19b-104">구문</span><span class="sxs-lookup"><span data-stu-id="2c19b-104">SYNTAX</span></span>

### <span data-ttu-id="2c19b-105">ByFieldsParameterSet</span><span class="sxs-lookup"><span data-stu-id="2c19b-105">ByFieldsParameterSet</span></span>
```
Remove-AzCdnEndpoint -EndpointName <String> -ProfileName <String> -ResourceGroupName <String> [-PassThru]
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2c19b-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="2c19b-106">ByObjectParameterSet</span></span>
```
Remove-AzCdnEndpoint -CdnEndpoint <PSEndpoint> [-PassThru] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2c19b-107">설명</span><span class="sxs-lookup"><span data-stu-id="2c19b-107">DESCRIPTION</span></span>
<span data-ttu-id="2c19b-108">**Remove-AzCdnEndpoint** cmdlet은 CDN(Azure Content Delivery Network) 엔드포인트를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="2c19b-108">The **Remove-AzCdnEndpoint** cmdlet removes an Azure Content Delivery Network (CDN) endpoint.</span></span>

## <span data-ttu-id="2c19b-109">예제</span><span class="sxs-lookup"><span data-stu-id="2c19b-109">EXAMPLES</span></span>

## <span data-ttu-id="2c19b-110">매개 변수</span><span class="sxs-lookup"><span data-stu-id="2c19b-110">PARAMETERS</span></span>

### <span data-ttu-id="2c19b-111">-CdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="2c19b-111">-CdnEndpoint</span></span>
<span data-ttu-id="2c19b-112">이 cmdlet이 제거하는 엔드포인트를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="2c19b-112">Specifies the endpoint that this cmdlet removes.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSEndpoint
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="2c19b-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2c19b-113">-DefaultProfile</span></span>
<span data-ttu-id="2c19b-114">azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독</span><span class="sxs-lookup"><span data-stu-id="2c19b-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="2c19b-115">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="2c19b-115">-EndpointName</span></span>
<span data-ttu-id="2c19b-116">이 cmdlet이 제거하는 엔드포인트의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="2c19b-116">Specifies the name of the endpoint that this cmdlet removes.</span></span>

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

### <span data-ttu-id="2c19b-117">-Force</span><span class="sxs-lookup"><span data-stu-id="2c19b-117">-Force</span></span>
<span data-ttu-id="2c19b-118">사용자 확인을 요청하지 않고 명령을 강제로 실행합니다.</span><span class="sxs-lookup"><span data-stu-id="2c19b-118">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="2c19b-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="2c19b-119">-PassThru</span></span>
<span data-ttu-id="2c19b-120">작업하는 항목을 나타내는 개체를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="2c19b-120">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="2c19b-121">기본적으로 이 cmdlet은 출력을 생성하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="2c19b-121">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="2c19b-122">-ProfileName</span><span class="sxs-lookup"><span data-stu-id="2c19b-122">-ProfileName</span></span>
<span data-ttu-id="2c19b-123">엔드포인트가 속한 프로필의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="2c19b-123">Specifies the name of the profile to which the endpoint belongs.</span></span>

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

### <span data-ttu-id="2c19b-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2c19b-124">-ResourceGroupName</span></span>
<span data-ttu-id="2c19b-125">엔드포인트가 속한 리소스 그룹의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="2c19b-125">Specifies the name of the resource group to which the endpoint belongs.</span></span>

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

### <span data-ttu-id="2c19b-126">-확인</span><span class="sxs-lookup"><span data-stu-id="2c19b-126">-Confirm</span></span>
<span data-ttu-id="2c19b-127">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="2c19b-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2c19b-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2c19b-128">-WhatIf</span></span>
<span data-ttu-id="2c19b-129">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="2c19b-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2c19b-130">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="2c19b-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2c19b-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2c19b-131">CommonParameters</span></span>
<span data-ttu-id="2c19b-132">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="2c19b-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2c19b-133">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="2c19b-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2c19b-134">입력</span><span class="sxs-lookup"><span data-stu-id="2c19b-134">INPUTS</span></span>

### <span data-ttu-id="2c19b-135">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSEndpoint</span><span class="sxs-lookup"><span data-stu-id="2c19b-135">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSEndpoint</span></span>

### <span data-ttu-id="2c19b-136">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="2c19b-136">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="2c19b-137">출력</span><span class="sxs-lookup"><span data-stu-id="2c19b-137">OUTPUTS</span></span>

### <span data-ttu-id="2c19b-138">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="2c19b-138">System.Boolean</span></span>

## <span data-ttu-id="2c19b-139">참고 사항</span><span class="sxs-lookup"><span data-stu-id="2c19b-139">NOTES</span></span>

## <span data-ttu-id="2c19b-140">관련 링크</span><span class="sxs-lookup"><span data-stu-id="2c19b-140">RELATED LINKS</span></span>

[<span data-ttu-id="2c19b-141">Get-AzCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="2c19b-141">Get-AzCdnEndpoint</span></span>](./Get-AzCdnEndpoint.md)

[<span data-ttu-id="2c19b-142">New-AzCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="2c19b-142">New-AzCdnEndpoint</span></span>](./New-AzCdnEndpoint.md)

[<span data-ttu-id="2c19b-143">Set-AzCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="2c19b-143">Set-AzCdnEndpoint</span></span>](./Set-AzCdnEndpoint.md)

[<span data-ttu-id="2c19b-144">Start-AzCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="2c19b-144">Start-AzCdnEndpoint</span></span>](./Start-AzCdnEndpoint.md)

[<span data-ttu-id="2c19b-145">Stop-AzCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="2c19b-145">Stop-AzCdnEndpoint</span></span>](./Stop-AzCdnEndpoint.md)


