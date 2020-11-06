---
external help file: Microsoft.Azure.Commands.TrafficManager.dll-Help.xml
Module Name: AzureRM.TrafficManager
ms.assetid: B6E043FF-F4DD-44B7-BEAA-6B17C8F21D58
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.trafficmanager/disable-azurermtrafficmanagerprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/TrafficManager/Commands.TrafficManager2/help/Disable-AzureRmTrafficManagerProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/TrafficManager/Commands.TrafficManager2/help/Disable-AzureRmTrafficManagerProfile.md
ms.openlocfilehash: e714caedb86bd647ccc0692c47233833bc2db867
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93525951"
---
# <span data-ttu-id="a0808-101">Disable-AzureRmTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="a0808-101">Disable-AzureRmTrafficManagerProfile</span></span>

## <span data-ttu-id="a0808-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a0808-102">SYNOPSIS</span></span>
<span data-ttu-id="a0808-103">Traffic Manager 프로필을 사용 하지 않도록 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a0808-103">Disables a Traffic Manager profile.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a0808-104">구문과</span><span class="sxs-lookup"><span data-stu-id="a0808-104">SYNTAX</span></span>

### <span data-ttu-id="a0808-105">필드인</span><span class="sxs-lookup"><span data-stu-id="a0808-105">Fields</span></span>
```
Disable-AzureRmTrafficManagerProfile -Name <String> -ResourceGroupName <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a0808-106">오브젝트가</span><span class="sxs-lookup"><span data-stu-id="a0808-106">Object</span></span>
```
Disable-AzureRmTrafficManagerProfile -TrafficManagerProfile <TrafficManagerProfile> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a0808-107">설명은</span><span class="sxs-lookup"><span data-stu-id="a0808-107">DESCRIPTION</span></span>
<span data-ttu-id="a0808-108">**AzureRmTrafficManagerProfile** Cmdlet은 Azure Traffic Manager 프로필을 사용 하지 않도록 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a0808-108">The **Disable-AzureRmTrafficManagerProfile** cmdlet disables an Azure Traffic Manager profile.</span></span>
<span data-ttu-id="a0808-109">파이프라인 또는 매개 변수 값을 사용 하 여 프로필 개체를 지정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="a0808-109">You can specify the profile object by using the pipeline or as a parameter value.</span></span>
<span data-ttu-id="a0808-110">또는 *Name* 및 *ResourceGroupName* 매개 변수를 사용 하 여 프로필을 지정할 수도 있습니다.</span><span class="sxs-lookup"><span data-stu-id="a0808-110">Alternatively, you can specify the profile by using the *Name* and *ResourceGroupName* parameters.</span></span>

## <span data-ttu-id="a0808-111">예제의</span><span class="sxs-lookup"><span data-stu-id="a0808-111">EXAMPLES</span></span>

### <span data-ttu-id="a0808-112">예제 1: 이름으로 지정 된 프로필 사용 안 함</span><span class="sxs-lookup"><span data-stu-id="a0808-112">Example 1: Disable a profile specified by name</span></span>
```
PS C:\>Disable-AzureRmTrafficManagerProfile -Name "ContosoProfile" -ResourceGroupName "ResourceGroup11"
```

<span data-ttu-id="a0808-113">이 명령은 ResourceGroup11에서 ContosoProfile 이라는 프로필을 사용 하지 않도록 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a0808-113">This command disables the profile named ContosoProfile in ResourceGroup11.</span></span>
<span data-ttu-id="a0808-114">명령에서 확인 하 라는 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="a0808-114">The command prompts you for confirmation.</span></span>

### <span data-ttu-id="a0808-115">예제 2: 파이프라인을 사용 하 여 프로필 비활성화</span><span class="sxs-lookup"><span data-stu-id="a0808-115">Example 2: Disable a profile by using the pipeline</span></span>
```
PS C:\>Get-AzureRmTrafficManagerProfile -Name "ContosoProfile" -ResourceGroupName "ResourceGroup11" | Disable-AzureRmTrafficManagerProfile -Force
```

<span data-ttu-id="a0808-116">이 명령은 ResourceGroup11에서 ContosoProfile 이라는 프로필을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="a0808-116">This command gets the profile named ContosoProfile in ResourceGroup11.</span></span>
<span data-ttu-id="a0808-117">그런 다음이 명령은 파이프라인 연산자를 사용 하 여 해당 프로필을 **AzureRmTrafficManagerProfile** cmdlet에 전달 합니다.</span><span class="sxs-lookup"><span data-stu-id="a0808-117">The command then passes that profile to the **Disable-AzureRmTrafficManagerProfile** cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="a0808-118">해당 cmdlet은 해당 프로필을 사용 하지 않도록 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a0808-118">That cmdlet disables that profile.</span></span>
<span data-ttu-id="a0808-119">명령에서 *Force* 매개 변수를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a0808-119">The command specifies the *Force* parameter.</span></span>
<span data-ttu-id="a0808-120">따라서 확인 메시지가 표시 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="a0808-120">Therefore, it does not prompt you for confirmation.</span></span>

