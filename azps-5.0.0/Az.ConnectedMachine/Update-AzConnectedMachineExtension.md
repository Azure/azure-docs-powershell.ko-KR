---
external help file: ''
Module Name: Az.ConnectedMachine
online version: https://docs.microsoft.com/en-us/powershell/module/az.connectedmachine/update-azconnectedmachineextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ConnectedMachine/help/Update-AzConnectedMachineExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ConnectedMachine/help/Update-AzConnectedMachineExtension.md
ms.openlocfilehash: 95334b4f67685183e499518b068f1003f5bb6547
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94218728"
---
# <span data-ttu-id="3f849-101">Update-AzConnectedMachineExtension</span><span class="sxs-lookup"><span data-stu-id="3f849-101">Update-AzConnectedMachineExtension</span></span>

## <span data-ttu-id="3f849-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3f849-102">SYNOPSIS</span></span>
<span data-ttu-id="3f849-103">확장을 만들거나 업데이트 하는 작업입니다.</span><span class="sxs-lookup"><span data-stu-id="3f849-103">The operation to create or update the extension.</span></span>

## <span data-ttu-id="3f849-104">구문과</span><span class="sxs-lookup"><span data-stu-id="3f849-104">SYNTAX</span></span>

### <span data-ttu-id="3f849-105">UpdateExpanded 됨 (기본값)</span><span class="sxs-lookup"><span data-stu-id="3f849-105">UpdateExpanded (Default)</span></span>
```
Update-AzConnectedMachineExtension -MachineName <String> -Name <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-AutoUpgradeMinorVersion] [-ForceRerun <String>]
 [-ProtectedSetting <IMachineExtensionUpdatePropertiesProtectedSettings>] [-Publisher <String>]
 [-Setting <IMachineExtensionUpdatePropertiesSettings>] [-Tag <Hashtable>] [-Type <String>]
 [-TypeHandlerVersion <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="3f849-106">Update</span><span class="sxs-lookup"><span data-stu-id="3f849-106">Update</span></span>
```
Update-AzConnectedMachineExtension -MachineName <String> -Name <String> -ResourceGroupName <String>
 -ExtensionParameter <IMachineExtensionUpdate> [-SubscriptionId <String>] [-DefaultProfile <PSObject>]
 [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="3f849-107">UpdateViaIdentity</span><span class="sxs-lookup"><span data-stu-id="3f849-107">UpdateViaIdentity</span></span>
```
Update-AzConnectedMachineExtension -InputObject <IConnectedMachineIdentity>
 -ExtensionParameter <IMachineExtensionUpdate> [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="3f849-108">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="3f849-108">UpdateViaIdentityExpanded</span></span>
```
Update-AzConnectedMachineExtension -InputObject <IConnectedMachineIdentity> [-AutoUpgradeMinorVersion]
 [-ForceRerun <String>] [-ProtectedSetting <IMachineExtensionUpdatePropertiesProtectedSettings>]
 [-Publisher <String>] [-Setting <IMachineExtensionUpdatePropertiesSettings>] [-Tag <Hashtable>]
 [-Type <String>] [-TypeHandlerVersion <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="3f849-109">설명은</span><span class="sxs-lookup"><span data-stu-id="3f849-109">DESCRIPTION</span></span>
<span data-ttu-id="3f849-110">확장을 만들거나 업데이트 하는 작업입니다.</span><span class="sxs-lookup"><span data-stu-id="3f849-110">The operation to create or update the extension.</span></span>

## <span data-ttu-id="3f849-111">예제의</span><span class="sxs-lookup"><span data-stu-id="3f849-111">EXAMPLES</span></span>

### <span data-ttu-id="3f849-112">예제 1: 확장 업데이트</span><span class="sxs-lookup"><span data-stu-id="3f849-112">Example 1: Update an extension</span></span>
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

<span data-ttu-id="3f849-113">특정 컴퓨터에서 확장을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="3f849-113">Updates an extension on a specific machine.</span></span>

### <span data-ttu-id="3f849-114">예제 2: 파이프라인을 통해 지정 된 위치를 사용 하 여 확장 업데이트</span><span class="sxs-lookup"><span data-stu-id="3f849-114">Example 2: Update an extension with location specified via the pipeline</span></span>
```powershell
PS C:\> $extToUpdate = Get-AzConnectedMachineExtension -ResourceGroupName connectedMachines -MachineName linux-eastus1_1 -Name customScript
PS C:\> $extToUpdate | Update-AzConnectedMachineExtension -Settings @{
                commandToExecute = "ls -l"
            }

Name         Location ProvisioningState
----         -------- -----------------
customScript eastus   Succeeded
```

<span data-ttu-id="3f849-115">파이프라인을 통해 전달 된 특정 확장을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="3f849-115">Updates a specific extension passed in via the pipeline.</span></span>
<span data-ttu-id="3f849-116">여기서는 파이프라인을 통해 전달 되는 확장을 사용 하 여 어떤 확장이 작동 하 고 있는지 식별 하 고 일반적인 매개 변수 (예:)를 통해 변경할 내용을 지정 합니다. `-Settings`</span><span class="sxs-lookup"><span data-stu-id="3f849-116">Here we are using the extension passed in via the pipeline to help us identify which extension we want to operate on and are specifying what we want to change via the normal parameters (like `-Settings`)</span></span>

### <span data-ttu-id="3f849-117">예제 3: 파이프라인을 통해 지정 된 확장 매개 변수를 사용 하 여 확장 업데이트</span><span class="sxs-lookup"><span data-stu-id="3f849-117">Example 3: Update an extension with extension parameters specified via the pipeline</span></span>
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

<span data-ttu-id="3f849-118">파이프라인을 통해 전달 된 특정 확장을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="3f849-118">Updates a specific extension passed in via the pipeline.</span></span>
<span data-ttu-id="3f849-119">여기에서는 파이프라인을 통해 전달 된 확장을 사용 하 여 확장에 대해 변경할 내용을 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="3f849-119">Here we are using the extension passed in via the pipeline to provide the changes we want to make on the extension.</span></span>
<span data-ttu-id="3f849-120">확장명의 위치는 파이프라인을 통해 검색 되지 않지만 splat 매개 변수를 통해 정상적으로 지정 된 매개 변수를 대신 합니다.</span><span class="sxs-lookup"><span data-stu-id="3f849-120">The location of the extension is not retrieved via the pipeline but rather via the parameters specified normally (by the splat parameter).</span></span>

### <span data-ttu-id="3f849-121">예제 4: 확장 개체를 업데이트를 위한 위치 및 매개 변수 모두 사용</span><span class="sxs-lookup"><span data-stu-id="3f849-121">Example 4: Using an extension object as both the location and parameters for updating</span></span>
```powershell
PS C:\> $extToUpdate = Get-AzConnectedMachineExtension -ResourceGroupName connectedMachines -MachineName linux-eastus1_1 -Name customScript
PS C:\> # Update the settings on the object that will be used via the pipeline
PS C:\> $extToUpdate.Setting.commandToExecute = "ls -l"
PS C:\> $extToUpdate | Update-AzConnectedMachineExtension -ExtensionParameter $extToUpdate

Name         Location ProvisioningState
----         -------- -----------------
customScript eastus   Succeeded
```

<span data-ttu-id="3f849-122">파이프라인을 통해 전달 된 특정 확장을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="3f849-122">Updates a specific extension passed in via the pipeline.</span></span>
<span data-ttu-id="3f849-123">여기서는 파이프라인을 통해 전달 되는 확장을 사용 하 여 어떤 확장명을 작업에 사용할 지를 식별 하는 데 도움을 주세요.</span><span class="sxs-lookup"><span data-stu-id="3f849-123">Here we are using the extension passed in via the pipeline to help us identify which extension we want to operate on.</span></span>
<span data-ttu-id="3f849-124">이 외에도 확장 개체의 매개 변수를 사용 하 여 업데이트할 항목을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="3f849-124">In addition to that, we are using the parameters of the extension object to specify what to update.</span></span>

## <span data-ttu-id="3f849-125">변수</span><span class="sxs-lookup"><span data-stu-id="3f849-125">PARAMETERS</span></span>

### <span data-ttu-id="3f849-126">-AsJob</span><span class="sxs-lookup"><span data-stu-id="3f849-126">-AsJob</span></span>
<span data-ttu-id="3f849-127">작업으로 명령 실행</span><span class="sxs-lookup"><span data-stu-id="3f849-127">Run the command as a job</span></span>

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

### <span data-ttu-id="3f849-128">-AutoUpgradeMinorVersion</span><span class="sxs-lookup"><span data-stu-id="3f849-128">-AutoUpgradeMinorVersion</span></span>
<span data-ttu-id="3f849-129">배포 시 사용할 수 있는 확장이 새 부 버전을 사용 해야 하는지 여부를 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="3f849-129">Indicates whether the extension should use a newer minor version if one is available at deployment time.</span></span>
<span data-ttu-id="3f849-130">그러나 배포 된 후에는이 속성이 true로 설정 된 경우에도 확장에서 부 버전이 업그레이드 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="3f849-130">Once deployed, however, the extension will not upgrade minor versions unless redeployed, even with this property set to true.</span></span>

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

### <span data-ttu-id="3f849-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3f849-131">-DefaultProfile</span></span>
<span data-ttu-id="3f849-132">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="3f849-132">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3f849-133">-ExtensionParameter 변수</span><span class="sxs-lookup"><span data-stu-id="3f849-133">-ExtensionParameter</span></span>
<span data-ttu-id="3f849-134">컴퓨터 확장 업데이트에 대해 설명 합니다.</span><span class="sxs-lookup"><span data-stu-id="3f849-134">Describes a Machine Extension Update.</span></span>
<span data-ttu-id="3f849-135">생성 하려면 EXTENSIONPARAMETER 속성에 대 한 참고 섹션을 참조 하 고 해시 테이블을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="3f849-135">To construct, see NOTES section for EXTENSIONPARAMETER properties and create a hash table.</span></span>

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

### <span data-ttu-id="3f849-136">-ForceRerun</span><span class="sxs-lookup"><span data-stu-id="3f849-136">-ForceRerun</span></span>
<span data-ttu-id="3f849-137">확장 구성이 변경 되지 않은 경우에도 확장 처리기를 강제로 업데이트 하는 방법</span><span class="sxs-lookup"><span data-stu-id="3f849-137">How the extension handler should be forced to update even if the extension configuration has not changed.</span></span>

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

### <span data-ttu-id="3f849-138">-InputObject</span><span class="sxs-lookup"><span data-stu-id="3f849-138">-InputObject</span></span>
<span data-ttu-id="3f849-139">생성할 id 매개 변수는 INPUTOBJECT 속성에 대 한 참고 섹션을 참조 하 고 해시 테이블을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="3f849-139">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="3f849-140">-MachineName</span><span class="sxs-lookup"><span data-stu-id="3f849-140">-MachineName</span></span>
<span data-ttu-id="3f849-141">확장명을 만들거나 업데이트 해야 하는 컴퓨터의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="3f849-141">The name of the machine where the extension should be created or updated.</span></span>

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

### <span data-ttu-id="3f849-142">-이름</span><span class="sxs-lookup"><span data-stu-id="3f849-142">-Name</span></span>
<span data-ttu-id="3f849-143">컴퓨터 확장의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="3f849-143">The name of the machine extension.</span></span>

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

### <span data-ttu-id="3f849-144">-NoWait</span><span class="sxs-lookup"><span data-stu-id="3f849-144">-NoWait</span></span>
<span data-ttu-id="3f849-145">비동기적으로 명령 실행</span><span class="sxs-lookup"><span data-stu-id="3f849-145">Run the command asynchronously</span></span>

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

### <span data-ttu-id="3f849-146">-ProtectedSetting</span><span class="sxs-lookup"><span data-stu-id="3f849-146">-ProtectedSetting</span></span>
<span data-ttu-id="3f849-147">확장명에는 protectedSettings 또는 protectedSettingsFromKeyVault를 포함할 수도 있고 보호 되는 설정이 전혀 없습니다.</span><span class="sxs-lookup"><span data-stu-id="3f849-147">The extension can contain either protectedSettings or protectedSettingsFromKeyVault or no protected settings at all.</span></span>

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

### <span data-ttu-id="3f849-148">-Publisher</span><span class="sxs-lookup"><span data-stu-id="3f849-148">-Publisher</span></span>
<span data-ttu-id="3f849-149">확장 처리기 게시자의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="3f849-149">The name of the extension handler publisher.</span></span>

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

### <span data-ttu-id="3f849-150">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3f849-150">-ResourceGroupName</span></span>
<span data-ttu-id="3f849-151">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="3f849-151">The name of the resource group.</span></span>

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

### <span data-ttu-id="3f849-152">-설정</span><span class="sxs-lookup"><span data-stu-id="3f849-152">-Setting</span></span>
<span data-ttu-id="3f849-153">확장에 대 한 Json 형식의 공용 설정입니다.</span><span class="sxs-lookup"><span data-stu-id="3f849-153">Json formatted public settings for the extension.</span></span>

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

### <span data-ttu-id="3f849-154">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="3f849-154">-SubscriptionId</span></span>
<span data-ttu-id="3f849-155">Microsoft Azure 구독을 고유 하 게 식별 하는 구독 자격 증명입니다.</span><span class="sxs-lookup"><span data-stu-id="3f849-155">Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="3f849-156">구독 ID는 모든 서비스 호출에 대 한 URI의 일부를 형성 합니다.</span><span class="sxs-lookup"><span data-stu-id="3f849-156">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="3f849-157">태그</span><span class="sxs-lookup"><span data-stu-id="3f849-157">-Tag</span></span>
<span data-ttu-id="3f849-158">리소스 태그</span><span class="sxs-lookup"><span data-stu-id="3f849-158">Resource tags</span></span>

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

### <span data-ttu-id="3f849-159">-Type</span><span class="sxs-lookup"><span data-stu-id="3f849-159">-Type</span></span>
<span data-ttu-id="3f849-160">확장명의 유형을 지정 합니다. 예를 들어 "CustomScriptExtension"이 있습니다.</span><span class="sxs-lookup"><span data-stu-id="3f849-160">Specifies the type of the extension; an example is "CustomScriptExtension".</span></span>

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

### <span data-ttu-id="3f849-161">-TypeHandlerVersion</span><span class="sxs-lookup"><span data-stu-id="3f849-161">-TypeHandlerVersion</span></span>
<span data-ttu-id="3f849-162">스크립트 처리기의 버전을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="3f849-162">Specifies the version of the script handler.</span></span>

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

### <span data-ttu-id="3f849-163">-확인</span><span class="sxs-lookup"><span data-stu-id="3f849-163">-Confirm</span></span>
<span data-ttu-id="3f849-164">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="3f849-164">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3f849-165">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3f849-165">-WhatIf</span></span>
<span data-ttu-id="3f849-166">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="3f849-166">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3f849-167">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="3f849-167">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3f849-168">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3f849-168">CommonParameters</span></span>
<span data-ttu-id="3f849-169">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="3f849-169">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3f849-170">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="3f849-170">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3f849-171">입력</span><span class="sxs-lookup"><span data-stu-id="3f849-171">INPUTS</span></span>

### <span data-ttu-id="3f849-172">ConnectedMachine. Api20200802. i a Nach....</span><span class="sxs-lookup"><span data-stu-id="3f849-172">Microsoft.Azure.PowerShell.Cmdlets.ConnectedMachine.Models.Api20200802.IMachineExtensionUpdate</span></span>

### <span data-ttu-id="3f849-173">ConnectedMachine. IConnectedMachineIdentity에 대 한 Microsoft PowerShell</span><span class="sxs-lookup"><span data-stu-id="3f849-173">Microsoft.Azure.PowerShell.Cmdlets.ConnectedMachine.Models.IConnectedMachineIdentity</span></span>

## <span data-ttu-id="3f849-174">출력</span><span class="sxs-lookup"><span data-stu-id="3f849-174">OUTPUTS</span></span>

### <span data-ttu-id="3f849-175">ConnectedMachine. Api20200802. i a m.. PowerShell.</span><span class="sxs-lookup"><span data-stu-id="3f849-175">Microsoft.Azure.PowerShell.Cmdlets.ConnectedMachine.Models.Api20200802.IMachineExtension</span></span>

## <span data-ttu-id="3f849-176">상속자</span><span class="sxs-lookup"><span data-stu-id="3f849-176">NOTES</span></span>

<span data-ttu-id="3f849-177">별칭과</span><span class="sxs-lookup"><span data-stu-id="3f849-177">ALIASES</span></span>

<span data-ttu-id="3f849-178">복합 매개 변수 속성</span><span class="sxs-lookup"><span data-stu-id="3f849-178">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="3f849-179">아래 설명 된 매개 변수를 만들려면 적절 한 속성을 포함 하는 해시 테이블을 생성 합니다.</span><span class="sxs-lookup"><span data-stu-id="3f849-179">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="3f849-180">해시 테이블에 대 한 자세한 내용은 Get-Help about_Hash_Tables를 실행 하세요.</span><span class="sxs-lookup"><span data-stu-id="3f849-180">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="3f849-181">EXTENSIONPARAMETER <IMachineExtensionUpdate> : 컴퓨터 확장 업데이트를 설명 합니다.</span><span class="sxs-lookup"><span data-stu-id="3f849-181">EXTENSIONPARAMETER <IMachineExtensionUpdate>: Describes a Machine Extension Update.</span></span>
  - <span data-ttu-id="3f849-182">`[Tag <IUpdateResourceTags>]`: 리소스 태그</span><span class="sxs-lookup"><span data-stu-id="3f849-182">`[Tag <IUpdateResourceTags>]`: Resource tags</span></span>
    - <span data-ttu-id="3f849-183">`[(Any) <String>]`:이 개체에 모든 속성이 추가 될 수 있음을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="3f849-183">`[(Any) <String>]`: This indicates any property can be added to this object.</span></span>
  - <span data-ttu-id="3f849-184">`[AutoUpgradeMinorVersion <Boolean?>]`: 배포 시 사용할 수 있는 경우 확장에서 최신 부 버전을 사용 해야 하는지 여부를 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="3f849-184">`[AutoUpgradeMinorVersion <Boolean?>]`: Indicates whether the extension should use a newer minor version if one is available at deployment time.</span></span> <span data-ttu-id="3f849-185">그러나 배포 된 후에는이 속성이 true로 설정 된 경우에도 확장에서 부 버전이 업그레이드 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="3f849-185">Once deployed, however, the extension will not upgrade minor versions unless redeployed, even with this property set to true.</span></span>
  - <span data-ttu-id="3f849-186">`[ForceUpdateTag <String>]`: 확장 구성이 변경 되지 않은 경우에도 확장 처리기를 강제로 업데이트 해야 하는 방법입니다.</span><span class="sxs-lookup"><span data-stu-id="3f849-186">`[ForceUpdateTag <String>]`: How the extension handler should be forced to update even if the extension configuration has not changed.</span></span>
  - <span data-ttu-id="3f849-187">`[ProtectedSetting <IMachineExtensionUpdatePropertiesProtectedSettings>]`: 확장명에는 protectedSettings 또는 protectedSettingsFromKeyVault를 포함할 수도 있고 보호 되는 설정이 전혀 없습니다.</span><span class="sxs-lookup"><span data-stu-id="3f849-187">`[ProtectedSetting <IMachineExtensionUpdatePropertiesProtectedSettings>]`: The extension can contain either protectedSettings or protectedSettingsFromKeyVault or no protected settings at all.</span></span>
  - <span data-ttu-id="3f849-188">`[Publisher <String>]`: 확장 처리기 게시자의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="3f849-188">`[Publisher <String>]`: The name of the extension handler publisher.</span></span>
  - <span data-ttu-id="3f849-189">`[Setting <IMachineExtensionUpdatePropertiesSettings>]`: 확장에 대 한 Json 형식의 공용 설정입니다.</span><span class="sxs-lookup"><span data-stu-id="3f849-189">`[Setting <IMachineExtensionUpdatePropertiesSettings>]`: Json formatted public settings for the extension.</span></span>
  - <span data-ttu-id="3f849-190">`[Type <String>]`: 확장의 형식을 지정 합니다. 예를 들어 "CustomScriptExtension"이 있습니다.</span><span class="sxs-lookup"><span data-stu-id="3f849-190">`[Type <String>]`: Specifies the type of the extension; an example is "CustomScriptExtension".</span></span>
  - <span data-ttu-id="3f849-191">`[TypeHandlerVersion <String>]`: 스크립트 처리기의 버전을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="3f849-191">`[TypeHandlerVersion <String>]`: Specifies the version of the script handler.</span></span>

<span data-ttu-id="3f849-192">INPUTOBJECT <IConnectedMachineIdentity> : Identity 매개 변수</span><span class="sxs-lookup"><span data-stu-id="3f849-192">INPUTOBJECT <IConnectedMachineIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="3f849-193">`[ExtensionName <String>]`: 컴퓨터 확장명의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="3f849-193">`[ExtensionName <String>]`: The name of the machine extension.</span></span>
  - <span data-ttu-id="3f849-194">`[Id <String>]`: 리소스 id 경로</span><span class="sxs-lookup"><span data-stu-id="3f849-194">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="3f849-195">`[Name <String>]`: 하이브리드 컴퓨터의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="3f849-195">`[Name <String>]`: The name of the hybrid machine.</span></span>
  - <span data-ttu-id="3f849-196">`[ResourceGroupName <String>]`: 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="3f849-196">`[ResourceGroupName <String>]`: The name of the resource group.</span></span>
  - <span data-ttu-id="3f849-197">`[SubscriptionId <String>]`: Microsoft Azure 구독을 고유 하 게 식별 하는 구독 자격 증명입니다.</span><span class="sxs-lookup"><span data-stu-id="3f849-197">`[SubscriptionId <String>]`: Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="3f849-198">구독 ID는 모든 서비스 호출에 대 한 URI의 일부를 형성 합니다.</span><span class="sxs-lookup"><span data-stu-id="3f849-198">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="3f849-199">관련 링크</span><span class="sxs-lookup"><span data-stu-id="3f849-199">RELATED LINKS</span></span>

