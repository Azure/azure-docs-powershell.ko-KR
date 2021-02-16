---
external help file: ''
Module Name: Az.ConnectedMachine
online version: https://docs.microsoft.com/en-us/powershell/module/az.connectedmachine/update-azconnectedmachineextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ConnectedMachine/help/Update-AzConnectedMachineExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ConnectedMachine/help/Update-AzConnectedMachineExtension.md
ms.openlocfilehash: 95334b4f67685183e499518b068f1003f5bb6547
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100177388"
---
# <span data-ttu-id="2bef0-101">Update-AzConnectedMachineExtension</span><span class="sxs-lookup"><span data-stu-id="2bef0-101">Update-AzConnectedMachineExtension</span></span>

## <span data-ttu-id="2bef0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2bef0-102">SYNOPSIS</span></span>
<span data-ttu-id="2bef0-103">확장을 만들거나 업데이트하는 작업입니다.</span><span class="sxs-lookup"><span data-stu-id="2bef0-103">The operation to create or update the extension.</span></span>

## <span data-ttu-id="2bef0-104">구문</span><span class="sxs-lookup"><span data-stu-id="2bef0-104">SYNTAX</span></span>

### <span data-ttu-id="2bef0-105">UpdateExpanded(기본값)</span><span class="sxs-lookup"><span data-stu-id="2bef0-105">UpdateExpanded (Default)</span></span>
```
Update-AzConnectedMachineExtension -MachineName <String> -Name <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-AutoUpgradeMinorVersion] [-ForceRerun <String>]
 [-ProtectedSetting <IMachineExtensionUpdatePropertiesProtectedSettings>] [-Publisher <String>]
 [-Setting <IMachineExtensionUpdatePropertiesSettings>] [-Tag <Hashtable>] [-Type <String>]
 [-TypeHandlerVersion <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="2bef0-106">업데이트</span><span class="sxs-lookup"><span data-stu-id="2bef0-106">Update</span></span>
```
Update-AzConnectedMachineExtension -MachineName <String> -Name <String> -ResourceGroupName <String>
 -ExtensionParameter <IMachineExtensionUpdate> [-SubscriptionId <String>] [-DefaultProfile <PSObject>]
 [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="2bef0-107">UpdateViaIdentity</span><span class="sxs-lookup"><span data-stu-id="2bef0-107">UpdateViaIdentity</span></span>
```
Update-AzConnectedMachineExtension -InputObject <IConnectedMachineIdentity>
 -ExtensionParameter <IMachineExtensionUpdate> [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="2bef0-108">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="2bef0-108">UpdateViaIdentityExpanded</span></span>
```
Update-AzConnectedMachineExtension -InputObject <IConnectedMachineIdentity> [-AutoUpgradeMinorVersion]
 [-ForceRerun <String>] [-ProtectedSetting <IMachineExtensionUpdatePropertiesProtectedSettings>]
 [-Publisher <String>] [-Setting <IMachineExtensionUpdatePropertiesSettings>] [-Tag <Hashtable>]
 [-Type <String>] [-TypeHandlerVersion <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="2bef0-109">설명</span><span class="sxs-lookup"><span data-stu-id="2bef0-109">DESCRIPTION</span></span>
<span data-ttu-id="2bef0-110">확장을 만들거나 업데이트하는 작업입니다.</span><span class="sxs-lookup"><span data-stu-id="2bef0-110">The operation to create or update the extension.</span></span>

## <span data-ttu-id="2bef0-111">예제</span><span class="sxs-lookup"><span data-stu-id="2bef0-111">EXAMPLES</span></span>

### <span data-ttu-id="2bef0-112">예제 1: 확장 업데이트</span><span class="sxs-lookup"><span data-stu-id="2bef0-112">Example 1: Update an extension</span></span>
```powershell
PS C:\> $splat = @{
            ResourceGroupName = "connectedMachines"
            MachineName = "linux-eastus1_1"
            Name = "customScript"
            Settings = @{
                commandToExecute = "ls -l"
            }
        }
PS C:\> Update-AzConnectedMachineExtension @splat

Name         Location ProvisioningState
----         -------- -----------------
customScript eastus   Succeeded
```

<span data-ttu-id="2bef0-113">특정 머신에서 확장을 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="2bef0-113">Updates an extension on a specific machine.</span></span>

### <span data-ttu-id="2bef0-114">예제 2: 파이프라인을 통해 지정된 위치로 확장 업데이트</span><span class="sxs-lookup"><span data-stu-id="2bef0-114">Example 2: Update an extension with location specified via the pipeline</span></span>
```powershell
PS C:\> $extToUpdate = Get-AzConnectedMachineExtension -ResourceGroupName connectedMachines -MachineName linux-eastus1_1 -Name customScript
PS C:\> $extToUpdate | Update-AzConnectedMachineExtension -Settings @{
                commandToExecute = "ls -l"
            }

Name         Location ProvisioningState
----         -------- -----------------
customScript eastus   Succeeded
```

<span data-ttu-id="2bef0-115">파이프라인을 통해 전달된 특정 확장을 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="2bef0-115">Updates a specific extension passed in via the pipeline.</span></span>
<span data-ttu-id="2bef0-116">여기서는 파이프라인을 통해 전달된 확장을 사용하여 작동하려는 확장을 식별하고 일반 매개 변수(예: )를 통해 변경하려는 확장을 `-Settings` 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="2bef0-116">Here we are using the extension passed in via the pipeline to help us identify which extension we want to operate on and are specifying what we want to change via the normal parameters (like `-Settings`)</span></span>

### <span data-ttu-id="2bef0-117">예제 3: 파이프라인을 통해 지정된 확장 매개 변수를 사용하여 확장 업데이트</span><span class="sxs-lookup"><span data-stu-id="2bef0-117">Example 3: Update an extension with extension parameters specified via the pipeline</span></span>
```powershell
PS C:\> $extToUpdate = Get-AzConnectedMachineExtension -ResourceGroupName connectedMachines -MachineName linux-eastus1_1 -Name customScript
PS C:\> # Update the settings on the object that will be used via the pipeline
PS C:\> $extToUpdate.Setting.commandToExecute = "ls -l"
PS C:\> $splat = @{
            ResourceGroupName = "connectedMachines"
            MachineName = "linux-eastus1_1"
            Name = "customScript"
        }
PS C:\> $extToUpdate | Update-AzConnectedMachineExtension @splat

Name         Location ProvisioningState
----         -------- -----------------
customScript eastus   Succeeded
```

<span data-ttu-id="2bef0-118">파이프라인을 통해 전달된 특정 확장을 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="2bef0-118">Updates a specific extension passed in via the pipeline.</span></span>
<span data-ttu-id="2bef0-119">여기서는 파이프라인을 통해 전달된 확장을 사용하여 확장에 적용하려는 변경 내용을 제공하고 있습니다.</span><span class="sxs-lookup"><span data-stu-id="2bef0-119">Here we are using the extension passed in via the pipeline to provide the changes we want to make on the extension.</span></span>
<span data-ttu-id="2bef0-120">확장의 위치는 파이프라인을 통해 검색되지 않고 일반적으로 지정된 매개 변수(Splat 매개 변수에 의해)를 통해 검색됩니다.</span><span class="sxs-lookup"><span data-stu-id="2bef0-120">The location of the extension is not retrieved via the pipeline but rather via the parameters specified normally (by the splat parameter).</span></span>

### <span data-ttu-id="2bef0-121">예제 4: 확장 개체를 업데이트할 위치 및 매개 변수로 사용</span><span class="sxs-lookup"><span data-stu-id="2bef0-121">Example 4: Using an extension object as both the location and parameters for updating</span></span>
```powershell
PS C:\> $extToUpdate = Get-AzConnectedMachineExtension -ResourceGroupName connectedMachines -MachineName linux-eastus1_1 -Name customScript
PS C:\> # Update the settings on the object that will be used via the pipeline
PS C:\> $extToUpdate.Setting.commandToExecute = "ls -l"
PS C:\> $extToUpdate | Update-AzConnectedMachineExtension -ExtensionParameter $extToUpdate

Name         Location ProvisioningState
----         -------- -----------------
customScript eastus   Succeeded
```

<span data-ttu-id="2bef0-122">파이프라인을 통해 전달된 특정 확장을 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="2bef0-122">Updates a specific extension passed in via the pipeline.</span></span>
<span data-ttu-id="2bef0-123">여기서는 파이프라인을 통해 전달된 확장을 사용하여 작동하려는 확장을 식별합니다.</span><span class="sxs-lookup"><span data-stu-id="2bef0-123">Here we are using the extension passed in via the pipeline to help us identify which extension we want to operate on.</span></span>
<span data-ttu-id="2bef0-124">또한 확장 개체의 매개 변수를 사용하여 업데이트할 대상을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="2bef0-124">In addition to that, we are using the parameters of the extension object to specify what to update.</span></span>

## <span data-ttu-id="2bef0-125">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="2bef0-125">PARAMETERS</span></span>

### <span data-ttu-id="2bef0-126">-AsJob</span><span class="sxs-lookup"><span data-stu-id="2bef0-126">-AsJob</span></span>
<span data-ttu-id="2bef0-127">작업으로 명령 실행</span><span class="sxs-lookup"><span data-stu-id="2bef0-127">Run the command as a job</span></span>

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

### <span data-ttu-id="2bef0-128">-AutoUpgradeMinorVersion</span><span class="sxs-lookup"><span data-stu-id="2bef0-128">-AutoUpgradeMinorVersion</span></span>
<span data-ttu-id="2bef0-129">배포 시 사용할 수 있는 경우 확장에서 최신 부 버전을 사용할지 여부를 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="2bef0-129">Indicates whether the extension should use a newer minor version if one is available at deployment time.</span></span>
<span data-ttu-id="2bef0-130">그러나 배포된 후 이 속성을 true로 설정한 경우에도 재배포하지 않는 한 확장은 부 버전을 업그레이드하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="2bef0-130">Once deployed, however, the extension will not upgrade minor versions unless redeployed, even with this property set to true.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: UpdateExpanded, UpdateViaIdentityExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2bef0-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2bef0-131">-DefaultProfile</span></span>
<span data-ttu-id="2bef0-132">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="2bef0-132">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2bef0-133">-ExtensionParameter</span><span class="sxs-lookup"><span data-stu-id="2bef0-133">-ExtensionParameter</span></span>
<span data-ttu-id="2bef0-134">컴퓨터 확장 업데이트를 설명 합니다.</span><span class="sxs-lookup"><span data-stu-id="2bef0-134">Describes a Machine Extension Update.</span></span>
<span data-ttu-id="2bef0-135">생성을 위해 EXTENSIONPARAMETER 속성에 대한 NOTES 섹션을 참조하고 해시 테이블을 만드십시오.</span><span class="sxs-lookup"><span data-stu-id="2bef0-135">To construct, see NOTES section for EXTENSIONPARAMETER properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.ConnectedMachine.Models.Api20200802.IMachineExtensionUpdate
Parameter Sets: Update, UpdateViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="2bef0-136">-ForceRerun</span><span class="sxs-lookup"><span data-stu-id="2bef0-136">-ForceRerun</span></span>
<span data-ttu-id="2bef0-137">확장 구성이 변경되지 않은 경우에도 확장 처리기 강제로 업데이트해야 하는 방식입니다.</span><span class="sxs-lookup"><span data-stu-id="2bef0-137">How the extension handler should be forced to update even if the extension configuration has not changed.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded, UpdateViaIdentityExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2bef0-138">-InputObject</span><span class="sxs-lookup"><span data-stu-id="2bef0-138">-InputObject</span></span>
<span data-ttu-id="2bef0-139">ID 매개 변수를 생성하는 경우 INPUTOBJECT 속성에 대한 NOTES 섹션을 참조하고 해시 테이블을 만드십시오.</span><span class="sxs-lookup"><span data-stu-id="2bef0-139">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.ConnectedMachine.Models.IConnectedMachineIdentity
Parameter Sets: UpdateViaIdentity, UpdateViaIdentityExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="2bef0-140">-MachineName</span><span class="sxs-lookup"><span data-stu-id="2bef0-140">-MachineName</span></span>
<span data-ttu-id="2bef0-141">확장을 만들거나 업데이트해야 하는 컴퓨터의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="2bef0-141">The name of the machine where the extension should be created or updated.</span></span>

```yaml
Type: System.String
Parameter Sets: Update, UpdateExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2bef0-142">-Name</span><span class="sxs-lookup"><span data-stu-id="2bef0-142">-Name</span></span>
<span data-ttu-id="2bef0-143">컴퓨터 확장의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="2bef0-143">The name of the machine extension.</span></span>

```yaml
Type: System.String
Parameter Sets: Update, UpdateExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2bef0-144">-NoWait</span><span class="sxs-lookup"><span data-stu-id="2bef0-144">-NoWait</span></span>
<span data-ttu-id="2bef0-145">명령을 비동기적으로 실행</span><span class="sxs-lookup"><span data-stu-id="2bef0-145">Run the command asynchronously</span></span>

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

### <span data-ttu-id="2bef0-146">-ProtectedSetting</span><span class="sxs-lookup"><span data-stu-id="2bef0-146">-ProtectedSetting</span></span>
<span data-ttu-id="2bef0-147">확장은 protectedSettings 또는 protectedSettingsFromKeyVault를 포함하거나 보호된 설정을 모두 포함할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="2bef0-147">The extension can contain either protectedSettings or protectedSettingsFromKeyVault or no protected settings at all.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.ConnectedMachine.Models.Api20200802.IMachineExtensionUpdatePropertiesProtectedSettings
Parameter Sets: UpdateExpanded, UpdateViaIdentityExpanded
Aliases: ProtectedSettings

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2bef0-148">-Publisher</span><span class="sxs-lookup"><span data-stu-id="2bef0-148">-Publisher</span></span>
<span data-ttu-id="2bef0-149">확장 처리기 게시자의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="2bef0-149">The name of the extension handler publisher.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded, UpdateViaIdentityExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2bef0-150">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2bef0-150">-ResourceGroupName</span></span>
<span data-ttu-id="2bef0-151">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="2bef0-151">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: Update, UpdateExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2bef0-152">-Setting</span><span class="sxs-lookup"><span data-stu-id="2bef0-152">-Setting</span></span>
<span data-ttu-id="2bef0-153">확장에 대한 Json 형식의 공용 설정입니다.</span><span class="sxs-lookup"><span data-stu-id="2bef0-153">Json formatted public settings for the extension.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.ConnectedMachine.Models.Api20200802.IMachineExtensionUpdatePropertiesSettings
Parameter Sets: UpdateExpanded, UpdateViaIdentityExpanded
Aliases: Settings

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2bef0-154">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="2bef0-154">-SubscriptionId</span></span>
<span data-ttu-id="2bef0-155">Microsoft Azure 구독을 고유하게 식별하는 구독 자격 증명입니다.</span><span class="sxs-lookup"><span data-stu-id="2bef0-155">Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="2bef0-156">구독 ID는 모든 서비스 호출에 대한 URI의 일부를 형성합니다.</span><span class="sxs-lookup"><span data-stu-id="2bef0-156">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String
Parameter Sets: Update, UpdateExpanded
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2bef0-157">-Tag</span><span class="sxs-lookup"><span data-stu-id="2bef0-157">-Tag</span></span>
<span data-ttu-id="2bef0-158">리소스 태그</span><span class="sxs-lookup"><span data-stu-id="2bef0-158">Resource tags</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: UpdateExpanded, UpdateViaIdentityExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2bef0-159">-Type</span><span class="sxs-lookup"><span data-stu-id="2bef0-159">-Type</span></span>
<span data-ttu-id="2bef0-160">확장의 유형을 지정합니다. 예를 들어 "CustomScriptExtension"입니다.</span><span class="sxs-lookup"><span data-stu-id="2bef0-160">Specifies the type of the extension; an example is "CustomScriptExtension".</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded, UpdateViaIdentityExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2bef0-161">-TypeHandlerVersion</span><span class="sxs-lookup"><span data-stu-id="2bef0-161">-TypeHandlerVersion</span></span>
<span data-ttu-id="2bef0-162">스크립트 처리기 버전을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="2bef0-162">Specifies the version of the script handler.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded, UpdateViaIdentityExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2bef0-163">-Confirm</span><span class="sxs-lookup"><span data-stu-id="2bef0-163">-Confirm</span></span>
<span data-ttu-id="2bef0-164">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="2bef0-164">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2bef0-165">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2bef0-165">-WhatIf</span></span>
<span data-ttu-id="2bef0-166">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="2bef0-166">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2bef0-167">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="2bef0-167">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2bef0-168">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2bef0-168">CommonParameters</span></span>
<span data-ttu-id="2bef0-169">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="2bef0-169">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2bef0-170">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="2bef0-170">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2bef0-171">입력</span><span class="sxs-lookup"><span data-stu-id="2bef0-171">INPUTS</span></span>

### <span data-ttu-id="2bef0-172">Microsoft.Azure.PowerShell.Cmdlets.ConnectedMachine.Models.Api20200802.IMachineExtensionUpdate</span><span class="sxs-lookup"><span data-stu-id="2bef0-172">Microsoft.Azure.PowerShell.Cmdlets.ConnectedMachine.Models.Api20200802.IMachineExtensionUpdate</span></span>

### <span data-ttu-id="2bef0-173">Microsoft.Azure.PowerShell.Cmdlets.ConnectedMachine.Models.IConnectedMachineIdentity</span><span class="sxs-lookup"><span data-stu-id="2bef0-173">Microsoft.Azure.PowerShell.Cmdlets.ConnectedMachine.Models.IConnectedMachineIdentity</span></span>

## <span data-ttu-id="2bef0-174">출력</span><span class="sxs-lookup"><span data-stu-id="2bef0-174">OUTPUTS</span></span>

### <span data-ttu-id="2bef0-175">Microsoft.Azure.PowerShell.Cmdlets.ConnectedMachine.Models.Api20200802.IMachineExtension</span><span class="sxs-lookup"><span data-stu-id="2bef0-175">Microsoft.Azure.PowerShell.Cmdlets.ConnectedMachine.Models.Api20200802.IMachineExtension</span></span>

## <span data-ttu-id="2bef0-176">참고 사항</span><span class="sxs-lookup"><span data-stu-id="2bef0-176">NOTES</span></span>

<span data-ttu-id="2bef0-177">별칭</span><span class="sxs-lookup"><span data-stu-id="2bef0-177">ALIASES</span></span>

<span data-ttu-id="2bef0-178">복합 매개 변수 속성</span><span class="sxs-lookup"><span data-stu-id="2bef0-178">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="2bef0-179">아래에 설명된 매개 변수를 만들 수 있도록 적절한 속성을 포함하는 해시 테이블을 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="2bef0-179">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="2bef0-180">해시 테이블에 대한 자세한 내용은 다음 Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="2bef0-180">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="2bef0-181">EXTENSIONPARAMETER: <IMachineExtensionUpdate> 컴퓨터 확장 업데이트를 설명 합니다.</span><span class="sxs-lookup"><span data-stu-id="2bef0-181">EXTENSIONPARAMETER <IMachineExtensionUpdate>: Describes a Machine Extension Update.</span></span>
  - <span data-ttu-id="2bef0-182">`[Tag <IUpdateResourceTags>]`: 리소스 태그</span><span class="sxs-lookup"><span data-stu-id="2bef0-182">`[Tag <IUpdateResourceTags>]`: Resource tags</span></span>
    - <span data-ttu-id="2bef0-183">`[(Any) <String>]`: 이 개체에 추가할 수 있는 속성을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="2bef0-183">`[(Any) <String>]`: This indicates any property can be added to this object.</span></span>
  - <span data-ttu-id="2bef0-184">`[AutoUpgradeMinorVersion <Boolean?>]`: 배포 시 사용할 수 있는 경우 확장에서 최신 부 버전을 사용할지 여부를 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="2bef0-184">`[AutoUpgradeMinorVersion <Boolean?>]`: Indicates whether the extension should use a newer minor version if one is available at deployment time.</span></span> <span data-ttu-id="2bef0-185">그러나 배포된 후 이 속성을 true로 설정한 경우에도 재배포하지 않는 한 확장은 부 버전을 업그레이드하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="2bef0-185">Once deployed, however, the extension will not upgrade minor versions unless redeployed, even with this property set to true.</span></span>
  - <span data-ttu-id="2bef0-186">`[ForceUpdateTag <String>]`: 확장 구성이 변경되지 않은 경우에도 확장 처리기 강제로 업데이트해야 하는 방식입니다.</span><span class="sxs-lookup"><span data-stu-id="2bef0-186">`[ForceUpdateTag <String>]`: How the extension handler should be forced to update even if the extension configuration has not changed.</span></span>
  - <span data-ttu-id="2bef0-187">`[ProtectedSetting <IMachineExtensionUpdatePropertiesProtectedSettings>]`: 확장은 protectedSettings 또는 protectedSettingsFromKeyVault를 포함하거나 보호된 설정을 모두 포함할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="2bef0-187">`[ProtectedSetting <IMachineExtensionUpdatePropertiesProtectedSettings>]`: The extension can contain either protectedSettings or protectedSettingsFromKeyVault or no protected settings at all.</span></span>
  - <span data-ttu-id="2bef0-188">`[Publisher <String>]`: 확장 처리기 게시자의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="2bef0-188">`[Publisher <String>]`: The name of the extension handler publisher.</span></span>
  - <span data-ttu-id="2bef0-189">`[Setting <IMachineExtensionUpdatePropertiesSettings>]`: 확장에 대한 Json 형식의 공용 설정입니다.</span><span class="sxs-lookup"><span data-stu-id="2bef0-189">`[Setting <IMachineExtensionUpdatePropertiesSettings>]`: Json formatted public settings for the extension.</span></span>
  - <span data-ttu-id="2bef0-190">`[Type <String>]`: 확장의 유형을 지정합니다. 예를 들어 "CustomScriptExtension"입니다.</span><span class="sxs-lookup"><span data-stu-id="2bef0-190">`[Type <String>]`: Specifies the type of the extension; an example is "CustomScriptExtension".</span></span>
  - <span data-ttu-id="2bef0-191">`[TypeHandlerVersion <String>]`: 스크립트 처리기 버전을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="2bef0-191">`[TypeHandlerVersion <String>]`: Specifies the version of the script handler.</span></span>

<span data-ttu-id="2bef0-192">INPUTOBJECT: <IConnectedMachineIdentity> ID 매개 변수</span><span class="sxs-lookup"><span data-stu-id="2bef0-192">INPUTOBJECT <IConnectedMachineIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="2bef0-193">`[ExtensionName <String>]`: 컴퓨터 확장의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="2bef0-193">`[ExtensionName <String>]`: The name of the machine extension.</span></span>
  - <span data-ttu-id="2bef0-194">`[Id <String>]`: 리소스 ID 경로</span><span class="sxs-lookup"><span data-stu-id="2bef0-194">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="2bef0-195">`[Name <String>]`: 하이브리드 컴퓨터의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="2bef0-195">`[Name <String>]`: The name of the hybrid machine.</span></span>
  - <span data-ttu-id="2bef0-196">`[ResourceGroupName <String>]`: 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="2bef0-196">`[ResourceGroupName <String>]`: The name of the resource group.</span></span>
  - <span data-ttu-id="2bef0-197">`[SubscriptionId <String>]`: Microsoft Azure 구독을 고유하게 식별하는 구독 자격 증명입니다.</span><span class="sxs-lookup"><span data-stu-id="2bef0-197">`[SubscriptionId <String>]`: Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="2bef0-198">구독 ID는 모든 서비스 호출에 대한 URI의 일부를 형성합니다.</span><span class="sxs-lookup"><span data-stu-id="2bef0-198">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="2bef0-199">관련 링크</span><span class="sxs-lookup"><span data-stu-id="2bef0-199">RELATED LINKS</span></span>

