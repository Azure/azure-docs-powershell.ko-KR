---
external help file: Microsoft.Azure.PowerShell.Cmdlets.TrafficManager.dll-Help.xml
Module Name: Az.TrafficManager
ms.assetid: B6E043FF-F4DD-44B7-BEAA-6B17C8F21D58
online version: https://docs.microsoft.com/en-us/powershell/module/az.trafficmanager/disable-aztrafficmanagerprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Disable-AzTrafficManagerProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Disable-AzTrafficManagerProfile.md
ms.openlocfilehash: fc1370da73b9217c5f5f8b24705047f154b50f31
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94225992"
---
# <span data-ttu-id="a5101-101">Disable-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="a5101-101">Disable-AzTrafficManagerProfile</span></span>

## <span data-ttu-id="a5101-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a5101-102">SYNOPSIS</span></span>
<span data-ttu-id="a5101-103">Traffic Manager 프로필을 사용 하지 않도록 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a5101-103">Disables a Traffic Manager profile.</span></span>

## <span data-ttu-id="a5101-104">구문과</span><span class="sxs-lookup"><span data-stu-id="a5101-104">SYNTAX</span></span>

### <span data-ttu-id="a5101-105">필드인</span><span class="sxs-lookup"><span data-stu-id="a5101-105">Fields</span></span>
```
Disable-AzTrafficManagerProfile -Name <String> -ResourceGroupName <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a5101-106">오브젝트가</span><span class="sxs-lookup"><span data-stu-id="a5101-106">Object</span></span>
```
Disable-AzTrafficManagerProfile -TrafficManagerProfile <TrafficManagerProfile> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a5101-107">설명은</span><span class="sxs-lookup"><span data-stu-id="a5101-107">DESCRIPTION</span></span>
<span data-ttu-id="a5101-108">**AzTrafficManagerProfile** Cmdlet은 Azure Traffic Manager 프로필을 사용 하지 않도록 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a5101-108">The **Disable-AzTrafficManagerProfile** cmdlet disables an Azure Traffic Manager profile.</span></span>
<span data-ttu-id="a5101-109">파이프라인 또는 매개 변수 값을 사용 하 여 프로필 개체를 지정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="a5101-109">You can specify the profile object by using the pipeline or as a parameter value.</span></span>
<span data-ttu-id="a5101-110">또는 *Name* 및 *ResourceGroupName* 매개 변수를 사용 하 여 프로필을 지정할 수도 있습니다.</span><span class="sxs-lookup"><span data-stu-id="a5101-110">Alternatively, you can specify the profile by using the *Name* and *ResourceGroupName* parameters.</span></span>

## <span data-ttu-id="a5101-111">예제의</span><span class="sxs-lookup"><span data-stu-id="a5101-111">EXAMPLES</span></span>

### <span data-ttu-id="a5101-112">예제 1: 이름으로 지정 된 프로필 사용 안 함</span><span class="sxs-lookup"><span data-stu-id="a5101-112">Example 1: Disable a profile specified by name</span></span>
```
PS C:\>Disable-AzTrafficManagerProfile -Name "ContosoProfile" -ResourceGroupName "ResourceGroup11"
```

<span data-ttu-id="a5101-113">이 명령은 ResourceGroup11에서 ContosoProfile 이라는 프로필을 사용 하지 않도록 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a5101-113">This command disables the profile named ContosoProfile in ResourceGroup11.</span></span>
<span data-ttu-id="a5101-114">명령에서 확인 하 라는 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="a5101-114">The command prompts you for confirmation.</span></span>

### <span data-ttu-id="a5101-115">예제 2: 파이프라인을 사용 하 여 프로필 비활성화</span><span class="sxs-lookup"><span data-stu-id="a5101-115">Example 2: Disable a profile by using the pipeline</span></span>
```
PS C:\>Get-AzTrafficManagerProfile -Name "ContosoProfile" -ResourceGroupName "ResourceGroup11" | Disable-AzTrafficManagerProfile -Force
```

<span data-ttu-id="a5101-116">이 명령은 ResourceGroup11에서 ContosoProfile 이라는 프로필을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="a5101-116">This command gets the profile named ContosoProfile in ResourceGroup11.</span></span>
<span data-ttu-id="a5101-117">그런 다음이 명령은 파이프라인 연산자를 사용 하 여 해당 프로필을 **AzTrafficManagerProfile** cmdlet에 전달 합니다.</span><span class="sxs-lookup"><span data-stu-id="a5101-117">The command then passes that profile to the **Disable-AzTrafficManagerProfile** cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="a5101-118">해당 cmdlet은 해당 프로필을 사용 하지 않도록 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a5101-118">That cmdlet disables that profile.</span></span>
<span data-ttu-id="a5101-119">명령에서 *Force* 매개 변수를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a5101-119">The command specifies the *Force* parameter.</span></span>
<span data-ttu-id="a5101-120">따라서 확인 메시지가 표시 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="a5101-120">Therefore, it does not prompt you for confirmation.</span></span>

