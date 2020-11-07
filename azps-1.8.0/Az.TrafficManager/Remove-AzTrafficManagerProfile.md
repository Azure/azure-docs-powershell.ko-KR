---
external help file: Microsoft.Azure.PowerShell.Cmdlets.TrafficManager.dll-Help.xml
Module Name: Az.TrafficManager
ms.assetid: 5A4D685F-B904-4C85-8B68-C9936B0627FA
online version: https://docs.microsoft.com/en-us/powershell/module/az.trafficmanager/remove-aztrafficmanagerprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Remove-AzTrafficManagerProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Remove-AzTrafficManagerProfile.md
ms.openlocfilehash: 19f226d79e0de1b32aacae2beda22eae20d40afa
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93698384"
---
# <span data-ttu-id="84936-101">Remove-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="84936-101">Remove-AzTrafficManagerProfile</span></span>

## <span data-ttu-id="84936-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="84936-102">SYNOPSIS</span></span>
<span data-ttu-id="84936-103">Traffic Manager 프로필을 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="84936-103">Deletes a Traffic Manager profile.</span></span>

## <span data-ttu-id="84936-104">구문과</span><span class="sxs-lookup"><span data-stu-id="84936-104">SYNTAX</span></span>

### <span data-ttu-id="84936-105">필드인</span><span class="sxs-lookup"><span data-stu-id="84936-105">Fields</span></span>
```
Remove-AzTrafficManagerProfile -Name <String> -ResourceGroupName <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="84936-106">오브젝트가</span><span class="sxs-lookup"><span data-stu-id="84936-106">Object</span></span>
```
Remove-AzTrafficManagerProfile -TrafficManagerProfile <TrafficManagerProfile> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="84936-107">설명은</span><span class="sxs-lookup"><span data-stu-id="84936-107">DESCRIPTION</span></span>
<span data-ttu-id="84936-108">**AzTrafficManagerProfile** Cmdlet은 Azure Traffic Manager 프로필을 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="84936-108">The **Remove-AzTrafficManagerProfile** cmdlet deletes an Azure Traffic Manager profile.</span></span>
<span data-ttu-id="84936-109">*Name* 및 *ResourceGroupName* 매개 변수를 사용 하 여 삭제할 프로필을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="84936-109">Specify the profile to delete by using the *Name* and *ResourceGroupName* parameters.</span></span>
<span data-ttu-id="84936-110">또는 *TrafficManagerProfile* 매개 변수를 사용 하 여 **TrafficManagerProfile** 개체를 지정 하거나 파이프라인을 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="84936-110">Alternatively, you can specify a **TrafficManagerProfile** object using the *TrafficManagerProfile* parameter, or you can use the pipeline.</span></span>

## <span data-ttu-id="84936-111">예제의</span><span class="sxs-lookup"><span data-stu-id="84936-111">EXAMPLES</span></span>

### <span data-ttu-id="84936-112">예제 1: 이름으로 지정 된 프로필 삭제</span><span class="sxs-lookup"><span data-stu-id="84936-112">Example 1: Delete a profile specified by name</span></span>
```
PS C:\>Remove-AzTrafficManagerProfile -Name "ContosoProfile" -ResourceGroupName "ResourceGroup11"
```

<span data-ttu-id="84936-113">이 명령은 ResourceGroup11에서 ContosoProfile 이라는 프로필을 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="84936-113">This command deletes the profile named ContosoProfile in ResourceGroup11.</span></span>
<span data-ttu-id="84936-114">명령에서 확인 하 라는 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="84936-114">The command prompts you for confirmation.</span></span>

### <span data-ttu-id="84936-115">예제 2: 파이프라인을 사용 하 여 프로필 삭제</span><span class="sxs-lookup"><span data-stu-id="84936-115">Example 2: Delete a profile by using the pipeline</span></span>
```
PS C:\>Get-AzTrafficManagerProfile -Name "ContosoProfile" -ResourceGroupName "ResourceGroup11" | Remove-AzTrafficManagerProfile -Force
```

<span data-ttu-id="84936-116">이 명령은 ResourceGroup11에서 ContosoProfile 이라는 프로필을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="84936-116">This command gets the profile named ContosoProfile in ResourceGroup11.</span></span>
<span data-ttu-id="84936-117">그런 다음이 명령은 파이프라인 연산자를 사용 하 여 해당 프로필을 **AzTrafficManagerProfile** cmdlet에 전달 합니다.</span><span class="sxs-lookup"><span data-stu-id="84936-117">The command then passes that profile to the **Remove-AzTrafficManagerProfile** cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="84936-118">해당 cmdlet은 해당 프로필을 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="84936-118">That cmdlet deletes that profile.</span></span>
<span data-ttu-id="84936-119">명령에서 *Force* 매개 변수를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="84936-119">The command specifies the *Force* parameter.</span></span>
<span data-ttu-id="84936-120">따라서 확인 메시지가 표시 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="84936-120">Therefore, it does not prompt you for confirmation.</span></span>

