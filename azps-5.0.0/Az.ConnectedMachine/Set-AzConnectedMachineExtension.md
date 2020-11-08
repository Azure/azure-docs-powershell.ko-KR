---
external help file: ''
Module Name: Az.ConnectedMachine
online version: https://docs.microsoft.com/en-us/powershell/module/az.connectedmachine/set-azconnectedmachineextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ConnectedMachine/help/Set-AzConnectedMachineExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ConnectedMachine/help/Set-AzConnectedMachineExtension.md
ms.openlocfilehash: b136f5194bdc7e0f4b4dfc969564d7ef8476d9bf
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94218732"
---
# <span data-ttu-id="da67e-101">Set-AzConnectedMachineExtension</span><span class="sxs-lookup"><span data-stu-id="da67e-101">Set-AzConnectedMachineExtension</span></span>

## <span data-ttu-id="da67e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="da67e-102">SYNOPSIS</span></span>
<span data-ttu-id="da67e-103">확장을 만들거나 업데이트 하는 작업입니다.</span><span class="sxs-lookup"><span data-stu-id="da67e-103">The operation to create or update the extension.</span></span>

## <span data-ttu-id="da67e-104">구문과</span><span class="sxs-lookup"><span data-stu-id="da67e-104">SYNTAX</span></span>

