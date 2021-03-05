---
external help file: Microsoft.Azure.PowerShell.Cmdlets.TrafficManager.dll-Help.xml
Module Name: Az.TrafficManager
ms.assetid: 5A4D685F-B904-4C85-8B68-C9936B0627FA
online version: https://docs.microsoft.com/powershell/module/az.trafficmanager/remove-aztrafficmanagerprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Remove-AzTrafficManagerProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Remove-AzTrafficManagerProfile.md
ms.openlocfilehash: 1b1dab7edc07242dab28daa6028adefb8b7090eb
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101988661"
---
# <span data-ttu-id="40a78-101">Remove-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="40a78-101">Remove-AzTrafficManagerProfile</span></span>

## <span data-ttu-id="40a78-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="40a78-102">SYNOPSIS</span></span>
<span data-ttu-id="40a78-103">Traffic Manager 프로필을 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="40a78-103">Deletes a Traffic Manager profile.</span></span>

## <span data-ttu-id="40a78-104">구문</span><span class="sxs-lookup"><span data-stu-id="40a78-104">SYNTAX</span></span>

### <span data-ttu-id="40a78-105">필드</span><span class="sxs-lookup"><span data-stu-id="40a78-105">Fields</span></span>
```
Remove-AzTrafficManagerProfile -Name <String> -ResourceGroupName <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="40a78-106">개체</span><span class="sxs-lookup"><span data-stu-id="40a78-106">Object</span></span>
```
Remove-AzTrafficManagerProfile -TrafficManagerProfile <TrafficManagerProfile> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="40a78-107">설명</span><span class="sxs-lookup"><span data-stu-id="40a78-107">DESCRIPTION</span></span>
<span data-ttu-id="40a78-108">**Remove-AzTrafficManagerProfile** cmdlet은 Azure Traffic Manager 프로필을 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="40a78-108">The **Remove-AzTrafficManagerProfile** cmdlet deletes an Azure Traffic Manager profile.</span></span>
<span data-ttu-id="40a78-109">이름 및 *ResourceGroupName* 매개 변수를 사용하여 삭제할 프로필을 지정합니다. </span><span class="sxs-lookup"><span data-stu-id="40a78-109">Specify the profile to delete by using the *Name* and *ResourceGroupName* parameters.</span></span>
<span data-ttu-id="40a78-110">또는 **TrafficManagerProfile** 매개 변수를 사용하여 *TrafficManagerProfile* 개체를 지정하거나 파이프라인을 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="40a78-110">Alternatively, you can specify a **TrafficManagerProfile** object using the *TrafficManagerProfile* parameter, or you can use the pipeline.</span></span>

## <span data-ttu-id="40a78-111">예제</span><span class="sxs-lookup"><span data-stu-id="40a78-111">EXAMPLES</span></span>

### <span data-ttu-id="40a78-112">예제 1: 이름으로 지정된 프로필 삭제</span><span class="sxs-lookup"><span data-stu-id="40a78-112">Example 1: Delete a profile specified by name</span></span>
```
PS C:\>Remove-AzTrafficManagerProfile -Name "ContosoProfile" -ResourceGroupName "ResourceGroup11"
```

<span data-ttu-id="40a78-113">이 명령은 ResourceGroup11에서 ContosoProfile이라는 프로필을 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="40a78-113">This command deletes the profile named ContosoProfile in ResourceGroup11.</span></span>
<span data-ttu-id="40a78-114">명령을 통해 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="40a78-114">The command prompts you for confirmation.</span></span>

### <span data-ttu-id="40a78-115">예제 2: 파이프라인을 사용하여 프로필 삭제</span><span class="sxs-lookup"><span data-stu-id="40a78-115">Example 2: Delete a profile by using the pipeline</span></span>
```
PS C:\>Get-AzTrafficManagerProfile -Name "ContosoProfile" -ResourceGroupName "ResourceGroup11" | Remove-AzTrafficManagerProfile -Force
```

<span data-ttu-id="40a78-116">이 명령은 ResourceGroup11에서 ContosoProfile이라는 프로필을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="40a78-116">This command gets the profile named ContosoProfile in ResourceGroup11.</span></span>
<span data-ttu-id="40a78-117">그런 다음 명령은 파이프라인 연산자를 사용하여 **Remove-AzTrafficManagerProfile** cmdlet에 해당 프로필을 전달합니다.</span><span class="sxs-lookup"><span data-stu-id="40a78-117">The command then passes that profile to the **Remove-AzTrafficManagerProfile** cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="40a78-118">해당 cmdlet은 해당 프로필을 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="40a78-118">That cmdlet deletes that profile.</span></span>
<span data-ttu-id="40a78-119">명령은 Force 매개 *변수를 지정합니다.*</span><span class="sxs-lookup"><span data-stu-id="40a78-119">The command specifies the *Force* parameter.</span></span>
<span data-ttu-id="40a78-120">따라서 확인을 묻는 메시지가 표시되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="40a78-120">Therefore, it does not prompt you for confirmation.</span></span>

