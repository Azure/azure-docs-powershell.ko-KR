---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
ms.assetid: 7ADF4CDE-638B-4E00-88B1-688702B084A5
online version: https://docs.microsoft.com/en-us/powershell/module/az.cdn/remove-azcdnendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Remove-AzCdnEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Remove-AzCdnEndpoint.md
ms.openlocfilehash: 780765ea56cd13ee7cbd09b64dc20db896234aec
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94219097"
---
# <span data-ttu-id="d623e-101">Remove-AzCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="d623e-101">Remove-AzCdnEndpoint</span></span>

## <span data-ttu-id="d623e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d623e-102">SYNOPSIS</span></span>
<span data-ttu-id="d623e-103">CDN 끝점을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="d623e-103">Removes a CDN endpoint.</span></span>

## <span data-ttu-id="d623e-104">구문과</span><span class="sxs-lookup"><span data-stu-id="d623e-104">SYNTAX</span></span>

### <span data-ttu-id="d623e-105">ByFieldsParameterSet</span><span class="sxs-lookup"><span data-stu-id="d623e-105">ByFieldsParameterSet</span></span>
```
Remove-AzCdnEndpoint -EndpointName <String> -ProfileName <String> -ResourceGroupName <String> [-PassThru]
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d623e-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="d623e-106">ByObjectParameterSet</span></span>
```
Remove-AzCdnEndpoint -CdnEndpoint <PSEndpoint> [-PassThru] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d623e-107">설명은</span><span class="sxs-lookup"><span data-stu-id="d623e-107">DESCRIPTION</span></span>
<span data-ttu-id="d623e-108">**AzCdnEndpoint** Cmdlet은 Azure CDN (콘텐츠 배달 네트워크) 끝점을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="d623e-108">The **Remove-AzCdnEndpoint** cmdlet removes an Azure Content Delivery Network (CDN) endpoint.</span></span>

## <span data-ttu-id="d623e-109">예제의</span><span class="sxs-lookup"><span data-stu-id="d623e-109">EXAMPLES</span></span>

## <span data-ttu-id="d623e-110">변수</span><span class="sxs-lookup"><span data-stu-id="d623e-110">PARAMETERS</span></span>

### <span data-ttu-id="d623e-111">-CdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="d623e-111">-CdnEndpoint</span></span>
<span data-ttu-id="d623e-112">이 cmdlet이 제거 하는 끝점을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d623e-112">Specifies the endpoint that this cmdlet removes.</span></span>

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

### <span data-ttu-id="d623e-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d623e-113">-DefaultProfile</span></span>
<span data-ttu-id="d623e-114">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="d623e-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="d623e-115">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="d623e-115">-EndpointName</span></span>
<span data-ttu-id="d623e-116">이 cmdlet이 제거 하는 끝점의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d623e-116">Specifies the name of the endpoint that this cmdlet removes.</span></span>

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

### <span data-ttu-id="d623e-117">-Force</span><span class="sxs-lookup"><span data-stu-id="d623e-117">-Force</span></span>
<span data-ttu-id="d623e-118">사용자 확인을 요청 하지 않고 명령을 강제로 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="d623e-118">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="d623e-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="d623e-119">-PassThru</span></span>
<span data-ttu-id="d623e-120">작업 중인 항목을 나타내는 개체를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="d623e-120">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="d623e-121">기본적으로이 cmdlet은 출력을 생성 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="d623e-121">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="d623e-122">-/Profile</span><span class="sxs-lookup"><span data-stu-id="d623e-122">-ProfileName</span></span>
<span data-ttu-id="d623e-123">종점이 속한 프로필의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d623e-123">Specifies the name of the profile to which the endpoint belongs.</span></span>

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

### <span data-ttu-id="d623e-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d623e-124">-ResourceGroupName</span></span>
<span data-ttu-id="d623e-125">끝점이 속한 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d623e-125">Specifies the name of the resource group to which the endpoint belongs.</span></span>

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

### <span data-ttu-id="d623e-126">-확인</span><span class="sxs-lookup"><span data-stu-id="d623e-126">-Confirm</span></span>
<span data-ttu-id="d623e-127">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="d623e-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d623e-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d623e-128">-WhatIf</span></span>
<span data-ttu-id="d623e-129">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="d623e-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d623e-130">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="d623e-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d623e-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d623e-131">CommonParameters</span></span>
<span data-ttu-id="d623e-132">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="d623e-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d623e-133">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="d623e-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d623e-134">입력</span><span class="sxs-lookup"><span data-stu-id="d623e-134">INPUTS</span></span>

### <span data-ttu-id="d623e-135">Microsoft. Cdn. Endpoint. PSEndpoint</span><span class="sxs-lookup"><span data-stu-id="d623e-135">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSEndpoint</span></span>

### <span data-ttu-id="d623e-136">System.webserver 매개 변수</span><span class="sxs-lookup"><span data-stu-id="d623e-136">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="d623e-137">출력</span><span class="sxs-lookup"><span data-stu-id="d623e-137">OUTPUTS</span></span>

### <span data-ttu-id="d623e-138">시스템 부울</span><span class="sxs-lookup"><span data-stu-id="d623e-138">System.Boolean</span></span>

## <span data-ttu-id="d623e-139">상속자</span><span class="sxs-lookup"><span data-stu-id="d623e-139">NOTES</span></span>

## <span data-ttu-id="d623e-140">관련 링크</span><span class="sxs-lookup"><span data-stu-id="d623e-140">RELATED LINKS</span></span>

[<span data-ttu-id="d623e-141">Get-AzCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="d623e-141">Get-AzCdnEndpoint</span></span>](./Get-AzCdnEndpoint.md)

[<span data-ttu-id="d623e-142">새로운 AzCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="d623e-142">New-AzCdnEndpoint</span></span>](./New-AzCdnEndpoint.md)

[<span data-ttu-id="d623e-143">Set-AzCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="d623e-143">Set-AzCdnEndpoint</span></span>](./Set-AzCdnEndpoint.md)

[<span data-ttu-id="d623e-144">시작-AzCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="d623e-144">Start-AzCdnEndpoint</span></span>](./Start-AzCdnEndpoint.md)

[<span data-ttu-id="d623e-145">중지-AzCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="d623e-145">Stop-AzCdnEndpoint</span></span>](./Stop-AzCdnEndpoint.md)


