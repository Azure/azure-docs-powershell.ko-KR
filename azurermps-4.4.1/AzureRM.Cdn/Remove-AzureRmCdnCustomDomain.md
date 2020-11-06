---
external help file: Microsoft.Azure.Commands.Cdn.dll-Help.xml
Module Name: AzureRM.Cdn
ms.assetid: 5727E2CA-0A0B-4050-9F4A-7E06758D9B53
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Cdn/Commands.Cdn/help/Remove-AzureRmCdnCustomDomain.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Cdn/Commands.Cdn/help/Remove-AzureRmCdnCustomDomain.md
ms.openlocfilehash: 2aa6b3932424f7a8375cca2584a7fc7916124c54
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93533135"
---
# <span data-ttu-id="602c3-101">Remove-AzureRmCdnCustomDomain</span><span class="sxs-lookup"><span data-stu-id="602c3-101">Remove-AzureRmCdnCustomDomain</span></span>

## <span data-ttu-id="602c3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="602c3-102">SYNOPSIS</span></span>
<span data-ttu-id="602c3-103">사용자 지정 도메인을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="602c3-103">Removes a custom domain.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="602c3-104">구문과</span><span class="sxs-lookup"><span data-stu-id="602c3-104">SYNTAX</span></span>

### <span data-ttu-id="602c3-105">필드 매개 변수에 대해 설정 되는 매개 변수 (기본값)</span><span class="sxs-lookup"><span data-stu-id="602c3-105">Parameter Set for fields parameters (Default)</span></span>
```
Remove-AzureRmCdnCustomDomain -CustomDomainName <String> -EndpointName <String> -ProfileName <String>
 -ResourceGroupName <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="602c3-106">개체 매개 변수에 대해 설정 되는 매개 변수</span><span class="sxs-lookup"><span data-stu-id="602c3-106">Parameter Set for object parameters</span></span>
```
Remove-AzureRmCdnCustomDomain -CdnCustomDomain <PSCustomDomain> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="602c3-107">설명은</span><span class="sxs-lookup"><span data-stu-id="602c3-107">DESCRIPTION</span></span>
<span data-ttu-id="602c3-108">**AzureRmCdnCustomDomain** CMDLET은 CDN (Azure Content Delivery Network) 끝점에서 사용자 지정 도메인을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="602c3-108">The **Remove-AzureRmCdnCustomDomain** cmdlet removes the custom domain from an Azure Content Delivery Network (CDN) endpoint.</span></span>

## <span data-ttu-id="602c3-109">예제의</span><span class="sxs-lookup"><span data-stu-id="602c3-109">EXAMPLES</span></span>

## <span data-ttu-id="602c3-110">변수</span><span class="sxs-lookup"><span data-stu-id="602c3-110">PARAMETERS</span></span>

### <span data-ttu-id="602c3-111">-CdnCustomDomain</span><span class="sxs-lookup"><span data-stu-id="602c3-111">-CdnCustomDomain</span></span>
<span data-ttu-id="602c3-112">이 cmdlet이 제거 하는 사용자 지정 도메인을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="602c3-112">Specifies the custom domain that this cmdlet removes.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Cdn.Models.CustomDomain.PSCustomDomain
Parameter Sets: Parameter Set for object parameters
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="602c3-113">-CustomDomainName</span><span class="sxs-lookup"><span data-stu-id="602c3-113">-CustomDomainName</span></span>
<span data-ttu-id="602c3-114">이 cmdlet이 제거 하는 사용자 지정 도메인의 리소스 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="602c3-114">Specifies the resource name of the custom domain that this cmdlet removes.</span></span>

