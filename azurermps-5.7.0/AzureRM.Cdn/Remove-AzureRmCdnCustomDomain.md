---
external help file: Microsoft.Azure.Commands.Cdn.dll-Help.xml
Module Name: AzureRM.Cdn
ms.assetid: 5727E2CA-0A0B-4050-9F4A-7E06758D9B53
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.cdn/remove-azurermcdncustomdomain
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Cdn/Commands.Cdn/help/Remove-AzureRmCdnCustomDomain.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Cdn/Commands.Cdn/help/Remove-AzureRmCdnCustomDomain.md
ms.openlocfilehash: 8c6e3629d4ac6e8592370393b94727234a6eb12a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93527008"
---
# <span data-ttu-id="e492f-101">Remove-AzureRmCdnCustomDomain</span><span class="sxs-lookup"><span data-stu-id="e492f-101">Remove-AzureRmCdnCustomDomain</span></span>

## <span data-ttu-id="e492f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e492f-102">SYNOPSIS</span></span>
<span data-ttu-id="e492f-103">사용자 지정 도메인을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="e492f-103">Removes a custom domain.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e492f-104">구문과</span><span class="sxs-lookup"><span data-stu-id="e492f-104">SYNTAX</span></span>

### <span data-ttu-id="e492f-105">ByFieldsParameterSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="e492f-105">ByFieldsParameterSet (Default)</span></span>
```
Remove-AzureRmCdnCustomDomain -CustomDomainName <String> -EndpointName <String> -ProfileName <String>
 -ResourceGroupName <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="e492f-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="e492f-106">ByObjectParameterSet</span></span>
```
Remove-AzureRmCdnCustomDomain -CdnCustomDomain <PSCustomDomain> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e492f-107">설명은</span><span class="sxs-lookup"><span data-stu-id="e492f-107">DESCRIPTION</span></span>
<span data-ttu-id="e492f-108">**AzureRmCdnCustomDomain** CMDLET은 CDN (Azure Content Delivery Network) 끝점에서 사용자 지정 도메인을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="e492f-108">The **Remove-AzureRmCdnCustomDomain** cmdlet removes the custom domain from an Azure Content Delivery Network (CDN) endpoint.</span></span>

## <span data-ttu-id="e492f-109">예제의</span><span class="sxs-lookup"><span data-stu-id="e492f-109">EXAMPLES</span></span>

## <span data-ttu-id="e492f-110">변수</span><span class="sxs-lookup"><span data-stu-id="e492f-110">PARAMETERS</span></span>

### <span data-ttu-id="e492f-111">-CdnCustomDomain</span><span class="sxs-lookup"><span data-stu-id="e492f-111">-CdnCustomDomain</span></span>
<span data-ttu-id="e492f-112">이 cmdlet이 제거 하는 사용자 지정 도메인을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="e492f-112">Specifies the custom domain that this cmdlet removes.</span></span>

```yaml
Type: PSCustomDomain
Parameter Sets: ByObjectParameterSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e492f-113">-CustomDomainName</span><span class="sxs-lookup"><span data-stu-id="e492f-113">-CustomDomainName</span></span>
<span data-ttu-id="e492f-114">이 cmdlet이 제거 하는 사용자 지정 도메인의 리소스 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="e492f-114">Specifies the resource name of the custom domain that this cmdlet removes.</span></span>

```yaml
Type: String
Parameter Sets: ByFieldsParameterSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e492f-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e492f-115">-DefaultProfile</span></span>
<span data-ttu-id="e492f-116">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="e492f-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e492f-117">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="e492f-117">-EndpointName</span></span>
<span data-ttu-id="e492f-118">이 cmdlet이 사용자 지정 도메인을 제거 하는 끝점의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="e492f-118">Specifies the name of the endpoint from which this cmdlet removes a custom domain.</span></span>

```yaml
Type: String
Parameter Sets: ByFieldsParameterSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e492f-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="e492f-119">-PassThru</span></span>
<span data-ttu-id="e492f-120">작업 중인 항목을 나타내는 개체를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="e492f-120">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="e492f-121">기본적으로이 cmdlet은 출력을 생성 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="e492f-121">By default, this cmdlet does not generate any output.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e492f-122">-/Profile</span><span class="sxs-lookup"><span data-stu-id="e492f-122">-ProfileName</span></span>
<span data-ttu-id="e492f-123">이 cmdlet에서 사용자 지정 도메인을 제거 하는 프로필의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="e492f-123">Specifies the name of the profile from which this cmdlet removes a custom domain.</span></span>

```yaml
Type: String
Parameter Sets: ByFieldsParameterSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e492f-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e492f-124">-ResourceGroupName</span></span>
<span data-ttu-id="e492f-125">이 cmdlet이 사용자 지정 도메인을 제거 하는 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="e492f-125">Specifies the name of the resource group from which this cmdlet removes a custom domain.</span></span>

```yaml
Type: String
Parameter Sets: ByFieldsParameterSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e492f-126">-확인</span><span class="sxs-lookup"><span data-stu-id="e492f-126">-Confirm</span></span>
<span data-ttu-id="e492f-127">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="e492f-127">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e492f-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e492f-128">-WhatIf</span></span>
<span data-ttu-id="e492f-129">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="e492f-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e492f-130">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="e492f-130">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e492f-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e492f-131">CommonParameters</span></span>
<span data-ttu-id="e492f-132">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="e492f-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e492f-133">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e492f-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e492f-134">입력</span><span class="sxs-lookup"><span data-stu-id="e492f-134">INPUTS</span></span>

### <span data-ttu-id="e492f-135">PSCustomDomain</span><span class="sxs-lookup"><span data-stu-id="e492f-135">PSCustomDomain</span></span>
<span data-ttu-id="e492f-136">' CdnCustomDomain ' 매개 변수는 파이프라인에서 ' PSCustomDomain ' 형식의 값을 허용 합니다.</span><span class="sxs-lookup"><span data-stu-id="e492f-136">Parameter 'CdnCustomDomain' accepts value of type 'PSCustomDomain' from the pipeline</span></span>

## <span data-ttu-id="e492f-137">출력</span><span class="sxs-lookup"><span data-stu-id="e492f-137">OUTPUTS</span></span>

### <span data-ttu-id="e492f-138">시스템 부울</span><span class="sxs-lookup"><span data-stu-id="e492f-138">System.Boolean</span></span>

## <span data-ttu-id="e492f-139">상속자</span><span class="sxs-lookup"><span data-stu-id="e492f-139">NOTES</span></span>

## <span data-ttu-id="e492f-140">관련 링크</span><span class="sxs-lookup"><span data-stu-id="e492f-140">RELATED LINKS</span></span>

[<span data-ttu-id="e492f-141">Get-AzureRmCdnCustomDomain</span><span class="sxs-lookup"><span data-stu-id="e492f-141">Get-AzureRmCdnCustomDomain</span></span>](./Get-AzureRmCdnCustomDomain.md)

[<span data-ttu-id="e492f-142">새로운 AzureRmCdnCustomDomain</span><span class="sxs-lookup"><span data-stu-id="e492f-142">New-AzureRmCdnCustomDomain</span></span>](./New-AzureRmCdnCustomDomain.md)

[<span data-ttu-id="e492f-143">테스트-AzureRmCdnCustomDomain</span><span class="sxs-lookup"><span data-stu-id="e492f-143">Test-AzureRmCdnCustomDomain</span></span>](./Test-AzureRmCdnCustomDomain.md)


