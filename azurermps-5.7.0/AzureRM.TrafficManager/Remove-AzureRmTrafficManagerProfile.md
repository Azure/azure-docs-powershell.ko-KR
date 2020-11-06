---
external help file: Microsoft.Azure.Commands.TrafficManager.dll-Help.xml
Module Name: AzureRM
ms.assetid: 5A4D685F-B904-4C85-8B68-C9936B0627FA
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.trafficmanager/remove-azurermtrafficmanagerprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/TrafficManager/Commands.TrafficManager2/help/Remove-AzureRmTrafficManagerProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/TrafficManager/Commands.TrafficManager2/help/Remove-AzureRmTrafficManagerProfile.md
ms.openlocfilehash: 459ede802e3a96805bb2c32e4e901592604f03b0
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93529678"
---
# <span data-ttu-id="23880-101">Remove-AzureRmTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="23880-101">Remove-AzureRmTrafficManagerProfile</span></span>

## <span data-ttu-id="23880-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="23880-102">SYNOPSIS</span></span>
<span data-ttu-id="23880-103">Traffic Manager 프로필을 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="23880-103">Deletes a Traffic Manager profile.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="23880-104">구문과</span><span class="sxs-lookup"><span data-stu-id="23880-104">SYNTAX</span></span>

### <span data-ttu-id="23880-105">필드인</span><span class="sxs-lookup"><span data-stu-id="23880-105">Fields</span></span>
```
Remove-AzureRmTrafficManagerProfile -Name <String> -ResourceGroupName <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="23880-106">오브젝트가</span><span class="sxs-lookup"><span data-stu-id="23880-106">Object</span></span>
```
Remove-AzureRmTrafficManagerProfile -TrafficManagerProfile <TrafficManagerProfile> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="23880-107">설명은</span><span class="sxs-lookup"><span data-stu-id="23880-107">DESCRIPTION</span></span>
<span data-ttu-id="23880-108">**AzureRmTrafficManagerProfile** Cmdlet은 Azure Traffic Manager 프로필을 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="23880-108">The **Remove-AzureRmTrafficManagerProfile** cmdlet deletes an Azure Traffic Manager profile.</span></span>
<span data-ttu-id="23880-109">*Name* 및 *ResourceGroupName* 매개 변수를 사용 하 여 삭제할 프로필을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="23880-109">Specify the profile to delete by using the *Name* and *ResourceGroupName* parameters.</span></span>
<span data-ttu-id="23880-110">또는 *TrafficManagerProfile* 매개 변수를 사용 하 여 **TrafficManagerProfile** 개체를 지정 하거나 파이프라인을 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="23880-110">Alternatively, you can specify a **TrafficManagerProfile** object using the *TrafficManagerProfile* parameter, or you can use the pipeline.</span></span>

## <span data-ttu-id="23880-111">예제의</span><span class="sxs-lookup"><span data-stu-id="23880-111">EXAMPLES</span></span>

### <span data-ttu-id="23880-112">예제 1: 이름으로 지정 된 프로필 삭제</span><span class="sxs-lookup"><span data-stu-id="23880-112">Example 1: Delete a profile specified by name</span></span>
```
PS C:\>Remove-AzureRmTrafficManagerProfile -Name "ContosoProfile" -ResourceGroupName "ResourceGroup11"
```

<span data-ttu-id="23880-113">이 명령은 ResourceGroup11에서 ContosoProfile 이라는 프로필을 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="23880-113">This command deletes the profile named ContosoProfile in ResourceGroup11.</span></span>
<span data-ttu-id="23880-114">명령에서 확인 하 라는 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="23880-114">The command prompts you for confirmation.</span></span>

### <span data-ttu-id="23880-115">예제 2: 파이프라인을 사용 하 여 프로필 삭제</span><span class="sxs-lookup"><span data-stu-id="23880-115">Example 2: Delete a profile by using the pipeline</span></span>
```
PS C:\>Get-AzureRmTrafficManagerProfile -Name "ContosoProfile" -ResourceGroupName "ResourceGroup11" | Remove-AzureRmTrafficManagerProfile -Force
```

<span data-ttu-id="23880-116">이 명령은 ResourceGroup11에서 ContosoProfile 이라는 프로필을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="23880-116">This command gets the profile named ContosoProfile in ResourceGroup11.</span></span>
<span data-ttu-id="23880-117">그런 다음이 명령은 파이프라인 연산자를 사용 하 여 해당 프로필을 **AzureRmTrafficManagerProfile** cmdlet에 전달 합니다.</span><span class="sxs-lookup"><span data-stu-id="23880-117">The command then passes that profile to the **Remove-AzureRmTrafficManagerProfile** cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="23880-118">해당 cmdlet은 해당 프로필을 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="23880-118">That cmdlet deletes that profile.</span></span>
<span data-ttu-id="23880-119">명령에서 *Force* 매개 변수를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="23880-119">The command specifies the *Force* parameter.</span></span>
<span data-ttu-id="23880-120">따라서 확인 메시지가 표시 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="23880-120">Therefore, it does not prompt you for confirmation.</span></span>