## <span data-ttu-id="40a78-121">매개 변수</span><span class="sxs-lookup"><span data-stu-id="40a78-121">PARAMETERS</span></span>

### <span data-ttu-id="40a78-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="40a78-122">-DefaultProfile</span></span>
<span data-ttu-id="40a78-123">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="40a78-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="40a78-124">-Force</span><span class="sxs-lookup"><span data-stu-id="40a78-124">-Force</span></span>
<span data-ttu-id="40a78-125">사용자 확인을 요청하지 않고 명령을 강제로 실행합니다.</span><span class="sxs-lookup"><span data-stu-id="40a78-125">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="40a78-126">-Name</span><span class="sxs-lookup"><span data-stu-id="40a78-126">-Name</span></span>
<span data-ttu-id="40a78-127">이 cmdlet이 삭제하는 Traffic Manager 프로필의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="40a78-127">Specifies the name of the Traffic Manager profile that this cmdlet deletes.</span></span>

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

### <span data-ttu-id="40a78-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="40a78-128">-ResourceGroupName</span></span>
<span data-ttu-id="40a78-129">리소스 그룹의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="40a78-129">Specifies the name of a resource group.</span></span>
<span data-ttu-id="40a78-130">이 cmdlet은 이 매개 변수가 지정하는 그룹의 Traffic Manager 프로필을 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="40a78-130">This cmdlet deletes a Traffic Manager profile in the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="40a78-131">-TrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="40a78-131">-TrafficManagerProfile</span></span>
<span data-ttu-id="40a78-132">삭제할 **TrafficManagerProfile** 개체를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="40a78-132">Specifies a **TrafficManagerProfile** object to delete.</span></span>
<span data-ttu-id="40a78-133">**TrafficManagerProfile** 개체를 얻은 경우 Get-AzTrafficManagerProfile cmdlet을 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="40a78-133">To obtain a **TrafficManagerProfile** object, use the Get-AzTrafficManagerProfile cmdlet.</span></span>

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

### <span data-ttu-id="40a78-134">-확인</span><span class="sxs-lookup"><span data-stu-id="40a78-134">-Confirm</span></span>
<span data-ttu-id="40a78-135">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="40a78-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="40a78-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="40a78-136">-WhatIf</span></span>
<span data-ttu-id="40a78-137">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="40a78-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="40a78-138">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="40a78-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="40a78-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="40a78-139">CommonParameters</span></span>
<span data-ttu-id="40a78-140">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="40a78-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="40a78-141">자세한 내용은 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="40a78-141">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="40a78-142">입력</span><span class="sxs-lookup"><span data-stu-id="40a78-142">INPUTS</span></span>

### <span data-ttu-id="40a78-143">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="40a78-143">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerProfile</span></span>

## <span data-ttu-id="40a78-144">출력</span><span class="sxs-lookup"><span data-stu-id="40a78-144">OUTPUTS</span></span>

### <span data-ttu-id="40a78-145">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="40a78-145">System.Boolean</span></span>

## <span data-ttu-id="40a78-146">참고 사항</span><span class="sxs-lookup"><span data-stu-id="40a78-146">NOTES</span></span>

## <span data-ttu-id="40a78-147">관련 링크</span><span class="sxs-lookup"><span data-stu-id="40a78-147">RELATED LINKS</span></span>

[<span data-ttu-id="40a78-148">Disable-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="40a78-148">Disable-AzTrafficManagerProfile</span></span>](./Disable-AzTrafficManagerProfile.md)

[<span data-ttu-id="40a78-149">Enable-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="40a78-149">Enable-AzTrafficManagerProfile</span></span>](./Enable-AzTrafficManagerProfile.md)

[<span data-ttu-id="40a78-150">Get-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="40a78-150">Get-AzTrafficManagerProfile</span></span>](./Get-AzTrafficManagerProfile.md)

[<span data-ttu-id="40a78-151">New-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="40a78-151">New-AzTrafficManagerProfile</span></span>](./New-AzTrafficManagerProfile.md)

[<span data-ttu-id="40a78-152">Set-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="40a78-152">Set-AzTrafficManagerProfile</span></span>](./Set-AzTrafficManagerProfile.md)