## <span data-ttu-id="a0808-121">변수</span><span class="sxs-lookup"><span data-stu-id="a0808-121">PARAMETERS</span></span>

### <span data-ttu-id="a0808-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a0808-122">-DefaultProfile</span></span>
<span data-ttu-id="a0808-123">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="a0808-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a0808-124">-Force</span><span class="sxs-lookup"><span data-stu-id="a0808-124">-Force</span></span>
<span data-ttu-id="a0808-125">사용자 확인을 요청 하지 않고 명령을 강제로 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="a0808-125">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="a0808-126">-이름</span><span class="sxs-lookup"><span data-stu-id="a0808-126">-Name</span></span>
<span data-ttu-id="a0808-127">이 cmdlet이 사용 하지 않도록 설정 하는 Traffic Manager 프로필의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a0808-127">Specifies the name of the Traffic Manager profile that this cmdlet disables.</span></span>

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

### <span data-ttu-id="a0808-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a0808-128">-ResourceGroupName</span></span>
<span data-ttu-id="a0808-129">리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a0808-129">Specifies the name of a resource group.</span></span>
<span data-ttu-id="a0808-130">이 cmdlet은이 매개 변수에서 지정 하는 그룹에서 Traffic Manager 프로필을 사용 하지 않도록 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a0808-130">This cmdlet disables a Traffic Manager profile in the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="a0808-131">-TrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="a0808-131">-TrafficManagerProfile</span></span>
<span data-ttu-id="a0808-132">사용 하지 않도록 설정할 **TrafficManagerProfile** 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a0808-132">Specifies a **TrafficManagerProfile** object to disable.</span></span>
<span data-ttu-id="a0808-133">**TrafficManagerProfile** 개체를 가져오려면 Get-AzureRmTrafficManagerProfile cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="a0808-133">To obtain a **TrafficManagerProfile** object, use the Get-AzureRmTrafficManagerProfile cmdlet.</span></span>

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

### <span data-ttu-id="a0808-134">-확인</span><span class="sxs-lookup"><span data-stu-id="a0808-134">-Confirm</span></span>
<span data-ttu-id="a0808-135">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="a0808-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a0808-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a0808-136">-WhatIf</span></span>
<span data-ttu-id="a0808-137">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="a0808-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a0808-138">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="a0808-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a0808-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a0808-139">CommonParameters</span></span>
<span data-ttu-id="a0808-140">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="a0808-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a0808-141">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a0808-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a0808-142">입력</span><span class="sxs-lookup"><span data-stu-id="a0808-142">INPUTS</span></span>

### <span data-ttu-id="a0808-143">TrafficManagerProfile (Network.)</span><span class="sxs-lookup"><span data-stu-id="a0808-143">Microsoft.Azure.Commands.Network.TrafficManagerProfile</span></span>
<span data-ttu-id="a0808-144">이 cmdlet은 **TrafficManagerProfile** 개체를 허용 합니다.</span><span class="sxs-lookup"><span data-stu-id="a0808-144">This cmdlet accepts a **TrafficManagerProfile** object.</span></span>

## <span data-ttu-id="a0808-145">출력</span><span class="sxs-lookup"><span data-stu-id="a0808-145">OUTPUTS</span></span>

### <span data-ttu-id="a0808-146">시스템 부울</span><span class="sxs-lookup"><span data-stu-id="a0808-146">System.Boolean</span></span>

## <span data-ttu-id="a0808-147">상속자</span><span class="sxs-lookup"><span data-stu-id="a0808-147">NOTES</span></span>

## <span data-ttu-id="a0808-148">관련 링크</span><span class="sxs-lookup"><span data-stu-id="a0808-148">RELATED LINKS</span></span>

[<span data-ttu-id="a0808-149">Enable-AzureRmTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="a0808-149">Enable-AzureRmTrafficManagerProfile</span></span>](./Enable-AzureRmTrafficManagerProfile.md)

[<span data-ttu-id="a0808-150">Get-AzureRmTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="a0808-150">Get-AzureRmTrafficManagerProfile</span></span>](./Get-AzureRmTrafficManagerProfile.md)

[<span data-ttu-id="a0808-151">새로운 AzureRmTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="a0808-151">New-AzureRmTrafficManagerProfile</span></span>](./New-AzureRmTrafficManagerProfile.md)

[<span data-ttu-id="a0808-152">제거-AzureRmTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="a0808-152">Remove-AzureRmTrafficManagerProfile</span></span>](./Remove-AzureRmTrafficManagerProfile.md)

[<span data-ttu-id="a0808-153">Set-AzureRmTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="a0808-153">Set-AzureRmTrafficManagerProfile</span></span>](./Set-AzureRmTrafficManagerProfile.md)


