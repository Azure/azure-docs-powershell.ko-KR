---
external help file: ''
Module Name: Az.ConnectedMachine
online version: https://docs.microsoft.com/en-us/powershell/module/az.connectedmachine/set-azconnectedmachineextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ConnectedMachine/help/Set-AzConnectedMachineExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ConnectedMachine/help/Set-AzConnectedMachineExtension.md
ms.openlocfilehash: b136f5194bdc7e0f4b4dfc969564d7ef8476d9bf
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98493771"
---
# <span data-ttu-id="796d2-101">Set-AzConnectedMachineExtension</span><span class="sxs-lookup"><span data-stu-id="796d2-101">Set-AzConnectedMachineExtension</span></span>

## <span data-ttu-id="796d2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="796d2-102">SYNOPSIS</span></span>
<span data-ttu-id="796d2-103">확장을 만들거나 업데이트하는 작업입니다.</span><span class="sxs-lookup"><span data-stu-id="796d2-103">The operation to create or update the extension.</span></span>

## <span data-ttu-id="796d2-104">구문</span><span class="sxs-lookup"><span data-stu-id="796d2-104">SYNTAX</span></span>

### <span data-ttu-id="796d2-105">UpdateExpanded(기본값)</span><span class="sxs-lookup"><span data-stu-id="796d2-105">UpdateExpanded (Default)</span></span>
```
Set-AzConnectedMachineExtension -MachineName <String> -Name <String> -ResourceGroupName <String>
 -Location <String> [-SubscriptionId <String>] [-AutoUpgradeMinorVersion] [-ExtensionType <String>]
 [-ForceRerun <String>] [-ProtectedSetting <IMachineExtensionPropertiesProtectedSettings>]
 [-Publisher <String>] [-Setting <IMachineExtensionPropertiesSettings>] [-Tag <Hashtable>]
 [-TypeHandlerVersion <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="796d2-106">업데이트</span><span class="sxs-lookup"><span data-stu-id="796d2-106">Update</span></span>
```
Set-AzConnectedMachineExtension -MachineName <String> -Name <String> -ResourceGroupName <String>
 -ExtensionParameter <IMachineExtension> [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="796d2-107">설명</span><span class="sxs-lookup"><span data-stu-id="796d2-107">DESCRIPTION</span></span>
<span data-ttu-id="796d2-108">확장을 만들거나 업데이트하는 작업입니다.</span><span class="sxs-lookup"><span data-stu-id="796d2-108">The operation to create or update the extension.</span></span>

## <span data-ttu-id="796d2-109">예제</span><span class="sxs-lookup"><span data-stu-id="796d2-109">EXAMPLES</span></span>

### <span data-ttu-id="796d2-110">예제 1: 머신에서 확장 설정</span><span class="sxs-lookup"><span data-stu-id="796d2-110">Example 1: Set an extension on a machine</span></span>
```powershell
PS C:\> $Settings = @{ "commandToExecute" = "powershell.exe -c Get-Process" }
PS C:\> Set-AzConnectedMachineExtension -Name custom -ResourceGroupName ContosoTest -MachineName win-eastus1 -Location eastus -Publisher "Microsoft.Compute" -TypeHandlerVersion 1.10 -Settings $Settings -ExtensionType CustomScriptExtension

Name   Location ProvisioningState
----   -------- -----------------
custom eastus   Succeeded
```

<span data-ttu-id="796d2-111">머신에서 확장을 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="796d2-111">Sets an extension on a machine.</span></span>

### <span data-ttu-id="796d2-112">예제 2: 파이프라인을 통해 지정된 확장 매개 변수를 사용하여 확장 설정</span><span class="sxs-lookup"><span data-stu-id="796d2-112">Example 2: Set an extension with extension parameters specified via the pipeline</span></span>
```powershell
PS C:\> $otherExtension = Get-AzConnectedMachineExtension -Name custom -ResourceGroupName ContosoTest -MachineName other
PS C:\> $otherExtension | Set-AzConnectedMachineExtension -Name custom -ResourceGroupName ContosoTest -MachineName important

Name   Location ProvisioningState
----   -------- -----------------
custom eastus   Succeeded
```

<span data-ttu-id="796d2-113">파이프라인을 통해 전달된 개체에서 제공하는 확장 매개 변수를 사용하여 확장을 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="796d2-113">This sets an extension with the extension parameters provided by the object passed in via the pipeline.</span></span>
<span data-ttu-id="796d2-114">이는 한 컴퓨터의 매개 변수를 잡고 다른 머신에 적용하려는 경우 매우 좋은 것입니다.</span><span class="sxs-lookup"><span data-stu-id="796d2-114">This is great if you want to grab the parameters of one machine and apply it to another machine.</span></span>

## <span data-ttu-id="796d2-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="796d2-115">PARAMETERS</span></span>

### <span data-ttu-id="796d2-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="796d2-116">-AsJob</span></span>
<span data-ttu-id="796d2-117">작업으로 명령 실행</span><span class="sxs-lookup"><span data-stu-id="796d2-117">Run the command as a job</span></span>

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

### <span data-ttu-id="796d2-118">-AutoUpgradeMinorVersion</span><span class="sxs-lookup"><span data-stu-id="796d2-118">-AutoUpgradeMinorVersion</span></span>
<span data-ttu-id="796d2-119">배포 시 사용할 수 있는 경우 확장에서 최신 부 버전을 사용할지 여부를 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="796d2-119">Indicates whether the extension should use a newer minor version if one is available at deployment time.</span></span>
<span data-ttu-id="796d2-120">그러나 배포된 후 이 속성을 true로 설정한 경우에도 재배포하지 않는 한 확장은 부 버전을 업그레이드하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="796d2-120">Once deployed, however, the extension will not upgrade minor versions unless redeployed, even with this property set to true.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: UpdateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="796d2-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="796d2-121">-DefaultProfile</span></span>
<span data-ttu-id="796d2-122">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="796d2-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: AzureRMContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="796d2-123">-ExtensionParameter</span><span class="sxs-lookup"><span data-stu-id="796d2-123">-ExtensionParameter</span></span>
<span data-ttu-id="796d2-124">컴퓨터 확장을 설명합니다.</span><span class="sxs-lookup"><span data-stu-id="796d2-124">Describes a Machine Extension.</span></span>
<span data-ttu-id="796d2-125">생성을 위해 EXTENSIONPARAMETER 속성에 대한 NOTES 섹션을 참조하고 해시 테이블을 만드십시오.</span><span class="sxs-lookup"><span data-stu-id="796d2-125">To construct, see NOTES section for EXTENSIONPARAMETER properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.ConnectedMachine.Models.Api20200802.IMachineExtension
Parameter Sets: Update
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="796d2-126">-ExtensionType</span><span class="sxs-lookup"><span data-stu-id="796d2-126">-ExtensionType</span></span>
<span data-ttu-id="796d2-127">확장의 유형을 지정합니다. 예를 들어 "CustomScriptExtension"입니다.</span><span class="sxs-lookup"><span data-stu-id="796d2-127">Specifies the type of the extension; an example is "CustomScriptExtension".</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="796d2-128">-ForceRerun</span><span class="sxs-lookup"><span data-stu-id="796d2-128">-ForceRerun</span></span>
<span data-ttu-id="796d2-129">확장 구성이 변경되지 않은 경우에도 확장 처리기 강제로 업데이트해야 하는 방식입니다.</span><span class="sxs-lookup"><span data-stu-id="796d2-129">How the extension handler should be forced to update even if the extension configuration has not changed.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="796d2-130">-Location</span><span class="sxs-lookup"><span data-stu-id="796d2-130">-Location</span></span>
<span data-ttu-id="796d2-131">리소스가 있는 지리적 위치</span><span class="sxs-lookup"><span data-stu-id="796d2-131">The geo-location where the resource lives</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="796d2-132">-MachineName</span><span class="sxs-lookup"><span data-stu-id="796d2-132">-MachineName</span></span>
<span data-ttu-id="796d2-133">확장을 만들거나 업데이트해야 하는 컴퓨터의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="796d2-133">The name of the machine where the extension should be created or updated.</span></span>

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

### <span data-ttu-id="796d2-134">-Name</span><span class="sxs-lookup"><span data-stu-id="796d2-134">-Name</span></span>
<span data-ttu-id="796d2-135">컴퓨터 확장의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="796d2-135">The name of the machine extension.</span></span>

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

### <span data-ttu-id="796d2-136">-NoWait</span><span class="sxs-lookup"><span data-stu-id="796d2-136">-NoWait</span></span>
<span data-ttu-id="796d2-137">명령을 비동기적으로 실행</span><span class="sxs-lookup"><span data-stu-id="796d2-137">Run the command asynchronously</span></span>

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

### <span data-ttu-id="796d2-138">-ProtectedSetting</span><span class="sxs-lookup"><span data-stu-id="796d2-138">-ProtectedSetting</span></span>
<span data-ttu-id="796d2-139">확장은 protectedSettings 또는 protectedSettingsFromKeyVault를 포함하거나 보호된 설정을 모두 포함할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="796d2-139">The extension can contain either protectedSettings or protectedSettingsFromKeyVault or no protected settings at all.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.ConnectedMachine.Models.Api20200802.IMachineExtensionPropertiesProtectedSettings
Parameter Sets: UpdateExpanded
Aliases: ProtectedSettings

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="796d2-140">-Publisher</span><span class="sxs-lookup"><span data-stu-id="796d2-140">-Publisher</span></span>
<span data-ttu-id="796d2-141">확장 처리기 게시자의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="796d2-141">The name of the extension handler publisher.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="796d2-142">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="796d2-142">-ResourceGroupName</span></span>
<span data-ttu-id="796d2-143">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="796d2-143">The name of the resource group.</span></span>

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

### <span data-ttu-id="796d2-144">-Setting</span><span class="sxs-lookup"><span data-stu-id="796d2-144">-Setting</span></span>
<span data-ttu-id="796d2-145">확장에 대한 Json 형식의 공용 설정입니다.</span><span class="sxs-lookup"><span data-stu-id="796d2-145">Json formatted public settings for the extension.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.ConnectedMachine.Models.Api20200802.IMachineExtensionPropertiesSettings
Parameter Sets: UpdateExpanded
Aliases: Settings

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="796d2-146">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="796d2-146">-SubscriptionId</span></span>
<span data-ttu-id="796d2-147">Microsoft Azure 구독을 고유하게 식별하는 구독 자격 증명입니다.</span><span class="sxs-lookup"><span data-stu-id="796d2-147">Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="796d2-148">구독 ID는 모든 서비스 호출에 대한 URI의 일부를 형성합니다.</span><span class="sxs-lookup"><span data-stu-id="796d2-148">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="796d2-149">-Tag</span><span class="sxs-lookup"><span data-stu-id="796d2-149">-Tag</span></span>
<span data-ttu-id="796d2-150">리소스 태그.</span><span class="sxs-lookup"><span data-stu-id="796d2-150">Resource tags.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: UpdateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="796d2-151">-TypeHandlerVersion</span><span class="sxs-lookup"><span data-stu-id="796d2-151">-TypeHandlerVersion</span></span>
<span data-ttu-id="796d2-152">스크립트 처리기 버전을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="796d2-152">Specifies the version of the script handler.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="796d2-153">-Confirm</span><span class="sxs-lookup"><span data-stu-id="796d2-153">-Confirm</span></span>
<span data-ttu-id="796d2-154">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="796d2-154">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="796d2-155">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="796d2-155">-WhatIf</span></span>
<span data-ttu-id="796d2-156">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="796d2-156">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="796d2-157">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="796d2-157">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="796d2-158">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="796d2-158">CommonParameters</span></span>
<span data-ttu-id="796d2-159">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="796d2-159">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="796d2-160">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="796d2-160">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="796d2-161">입력</span><span class="sxs-lookup"><span data-stu-id="796d2-161">INPUTS</span></span>

### <span data-ttu-id="796d2-162">Microsoft.Azure.PowerShell.Cmdlets.ConnectedMachine.Models.Api20200802.IMachineExtension</span><span class="sxs-lookup"><span data-stu-id="796d2-162">Microsoft.Azure.PowerShell.Cmdlets.ConnectedMachine.Models.Api20200802.IMachineExtension</span></span>

## <span data-ttu-id="796d2-163">출력</span><span class="sxs-lookup"><span data-stu-id="796d2-163">OUTPUTS</span></span>

### <span data-ttu-id="796d2-164">Microsoft.Azure.PowerShell.Cmdlets.ConnectedMachine.Models.Api20200802.IMachineExtension</span><span class="sxs-lookup"><span data-stu-id="796d2-164">Microsoft.Azure.PowerShell.Cmdlets.ConnectedMachine.Models.Api20200802.IMachineExtension</span></span>

## <span data-ttu-id="796d2-165">참고 사항</span><span class="sxs-lookup"><span data-stu-id="796d2-165">NOTES</span></span>

<span data-ttu-id="796d2-166">별칭</span><span class="sxs-lookup"><span data-stu-id="796d2-166">ALIASES</span></span>

<span data-ttu-id="796d2-167">복합 매개 변수 속성</span><span class="sxs-lookup"><span data-stu-id="796d2-167">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="796d2-168">아래에 설명된 매개 변수를 만들 수 있도록 적절한 속성을 포함하는 해시 테이블을 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="796d2-168">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="796d2-169">해시 테이블에 대한 자세한 내용은 다음 Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="796d2-169">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="796d2-170">EXTENSIONPARAMETER: <IMachineExtension> 컴퓨터 확장을 설명합니다.</span><span class="sxs-lookup"><span data-stu-id="796d2-170">EXTENSIONPARAMETER <IMachineExtension>: Describes a Machine Extension.</span></span>
  - <span data-ttu-id="796d2-171">`Location <String>`: 리소스가 있는 지리적 위치</span><span class="sxs-lookup"><span data-stu-id="796d2-171">`Location <String>`: The geo-location where the resource lives</span></span>
  - <span data-ttu-id="796d2-172">`[Tag <ITrackedResourceTags>]`: 리소스 태그입니다.</span><span class="sxs-lookup"><span data-stu-id="796d2-172">`[Tag <ITrackedResourceTags>]`: Resource tags.</span></span>
    - <span data-ttu-id="796d2-173">`[(Any) <String>]`: 이 개체에 추가할 수 있는 속성을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="796d2-173">`[(Any) <String>]`: This indicates any property can be added to this object.</span></span>
  - <span data-ttu-id="796d2-174">`[AutoUpgradeMinorVersion <Boolean?>]`: 배포 시 사용할 수 있는 경우 확장에서 최신 부 버전을 사용할지 여부를 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="796d2-174">`[AutoUpgradeMinorVersion <Boolean?>]`: Indicates whether the extension should use a newer minor version if one is available at deployment time.</span></span> <span data-ttu-id="796d2-175">그러나 배포된 후 이 속성을 true로 설정한 경우에도 재배포하지 않는 한 확장은 부 버전을 업그레이드하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="796d2-175">Once deployed, however, the extension will not upgrade minor versions unless redeployed, even with this property set to true.</span></span>
  - <span data-ttu-id="796d2-176">`[ForceUpdateTag <String>]`: 확장 구성이 변경되지 않은 경우에도 확장 처리기 강제로 업데이트해야 하는 방식입니다.</span><span class="sxs-lookup"><span data-stu-id="796d2-176">`[ForceUpdateTag <String>]`: How the extension handler should be forced to update even if the extension configuration has not changed.</span></span>
  - <span data-ttu-id="796d2-177">`[MachineExtensionType <String>]`: 확장의 유형을 지정합니다. 예를 들어 "CustomScriptExtension"입니다.</span><span class="sxs-lookup"><span data-stu-id="796d2-177">`[MachineExtensionType <String>]`: Specifies the type of the extension; an example is "CustomScriptExtension".</span></span>
  - <span data-ttu-id="796d2-178">`[ProtectedSetting <IMachineExtensionPropertiesProtectedSettings>]`: 확장은 protectedSettings 또는 protectedSettingsFromKeyVault를 포함하거나 보호된 설정을 모두 포함할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="796d2-178">`[ProtectedSetting <IMachineExtensionPropertiesProtectedSettings>]`: The extension can contain either protectedSettings or protectedSettingsFromKeyVault or no protected settings at all.</span></span>
  - <span data-ttu-id="796d2-179">`[Publisher <String>]`: 확장 처리기 게시자의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="796d2-179">`[Publisher <String>]`: The name of the extension handler publisher.</span></span>
  - <span data-ttu-id="796d2-180">`[Setting <IMachineExtensionPropertiesSettings>]`: 확장에 대한 Json 형식 공용 설정입니다.</span><span class="sxs-lookup"><span data-stu-id="796d2-180">`[Setting <IMachineExtensionPropertiesSettings>]`: Json formatted public settings for the extension.</span></span>
  - <span data-ttu-id="796d2-181">`[TypeHandlerVersion <String>]`: 스크립트 처리기 버전을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="796d2-181">`[TypeHandlerVersion <String>]`: Specifies the version of the script handler.</span></span>

## <span data-ttu-id="796d2-182">관련 링크</span><span class="sxs-lookup"><span data-stu-id="796d2-182">RELATED LINKS</span></span>

