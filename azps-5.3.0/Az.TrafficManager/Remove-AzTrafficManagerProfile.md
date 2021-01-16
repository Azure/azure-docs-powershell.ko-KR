---
external help file: Microsoft.Azure.PowerShell.Cmdlets.TrafficManager.dll-Help.xml
Module Name: Az.TrafficManager
ms.assetid: 5A4D685F-B904-4C85-8B68-C9936B0627FA
online version: https://docs.microsoft.com/en-us/powershell/module/az.trafficmanager/remove-aztrafficmanagerprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Remove-AzTrafficManagerProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Remove-AzTrafficManagerProfile.md
ms.openlocfilehash: 640aed5ccfb38a2dca6989048e3185774ceda15a
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98375817"
---
# <span data-ttu-id="817d4-101">Remove-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="817d4-101">Remove-AzTrafficManagerProfile</span></span>

## <span data-ttu-id="817d4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="817d4-102">SYNOPSIS</span></span>
<span data-ttu-id="817d4-103">Traffic Manager 프로필을 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="817d4-103">Deletes a Traffic Manager profile.</span></span>

## <span data-ttu-id="817d4-104">구문</span><span class="sxs-lookup"><span data-stu-id="817d4-104">SYNTAX</span></span>

### <span data-ttu-id="817d4-105">필드</span><span class="sxs-lookup"><span data-stu-id="817d4-105">Fields</span></span>
```
Remove-AzTrafficManagerProfile -Name <String> -ResourceGroupName <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="817d4-106">개체</span><span class="sxs-lookup"><span data-stu-id="817d4-106">Object</span></span>
```
Remove-AzTrafficManagerProfile -TrafficManagerProfile <TrafficManagerProfile> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="817d4-107">설명</span><span class="sxs-lookup"><span data-stu-id="817d4-107">DESCRIPTION</span></span>
<span data-ttu-id="817d4-108">**Remove-AzTrafficManagerProfile** cmdlet은 Azure Traffic Manager 프로필을 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="817d4-108">The **Remove-AzTrafficManagerProfile** cmdlet deletes an Azure Traffic Manager profile.</span></span>
<span data-ttu-id="817d4-109">*이름* 및 *ResourceGroupName* 매개 변수를 사용하여 삭제할 프로필을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="817d4-109">Specify the profile to delete by using the *Name* and *ResourceGroupName* parameters.</span></span>
<span data-ttu-id="817d4-110">또는 **TrafficManagerProfile** 매개 변수를 사용하여 *TrafficManagerProfile* 개체를 지정하거나 파이프라인을 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="817d4-110">Alternatively, you can specify a **TrafficManagerProfile** object using the *TrafficManagerProfile* parameter, or you can use the pipeline.</span></span>

## <span data-ttu-id="817d4-111">예제</span><span class="sxs-lookup"><span data-stu-id="817d4-111">EXAMPLES</span></span>

### <span data-ttu-id="817d4-112">예제 1: 이름으로 지정된 프로필 삭제</span><span class="sxs-lookup"><span data-stu-id="817d4-112">Example 1: Delete a profile specified by name</span></span>
```
PS C:\>Remove-AzTrafficManagerProfile -Name "ContosoProfile" -ResourceGroupName "ResourceGroup11"
```

<span data-ttu-id="817d4-113">이 명령은 ResourceGroup11에서 ContosoProfile이라는 프로필을 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="817d4-113">This command deletes the profile named ContosoProfile in ResourceGroup11.</span></span>
<span data-ttu-id="817d4-114">이 명령은 확인을 요청하는 메시지를 제공합니다.</span><span class="sxs-lookup"><span data-stu-id="817d4-114">The command prompts you for confirmation.</span></span>

### <span data-ttu-id="817d4-115">예제 2: 파이프라인을 사용하여 프로필 삭제</span><span class="sxs-lookup"><span data-stu-id="817d4-115">Example 2: Delete a profile by using the pipeline</span></span>
```
PS C:\>Get-AzTrafficManagerProfile -Name "ContosoProfile" -ResourceGroupName "ResourceGroup11" | Remove-AzTrafficManagerProfile -Force
```

<span data-ttu-id="817d4-116">이 명령은 ResourceGroup11에서 ContosoProfile이라는 프로필을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="817d4-116">This command gets the profile named ContosoProfile in ResourceGroup11.</span></span>
<span data-ttu-id="817d4-117">그런 다음 이 명령은 파이프라인 연산자를 사용하여 **Remove-AzTrafficManagerProfile** cmdlet에 해당 프로필을 전달합니다.</span><span class="sxs-lookup"><span data-stu-id="817d4-117">The command then passes that profile to the **Remove-AzTrafficManagerProfile** cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="817d4-118">해당 cmdlet은 해당 프로필을 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="817d4-118">That cmdlet deletes that profile.</span></span>
<span data-ttu-id="817d4-119">이 명령은 Force 매개 *변수를 지정합니다.*</span><span class="sxs-lookup"><span data-stu-id="817d4-119">The command specifies the *Force* parameter.</span></span>
<span data-ttu-id="817d4-120">따라서 확인을 묻는 메시지가 표시되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="817d4-120">Therefore, it does not prompt you for confirmation.</span></span>

