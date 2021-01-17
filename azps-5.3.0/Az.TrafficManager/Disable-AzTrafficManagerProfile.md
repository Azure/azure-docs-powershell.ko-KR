---
external help file: Microsoft.Azure.PowerShell.Cmdlets.TrafficManager.dll-Help.xml
Module Name: Az.TrafficManager
ms.assetid: B6E043FF-F4DD-44B7-BEAA-6B17C8F21D58
online version: https://docs.microsoft.com/en-us/powershell/module/az.trafficmanager/disable-aztrafficmanagerprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Disable-AzTrafficManagerProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Disable-AzTrafficManagerProfile.md
ms.openlocfilehash: fc1370da73b9217c5f5f8b24705047f154b50f31
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98382901"
---
# <span data-ttu-id="34e00-101">Disable-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="34e00-101">Disable-AzTrafficManagerProfile</span></span>

## <span data-ttu-id="34e00-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="34e00-102">SYNOPSIS</span></span>
<span data-ttu-id="34e00-103">Traffic Manager 프로필을 비활성화합니다.</span><span class="sxs-lookup"><span data-stu-id="34e00-103">Disables a Traffic Manager profile.</span></span>

## <span data-ttu-id="34e00-104">구문</span><span class="sxs-lookup"><span data-stu-id="34e00-104">SYNTAX</span></span>

### <span data-ttu-id="34e00-105">필드</span><span class="sxs-lookup"><span data-stu-id="34e00-105">Fields</span></span>
```
Disable-AzTrafficManagerProfile -Name <String> -ResourceGroupName <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="34e00-106">개체</span><span class="sxs-lookup"><span data-stu-id="34e00-106">Object</span></span>
```
Disable-AzTrafficManagerProfile -TrafficManagerProfile <TrafficManagerProfile> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="34e00-107">설명</span><span class="sxs-lookup"><span data-stu-id="34e00-107">DESCRIPTION</span></span>
<span data-ttu-id="34e00-108">**Disable-AzTrafficManagerProfile** cmdlet은 Azure Traffic Manager 프로필을 사용하지 않도록 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="34e00-108">The **Disable-AzTrafficManagerProfile** cmdlet disables an Azure Traffic Manager profile.</span></span>
<span data-ttu-id="34e00-109">파이프라인을 사용하여 또는 매개 변수 값으로 프로필 개체를 지정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="34e00-109">You can specify the profile object by using the pipeline or as a parameter value.</span></span>
<span data-ttu-id="34e00-110">또는 Name 및 *ResourceGroupName* 매개 변수를 사용하여 프로필을 지정할 수 있습니다. </span><span class="sxs-lookup"><span data-stu-id="34e00-110">Alternatively, you can specify the profile by using the *Name* and *ResourceGroupName* parameters.</span></span>

## <span data-ttu-id="34e00-111">예제</span><span class="sxs-lookup"><span data-stu-id="34e00-111">EXAMPLES</span></span>

### <span data-ttu-id="34e00-112">예제 1: 이름으로 지정된 프로필 사용 안</span><span class="sxs-lookup"><span data-stu-id="34e00-112">Example 1: Disable a profile specified by name</span></span>
```
PS C:\>Disable-AzTrafficManagerProfile -Name "ContosoProfile" -ResourceGroupName "ResourceGroup11"
```

<span data-ttu-id="34e00-113">이 명령은 ResourceGroup11에서 ContosoProfile이라는 프로필을 사용하지 않도록 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="34e00-113">This command disables the profile named ContosoProfile in ResourceGroup11.</span></span>
<span data-ttu-id="34e00-114">이 명령은 확인을 요청하는 메시지를 제공합니다.</span><span class="sxs-lookup"><span data-stu-id="34e00-114">The command prompts you for confirmation.</span></span>

### <span data-ttu-id="34e00-115">예제 2: 파이프라인을 사용하여 프로필 비활성화</span><span class="sxs-lookup"><span data-stu-id="34e00-115">Example 2: Disable a profile by using the pipeline</span></span>
```
PS C:\>Get-AzTrafficManagerProfile -Name "ContosoProfile" -ResourceGroupName "ResourceGroup11" | Disable-AzTrafficManagerProfile -Force
```