## <span data-ttu-id="a5101-121">변수</span><span class="sxs-lookup"><span data-stu-id="a5101-121">PARAMETERS</span></span>

### <span data-ttu-id="a5101-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a5101-122">-DefaultProfile</span></span>
<span data-ttu-id="a5101-123">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="a5101-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a5101-124">-Force</span><span class="sxs-lookup"><span data-stu-id="a5101-124">-Force</span></span>
<span data-ttu-id="a5101-125">사용자 확인을 요청 하지 않고 명령을 강제로 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="a5101-125">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="a5101-126">-이름</span><span class="sxs-lookup"><span data-stu-id="a5101-126">-Name</span></span>
<span data-ttu-id="a5101-127">이 cmdlet이 사용 하지 않도록 설정 하는 Traffic Manager 프로필의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a5101-127">Specifies the name of the Traffic Manager profile that this cmdlet disables.</span></span>

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

### <span data-ttu-id="a5101-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a5101-128">-ResourceGroupName</span></span>
<span data-ttu-id="a5101-129">리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a5101-129">Specifies the name of a resource group.</span></span>
<span data-ttu-id="a5101-130">이 cmdlet은이 매개 변수에서 지정 하는 그룹에서 Traffic Manager 프로필을 사용 하지 않도록 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a5101-130">This cmdlet disables a Traffic Manager profile in the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="a5101-131">-TrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="a5101-131">-TrafficManagerProfile</span></span>
<span data-ttu-id="a5101-132">사용 하지 않도록 설정할 **TrafficManagerProfile** 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a5101-132">Specifies a **TrafficManagerProfile** object to disable.</span></span>
<span data-ttu-id="a5101-133">**TrafficManagerProfile** 개체를 가져오려면 Get-AzTrafficManagerProfile cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="a5101-133">To obtain a **TrafficManagerProfile** object, use the Get-AzTrafficManagerProfile cmdlet.</span></span>

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

### <span data-ttu-id="a5101-134">-확인</span><span class="sxs-lookup"><span data-stu-id="a5101-134">-Confirm</span></span>
<span data-ttu-id="a5101-135">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="a5101-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a5101-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a5101-136">-WhatIf</span></span>
<span data-ttu-id="a5101-137">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="a5101-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a5101-138">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="a5101-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a5101-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a5101-139">CommonParameters</span></span>
<span data-ttu-id="a5101-140">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="a5101-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a5101-141">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a5101-141">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a5101-142">입력</span><span class="sxs-lookup"><span data-stu-id="a5101-142">INPUTS</span></span>

### <span data-ttu-id="a5101-143">TrafficManager. TrafficManagerProfile/.</span><span class="sxs-lookup"><span data-stu-id="a5101-143">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerProfile</span></span>

## <span data-ttu-id="a5101-144">출력</span><span class="sxs-lookup"><span data-stu-id="a5101-144">OUTPUTS</span></span>

### <span data-ttu-id="a5101-145">시스템 부울</span><span class="sxs-lookup"><span data-stu-id="a5101-145">System.Boolean</span></span>

## <span data-ttu-id="a5101-146">상속자</span><span class="sxs-lookup"><span data-stu-id="a5101-146">NOTES</span></span>

## <span data-ttu-id="a5101-147">관련 링크</span><span class="sxs-lookup"><span data-stu-id="a5101-147">RELATED LINKS</span></span>

[<span data-ttu-id="a5101-148">Enable-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="a5101-148">Enable-AzTrafficManagerProfile</span></span>](./Enable-AzTrafficManagerProfile.md)

[<span data-ttu-id="a5101-149">Get-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="a5101-149">Get-AzTrafficManagerProfile</span></span>](./Get-AzTrafficManagerProfile.md)

[<span data-ttu-id="a5101-150">새로운 AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="a5101-150">New-AzTrafficManagerProfile</span></span>](./New-AzTrafficManagerProfile.md)

[<span data-ttu-id="a5101-151">제거-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="a5101-151">Remove-AzTrafficManagerProfile</span></span>](./Remove-AzTrafficManagerProfile.md)

[<span data-ttu-id="a5101-152">Set-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="a5101-152">Set-AzTrafficManagerProfile</span></span>](./Set-AzTrafficManagerProfile.md)


