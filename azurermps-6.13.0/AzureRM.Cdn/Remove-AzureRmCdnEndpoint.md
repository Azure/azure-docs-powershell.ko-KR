---
external help file: Microsoft.Azure.Commands.Cdn.dll-Help.xml
Module Name: AzureRM.Cdn
ms.assetid: 7ADF4CDE-638B-4E00-88B1-688702B084A5
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.cdn/remove-azurermcdnendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Cdn/Commands.Cdn/help/Remove-AzureRmCdnEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Cdn/Commands.Cdn/help/Remove-AzureRmCdnEndpoint.md
ms.openlocfilehash: 6feb7eb3f20e06c8dfffaa3dd9a1fb2bf3cc4c68
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93531426"
---
# <span data-ttu-id="e7d09-101">Remove-AzureRmCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="e7d09-101">Remove-AzureRmCdnEndpoint</span></span>

## <span data-ttu-id="e7d09-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e7d09-102">SYNOPSIS</span></span>
<span data-ttu-id="e7d09-103">CDN 끝점을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="e7d09-103">Removes a CDN endpoint.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e7d09-104">구문과</span><span class="sxs-lookup"><span data-stu-id="e7d09-104">SYNTAX</span></span>

### <span data-ttu-id="e7d09-105">ByFieldsParameterSet</span><span class="sxs-lookup"><span data-stu-id="e7d09-105">ByFieldsParameterSet</span></span>
```
Remove-AzureRmCdnEndpoint -EndpointName <String> -ProfileName <String> -ResourceGroupName <String> [-PassThru]
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e7d09-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="e7d09-106">ByObjectParameterSet</span></span>
```
Remove-AzureRmCdnEndpoint -CdnEndpoint <PSEndpoint> [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e7d09-107">설명은</span><span class="sxs-lookup"><span data-stu-id="e7d09-107">DESCRIPTION</span></span>
<span data-ttu-id="e7d09-108">**AzureRmCdnEndpoint** Cmdlet은 Azure CDN (콘텐츠 배달 네트워크) 끝점을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="e7d09-108">The **Remove-AzureRmCdnEndpoint** cmdlet removes an Azure Content Delivery Network (CDN) endpoint.</span></span>

## <span data-ttu-id="e7d09-109">예제의</span><span class="sxs-lookup"><span data-stu-id="e7d09-109">EXAMPLES</span></span>

## <span data-ttu-id="e7d09-110">변수</span><span class="sxs-lookup"><span data-stu-id="e7d09-110">PARAMETERS</span></span>

### <span data-ttu-id="e7d09-111">-CdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="e7d09-111">-CdnEndpoint</span></span>
<span data-ttu-id="e7d09-112">이 cmdlet이 제거 하는 끝점을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="e7d09-112">Specifies the endpoint that this cmdlet removes.</span></span>

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

### <span data-ttu-id="e7d09-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e7d09-113">-DefaultProfile</span></span>
<span data-ttu-id="e7d09-114">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="e7d09-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e7d09-115">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="e7d09-115">-EndpointName</span></span>
<span data-ttu-id="e7d09-116">이 cmdlet이 제거 하는 끝점의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="e7d09-116">Specifies the name of the endpoint that this cmdlet removes.</span></span>

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

### <span data-ttu-id="e7d09-117">-Force</span><span class="sxs-lookup"><span data-stu-id="e7d09-117">-Force</span></span>
<span data-ttu-id="e7d09-118">사용자 확인을 요청 하지 않고 명령을 강제로 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="e7d09-118">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="e7d09-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="e7d09-119">-PassThru</span></span>
<span data-ttu-id="e7d09-120">작업 중인 항목을 나타내는 개체를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="e7d09-120">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="e7d09-121">기본적으로이 cmdlet은 출력을 생성 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="e7d09-121">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="e7d09-122">-/Profile</span><span class="sxs-lookup"><span data-stu-id="e7d09-122">-ProfileName</span></span>
<span data-ttu-id="e7d09-123">종점이 속한 프로필의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="e7d09-123">Specifies the name of the profile to which the endpoint belongs.</span></span>

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

### <span data-ttu-id="e7d09-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e7d09-124">-ResourceGroupName</span></span>
<span data-ttu-id="e7d09-125">끝점이 속한 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="e7d09-125">Specifies the name of the resource group to which the endpoint belongs.</span></span>

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

### <span data-ttu-id="e7d09-126">-확인</span><span class="sxs-lookup"><span data-stu-id="e7d09-126">-Confirm</span></span>
<span data-ttu-id="e7d09-127">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="e7d09-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e7d09-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e7d09-128">-WhatIf</span></span>
<span data-ttu-id="e7d09-129">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="e7d09-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e7d09-130">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="e7d09-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e7d09-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e7d09-131">CommonParameters</span></span>
<span data-ttu-id="e7d09-132">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="e7d09-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e7d09-133">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e7d09-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e7d09-134">입력</span><span class="sxs-lookup"><span data-stu-id="e7d09-134">INPUTS</span></span>

### <span data-ttu-id="e7d09-135">Microsoft. Cdn. Endpoint. PSEndpoint</span><span class="sxs-lookup"><span data-stu-id="e7d09-135">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSEndpoint</span></span>
<span data-ttu-id="e7d09-136">매개 변수: CdnEndpoint (ByValue)</span><span class="sxs-lookup"><span data-stu-id="e7d09-136">Parameters: CdnEndpoint (ByValue)</span></span>

### <span data-ttu-id="e7d09-137">System.webserver 매개 변수</span><span class="sxs-lookup"><span data-stu-id="e7d09-137">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="e7d09-138">출력</span><span class="sxs-lookup"><span data-stu-id="e7d09-138">OUTPUTS</span></span>

### <span data-ttu-id="e7d09-139">시스템 부울</span><span class="sxs-lookup"><span data-stu-id="e7d09-139">System.Boolean</span></span>

## <span data-ttu-id="e7d09-140">상속자</span><span class="sxs-lookup"><span data-stu-id="e7d09-140">NOTES</span></span>

## <span data-ttu-id="e7d09-141">관련 링크</span><span class="sxs-lookup"><span data-stu-id="e7d09-141">RELATED LINKS</span></span>

[<span data-ttu-id="e7d09-142">Get-AzureRmCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="e7d09-142">Get-AzureRmCdnEndpoint</span></span>](./Get-AzureRmCdnEndpoint.md)

[<span data-ttu-id="e7d09-143">새로운 AzureRmCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="e7d09-143">New-AzureRmCdnEndpoint</span></span>](./New-AzureRmCdnEndpoint.md)

[<span data-ttu-id="e7d09-144">Set-AzureRmCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="e7d09-144">Set-AzureRmCdnEndpoint</span></span>](./Set-AzureRmCdnEndpoint.md)

[<span data-ttu-id="e7d09-145">시작-AzureRmCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="e7d09-145">Start-AzureRmCdnEndpoint</span></span>](./Start-AzureRmCdnEndpoint.md)

[<span data-ttu-id="e7d09-146">중지-AzureRmCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="e7d09-146">Stop-AzureRmCdnEndpoint</span></span>](./Stop-AzureRmCdnEndpoint.md)


