---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
ms.assetid: 3A4F8442-1268-44BC-91ED-47C03CD20C47
online version: https://docs.microsoft.com/powershell/module/az.cdn/remove-azcdnprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Remove-AzCdnProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Remove-AzCdnProfile.md
ms.openlocfilehash: 904af1f1d1f6cba7bd0a44ee0811b55fef01e106
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101996898"
---
# <span data-ttu-id="94571-101">Remove-AzCdnProfile</span><span class="sxs-lookup"><span data-stu-id="94571-101">Remove-AzCdnProfile</span></span>

## <span data-ttu-id="94571-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="94571-102">SYNOPSIS</span></span>
<span data-ttu-id="94571-103">CDN 프로필을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="94571-103">Removes a CDN profile.</span></span>

## <span data-ttu-id="94571-104">구문</span><span class="sxs-lookup"><span data-stu-id="94571-104">SYNTAX</span></span>

### <span data-ttu-id="94571-105">ByFieldsParameterSet</span><span class="sxs-lookup"><span data-stu-id="94571-105">ByFieldsParameterSet</span></span>
```
Remove-AzCdnProfile -ProfileName <String> -ResourceGroupName <String> [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="94571-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="94571-106">ByObjectParameterSet</span></span>
```
Remove-AzCdnProfile -CdnProfile <PSProfile> [-PassThru] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="94571-107">설명</span><span class="sxs-lookup"><span data-stu-id="94571-107">DESCRIPTION</span></span>
<span data-ttu-id="94571-108">**Remove-AzCdnProfile** cmdlet은 CDN(Azure Content Delivery Network) 프로필을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="94571-108">The **Remove-AzCdnProfile** cmdlet removes a Azure Content Delivery Network (CDN) profile.</span></span>

## <span data-ttu-id="94571-109">예제</span><span class="sxs-lookup"><span data-stu-id="94571-109">EXAMPLES</span></span>

## <span data-ttu-id="94571-110">매개 변수</span><span class="sxs-lookup"><span data-stu-id="94571-110">PARAMETERS</span></span>

### <span data-ttu-id="94571-111">-CdnProfile</span><span class="sxs-lookup"><span data-stu-id="94571-111">-CdnProfile</span></span>
<span data-ttu-id="94571-112">이 cmdlet이 제거한 프로필을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="94571-112">Specifies the profile that this cmdlet removes.</span></span>

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

### <span data-ttu-id="94571-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="94571-113">-DefaultProfile</span></span>
<span data-ttu-id="94571-114">azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독</span><span class="sxs-lookup"><span data-stu-id="94571-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="94571-115">-Force</span><span class="sxs-lookup"><span data-stu-id="94571-115">-Force</span></span>
<span data-ttu-id="94571-116">사용자 확인을 요청하지 않고 명령을 강제로 실행합니다.</span><span class="sxs-lookup"><span data-stu-id="94571-116">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="94571-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="94571-117">-PassThru</span></span>
<span data-ttu-id="94571-118">작업하는 항목을 나타내는 개체를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="94571-118">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="94571-119">기본적으로 이 cmdlet은 출력을 생성하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="94571-119">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="94571-120">-ProfileName</span><span class="sxs-lookup"><span data-stu-id="94571-120">-ProfileName</span></span>
<span data-ttu-id="94571-121">이 cmdlet에서 제거한 프로필의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="94571-121">Specifies the name of the profile that this cmdlet removes.</span></span>

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

### <span data-ttu-id="94571-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="94571-122">-ResourceGroupName</span></span>
<span data-ttu-id="94571-123">프로필이 속한 리소스 그룹의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="94571-123">Specifies the name of the resource group to which the profile belongs.</span></span>

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

### <span data-ttu-id="94571-124">-확인</span><span class="sxs-lookup"><span data-stu-id="94571-124">-Confirm</span></span>
<span data-ttu-id="94571-125">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="94571-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="94571-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="94571-126">-WhatIf</span></span>
<span data-ttu-id="94571-127">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="94571-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="94571-128">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="94571-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="94571-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="94571-129">CommonParameters</span></span>
<span data-ttu-id="94571-130">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="94571-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="94571-131">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="94571-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="94571-132">입력</span><span class="sxs-lookup"><span data-stu-id="94571-132">INPUTS</span></span>

### <span data-ttu-id="94571-133">Microsoft.Azure.Commands.Cdn.Models.Profile.PSProfile</span><span class="sxs-lookup"><span data-stu-id="94571-133">Microsoft.Azure.Commands.Cdn.Models.Profile.PSProfile</span></span>

### <span data-ttu-id="94571-134">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="94571-134">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="94571-135">출력</span><span class="sxs-lookup"><span data-stu-id="94571-135">OUTPUTS</span></span>

### <span data-ttu-id="94571-136">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="94571-136">System.Boolean</span></span>

## <span data-ttu-id="94571-137">참고 사항</span><span class="sxs-lookup"><span data-stu-id="94571-137">NOTES</span></span>

## <span data-ttu-id="94571-138">관련 링크</span><span class="sxs-lookup"><span data-stu-id="94571-138">RELATED LINKS</span></span>

[<span data-ttu-id="94571-139">Get-AzCdnProfile</span><span class="sxs-lookup"><span data-stu-id="94571-139">Get-AzCdnProfile</span></span>](./Get-AzCdnProfile.md)

[<span data-ttu-id="94571-140">New-AzCdnProfile</span><span class="sxs-lookup"><span data-stu-id="94571-140">New-AzCdnProfile</span></span>](./New-AzCdnProfile.md)

[<span data-ttu-id="94571-141">Set-AzCdnProfile</span><span class="sxs-lookup"><span data-stu-id="94571-141">Set-AzCdnProfile</span></span>](./Set-AzCdnProfile.md)


