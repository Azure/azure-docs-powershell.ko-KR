---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
ms.assetid: 3A4F8442-1268-44BC-91ED-47C03CD20C47
online version: https://docs.microsoft.com/en-us/powershell/module/az.cdn/remove-azcdnprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Remove-AzCdnProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Remove-AzCdnProfile.md
ms.openlocfilehash: ba45ea8d4c1b58290623f7f415f09cdb7663f575
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94042830"
---
# <span data-ttu-id="83093-101">Remove-AzCdnProfile</span><span class="sxs-lookup"><span data-stu-id="83093-101">Remove-AzCdnProfile</span></span>

## <span data-ttu-id="83093-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="83093-102">SYNOPSIS</span></span>
<span data-ttu-id="83093-103">CDN 프로필을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="83093-103">Removes a CDN profile.</span></span>

## <span data-ttu-id="83093-104">구문과</span><span class="sxs-lookup"><span data-stu-id="83093-104">SYNTAX</span></span>

### <span data-ttu-id="83093-105">ByFieldsParameterSet</span><span class="sxs-lookup"><span data-stu-id="83093-105">ByFieldsParameterSet</span></span>
```
Remove-AzCdnProfile -ProfileName <String> -ResourceGroupName <String> [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="83093-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="83093-106">ByObjectParameterSet</span></span>
```
Remove-AzCdnProfile -CdnProfile <PSProfile> [-PassThru] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="83093-107">설명은</span><span class="sxs-lookup"><span data-stu-id="83093-107">DESCRIPTION</span></span>
<span data-ttu-id="83093-108">**AzCdnProfile** Cmdlet은 Azure CDN (콘텐츠 배달 네트워크) 프로필을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="83093-108">The **Remove-AzCdnProfile** cmdlet removes a Azure Content Delivery Network (CDN) profile.</span></span>

## <span data-ttu-id="83093-109">예제의</span><span class="sxs-lookup"><span data-stu-id="83093-109">EXAMPLES</span></span>

## <span data-ttu-id="83093-110">변수</span><span class="sxs-lookup"><span data-stu-id="83093-110">PARAMETERS</span></span>

### <span data-ttu-id="83093-111">-CdnProfile</span><span class="sxs-lookup"><span data-stu-id="83093-111">-CdnProfile</span></span>
<span data-ttu-id="83093-112">이 cmdlet이 제거 하는 프로필을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="83093-112">Specifies the profile that this cmdlet removes.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Cdn.Models.Profile.PSProfile
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="83093-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="83093-113">-DefaultProfile</span></span>
<span data-ttu-id="83093-114">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="83093-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="83093-115">-Force</span><span class="sxs-lookup"><span data-stu-id="83093-115">-Force</span></span>
<span data-ttu-id="83093-116">사용자 확인을 요청 하지 않고 명령을 강제로 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="83093-116">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="83093-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="83093-117">-PassThru</span></span>
<span data-ttu-id="83093-118">작업 중인 항목을 나타내는 개체를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="83093-118">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="83093-119">기본적으로이 cmdlet은 출력을 생성 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="83093-119">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="83093-120">-/Profile</span><span class="sxs-lookup"><span data-stu-id="83093-120">-ProfileName</span></span>
<span data-ttu-id="83093-121">이 cmdlet이 제거 하는 프로필의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="83093-121">Specifies the name of the profile that this cmdlet removes.</span></span>

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

### <span data-ttu-id="83093-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="83093-122">-ResourceGroupName</span></span>
<span data-ttu-id="83093-123">프로필이 속한 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="83093-123">Specifies the name of the resource group to which the profile belongs.</span></span>

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

### <span data-ttu-id="83093-124">-확인</span><span class="sxs-lookup"><span data-stu-id="83093-124">-Confirm</span></span>
<span data-ttu-id="83093-125">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="83093-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="83093-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="83093-126">-WhatIf</span></span>
<span data-ttu-id="83093-127">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="83093-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="83093-128">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="83093-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="83093-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="83093-129">CommonParameters</span></span>
<span data-ttu-id="83093-130">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="83093-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="83093-131">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="83093-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="83093-132">입력</span><span class="sxs-lookup"><span data-stu-id="83093-132">INPUTS</span></span>

### <span data-ttu-id="83093-133">Microsoft. Cdn. 프로필. PSProfile</span><span class="sxs-lookup"><span data-stu-id="83093-133">Microsoft.Azure.Commands.Cdn.Models.Profile.PSProfile</span></span>

### <span data-ttu-id="83093-134">System.webserver 매개 변수</span><span class="sxs-lookup"><span data-stu-id="83093-134">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="83093-135">출력</span><span class="sxs-lookup"><span data-stu-id="83093-135">OUTPUTS</span></span>

### <span data-ttu-id="83093-136">시스템 부울</span><span class="sxs-lookup"><span data-stu-id="83093-136">System.Boolean</span></span>

## <span data-ttu-id="83093-137">상속자</span><span class="sxs-lookup"><span data-stu-id="83093-137">NOTES</span></span>

## <span data-ttu-id="83093-138">관련 링크</span><span class="sxs-lookup"><span data-stu-id="83093-138">RELATED LINKS</span></span>

[<span data-ttu-id="83093-139">Get-AzCdnProfile</span><span class="sxs-lookup"><span data-stu-id="83093-139">Get-AzCdnProfile</span></span>](./Get-AzCdnProfile.md)

[<span data-ttu-id="83093-140">새로운 AzCdnProfile</span><span class="sxs-lookup"><span data-stu-id="83093-140">New-AzCdnProfile</span></span>](./New-AzCdnProfile.md)

[<span data-ttu-id="83093-141">Set-AzCdnProfile</span><span class="sxs-lookup"><span data-stu-id="83093-141">Set-AzCdnProfile</span></span>](./Set-AzCdnProfile.md)