### <span data-ttu-id="da67e-105">UpdateExpanded 됨 (기본값)</span><span class="sxs-lookup"><span data-stu-id="da67e-105">UpdateExpanded (Default)</span></span>
```
Set-AzConnectedMachineExtension -MachineName <String> -Name <String> -ResourceGroupName <String>
 -Location <String> [-SubscriptionId <String>] [-AutoUpgradeMinorVersion] [-ExtensionType <String>]
 [-ForceRerun <String>] [-ProtectedSetting <IMachineExtensionPropertiesProtectedSettings>]
 [-Publisher <String>] [-Setting <IMachineExtensionPropertiesSettings>] [-Tag <Hashtable>]
 [-TypeHandlerVersion <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="da67e-106">Update</span><span class="sxs-lookup"><span data-stu-id="da67e-106">Update</span></span>
```
Set-AzConnectedMachineExtension -MachineName <String> -Name <String> -ResourceGroupName <String>
 -ExtensionParameter <IMachineExtension> [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="da67e-107">설명은</span><span class="sxs-lookup"><span data-stu-id="da67e-107">DESCRIPTION</span></span>
<span data-ttu-id="da67e-108">확장을 만들거나 업데이트 하는 작업입니다.</span><span class="sxs-lookup"><span data-stu-id="da67e-108">The operation to create or update the extension.</span></span>

## <span data-ttu-id="da67e-109">예제의</span><span class="sxs-lookup"><span data-stu-id="da67e-109">EXAMPLES</span></span>

### <span data-ttu-id="da67e-110">예제 1: 컴퓨터에서 확장 설정</span><span class="sxs-lookup"><span data-stu-id="da67e-110">Example 1: Set an extension on a machine</span></span>
```powershell
PS C:\> $Settings = @{ "commandToExecute" = "powershell.exe -c Get-Process" }
PS C:\> Set-AzConnectedMachineExtension -Name custom -ResourceGroupName ContosoTest -MachineName win-eastus1 -Location eastus -Publisher "Microsoft.Compute" -TypeHandlerVersion 1.10 -Settings $Settings -ExtensionType CustomScriptExtension

Name   Location ProvisioningState
----   -------- -----------------
custom eastus   Succeeded
```

<span data-ttu-id="da67e-111">컴퓨터에서 확장을 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="da67e-111">Sets an extension on a machine.</span></span>

### <span data-ttu-id="da67e-112">예제 2: 파이프라인을 통해 지정 된 확장 매개 변수를 사용 하 여 확장 설정</span><span class="sxs-lookup"><span data-stu-id="da67e-112">Example 2: Set an extension with extension parameters specified via the pipeline</span></span>
```powershell
PS C:\> $otherExtension = Get-AzConnectedMachineExtension -Name custom -ResourceGroupName ContosoTest -MachineName other
PS C:\> $otherExtension | Set-AzConnectedMachineExtension -Name custom -ResourceGroupName ContosoTest -MachineName important

Name   Location ProvisioningState
----   -------- -----------------
custom eastus   Succeeded
```

<span data-ttu-id="da67e-113">파이프라인을 통해 전달 된 개체에서 제공 하는 확장 매개 변수를 사용 하 여 확장명을 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="da67e-113">This sets an extension with the extension parameters provided by the object passed in via the pipeline.</span></span>
<span data-ttu-id="da67e-114">이는 한 컴퓨터의 매개 변수를 가져와 다른 컴퓨터에 적용 하려는 경우에 유용 합니다.</span><span class="sxs-lookup"><span data-stu-id="da67e-114">This is great if you want to grab the parameters of one machine and apply it to another machine.</span></span>

## <span data-ttu-id="da67e-115">변수</span><span class="sxs-lookup"><span data-stu-id="da67e-115">PARAMETERS</span></span>

### <span data-ttu-id="da67e-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="da67e-116">-AsJob</span></span>
<span data-ttu-id="da67e-117">작업으로 명령 실행</span><span class="sxs-lookup"><span data-stu-id="da67e-117">Run the command as a job</span></span>

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

### <span data-ttu-id="da67e-118">-AutoUpgradeMinorVersion</span><span class="sxs-lookup"><span data-stu-id="da67e-118">-AutoUpgradeMinorVersion</span></span>
<span data-ttu-id="da67e-119">배포 시 사용할 수 있는 확장이 새 부 버전을 사용 해야 하는지 여부를 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="da67e-119">Indicates whether the extension should use a newer minor version if one is available at deployment time.</span></span>
<span data-ttu-id="da67e-120">그러나 배포 된 후에는이 속성이 true로 설정 된 경우에도 확장에서 부 버전이 업그레이드 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="da67e-120">Once deployed, however, the extension will not upgrade minor versions unless redeployed, even with this property set to true.</span></span>

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

### <span data-ttu-id="da67e-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="da67e-121">-DefaultProfile</span></span>
<span data-ttu-id="da67e-122">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="da67e-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="da67e-123">-ExtensionParameter 변수</span><span class="sxs-lookup"><span data-stu-id="da67e-123">-ExtensionParameter</span></span>
<span data-ttu-id="da67e-124">컴퓨터 확장에 대해 설명 합니다.</span><span class="sxs-lookup"><span data-stu-id="da67e-124">Describes a Machine Extension.</span></span>
<span data-ttu-id="da67e-125">생성 하려면 EXTENSIONPARAMETER 속성에 대 한 참고 섹션을 참조 하 고 해시 테이블을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="da67e-125">To construct, see NOTES section for EXTENSIONPARAMETER properties and create a hash table.</span></span>

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

### <span data-ttu-id="da67e-126">-ExtensionType</span><span class="sxs-lookup"><span data-stu-id="da67e-126">-ExtensionType</span></span>
<span data-ttu-id="da67e-127">확장명의 유형을 지정 합니다. 예를 들어 "CustomScriptExtension"이 있습니다.</span><span class="sxs-lookup"><span data-stu-id="da67e-127">Specifies the type of the extension; an example is "CustomScriptExtension".</span></span>

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

### <span data-ttu-id="da67e-128">-ForceRerun</span><span class="sxs-lookup"><span data-stu-id="da67e-128">-ForceRerun</span></span>
<span data-ttu-id="da67e-129">확장 구성이 변경 되지 않은 경우에도 확장 처리기를 강제로 업데이트 하는 방법</span><span class="sxs-lookup"><span data-stu-id="da67e-129">How the extension handler should be forced to update even if the extension configuration has not changed.</span></span>

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

### <span data-ttu-id="da67e-130">-위치</span><span class="sxs-lookup"><span data-stu-id="da67e-130">-Location</span></span>
<span data-ttu-id="da67e-131">리소스가 상주 하는 지리적 위치</span><span class="sxs-lookup"><span data-stu-id="da67e-131">The geo-location where the resource lives</span></span>

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

### <span data-ttu-id="da67e-132">-MachineName</span><span class="sxs-lookup"><span data-stu-id="da67e-132">-MachineName</span></span>
<span data-ttu-id="da67e-133">확장명을 만들거나 업데이트 해야 하는 컴퓨터의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="da67e-133">The name of the machine where the extension should be created or updated.</span></span>

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

### <span data-ttu-id="da67e-134">-이름</span><span class="sxs-lookup"><span data-stu-id="da67e-134">-Name</span></span>
<span data-ttu-id="da67e-135">컴퓨터 확장의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="da67e-135">The name of the machine extension.</span></span>

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

### <span data-ttu-id="da67e-136">-NoWait</span><span class="sxs-lookup"><span data-stu-id="da67e-136">-NoWait</span></span>
<span data-ttu-id="da67e-137">비동기적으로 명령 실행</span><span class="sxs-lookup"><span data-stu-id="da67e-137">Run the command asynchronously</span></span>

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

### <span data-ttu-id="da67e-138">-ProtectedSetting</span><span class="sxs-lookup"><span data-stu-id="da67e-138">-ProtectedSetting</span></span>
<span data-ttu-id="da67e-139">확장명에는 protectedSettings 또는 protectedSettingsFromKeyVault를 포함할 수도 있고 보호 되는 설정이 전혀 없습니다.</span><span class="sxs-lookup"><span data-stu-id="da67e-139">The extension can contain either protectedSettings or protectedSettingsFromKeyVault or no protected settings at all.</span></span>

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

### <span data-ttu-id="da67e-140">-Publisher</span><span class="sxs-lookup"><span data-stu-id="da67e-140">-Publisher</span></span>
<span data-ttu-id="da67e-141">확장 처리기 게시자의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="da67e-141">The name of the extension handler publisher.</span></span>

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

### <span data-ttu-id="da67e-142">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="da67e-142">-ResourceGroupName</span></span>
<span data-ttu-id="da67e-143">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="da67e-143">The name of the resource group.</span></span>

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

### <span data-ttu-id="da67e-144">-설정</span><span class="sxs-lookup"><span data-stu-id="da67e-144">-Setting</span></span>
<span data-ttu-id="da67e-145">확장에 대 한 Json 형식의 공용 설정입니다.</span><span class="sxs-lookup"><span data-stu-id="da67e-145">Json formatted public settings for the extension.</span></span>

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

### <span data-ttu-id="da67e-146">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="da67e-146">-SubscriptionId</span></span>
<span data-ttu-id="da67e-147">Microsoft Azure 구독을 고유 하 게 식별 하는 구독 자격 증명입니다.</span><span class="sxs-lookup"><span data-stu-id="da67e-147">Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="da67e-148">구독 ID는 모든 서비스 호출에 대 한 URI의 일부를 형성 합니다.</span><span class="sxs-lookup"><span data-stu-id="da67e-148">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="da67e-149">태그</span><span class="sxs-lookup"><span data-stu-id="da67e-149">-Tag</span></span>
<span data-ttu-id="da67e-150">리소스 태그.</span><span class="sxs-lookup"><span data-stu-id="da67e-150">Resource tags.</span></span>

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

### <span data-ttu-id="da67e-151">-TypeHandlerVersion</span><span class="sxs-lookup"><span data-stu-id="da67e-151">-TypeHandlerVersion</span></span>
<span data-ttu-id="da67e-152">스크립트 처리기의 버전을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="da67e-152">Specifies the version of the script handler.</span></span>

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

### <span data-ttu-id="da67e-153">-확인</span><span class="sxs-lookup"><span data-stu-id="da67e-153">-Confirm</span></span>
<span data-ttu-id="da67e-154">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="da67e-154">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="da67e-155">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="da67e-155">-WhatIf</span></span>
<span data-ttu-id="da67e-156">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="da67e-156">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="da67e-157">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="da67e-157">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="da67e-158">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="da67e-158">CommonParameters</span></span>
<span data-ttu-id="da67e-159">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="da67e-159">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="da67e-160">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="da67e-160">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="da67e-161">입력</span><span class="sxs-lookup"><span data-stu-id="da67e-161">INPUTS</span></span>

### <span data-ttu-id="da67e-162">ConnectedMachine. Api20200802. i a m.. PowerShell.</span><span class="sxs-lookup"><span data-stu-id="da67e-162">Microsoft.Azure.PowerShell.Cmdlets.ConnectedMachine.Models.Api20200802.IMachineExtension</span></span>

## <span data-ttu-id="da67e-163">출력</span><span class="sxs-lookup"><span data-stu-id="da67e-163">OUTPUTS</span></span>

### <span data-ttu-id="da67e-164">ConnectedMachine. Api20200802. i a m.. PowerShell.</span><span class="sxs-lookup"><span data-stu-id="da67e-164">Microsoft.Azure.PowerShell.Cmdlets.ConnectedMachine.Models.Api20200802.IMachineExtension</span></span>

## <span data-ttu-id="da67e-165">상속자</span><span class="sxs-lookup"><span data-stu-id="da67e-165">NOTES</span></span>

<span data-ttu-id="da67e-166">별칭과</span><span class="sxs-lookup"><span data-stu-id="da67e-166">ALIASES</span></span>

<span data-ttu-id="da67e-167">복합 매개 변수 속성</span><span class="sxs-lookup"><span data-stu-id="da67e-167">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="da67e-168">아래 설명 된 매개 변수를 만들려면 적절 한 속성을 포함 하는 해시 테이블을 생성 합니다.</span><span class="sxs-lookup"><span data-stu-id="da67e-168">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="da67e-169">해시 테이블에 대 한 자세한 내용은 Get-Help about_Hash_Tables를 실행 하세요.</span><span class="sxs-lookup"><span data-stu-id="da67e-169">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="da67e-170">EXTENSIONPARAMETER <IMachineExtension> : 컴퓨터 확장명을 설명 합니다.</span><span class="sxs-lookup"><span data-stu-id="da67e-170">EXTENSIONPARAMETER <IMachineExtension>: Describes a Machine Extension.</span></span>
  - <span data-ttu-id="da67e-171">`Location <String>`: 리소스가 상주 하는 지리적 위치</span><span class="sxs-lookup"><span data-stu-id="da67e-171">`Location <String>`: The geo-location where the resource lives</span></span>
  - <span data-ttu-id="da67e-172">`[Tag <ITrackedResourceTags>]`: 리소스 태그.</span><span class="sxs-lookup"><span data-stu-id="da67e-172">`[Tag <ITrackedResourceTags>]`: Resource tags.</span></span>
    - <span data-ttu-id="da67e-173">`[(Any) <String>]`:이 개체에 모든 속성이 추가 될 수 있음을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="da67e-173">`[(Any) <String>]`: This indicates any property can be added to this object.</span></span>
  - <span data-ttu-id="da67e-174">`[AutoUpgradeMinorVersion <Boolean?>]`: 배포 시 사용할 수 있는 경우 확장에서 최신 부 버전을 사용 해야 하는지 여부를 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="da67e-174">`[AutoUpgradeMinorVersion <Boolean?>]`: Indicates whether the extension should use a newer minor version if one is available at deployment time.</span></span> <span data-ttu-id="da67e-175">그러나 배포 된 후에는이 속성이 true로 설정 된 경우에도 확장에서 부 버전이 업그레이드 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="da67e-175">Once deployed, however, the extension will not upgrade minor versions unless redeployed, even with this property set to true.</span></span>
  - <span data-ttu-id="da67e-176">`[ForceUpdateTag <String>]`: 확장 구성이 변경 되지 않은 경우에도 확장 처리기를 강제로 업데이트 해야 하는 방법입니다.</span><span class="sxs-lookup"><span data-stu-id="da67e-176">`[ForceUpdateTag <String>]`: How the extension handler should be forced to update even if the extension configuration has not changed.</span></span>
  - <span data-ttu-id="da67e-177">`[MachineExtensionType <String>]`: 확장의 형식을 지정 합니다. 예를 들어 "CustomScriptExtension"이 있습니다.</span><span class="sxs-lookup"><span data-stu-id="da67e-177">`[MachineExtensionType <String>]`: Specifies the type of the extension; an example is "CustomScriptExtension".</span></span>
  - <span data-ttu-id="da67e-178">`[ProtectedSetting <IMachineExtensionPropertiesProtectedSettings>]`: 확장명에는 protectedSettings 또는 protectedSettingsFromKeyVault를 포함할 수도 있고 보호 되는 설정이 전혀 없습니다.</span><span class="sxs-lookup"><span data-stu-id="da67e-178">`[ProtectedSetting <IMachineExtensionPropertiesProtectedSettings>]`: The extension can contain either protectedSettings or protectedSettingsFromKeyVault or no protected settings at all.</span></span>
  - <span data-ttu-id="da67e-179">`[Publisher <String>]`: 확장 처리기 게시자의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="da67e-179">`[Publisher <String>]`: The name of the extension handler publisher.</span></span>
  - <span data-ttu-id="da67e-180">`[Setting <IMachineExtensionPropertiesSettings>]`: 확장에 대 한 Json 형식의 공용 설정입니다.</span><span class="sxs-lookup"><span data-stu-id="da67e-180">`[Setting <IMachineExtensionPropertiesSettings>]`: Json formatted public settings for the extension.</span></span>
  - <span data-ttu-id="da67e-181">`[TypeHandlerVersion <String>]`: 스크립트 처리기의 버전을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="da67e-181">`[TypeHandlerVersion <String>]`: Specifies the version of the script handler.</span></span>

## <span data-ttu-id="da67e-182">관련 링크</span><span class="sxs-lookup"><span data-stu-id="da67e-182">RELATED LINKS</span></span>