## <span data-ttu-id="84936-121">변수</span><span class="sxs-lookup"><span data-stu-id="84936-121">PARAMETERS</span></span>

### <span data-ttu-id="84936-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="84936-122">-DefaultProfile</span></span>
<span data-ttu-id="84936-123">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="84936-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="84936-124">-Force</span><span class="sxs-lookup"><span data-stu-id="84936-124">-Force</span></span>
<span data-ttu-id="84936-125">사용자 확인을 요청 하지 않고 명령을 강제로 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="84936-125">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="84936-126">-이름</span><span class="sxs-lookup"><span data-stu-id="84936-126">-Name</span></span>
<span data-ttu-id="84936-127">이 cmdlet이 삭제 하는 Traffic Manager 프로필의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="84936-127">Specifies the name of the Traffic Manager profile that this cmdlet deletes.</span></span>

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

### <span data-ttu-id="84936-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="84936-128">-ResourceGroupName</span></span>
<span data-ttu-id="84936-129">리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="84936-129">Specifies the name of a resource group.</span></span>
<span data-ttu-id="84936-130">이 cmdlet은이 매개 변수에서 지정 하는 그룹에서 Traffic Manager 프로필을 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="84936-130">This cmdlet deletes a Traffic Manager profile in the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="84936-131">-TrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="84936-131">-TrafficManagerProfile</span></span>
<span data-ttu-id="84936-132">삭제할 **TrafficManagerProfile** 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="84936-132">Specifies a **TrafficManagerProfile** object to delete.</span></span>
<span data-ttu-id="84936-133">**TrafficManagerProfile** 개체를 가져오려면 Get-AzTrafficManagerProfile cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="84936-133">To obtain a **TrafficManagerProfile** object, use the Get-AzTrafficManagerProfile cmdlet.</span></span>

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

### <span data-ttu-id="84936-134">-확인</span><span class="sxs-lookup"><span data-stu-id="84936-134">-Confirm</span></span>
<span data-ttu-id="84936-135">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="84936-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="84936-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="84936-136">-WhatIf</span></span>
<span data-ttu-id="84936-137">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="84936-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="84936-138">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="84936-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="84936-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="84936-139">CommonParameters</span></span>
<span data-ttu-id="84936-140">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="84936-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="84936-141">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="84936-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="84936-142">입력</span><span class="sxs-lookup"><span data-stu-id="84936-142">INPUTS</span></span>

### <span data-ttu-id="84936-143">TrafficManager. TrafficManagerProfile/.</span><span class="sxs-lookup"><span data-stu-id="84936-143">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerProfile</span></span>

## <span data-ttu-id="84936-144">출력</span><span class="sxs-lookup"><span data-stu-id="84936-144">OUTPUTS</span></span>

### <span data-ttu-id="84936-145">시스템 부울</span><span class="sxs-lookup"><span data-stu-id="84936-145">System.Boolean</span></span>

## <span data-ttu-id="84936-146">상속자</span><span class="sxs-lookup"><span data-stu-id="84936-146">NOTES</span></span>

## <span data-ttu-id="84936-147">관련 링크</span><span class="sxs-lookup"><span data-stu-id="84936-147">RELATED LINKS</span></span>

[<span data-ttu-id="84936-148">Disable-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="84936-148">Disable-AzTrafficManagerProfile</span></span>](./Disable-AzTrafficManagerProfile.md)

[<span data-ttu-id="84936-149">Enable-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="84936-149">Enable-AzTrafficManagerProfile</span></span>](./Enable-AzTrafficManagerProfile.md)

[<span data-ttu-id="84936-150">Get-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="84936-150">Get-AzTrafficManagerProfile</span></span>](./Get-AzTrafficManagerProfile.md)

[<span data-ttu-id="84936-151">새로운 AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="84936-151">New-AzTrafficManagerProfile</span></span>](./New-AzTrafficManagerProfile.md)

[<span data-ttu-id="84936-152">Set-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="84936-152">Set-AzTrafficManagerProfile</span></span>](./Set-AzTrafficManagerProfile.md)


