---
external help file: Microsoft.Azure.PowerShell.Cmdlets.TrafficManager.dll-Help.xml
Module Name: Az.TrafficManager
ms.assetid: B6E043FF-F4DD-44B7-BEAA-6B17C8F21D58
online version: https://docs.microsoft.com/powershell/module/az.trafficmanager/disable-aztrafficmanagerprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Disable-AzTrafficManagerProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Disable-AzTrafficManagerProfile.md
ms.openlocfilehash: 4d667b1435a7396082f0626d8f55882f7c37b8ad
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101950811"
---
# <span data-ttu-id="2b40b-101">Disable-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="2b40b-101">Disable-AzTrafficManagerProfile</span></span>

## <span data-ttu-id="2b40b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2b40b-102">SYNOPSIS</span></span>
<span data-ttu-id="2b40b-103">Traffic Manager 프로필을 사용하지 않도록 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="2b40b-103">Disables a Traffic Manager profile.</span></span>

## <span data-ttu-id="2b40b-104">구문</span><span class="sxs-lookup"><span data-stu-id="2b40b-104">SYNTAX</span></span>

### <span data-ttu-id="2b40b-105">필드</span><span class="sxs-lookup"><span data-stu-id="2b40b-105">Fields</span></span>
```
Disable-AzTrafficManagerProfile -Name <String> -ResourceGroupName <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2b40b-106">개체</span><span class="sxs-lookup"><span data-stu-id="2b40b-106">Object</span></span>
```
Disable-AzTrafficManagerProfile -TrafficManagerProfile <TrafficManagerProfile> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2b40b-107">설명</span><span class="sxs-lookup"><span data-stu-id="2b40b-107">DESCRIPTION</span></span>
<span data-ttu-id="2b40b-108">**Disable-AzTrafficManagerProfile** cmdlet은 Azure Traffic Manager 프로필을 사용하지 않도록 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="2b40b-108">The **Disable-AzTrafficManagerProfile** cmdlet disables an Azure Traffic Manager profile.</span></span>
<span data-ttu-id="2b40b-109">파이프라인을 사용하여 또는 매개 변수 값으로 프로필 개체를 지정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="2b40b-109">You can specify the profile object by using the pipeline or as a parameter value.</span></span>
<span data-ttu-id="2b40b-110">또는 이름 및 *ResourceGroupName* 매개 변수를 사용하여 프로필을 지정할 수 있습니다. </span><span class="sxs-lookup"><span data-stu-id="2b40b-110">Alternatively, you can specify the profile by using the *Name* and *ResourceGroupName* parameters.</span></span>

## <span data-ttu-id="2b40b-111">예제</span><span class="sxs-lookup"><span data-stu-id="2b40b-111">EXAMPLES</span></span>

### <span data-ttu-id="2b40b-112">예제 1: 이름으로 지정된 프로필 사용 안 하세요.</span><span class="sxs-lookup"><span data-stu-id="2b40b-112">Example 1: Disable a profile specified by name</span></span>
```
PS C:\>Disable-AzTrafficManagerProfile -Name "ContosoProfile" -ResourceGroupName "ResourceGroup11"
```

<span data-ttu-id="2b40b-113">이 명령은 ResourceGroup11에서 ContosoProfile이라는 프로필을 사용하지 않도록 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="2b40b-113">This command disables the profile named ContosoProfile in ResourceGroup11.</span></span>
<span data-ttu-id="2b40b-114">명령을 통해 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="2b40b-114">The command prompts you for confirmation.</span></span>

### <span data-ttu-id="2b40b-115">예제 2: 파이프라인을 사용하여 프로필 사용 안 하세요.</span><span class="sxs-lookup"><span data-stu-id="2b40b-115">Example 2: Disable a profile by using the pipeline</span></span>
```
PS C:\>Get-AzTrafficManagerProfile -Name "ContosoProfile" -ResourceGroupName "ResourceGroup11" | Disable-AzTrafficManagerProfile -Force
```

<span data-ttu-id="2b40b-116">이 명령은 ResourceGroup11에서 ContosoProfile이라는 프로필을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="2b40b-116">This command gets the profile named ContosoProfile in ResourceGroup11.</span></span>
<span data-ttu-id="2b40b-117">그런 다음 명령은 파이프라인 연산자를 사용하여 해당 프로필을 **Disable-AzTrafficManagerProfile** cmdlet에 전달합니다.</span><span class="sxs-lookup"><span data-stu-id="2b40b-117">The command then passes that profile to the **Disable-AzTrafficManagerProfile** cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="2b40b-118">이 cmdlet은 프로필을 사용하지 않도록 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="2b40b-118">That cmdlet disables that profile.</span></span>
<span data-ttu-id="2b40b-119">명령은 Force 매개 *변수를 지정합니다.*</span><span class="sxs-lookup"><span data-stu-id="2b40b-119">The command specifies the *Force* parameter.</span></span>
<span data-ttu-id="2b40b-120">따라서 확인을 묻는 메시지가 표시되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="2b40b-120">Therefore, it does not prompt you for confirmation.</span></span>