<span data-ttu-id="34e00-116">이 명령은 ResourceGroup11에서 ContosoProfile이라는 프로필을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="34e00-116">This command gets the profile named ContosoProfile in ResourceGroup11.</span></span>
<span data-ttu-id="34e00-117">그런 다음 이 명령은 파이프라인 연산자를 사용하여 해당 프로필을 **Disable-AzTrafficManagerProfile** cmdlet에 전달합니다.</span><span class="sxs-lookup"><span data-stu-id="34e00-117">The command then passes that profile to the **Disable-AzTrafficManagerProfile** cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="34e00-118">이 cmdlet은 프로필을 비활성화합니다.</span><span class="sxs-lookup"><span data-stu-id="34e00-118">That cmdlet disables that profile.</span></span>
<span data-ttu-id="34e00-119">이 명령은 Force 매개 *변수를 지정합니다.*</span><span class="sxs-lookup"><span data-stu-id="34e00-119">The command specifies the *Force* parameter.</span></span>
<span data-ttu-id="34e00-120">따라서 확인을 묻는 메시지가 표시되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="34e00-120">Therefore, it does not prompt you for confirmation.</span></span>

## <span data-ttu-id="34e00-121">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="34e00-121">PARAMETERS</span></span>

### <span data-ttu-id="34e00-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="34e00-122">-DefaultProfile</span></span>
<span data-ttu-id="34e00-123">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="34e00-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="34e00-124">-Force</span><span class="sxs-lookup"><span data-stu-id="34e00-124">-Force</span></span>
<span data-ttu-id="34e00-125">사용자 확인을 요청하지 않고 명령을 강제로 실행합니다.</span><span class="sxs-lookup"><span data-stu-id="34e00-125">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="34e00-126">-Name</span><span class="sxs-lookup"><span data-stu-id="34e00-126">-Name</span></span>
<span data-ttu-id="34e00-127">이 cmdlet에서 사용하지 않도록 설정하는 Traffic Manager 프로필의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="34e00-127">Specifies the name of the Traffic Manager profile that this cmdlet disables.</span></span>

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

### <span data-ttu-id="34e00-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="34e00-128">-ResourceGroupName</span></span>
<span data-ttu-id="34e00-129">리소스 그룹의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="34e00-129">Specifies the name of a resource group.</span></span>
<span data-ttu-id="34e00-130">이 cmdlet은 이 매개 변수가 지정하는 그룹에서 Traffic Manager 프로필을 사용하지 않도록 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="34e00-130">This cmdlet disables a Traffic Manager profile in the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="34e00-131">-TrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="34e00-131">-TrafficManagerProfile</span></span>
<span data-ttu-id="34e00-132">사용하지 않도록 **설정할 TrafficManagerProfile** 개체를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="34e00-132">Specifies a **TrafficManagerProfile** object to disable.</span></span>
<span data-ttu-id="34e00-133">**TrafficManagerProfile** 개체를 얻습니다. Get-AzTrafficManagerProfile cmdlet을 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="34e00-133">To obtain a **TrafficManagerProfile** object, use the Get-AzTrafficManagerProfile cmdlet.</span></span>

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

### <span data-ttu-id="34e00-134">-Confirm</span><span class="sxs-lookup"><span data-stu-id="34e00-134">-Confirm</span></span>
<span data-ttu-id="34e00-135">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="34e00-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="34e00-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="34e00-136">-WhatIf</span></span>
<span data-ttu-id="34e00-137">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="34e00-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="34e00-138">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="34e00-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="34e00-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="34e00-139">CommonParameters</span></span>
<span data-ttu-id="34e00-140">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="34e00-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="34e00-141">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="34e00-141">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="34e00-142">입력</span><span class="sxs-lookup"><span data-stu-id="34e00-142">INPUTS</span></span>

### <span data-ttu-id="34e00-143">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="34e00-143">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerProfile</span></span>

## <span data-ttu-id="34e00-144">출력</span><span class="sxs-lookup"><span data-stu-id="34e00-144">OUTPUTS</span></span>

### <span data-ttu-id="34e00-145">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="34e00-145">System.Boolean</span></span>

## <span data-ttu-id="34e00-146">참고 사항</span><span class="sxs-lookup"><span data-stu-id="34e00-146">NOTES</span></span>

## <span data-ttu-id="34e00-147">관련 링크</span><span class="sxs-lookup"><span data-stu-id="34e00-147">RELATED LINKS</span></span>

[<span data-ttu-id="34e00-148">Enable-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="34e00-148">Enable-AzTrafficManagerProfile</span></span>](./Enable-AzTrafficManagerProfile.md)

[<span data-ttu-id="34e00-149">Get-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="34e00-149">Get-AzTrafficManagerProfile</span></span>](./Get-AzTrafficManagerProfile.md)

[<span data-ttu-id="34e00-150">New-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="34e00-150">New-AzTrafficManagerProfile</span></span>](./New-AzTrafficManagerProfile.md)

[<span data-ttu-id="34e00-151">Remove-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="34e00-151">Remove-AzTrafficManagerProfile</span></span>](./Remove-AzTrafficManagerProfile.md)

[<span data-ttu-id="34e00-152">Set-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="34e00-152">Set-AzTrafficManagerProfile</span></span>](./Set-AzTrafficManagerProfile.md)


