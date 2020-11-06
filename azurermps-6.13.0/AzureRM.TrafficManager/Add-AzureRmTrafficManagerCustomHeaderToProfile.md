---
external help file: Microsoft.Azure.Commands.TrafficManager.dll-Help.xml
Module Name: AzureRM.TrafficManager
ms.assetid: 25E3F297-1D91-4102-B4D3-1E7195A5D33F
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.trafficmanager/add-azurertmtrafficmanagercustomheadertoprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/TrafficManager/Commands.TrafficManager2/help/Add-AzureRmTrafficManagerCustomHeaderToProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/TrafficManager/Commands.TrafficManager2/help/Add-AzureRmTrafficManagerCustomHeaderToProfile.md
ms.openlocfilehash: c14854da187101f3b15db178c656005942c1bff0
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93536468"
---
# <span data-ttu-id="f3f75-101">Add-AzureRmTrafficManagerCustomHeaderToProfile</span><span class="sxs-lookup"><span data-stu-id="f3f75-101">Add-AzureRmTrafficManagerCustomHeaderToProfile</span></span>

## <span data-ttu-id="f3f75-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f3f75-102">SYNOPSIS</span></span>
<span data-ttu-id="f3f75-103">로컬 Traffic Manager 프로필 개체에 사용자 지정 헤더 정보를 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="f3f75-103">Adds custom header information to a local Traffic Manager profile object.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f3f75-104">구문과</span><span class="sxs-lookup"><span data-stu-id="f3f75-104">SYNTAX</span></span>