```yaml
Type: System.String
Parameter Sets: Parameter Set for fields parameters
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="602c3-115">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="602c3-115">-EndpointName</span></span>
<span data-ttu-id="602c3-116">이 cmdlet이 사용자 지정 도메인을 제거 하는 끝점의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="602c3-116">Specifies the name of the endpoint from which this cmdlet removes a custom domain.</span></span>

```yaml
Type: System.String
Parameter Sets: Parameter Set for fields parameters
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="602c3-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="602c3-117">-PassThru</span></span>
<span data-ttu-id="602c3-118">작업 중인 항목을 나타내는 개체를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="602c3-118">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="602c3-119">기본적으로이 cmdlet은 출력을 생성 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="602c3-119">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="602c3-120">-/Profile</span><span class="sxs-lookup"><span data-stu-id="602c3-120">-ProfileName</span></span>
<span data-ttu-id="602c3-121">이 cmdlet에서 사용자 지정 도메인을 제거 하는 프로필의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="602c3-121">Specifies the name of the profile from which this cmdlet removes a custom domain.</span></span>

```yaml
Type: System.String
Parameter Sets: Parameter Set for fields parameters
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="602c3-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="602c3-122">-ResourceGroupName</span></span>
<span data-ttu-id="602c3-123">이 cmdlet이 사용자 지정 도메인을 제거 하는 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="602c3-123">Specifies the name of the resource group from which this cmdlet removes a custom domain.</span></span>

```yaml
Type: System.String
Parameter Sets: Parameter Set for fields parameters
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="602c3-124">-확인</span><span class="sxs-lookup"><span data-stu-id="602c3-124">-Confirm</span></span>
<span data-ttu-id="602c3-125">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="602c3-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="602c3-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="602c3-126">-WhatIf</span></span>
<span data-ttu-id="602c3-127">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="602c3-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="602c3-128">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="602c3-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="602c3-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="602c3-129">-DefaultProfile</span></span>
<span data-ttu-id="602c3-130">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="602c3-130">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="602c3-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="602c3-131">CommonParameters</span></span>
<span data-ttu-id="602c3-132">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="602c3-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="602c3-133">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="602c3-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="602c3-134">입력</span><span class="sxs-lookup"><span data-stu-id="602c3-134">INPUTS</span></span>

### <span data-ttu-id="602c3-135">PSCustomDomain</span><span class="sxs-lookup"><span data-stu-id="602c3-135">PSCustomDomain</span></span>
<span data-ttu-id="602c3-136">' CdnCustomDomain ' 매개 변수는 파이프라인에서 ' PSCustomDomain ' 형식의 값을 허용 합니다.</span><span class="sxs-lookup"><span data-stu-id="602c3-136">Parameter 'CdnCustomDomain' accepts value of type 'PSCustomDomain' from the pipeline</span></span>

## <span data-ttu-id="602c3-137">출력</span><span class="sxs-lookup"><span data-stu-id="602c3-137">OUTPUTS</span></span>

### <span data-ttu-id="602c3-138">시스템 부울</span><span class="sxs-lookup"><span data-stu-id="602c3-138">System.Boolean</span></span>

## <span data-ttu-id="602c3-139">상속자</span><span class="sxs-lookup"><span data-stu-id="602c3-139">NOTES</span></span>

## <span data-ttu-id="602c3-140">관련 링크</span><span class="sxs-lookup"><span data-stu-id="602c3-140">RELATED LINKS</span></span>

[<span data-ttu-id="602c3-141">Get-AzureRmCdnCustomDomain</span><span class="sxs-lookup"><span data-stu-id="602c3-141">Get-AzureRmCdnCustomDomain</span></span>](./Get-AzureRmCdnCustomDomain.md)

[<span data-ttu-id="602c3-142">새로운 AzureRmCdnCustomDomain</span><span class="sxs-lookup"><span data-stu-id="602c3-142">New-AzureRmCdnCustomDomain</span></span>](./New-AzureRmCdnCustomDomain.md)

[<span data-ttu-id="602c3-143">테스트-AzureRmCdnCustomDomain</span><span class="sxs-lookup"><span data-stu-id="602c3-143">Test-AzureRmCdnCustomDomain</span></span>](./Test-AzureRmCdnCustomDomain.md)