## <span data-ttu-id="2b40b-121">매개 변수</span><span class="sxs-lookup"><span data-stu-id="2b40b-121">PARAMETERS</span></span>

### <span data-ttu-id="2b40b-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2b40b-122">-DefaultProfile</span></span>
<span data-ttu-id="2b40b-123">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="2b40b-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2b40b-124">-Force</span><span class="sxs-lookup"><span data-stu-id="2b40b-124">-Force</span></span>
<span data-ttu-id="2b40b-125">사용자 확인을 요청하지 않고 명령을 강제로 실행합니다.</span><span class="sxs-lookup"><span data-stu-id="2b40b-125">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="2b40b-126">-Name</span><span class="sxs-lookup"><span data-stu-id="2b40b-126">-Name</span></span>
<span data-ttu-id="2b40b-127">이 cmdlet에서 사용하지 않도록 설정하는 Traffic Manager 프로필의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="2b40b-127">Specifies the name of the Traffic Manager profile that this cmdlet disables.</span></span>

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

### <span data-ttu-id="2b40b-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2b40b-128">-ResourceGroupName</span></span>
<span data-ttu-id="2b40b-129">리소스 그룹의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="2b40b-129">Specifies the name of a resource group.</span></span>
<span data-ttu-id="2b40b-130">이 cmdlet은 이 매개 변수가 지정하는 그룹의 Traffic Manager 프로필을 사용하지 않도록 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="2b40b-130">This cmdlet disables a Traffic Manager profile in the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="2b40b-131">-TrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="2b40b-131">-TrafficManagerProfile</span></span>
<span data-ttu-id="2b40b-132">사용 안 하게 **TrafficManagerProfile** 개체를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="2b40b-132">Specifies a **TrafficManagerProfile** object to disable.</span></span>
<span data-ttu-id="2b40b-133">**TrafficManagerProfile** 개체를 얻은 경우 Get-AzTrafficManagerProfile cmdlet을 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="2b40b-133">To obtain a **TrafficManagerProfile** object, use the Get-AzTrafficManagerProfile cmdlet.</span></span>

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

### <span data-ttu-id="2b40b-134">-확인</span><span class="sxs-lookup"><span data-stu-id="2b40b-134">-Confirm</span></span>
<span data-ttu-id="2b40b-135">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="2b40b-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2b40b-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2b40b-136">-WhatIf</span></span>
<span data-ttu-id="2b40b-137">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="2b40b-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2b40b-138">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="2b40b-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2b40b-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2b40b-139">CommonParameters</span></span>
<span data-ttu-id="2b40b-140">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="2b40b-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2b40b-141">자세한 내용은 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="2b40b-141">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2b40b-142">입력</span><span class="sxs-lookup"><span data-stu-id="2b40b-142">INPUTS</span></span>

### <span data-ttu-id="2b40b-143">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="2b40b-143">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerProfile</span></span>

## <span data-ttu-id="2b40b-144">출력</span><span class="sxs-lookup"><span data-stu-id="2b40b-144">OUTPUTS</span></span>

### <span data-ttu-id="2b40b-145">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="2b40b-145">System.Boolean</span></span>

## <span data-ttu-id="2b40b-146">참고 사항</span><span class="sxs-lookup"><span data-stu-id="2b40b-146">NOTES</span></span>

## <span data-ttu-id="2b40b-147">관련 링크</span><span class="sxs-lookup"><span data-stu-id="2b40b-147">RELATED LINKS</span></span>

[<span data-ttu-id="2b40b-148">Enable-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="2b40b-148">Enable-AzTrafficManagerProfile</span></span>](./Enable-AzTrafficManagerProfile.md)

[<span data-ttu-id="2b40b-149">Get-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="2b40b-149">Get-AzTrafficManagerProfile</span></span>](./Get-AzTrafficManagerProfile.md)

[<span data-ttu-id="2b40b-150">New-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="2b40b-150">New-AzTrafficManagerProfile</span></span>](./New-AzTrafficManagerProfile.md)

[<span data-ttu-id="2b40b-151">Remove-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="2b40b-151">Remove-AzTrafficManagerProfile</span></span>](./Remove-AzTrafficManagerProfile.md)

[<span data-ttu-id="2b40b-152">Set-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="2b40b-152">Set-AzTrafficManagerProfile</span></span>](./Set-AzTrafficManagerProfile.md)