```
Add-AzureRmTrafficManagerCustomHeaderToProfile -Name <String> -Value <String>
 -TrafficManagerProfile <TrafficManagerProfile> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="f3f75-105">설명은</span><span class="sxs-lookup"><span data-stu-id="f3f75-105">DESCRIPTION</span></span>
<span data-ttu-id="f3f75-106">**Add-AzureRmTrafficManagerCustomHeaderToProfile** cmdlet은 사용자 지정 헤더 정보를 로컬 Azure Traffic Manager 프로필 개체에 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="f3f75-106">The **Add-AzureRmTrafficManagerCustomHeaderToProfile** cmdlet adds custom header information to a local Azure Traffic Manager profile object.</span></span>
<span data-ttu-id="f3f75-107">New-AzureRmTrafficManagerProfile 또는 Get-AzureRmTrafficManagerProfile cmdlet을 사용 하 여 프로필을 가져올 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="f3f75-107">You can get a profile by using the New-AzureRmTrafficManagerProfile or Get-AzureRmTrafficManagerProfile cmdlets.</span></span>

<span data-ttu-id="f3f75-108">이 cmdlet은 로컬 프로필 개체에서 작동 합니다.</span><span class="sxs-lookup"><span data-stu-id="f3f75-108">This cmdlet operates on the local profile object.</span></span>
<span data-ttu-id="f3f75-109">Set-AzureRmTrafficManagerProfile cmdlet을 사용 하 여 트래픽 관리자의 프로필에 대 한 변경 내용을 커밋합니다.</span><span class="sxs-lookup"><span data-stu-id="f3f75-109">Commit your changes to the profile for Traffic Manager by using the Set-AzureRmTrafficManagerProfile cmdlet.</span></span>

## <span data-ttu-id="f3f75-110">예제의</span><span class="sxs-lookup"><span data-stu-id="f3f75-110">EXAMPLES</span></span>

### <span data-ttu-id="f3f75-111">예제 1: 프로필에 사용자 지정 헤더 정보 추가</span><span class="sxs-lookup"><span data-stu-id="f3f75-111">Example 1: Add custom header information to a profile</span></span>
```
PS C:\> $TrafficManagerProfile = Get-AzureRmTrafficManagerProfile -Name "ContosoProfile" -ResourceGroupName "ResourceGroup11"
PS C:\> Add-AzureRmTrafficManagerCustomHeaderToProfile -TrafficManagerProfile $TrafficManagerProfile -Name "host" -Value "www.contoso.com"
PS C:\> Set-AzureRmTrafficManagerProfile -TrafficManagerProfile $TrafficManagerProfile
```

<span data-ttu-id="f3f75-112">첫 번째 명령은 **AzureRmTrafficManagerProfile** cmdlet을 사용 하 여 Azure Traffic Manager 프로필을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="f3f75-112">The first command gets an Azure Traffic Manager profile by using the **Get-AzureRmTrafficManagerProfile** cmdlet.</span></span>
<span data-ttu-id="f3f75-113">명령은 로컬 프로필을 $TrafficManagerProfile 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="f3f75-113">The command stores the local profile in the $TrafficManagerProfile variable.</span></span>
<span data-ttu-id="f3f75-114">두 번째 명령은 $TrafficManagerProfile에 저장 된 프로필에 사용자 지정 헤더 정보를 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="f3f75-114">The second command adds custom header information to the profile stored in $TrafficManagerProfile.</span></span>
<span data-ttu-id="f3f75-115">마지막 명령은 $TrafficManagerProfile의 로컬 값과 일치 하도록 Traffic Manager에서 프로필을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="f3f75-115">The final command updates the profile in Traffic Manager to match the local value in $TrafficManagerProfile.</span></span>

## <span data-ttu-id="f3f75-116">변수</span><span class="sxs-lookup"><span data-stu-id="f3f75-116">PARAMETERS</span></span>

### <span data-ttu-id="f3f75-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f3f75-117">-DefaultProfile</span></span>
<span data-ttu-id="f3f75-118">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="f3f75-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f3f75-119">-이름</span><span class="sxs-lookup"><span data-stu-id="f3f75-119">-Name</span></span>
<span data-ttu-id="f3f75-120">추가할 사용자 지정 머리글 정보의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="f3f75-120">Specifies the name of the custom header information to be added.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f3f75-121">-TrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="f3f75-121">-TrafficManagerProfile</span></span>
<span data-ttu-id="f3f75-122">로컬 **TrafficManagerProfile** 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="f3f75-122">Specifies a local **TrafficManagerProfile** object.</span></span>
<span data-ttu-id="f3f75-123">이 cmdlet은이 로컬 개체를 수정 합니다.</span><span class="sxs-lookup"><span data-stu-id="f3f75-123">This cmdlet modifies this local object.</span></span>
<span data-ttu-id="f3f75-124">**TrafficManagerProfile** 개체를 가져오려면 Get-AzureRmTrafficManagerProfile cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="f3f75-124">To obtain a **TrafficManagerProfile** object, use the Get-AzureRmTrafficManagerProfile cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerProfile
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f3f75-125">-값</span><span class="sxs-lookup"><span data-stu-id="f3f75-125">-Value</span></span>
<span data-ttu-id="f3f75-126">추가할 사용자 지정 헤더 정보의 값을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="f3f75-126">Specifies the value of the custom header information to be added.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f3f75-127">-확인</span><span class="sxs-lookup"><span data-stu-id="f3f75-127">-Confirm</span></span>
<span data-ttu-id="f3f75-128">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="f3f75-128">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f3f75-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f3f75-129">-WhatIf</span></span>
<span data-ttu-id="f3f75-130">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="f3f75-130">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="f3f75-131">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="f3f75-131">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f3f75-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f3f75-132">CommonParameters</span></span>
<span data-ttu-id="f3f75-133">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="f3f75-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f3f75-134">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f3f75-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f3f75-135">입력</span><span class="sxs-lookup"><span data-stu-id="f3f75-135">INPUTS</span></span>

### <span data-ttu-id="f3f75-136">TrafficManagerProfile (Network.)</span><span class="sxs-lookup"><span data-stu-id="f3f75-136">Microsoft.Azure.Commands.Network.TrafficManagerProfile</span></span>
<span data-ttu-id="f3f75-137">이 cmdlet은이 cmdlet에 대 한 **TrafficManagerProfile** 개체를 허용 합니다.</span><span class="sxs-lookup"><span data-stu-id="f3f75-137">This cmdlet accepts a **TrafficManagerProfile** object to this cmdlet.</span></span>

## <span data-ttu-id="f3f75-138">출력</span><span class="sxs-lookup"><span data-stu-id="f3f75-138">OUTPUTS</span></span>

### <span data-ttu-id="f3f75-139">TrafficManagerProfile (Network.)</span><span class="sxs-lookup"><span data-stu-id="f3f75-139">Microsoft.Azure.Commands.Network.TrafficManagerProfile</span></span>
<span data-ttu-id="f3f75-140">이 cmdlet은 수정 된 **TrafficManagerProfile** 개체를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="f3f75-140">This cmdlet returns a modified **TrafficManagerProfile** object.</span></span>

## <span data-ttu-id="f3f75-141">상속자</span><span class="sxs-lookup"><span data-stu-id="f3f75-141">NOTES</span></span>

## <span data-ttu-id="f3f75-142">관련 링크</span><span class="sxs-lookup"><span data-stu-id="f3f75-142">RELATED LINKS</span></span>

[<span data-ttu-id="f3f75-143">제거-AzureRmTrafficManagerCustomHeaderFromProfile</span><span class="sxs-lookup"><span data-stu-id="f3f75-143">Remove-AzureRmTrafficManagerCustomHeaderFromProfile</span></span>](./Remove-AzureRmTrafficManagerCustomHeaderFromProfile.md)

[<span data-ttu-id="f3f75-144">Get-AzureRmTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="f3f75-144">Get-AzureRmTrafficManagerProfile</span></span>](./Get-AzureRmTrafficManagerProfile.md)

[<span data-ttu-id="f3f75-145">Set-AzureRmTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="f3f75-145">Set-AzureRmTrafficManagerProfile</span></span>](./Set-AzureRmTrafficManagerProfile.md)
