---
external help file: Microsoft.Azure.Commands.Cdn.dll-Help.xml
Module Name: AzureRM.Cdn
ms.assetid: 3A4F8442-1268-44BC-91ED-47C03CD20C47
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.cdn/remove-azurermcdnprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Cdn/Commands.Cdn/help/Remove-AzureRmCdnProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Cdn/Commands.Cdn/help/Remove-AzureRmCdnProfile.md
ms.openlocfilehash: 0c39e6ee26faffc9c12e2fc3b5f00ccaadfa9389
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93531425"
---
# <span data-ttu-id="39417-101">Remove-AzureRmCdnProfile</span><span class="sxs-lookup"><span data-stu-id="39417-101">Remove-AzureRmCdnProfile</span></span>

## <span data-ttu-id="39417-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="39417-102">SYNOPSIS</span></span>
<span data-ttu-id="39417-103">CDN 프로필을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="39417-103">Removes a CDN profile.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="39417-104">구문과</span><span class="sxs-lookup"><span data-stu-id="39417-104">SYNTAX</span></span>

### <span data-ttu-id="39417-105">ByFieldsParameterSet</span><span class="sxs-lookup"><span data-stu-id="39417-105">ByFieldsParameterSet</span></span>
```
Remove-AzureRmCdnProfile -ProfileName <String> -ResourceGroupName <String> [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="39417-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="39417-106">ByObjectParameterSet</span></span>
```
Remove-AzureRmCdnProfile -CdnProfile <PSProfile> [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="39417-107">설명은</span><span class="sxs-lookup"><span data-stu-id="39417-107">DESCRIPTION</span></span>
<span data-ttu-id="39417-108">**AzureRmCdnProfile** Cmdlet은 Azure CDN (콘텐츠 배달 네트워크) 프로필을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="39417-108">The **Remove-AzureRmCdnProfile** cmdlet removes a Azure Content Delivery Network (CDN) profile.</span></span>

## <span data-ttu-id="39417-109">예제의</span><span class="sxs-lookup"><span data-stu-id="39417-109">EXAMPLES</span></span>

## <span data-ttu-id="39417-110">변수</span><span class="sxs-lookup"><span data-stu-id="39417-110">PARAMETERS</span></span>

### <span data-ttu-id="39417-111">-CdnProfile</span><span class="sxs-lookup"><span data-stu-id="39417-111">-CdnProfile</span></span>
<span data-ttu-id="39417-112">이 cmdlet이 제거 하는 프로필을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="39417-112">Specifies the profile that this cmdlet removes.</span></span>

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

### <span data-ttu-id="39417-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="39417-113">-DefaultProfile</span></span>
<span data-ttu-id="39417-114">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="39417-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="39417-115">-Force</span><span class="sxs-lookup"><span data-stu-id="39417-115">-Force</span></span>
<span data-ttu-id="39417-116">사용자 확인을 요청 하지 않고 명령을 강제로 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="39417-116">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="39417-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="39417-117">-PassThru</span></span>
<span data-ttu-id="39417-118">작업 중인 항목을 나타내는 개체를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="39417-118">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="39417-119">기본적으로이 cmdlet은 출력을 생성 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="39417-119">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="39417-120">-/Profile</span><span class="sxs-lookup"><span data-stu-id="39417-120">-ProfileName</span></span>
<span data-ttu-id="39417-121">이 cmdlet이 제거 하는 프로필의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="39417-121">Specifies the name of the profile that this cmdlet removes.</span></span>

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

### <span data-ttu-id="39417-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="39417-122">-ResourceGroupName</span></span>
<span data-ttu-id="39417-123">프로필이 속한 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="39417-123">Specifies the name of the resource group to which the profile belongs.</span></span>

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

### <span data-ttu-id="39417-124">-확인</span><span class="sxs-lookup"><span data-stu-id="39417-124">-Confirm</span></span>
<span data-ttu-id="39417-125">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="39417-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="39417-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="39417-126">-WhatIf</span></span>
<span data-ttu-id="39417-127">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="39417-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="39417-128">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="39417-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="39417-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="39417-129">CommonParameters</span></span>
<span data-ttu-id="39417-130">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="39417-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="39417-131">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="39417-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="39417-132">입력</span><span class="sxs-lookup"><span data-stu-id="39417-132">INPUTS</span></span>

### <span data-ttu-id="39417-133">Microsoft. Cdn. 프로필. PSProfile</span><span class="sxs-lookup"><span data-stu-id="39417-133">Microsoft.Azure.Commands.Cdn.Models.Profile.PSProfile</span></span>
<span data-ttu-id="39417-134">매개 변수: CdnProfile (ByValue)</span><span class="sxs-lookup"><span data-stu-id="39417-134">Parameters: CdnProfile (ByValue)</span></span>

### <span data-ttu-id="39417-135">System.webserver 매개 변수</span><span class="sxs-lookup"><span data-stu-id="39417-135">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="39417-136">출력</span><span class="sxs-lookup"><span data-stu-id="39417-136">OUTPUTS</span></span>

### <span data-ttu-id="39417-137">시스템 부울</span><span class="sxs-lookup"><span data-stu-id="39417-137">System.Boolean</span></span>

## <span data-ttu-id="39417-138">상속자</span><span class="sxs-lookup"><span data-stu-id="39417-138">NOTES</span></span>

## <span data-ttu-id="39417-139">관련 링크</span><span class="sxs-lookup"><span data-stu-id="39417-139">RELATED LINKS</span></span>

[<span data-ttu-id="39417-140">Get-AzureRMCdnProfile</span><span class="sxs-lookup"><span data-stu-id="39417-140">Get-AzureRMCdnProfile</span></span>](./Get-AzureRMCdnProfile.md)

[<span data-ttu-id="39417-141">새로운 AzureRmCdnProfile</span><span class="sxs-lookup"><span data-stu-id="39417-141">New-AzureRmCdnProfile</span></span>](./New-AzureRmCdnProfile.md)

[<span data-ttu-id="39417-142">Set-AzureRmCdnProfile</span><span class="sxs-lookup"><span data-stu-id="39417-142">Set-AzureRmCdnProfile</span></span>](./Set-AzureRmCdnProfile.md)