## <span data-ttu-id="23880-121">변수</span><span class="sxs-lookup"><span data-stu-id="23880-121">PARAMETERS</span></span>

### <span data-ttu-id="23880-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="23880-122">-DefaultProfile</span></span>
<span data-ttu-id="23880-123">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="23880-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="23880-124">-Force</span><span class="sxs-lookup"><span data-stu-id="23880-124">-Force</span></span>
<span data-ttu-id="23880-125">사용자 확인을 요청 하지 않고 명령을 강제로 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="23880-125">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="23880-126">-이름</span><span class="sxs-lookup"><span data-stu-id="23880-126">-Name</span></span>
<span data-ttu-id="23880-127">이 cmdlet이 삭제 하는 Traffic Manager 프로필의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="23880-127">Specifies the name of the Traffic Manager profile that this cmdlet deletes.</span></span>

```yaml
Type: String
Parameter Sets: Fields
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="23880-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="23880-128">-ResourceGroupName</span></span>
<span data-ttu-id="23880-129">리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="23880-129">Specifies the name of a resource group.</span></span>
<span data-ttu-id="23880-130">이 cmdlet은이 매개 변수에서 지정 하는 그룹에서 Traffic Manager 프로필을 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="23880-130">This cmdlet deletes a Traffic Manager profile in the group that this parameter specifies.</span></span>

```yaml
Type: String
Parameter Sets: Fields
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="23880-131">-TrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="23880-131">-TrafficManagerProfile</span></span>
<span data-ttu-id="23880-132">삭제할 **TrafficManagerProfile** 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="23880-132">Specifies a **TrafficManagerProfile** object to delete.</span></span>
<span data-ttu-id="23880-133">**TrafficManagerProfile** 개체를 가져오려면 Get-AzureRmTrafficManagerProfile cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="23880-133">To obtain a **TrafficManagerProfile** object, use the Get-AzureRmTrafficManagerProfile cmdlet.</span></span>

```yaml
Type: TrafficManagerProfile
Parameter Sets: Object
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="23880-134">-확인</span><span class="sxs-lookup"><span data-stu-id="23880-134">-Confirm</span></span>
<span data-ttu-id="23880-135">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="23880-135">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="23880-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="23880-136">-WhatIf</span></span>
<span data-ttu-id="23880-137">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="23880-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="23880-138">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="23880-138">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="23880-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="23880-139">CommonParameters</span></span>
<span data-ttu-id="23880-140">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="23880-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="23880-141">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="23880-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="23880-142">입력</span><span class="sxs-lookup"><span data-stu-id="23880-142">INPUTS</span></span>

### <span data-ttu-id="23880-143">TrafficManagerProfile (Network.)</span><span class="sxs-lookup"><span data-stu-id="23880-143">Microsoft.Azure.Commands.Network.TrafficManagerProfile</span></span>
<span data-ttu-id="23880-144">이 cmdlet은 **TrafficManagerProfile** 개체를 허용 합니다.</span><span class="sxs-lookup"><span data-stu-id="23880-144">This cmdlet accepts a **TrafficManagerProfile** object.</span></span>

## <span data-ttu-id="23880-145">출력</span><span class="sxs-lookup"><span data-stu-id="23880-145">OUTPUTS</span></span>

### <span data-ttu-id="23880-146">나타내는</span><span class="sxs-lookup"><span data-stu-id="23880-146">Boolean</span></span>
<span data-ttu-id="23880-147">이 cmdlet은 성공할 경우 $True 값을 반환 하 고, 삭제에 실패 하는 경우에는 $False 값을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="23880-147">This cmdlet returns a value of $True, if it succeeds or, if the deletion fails, a value of $False.</span></span>

## <span data-ttu-id="23880-148">상속자</span><span class="sxs-lookup"><span data-stu-id="23880-148">NOTES</span></span>

## <span data-ttu-id="23880-149">관련 링크</span><span class="sxs-lookup"><span data-stu-id="23880-149">RELATED LINKS</span></span>

[<span data-ttu-id="23880-150">Disable-AzureRmTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="23880-150">Disable-AzureRmTrafficManagerProfile</span></span>](./Disable-AzureRmTrafficManagerProfile.md)

[<span data-ttu-id="23880-151">Enable-AzureRmTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="23880-151">Enable-AzureRmTrafficManagerProfile</span></span>](./Enable-AzureRmTrafficManagerProfile.md)

[<span data-ttu-id="23880-152">Get-AzureRmTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="23880-152">Get-AzureRmTrafficManagerProfile</span></span>](./Get-AzureRmTrafficManagerProfile.md)

[<span data-ttu-id="23880-153">새로운 AzureRmTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="23880-153">New-AzureRmTrafficManagerProfile</span></span>](./New-AzureRmTrafficManagerProfile.md)

[<span data-ttu-id="23880-154">Set-AzureRmTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="23880-154">Set-AzureRmTrafficManagerProfile</span></span>](./Set-AzureRmTrafficManagerProfile.md)