## <span data-ttu-id="817d4-121">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="817d4-121">PARAMETERS</span></span>

### <span data-ttu-id="817d4-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="817d4-122">-DefaultProfile</span></span>
<span data-ttu-id="817d4-123">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="817d4-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="817d4-124">-Force</span><span class="sxs-lookup"><span data-stu-id="817d4-124">-Force</span></span>
<span data-ttu-id="817d4-125">사용자 확인을 요청하지 않고 명령을 강제로 실행합니다.</span><span class="sxs-lookup"><span data-stu-id="817d4-125">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="817d4-126">-Name</span><span class="sxs-lookup"><span data-stu-id="817d4-126">-Name</span></span>
<span data-ttu-id="817d4-127">이 cmdlet이 삭제하는 Traffic Manager 프로필의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="817d4-127">Specifies the name of the Traffic Manager profile that this cmdlet deletes.</span></span>

```yaml
Type: System.String
Parameter Sets: Fields
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="817d4-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="817d4-128">-ResourceGroupName</span></span>
<span data-ttu-id="817d4-129">리소스 그룹의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="817d4-129">Specifies the name of a resource group.</span></span>
<span data-ttu-id="817d4-130">이 cmdlet은 이 매개 변수가 지정하는 그룹에서 Traffic Manager 프로필을 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="817d4-130">This cmdlet deletes a Traffic Manager profile in the group that this parameter specifies.</span></span>

```yaml
Type: System.String
Parameter Sets: Fields
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="817d4-131">-TrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="817d4-131">-TrafficManagerProfile</span></span>
<span data-ttu-id="817d4-132">삭제할 **TrafficManagerProfile** 개체를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="817d4-132">Specifies a **TrafficManagerProfile** object to delete.</span></span>
<span data-ttu-id="817d4-133">**TrafficManagerProfile** 개체를 얻습니다. Get-AzTrafficManagerProfile cmdlet을 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="817d4-133">To obtain a **TrafficManagerProfile** object, use the Get-AzTrafficManagerProfile cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerProfile
Parameter Sets: Object
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="817d4-134">-Confirm</span><span class="sxs-lookup"><span data-stu-id="817d4-134">-Confirm</span></span>
<span data-ttu-id="817d4-135">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="817d4-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="817d4-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="817d4-136">-WhatIf</span></span>
<span data-ttu-id="817d4-137">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="817d4-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="817d4-138">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="817d4-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="817d4-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="817d4-139">CommonParameters</span></span>
<span data-ttu-id="817d4-140">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="817d4-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="817d4-141">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="817d4-141">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="817d4-142">입력</span><span class="sxs-lookup"><span data-stu-id="817d4-142">INPUTS</span></span>

### <span data-ttu-id="817d4-143">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="817d4-143">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerProfile</span></span>

## <span data-ttu-id="817d4-144">출력</span><span class="sxs-lookup"><span data-stu-id="817d4-144">OUTPUTS</span></span>

### <span data-ttu-id="817d4-145">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="817d4-145">System.Boolean</span></span>

## <span data-ttu-id="817d4-146">참고 사항</span><span class="sxs-lookup"><span data-stu-id="817d4-146">NOTES</span></span>

## <span data-ttu-id="817d4-147">관련 링크</span><span class="sxs-lookup"><span data-stu-id="817d4-147">RELATED LINKS</span></span>

[<span data-ttu-id="817d4-148">Disable-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="817d4-148">Disable-AzTrafficManagerProfile</span></span>](./Disable-AzTrafficManagerProfile.md)

[<span data-ttu-id="817d4-149">Enable-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="817d4-149">Enable-AzTrafficManagerProfile</span></span>](./Enable-AzTrafficManagerProfile.md)

[<span data-ttu-id="817d4-150">Get-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="817d4-150">Get-AzTrafficManagerProfile</span></span>](./Get-AzTrafficManagerProfile.md)

[<span data-ttu-id="817d4-151">New-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="817d4-151">New-AzTrafficManagerProfile</span></span>](./New-AzTrafficManagerProfile.md)

[<span data-ttu-id="817d4-152">Set-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="817d4-152">Set-AzTrafficManagerProfile</span></span>](./Set-AzTrafficManagerProfile.md)


